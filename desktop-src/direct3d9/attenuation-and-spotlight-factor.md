---
description: 全域照明方程式的擴散和聚光燈型光源元件內含描述光衰減及焦點圓錐的字詞。 以下將說明這些字詞。
ms.assetid: 960b5fc2-3074-4e51-b3de-5ed370379b01
title: " (Direct3D 9) 的衰減和焦點因素"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb80fff287749e2979a89f2e20c830fdad3961d90ec05bf90a4ee2f6a51f8bcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850611"
---
# <a name="attenuation-and-spotlight-factor-direct3d-9"></a> (Direct3D 9) 的衰減和焦點因素

全域照明方程式的擴散和聚光燈型光源元件內含描述光衰減及焦點圓錐的字詞。 以下將說明這些字詞。

## <a name="attenuation"></a>衰減

光線的衰減取決於光線的類型以及光線與頂點位置之間的距離。 若要計算衰減，請使用下列其中一個方程式。

Atten = 1/ ( att0<sub>i</sub> + att1<sub>i</sub> \* d + att2<sub>i</sub> \* d ²) 

其中：



| 參數        | 預設值 | 類型  | 描述                                     | 範圍          |
|------------------|---------------|-------|-------------------------------------------------|----------------|
| att0<sub>i</sub> | 0.0           | FLOAT | 定值衰減因數                     | 0 至 +infinity |
| att1<sub>i</sub> | 0.0           | FLOAT | 線性衰減因數                       | 0 至 +infinity |
| att2<sub>i</sub> | 0.0           | FLOAT | 二次方衰減因數                    | 0 至 +infinity |
| d                | N/A           | FLOAT | 頂點位置至光源位置的距離 | N/A            |



 

-   若光線為定向光線，則 Atten = 1。
-   若光線與頂點之間的距離超過光線範圍，則 Atten = 0。

Att0、att1、att2 值是由 [**Attenuation1**](d3dlight9.md)的 Attenuation0、Attenuation2 和 D3DLIGHT9 成員所指定。

光線與頂點位置之間的距離一律為正值。

d = \| L<sub>dir</sub>\|

其中：



| 參數       | 預設值 | 類型      | 描述                                                 |
|-----------------|---------------|-----------|-------------------------------------------------------------|
| L<sub>dir</sub> | N/A           | D3DVECTOR | 從頂點位置至光線位置的方向向量 |



 

如果 d 大於光的範圍，也就是 [**D3DLIGHT9**](d3dlight9.md) 結構的範圍成員，Direct3D 不會進行進一步的衰減計算，也不會對頂點套用任何效果。

衰減定值作為公式中的係數，您可對其進行簡單的調整來產生多種出現衰減曲線。 您可將 Attenuation1 設為 1.0，以建立不會衰減但仍受限於範圍的光線，或您可以嘗試使用不同的值，以取得各種衰減效果。

衰減的光線範圍上限不是 0.0。 若要防止光線在光線範圍時突然出現，應用程式可以增加光線範圍。 或者，應用程式可以設定衰減定值，使衰減因數的光線範圍接近 0.0。 衰減值會乘以光線色彩的紅、綠及藍元件，以將光線的強度擴充作為光線傳輸至頂點之距離的因數。

## <a name="spotlight-factor"></a>焦點因數

以下方程式指定焦點因數。

![焦點因數的方程式](images/dx8light9.png)



| 參數         | 預設值 | 類型  | 描述                              | 範圍                    |
|-------------------|---------------|-------|------------------------------------------|--------------------------|
| rho<sub>i</sub>   | N/A           | FLOAT | spotlight i 的 cosine(angle)            | N/A                      |
| phi<sub>i</sub>   | 0.0           | FLOAT | 焦點 i 在弧度的半影角度 | \[theta<sub>i</sub>、pi)  |
| theta<sub>i</sub> | 0.0           | FLOAT | 焦點 i 在弧度的本影角度    | \[0、pi)                  |
| falloff           | 0.0           | FLOAT | Falloff 因數                           | (-infinity, +infinity)   |



 

其中：

rho = norm(L<sub>dcs</sub>)<sup>.</sup>norm(L<sub>dir</sub>)

以及：



| 參數       | 預設值 | 類型      | 描述                                                 |
|-----------------|---------------|-----------|-------------------------------------------------------------|
| L<sub>dc</sub> | N/A           | D3DVECTOR | 相機空間光線方向的負值         |
| L<sub>dir</sub> | N/A           | D3DVECTOR | 從頂點位置至光線位置的方向向量 |



 

在計算光線衰減之後，Direct3D 也會考慮焦點效果（如果適用的話）、光線從介面反映的角度，以及目前材質的反射率來計算該頂點的擴散和反射元件。 如需詳細資訊，請參閱 [焦點](light-types.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[燈光數學](mathematics-of-lighting.md)
</dt> </dl>

 

 



