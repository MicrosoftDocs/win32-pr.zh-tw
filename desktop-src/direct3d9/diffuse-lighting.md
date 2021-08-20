---
description: 在調整任何衰減效果的光線強度之後，光源引擎會計算從頂點反射的剩餘光線有多少，假設頂點角度為垂直，事件的方向為光源。
ms.assetid: 29280a02-1c26-4b54-8468-707dd96dea1d
title: " (Direct3D 9) 的擴散照明"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9906742b47b959336fd882748388a2f10776b6adb06eb98bc23effb6576793be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675756"
---
# <a name="diffuse-lighting-direct3d-9"></a> (Direct3D 9) 的擴散照明

在調整任何衰減效果的光線強度之後，光源引擎會計算從頂點反射的剩餘光線有多少，假設頂點角度為垂直，事件的方向為光源。 光源引擎會針對方向光源跳至此步驟，因為它們不會因為距離而衰減。 系統會考量兩種反射類型：擴散和反射，並使用不同的公式判斷分別反射的光線量。 在計算反射光線量之後，Direct3D 會將這些新值套用至目前材質的擴散和反射的反射率屬性。 產生的色彩值會是擴散和反射元件，點陣化用來產生 Gouraud Shading 和反射強光。

擴散光源以下列方程式描述。

擴散光源 = 加總 \[ C<sub>d</sub> \* L<sub>d</sub> \* (N<sup>。</sup>L<sub>dir</sub>) \* Atten \* 位置\]



| 參數       | 預設值 | 類型          | 描述                                                                                                   |
|-----------------|---------------|---------------|---------------------------------------------------------------------------------------------------------------|
| Sum             | N/A           | N/A           | 每道光的擴散元件的總和。                                                                  |
| C<sub>d</sub>   | (0,0,0,0)     | D3DCOLORVALUE | 擴散色彩。                                                                                                |
| L<sub>d</sub>   | (0,0,0,0)     | D3DCOLORVALUE | 光線擴散色彩。                                                                                          |
| N               | N/A           | D3DVECTOR     | 頂點垂直                                                                                                 |
| L<sub>dir</sub> | N/A           | D3DVECTOR     | 從物件頂點到光線的方向向量。                                                             |
| Atten           | N/A           | FLOAT         | 光線衰減。 請參閱 [ (Direct3D 9) 的衰減和焦點因素 ](attenuation-and-spotlight-factor.md)。 |
| 付現            | N/A           | FLOAT         | 聚光燈係數。 請參閱 [ (Direct3D 9) 的衰減和焦點因素 ](attenuation-and-spotlight-factor.md)。  |



 

C<sub>d</sub> 的值可能是：

-   頂點 color1 （如果 DIFFUSEMATERIALSOURCE = D3DMCS \_ color1）和第一個頂點色彩是在頂點宣告中提供。
-   頂點 color2 （如果 DIFFUSEMATERIALSOURCE = D3DMCS \_ color2），而第二個頂點色彩則是在頂點宣告中提供。
-   材質擴散色彩

> [!Note]  
> 如果使用任一個 DIFFUSEMATERIALSOURCE 選項，而且未提供頂點色彩，則會使用材質擴散色彩。

 

若要計算衰減 (Atten) 或焦點特性 (找出) ，請參閱 [ (Direct3D 9) 的衰減和焦點因素 ](attenuation-and-spotlight-factor.md)。

所有的光分開處理和插補之後，擴散元件會鉗制為從 0 到 255。 產生的擴散光源值是環境、擴散及發光值的組合。

## <a name="example"></a>範例

在這個範例中，物件是使用淺擴散色彩和材質擴散色彩著色。 程式碼如下所示。


```
D3DMATERIAL9 mtrl;
ZeroMemory( &mtrl, sizeof(mtrl) );

D3DLIGHT9 light;
ZeroMemory( &light, sizeof(light) );
light.Type = D3DLIGHT_DIRECTIONAL;

D3DXVECTOR3 vecDir;
vecDir = D3DXVECTOR3(0.5f, 0.0f, -0.5f);
D3DXVec3Normalize( (D3DXVECTOR3*)&light.Direction, &vecDir );

// set directional light diffuse color
light.Diffuse.r = 1.0f;
light.Diffuse.g = 1.0f;
light.Diffuse.b = 1.0f;
light.Diffuse.a = 1.0f;
m_pd3dDevice->SetLight( 0, &light );
m_pd3dDevice->LightEnable( 0, TRUE );

// if a material is used, SetRenderState must be used
// vertex color = light diffuse color * material diffuse color
mtrl.Diffuse.r = 0.75f;
mtrl.Diffuse.g = 0.0f;
mtrl.Diffuse.b = 0.0f;
mtrl.Diffuse.a = 0.0f;
m_pd3dDevice->SetMaterial( &mtrl );
m_pd3dDevice->SetRenderState(D3DRS_DIFFUSEMATERIALSOURCE, D3DMCS_MATERIAL);
```



根據方程式，為物件端點產生的色彩是材質色彩和淺色的組合。

下方兩個圖例顯示材質色彩 (灰色)，以及淺色 (鮮紅)。

![灰球體圖例](images/amb1.jpg)![紅色球體圖例](images/lightred.jpg)

下圖顯示產生的場景。 場景中唯一的物件為球體。 擴散光線計算會採用材質和淺擴散色彩，並使用內積修改光線方向和頂點直角之間的角度。 如此一來，球體的背面會隨著球體表面曲線遠離光源而變暗。

![使用擴散光源的球體圖例](images/lightd.jpg)

結合前一個範例的擴散光源與環境光源形成物體表面的整體色調。 環境光源形成整個表面的色調，擴散光源則幫助顯現物體的 3D 形狀，如下圖所示。

![擴散光源與環境光源的球體圖例](images/lightad.jpg)

擴散光源比環境光源需要較多運算資源。 因為它取決於頂點直角和光線方向，因此您可以看到 3D 空間的物體幾何，它會產生比環境光源更真實的光源。 您可以使用反射強光達到更真實的外觀。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[燈光數學](mathematics-of-lighting.md)
</dt> </dl>

 

 



