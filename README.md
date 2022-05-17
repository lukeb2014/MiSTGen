# MiSTGen: Minimum Snap Trajectory Generator

## 1 Overview

![](figs/fig1.png)

## 2 How to use

### 3.1 Installing

```shell
pip install -i https://test.pypi.org/simple/ mistgen==0.1.0
```

### 3.2 Usage

```python
def main_demo_v010():
	ax = [0.0, 5.0,5.0,0.0]
    ay = [0.0, 0.0,6.0,6.0]
    
    waypts_ori = np.array([ax,ay])
    
    T = 10
    v0 = np.array([0,0])
    a0 = np.array([0,0])
    ve = np.array([0,0])
    ae = np.array([0,0])
    
    myMistGen = mist_generator()
    xxs,yys,tts = myMistGen.mist_2d_gen(waypts_ori,v0,a0,ve,ae,T)
    vaj_xy = myMistGen.mist_2d_vaj_gen(xxs,yys,tts)
    myMistGen.mist_2d_vis(waypts_ori,xxs,yys,tts,vaj_xy,True,True,True)
```

## Reference

[1] Minimum Snap Trajectory Generation and Control for Quadrotors

