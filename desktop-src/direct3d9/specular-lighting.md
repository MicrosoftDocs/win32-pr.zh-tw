---
description: 模型反射反映需要系統不僅知道光線的移動方向，也需要查看檢視器的眼睛方向。
ms.assetid: 35da0ac3-4e68-4d37-a987-405fc15d0cbf
title: " (Direct3D 9) 的反射光源"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ab378d4ca3f00ef81c5048e6ad6cc85eaeb18ad
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104559533"
---
# <a name="specular-lighting-direct3d-9"></a> (Direct3D 9) 的反射光源

模型反射反映需要系統不僅知道光線的移動方向，也需要查看檢視器的眼睛方向。 系統使用簡化 Phong 鏡面反射模型的版本，運用半程向量來近似計算鏡面反射的強度。

預設光源狀態不計算反射強光。 若要啟用反射光源，請務必將 D3DRS \_ SPECULARENABLE 設定為 **TRUE**。

## <a name="specular-lighting-equation"></a>反射光源方程式

反射光源以下列方程式描述。



|                                                                             |
|-----------------------------------------------------------------------------|
| 反射光源 = Cs \* 總和 \[ Ls \* (N ·H) <sup>P</sup> \* Atten \* 位置\] |



 

下表識別變數、其類型，以及其範圍。



| 參數    | 預設值 | 類型          | Description                                                                                                         |
|--------------|---------------|---------------|---------------------------------------------------------------------------------------------------------------------|
| Cₛ           | (0,0,0,0)     | D3DCOLORVALUE | 反射色彩。                                                                                                     |
| Sum          | N/A           | N/A           | 每道光的反射元件的總和。                                                                       |
| N            | N/A           | D3DVECTOR     | 頂點標準。                                                                                                      |
| H            | N/A           | D3DVECTOR     | 半程向量。 請參閱有關半程向量的一節。                                                             |
| <sup>P</sup> | 0.0           | FLOAT         | 鏡面反射力。 範圍是 0 到 + 無限大                                                                  |
| Lₛ           | (0,0,0,0)     | D3DCOLORVALUE | 淺色反射。                                                                                               |
| Atten        | N/A           | FLOAT         | 光衰減值。 請參閱 [ (Direct3D 9) 的衰減和焦點因素 ](attenuation-and-spotlight-factor.md)。 |
| 付現         | N/A           | FLOAT         | 聚光燈係數。 請參閱 [ (Direct3D 9) 的衰減和焦點因素 ](attenuation-and-spotlight-factor.md)。        |



 

Cₛ 的值為：


```
if(SPECULARMATERIALSOURCE == D3DMCS_COLOR1)
  C = color1;
```



-   頂點 color1，如果反射材質來源為 D3DMCS \_ color1，且頂點宣告中提供第一個頂點色彩。
-   頂點 color2，如果反射材質來源為 D3DMCS \_ color2，且頂點宣告中提供第二個頂點色彩。
-   材料反射色彩

> [!Note]  
> 如果使用任一種 [反射材質來源] 選項，而且未提供頂點色彩，則會使用材質反射色彩。

 

所有的光分開處理和插補之後，反射元件會鉗制為從 0 到 255。

## <a name="the-halfway-vector"></a>半程向量

半程向量 (H) 存在於兩個向量之間路程的一半：從物件頂點到光源的向量，以及從物件頂點到相機位置的向量。 Direct3D 提供兩種方式來計算半程向量。 當 D3DRS \_ LOCALVIEWER 設定為 **TRUE** 時，系統會使用相機的位置和頂點的位置，以及光線的方向向量來計算中間向量。 下列公式說明這點。



|                                           |
|-------------------------------------------|
| H = norm(norm(Cₚ - Vₚ) + L<sub>dir</sub>) |



 



| 參數       | 預設值 | 類型      | Description                                                  |
|-----------------|---------------|-----------|--------------------------------------------------------------|
| Cₚ              | N/A           | D3DVECTOR | 相機位置。                                             |
| Vₚ              | N/A           | D3DVECTOR | 頂點位置。                                             |
| L<sub>dir</sub> | N/A           | D3DVECTOR | 從頂點位置至光線位置的方向向量。 |



 

以這種方式判斷半程向量可能會需要大量運算資源。 另一種方式是設定 D3DRS \_ LOCALVIEWER = **FALSE** ，指示系統在 Z 軸上有無限遠的角度時，採取行動。 其計算公式如下。



|                                     |
|-------------------------------------|
| H = norm((0,0,1) + L<sub>dir</sub>) |



 

此設定比較不需要大量運算資源，但比較不精確，因此最適合供使用正交投影的應用程式使用。

## <a name="example"></a>範例

在這個範例，物件使用場景反射淺色和材料反射色彩來著色。 程式碼如下所示。


```
D3DMATERIAL9 mtrl;
ZeroMemory( &mtrl, sizeof(mtrl) );

D3DLIGHT9 light;
ZeroMemory( &light, sizeof(light) );
light.Type = D3DLIGHT_DIRECTIONAL;

D3DXVECTOR3 vecDir;
vecDir = D3DXVECTOR3(0.5f, 0.0f, -0.5f);
D3DXVec3Normalize( (D3DXVECTOR3*)&light.Direction, &vecDir );

light.Specular.r = 1.0f;
light.Specular.g = 1.0f;
light.Specular.b = 1.0f;
light.Specular.a = 1.0f;

light.Range = 1000;
light.Falloff = 0;
light.Attenuation0 = 1;
light.Attenuation1 = 0;
light.Attenuation2 = 0;
m_pd3dDevice->SetLight( 0, &light );
m_pd3dDevice->LightEnable( 0, TRUE );
m_pd3dDevice->SetRenderState( D3DRS_SPECULARENABLE, TRUE );

mtrl.Specular.r = 0.5f;
mtrl.Specular.g = 0.5f;
mtrl.Specular.b = 0.5f;
mtrl.Specular.a = 0.5f;
mtrl.Power = 20;
m_pd3dDevice->SetMaterial( &mtrl );
m_pd3dDevice->SetRenderState(D3DRS_SPECULARMATERIALSOURCE, D3DMCS_MATERIAL);
```



根據方程式，為物件端點產生的色彩是材質色彩和淺色的組合。

下列兩圖顯示反射材料色彩 (灰色)，以及反射淺色 (白色)。

![灰球體圖例](images/amb1.jpg)![白色球體的圖例](images/lightwhite.jpg)

下圖顯示結果反射強光。

![反射強光的圖例](images/lights.jpg)

結合反射強光與周遭環境和擴散光源會產生下圖。 在套用所有三種光源類型時，這更加清楚地類似寫實物件。

![結合反射強光、周遭環境光源和擴散光源的圖例](images/lightads.jpg)

反射光源比擴散光源需要較多運算資源。 這通常用來提供表面材料的視覺線索。 根據表面材料，反射強光在大小和色彩上不同。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[燈光數學](mathematics-of-lighting.md)
</dt> </dl>

 

 



