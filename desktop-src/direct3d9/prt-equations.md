---
description: 若要完全瞭解執行 PRT 的著色器，請先衍生出著色器用來計算 exit radiance 的公式。
ms.assetid: 66876e9e-cde1-4d04-9b31-30be1c115e6b
title: 'PRT 方 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a65559fada82fda7f7eed1c7d05543883a06a19e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109380"
---
# <a name="prt-equations-direct3d-9"></a>PRT 方 (Direct3D 9) 

若要完全瞭解執行 PRT 的著色器，請先衍生出著色器用來計算 exit radiance 的公式。

若要開始，請使用下列方程式，計算在具有任意距離光源的擴散物件上，直接光源所產生的結束 radiance。

![結束 radiance 的方程式，由具有任意距離光線的擴散物件上的直接光源所產生](images/prt-theory-eq1.png)

其中：



| 參數     | Description                                                                                             |
|---------------|---------------------------------------------------------------------------------------------------------|
| Rp            | 位於頂點 p 的結束 radiance。 在網格上的每個頂點上進行評估。                                   |
| p<sub>d</sub> | 介面的 >albedo。                                                                              |
| pi            | 常數，用來做為能源節約正規化因素。                                        |
| L (s)           | 燈光環境 (來源 radiance) 。                                                             |
| Vp ₍ s ₎         | 點 p 的二進位可見度函數。 如果點可以看到燈，則為1，否則為0。             |
| Hnp ₍ s ₎        | Lambert 法則的余弦詞彙。 等於 max ( (Np ·s) 、0) ，其中 Np 是位於點 p 的法線曲面。 |
| s             | 在球體上整合的變數。                                                           |



 

使用球形的函式（例如球形諧波）時，下列方程式近似于光源環境。

![光源環境的方程式](images/prt-theory-eq2.png)

其中：



| 參數        | Description                                              |
|------------------|----------------------------------------------------------|
| L (s)              | 燈光環境 (來源 radiance) 。              |
| i                | 以基礎函數的數目加總的整數。 |
| O                | 球形諧波的順序。                        |
| l<sub>i</sub>    | 係數。                                           |
| Y<sub>i (s) </sub> | 對球體的一些基礎函數。                     |



 

這些係數的集合（L '）提供函數 L (s) 的最佳近似值，其基礎函數為 Y (s) 。 替代和散發會產生下列方程式。

![替代 l (s) 並散發之後的結束 radiance 方程式](images/prt-theory-eq3.png)

Y<sub>i (s </sub>的整數) Vp ₍ s ₎ Hnp ₍ s ₎是模擬器針對網格上每個頂點所 precomputes 的傳輸係數 t<sub>pi</sub> 。 替代此項會產生下列方程式。

![替代傳輸係數之後的結束 radiance 方程式](images/prt-theory-eq4.png)

將此變更為向量標記法會產生下列未壓縮的方程式，以計算每個通道的結束 radiance。

![變更為向量標記法之後，結束 radiance 的方程式](images/prt-theory-eq5.png)

其中：



| 參數     | Description                                                                                                                                                                         |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Rp            | 位於頂點 p 的結束 radiance。                                                                                                                                                      |
| p<sub>d</sub> | 介面的 >albedo。                                                                                                                                                          |
| L            | L<sub>i</sub>的向量，以及將來源 radiance 投射到球形調和基礎函式的投射。 這是球形調和係數的 order ²向量。 |
| Tp            | 頂點 p 的 order ²傳送向量。 模擬器會將傳輸係數除以 p。                                                                                       |



 

這兩個向量都是球面調和係數的 order ²向量，所以請注意，這只是一個點乘積。 視順序而定，點可能很昂貴，因此可以使用壓縮。 稱為「叢集主體元件分析」的演算法 (CPCA) 有效率地將資料壓縮。 這可讓您使用較高順序的球面調和近似值，以產生更清晰的陰影。

CPCA 提供下列方程式，以接近傳輸向量。

![近似值傳送向量的方程式](images/prt-theory-eq6.png)

其中：



| 參數      | Description                                          |
|----------------|------------------------------------------------------|
| Tp             | 頂點 p 的傳送向量。                    |
| Mk             | 群集 k 的平均值。                              |
| j              | 加總 PCA 向量數目的整數。 |
| N              | PCA 向量的數目。                           |
| w<sub>pj</sub> | 點 p 的第 j 個 PCA 加權。                      |
| B<sub>kj</sub> | 適用于群集 k 的第 j 個 PCA 基礎向量。              |



 

群集只是共用相同 mean 向量的一些頂點。 以下會討論如何取得叢集平均數、PCA 加權、PCA 基礎向量和頂點的叢集識別碼。

以這兩個方會產生：

![替代傳送向量之後，exit radiance 的方程式](images/prt-theory-eq7.png)

然後，發佈點乘積會產生下列方程式。

![發佈點乘積之後的結束 radiance 方程式](images/prt-theory-eq8.png)

因為這兩個 (Mk ·L ' ) 和 (B<sub>kj</sub>·L ' ) 是每個頂點的常數，此範例會以 CPU 計算這些值，並將它們以常數的形式傳遞至頂點著色器;因為 w<sub>pj</sub> 每個頂點的變更，此範例會將每個頂點的資料儲存在頂點緩衝區中。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[預先計算 Radiance 傳輸](precomputed-radiance-transfer.md)
</dt> </dl>

 

 



