# Conditional WaveNet
這篇的內容主要是展示了一個受WaveNet啟發的CNN模型，那它是有針對時間序列預測進行簡化和優化的結構，這篇的作者把它應用在財務相關領域，然後在conditional WaveNet的情況下，能夠提取時間序列之間的時間關係來改進預測，同時也不需要較長時間的歷史資訊，也可以減少noise，以下為作者使用的主要架構：
![image](https://asset-pdf.scinapse.io/prod/2603648311/figures/figure-2.3.jpg)

## 實作成果
綠色實線為true data(混沌Lorenz system)，紅色實線為unconditional WaveNet(uWN)的預測結果，藍色虛線為conditional WaveNet(cWN)的預測結果。  
X-coordinate :  
<img src="https://raw.githubusercontent.com/XieYiZhi78/cWaveNet/main/img/WaveNet_x_final.png" alt="resultx" width="400"/>  
Y-coordinate :  
<img src="https://raw.githubusercontent.com/XieYiZhi78/cWaveNet/main/img/WaveNet_y_final.png" alt="resultx" width="400"/>  
Z-coordinate :  
<img src="https://raw.githubusercontent.com/XieYiZhi78/cWaveNet/main/img/WaveNet_z_final.png" alt="resultx" width="400"/>  


在uWN的部分，X和Y的結果似乎還有受到一些訊息的影響，無法模擬出像paper一樣的平滑曲線，而Z的結果波動性更強烈，但一直無法順利改進。  
在cWN的部分，X和Y在大於0的時候似乎無法預測，而Z的預測非常不準確。  
<br/>
下表為預測多次後的平均RMSE：
|RMSE|uWN(paper)|uWN(實作)|cWN(paper)|cWN(實作)|
|:----:|:----:|:----:|:----:|:----:|
|X|0.00577|0.227|0.00174|0.313|
|Y|0.00864|0.177|0.00583|0.287|
|Z|0.00496|0.168|0.00536|0.166|

## References
[Conditional time series forecasting with convolutional neural
networks](https://arxiv.org/pdf/1703.04691.pdf)
