# Conditional WaveNet
這篇的內容主要是展示了一個受WaveNet啟發的CNN模型，那它是有針對時間序列預測進行簡化和優化的結構，這篇的作者把它應用在財務相關領域，然後在conditional WaveNet的情況下，能夠提取時間序列之間的時間關係來改進預測，同時也不需要較長時間的歷史資訊，也可以減少noise，以下為作者使用的主要架構：
![image](https://asset-pdf.scinapse.io/prod/2603648311/figures/figure-2.3.jpg)

## 實作成果
綠色實線為true data，紅色實線為unconditional WaveNet的預測結果，藍色虛線為conditional WaveNet  
X-coordinate :  
<img src="https://raw.githubusercontent.com/XieYiZhi78/cWaveNet/main/img/WaveNet_x_final.png" alt="resultx" width="400"/>  
Y-coordinate :  
<img src="https://raw.githubusercontent.com/XieYiZhi78/cWaveNet/main/img/WaveNet_y_final.png" alt="resultx" width="400"/>  
Z-coordinate :  
<img src="https://raw.githubusercontent.com/XieYiZhi78/cWaveNet/main/img/WaveNet_z_final.png" alt="resultx" width="400"/>  


在X和Y的部分，
