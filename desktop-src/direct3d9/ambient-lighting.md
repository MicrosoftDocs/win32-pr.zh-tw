---
description: 環境光線為場景提供定值光線。
ms.assetid: 327095a7-f4e0-48c2-9e4d-bec8493fe37e
title: " (Direct3D 9) 的環境光源"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e991981a9c1d7d24714e7014d08cefeaa94fe20f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510621"
---
# <a name="ambient-lighting-direct3d-9"></a> (Direct3D 9) 的環境光源

環境光線為場景提供定值光線。 它同等地照亮所有物件端點，因為其不取決於任何其他照明因素，例如頂點標準、光源方向、光源位置、範圍或衰減。 這是最快速的照明類型，但會產生最不實際的結果。 Direct3D 包含單一全域環境光線屬性，您可加以使用而不需建立任何光線。 或者，您可以將任何光線物件設為提供環境光線。 場景的環境光線由下列方程式描述。

環境光源 = C ₐ \* \[ g ₐ + Sum (Atten<sub>我</sub> \* 找<sub></sub>出 \* <sub>ai</sub>) \]

其中：



| 參數         | 預設值 | 類型          | Description                                                                                                                    |
|-------------------|---------------|---------------|--------------------------------------------------------------------------------------------------------------------------------|
| Cₐ                | (0,0,0,0)     | D3DCOLORVALUE | 材料環境色彩                                                                                                         |
| Gₐ                | (0,0,0,0)     | D3DCOLORVALUE | 全域環境色彩                                                                                                           |
| Atten<sub>i</sub> | (0,0,0,0)     | D3DCOLORVALUE | 第 i 個光線的光衰減。 請參閱 [ (Direct3D 9) 的衰減和焦點因素 ](attenuation-and-spotlight-factor.md)。 |
| 找<sub>我</sub>  | (0,0,0,0)     | D3DVECTOR     | 第 i 個光線的聚光燈係數。 請參閱 [ (Direct3D 9) 的衰減和焦點因素 ](attenuation-and-spotlight-factor.md)。  |
| Sum               | N/A           | N/A           | 環境光線的加總                                                                                                       |
| L<sub>ai</sub>    | (0,0,0,0)     | D3DVECTOR     | 第 i 個光線的環境光線色彩                                                                                           |



 

Cₐ 的值為︰

-   頂點 color1 （如果 AMBIENTMATERIALSOURCE = D3DMCS \_ color1）和第一個頂點色彩是在頂點宣告中提供。
-   頂點 color2 （如果 AMBIENTMATERIALSOURCE = D3DMCS \_ color2），而第二個頂點色彩則是在頂點宣告中提供。
-   材料環境色彩。

> [!Note]  
> 如果使用任一個 AMBIENTMATERIALSOURCE 選項，而且未提供頂點色彩，則會使用材質環境色彩。

 

若要使用材料環境色彩，請使用下方範例程式碼所示的 SetMaterial。

Gₐ 是全域環境色彩。 它是使用 Graphicsdevice (D3DRS \_ 環境) 來設定。 Direct3D 場景中有一個全域環境色彩。 此參數與 Direct3D 光線物件無關聯。

L<sub>ai</sub> 是場景中第 i 個光線的環境色彩。 每個 Direct3D 光線都有一組屬性，其中一項是環境色彩。 sum(L<sub>ai</sub>) 這項字詞是場景中所有環境色彩的加總。

## <a name="example"></a>範例

在此範例中，物件使用場景環境光線和材料環境色彩上色。


```
#define GRAY_COLOR  0x00bfbfbf

// create material
D3DMATERIAL9 mtrl;
ZeroMemory(&mtrl, sizeof(mtrl));
mtrl.Ambient.r = 0.75f;
mtrl.Ambient.g = 0.0f;
mtrl.Ambient.b = 0.0f;
mtrl.Ambient.a = 0.0f;
m_pd3dDevice->SetMaterial(&mtrl);
m_pd3dDevice->SetRenderState(D3DRS_AMBIENT, GRAY_COLOR);
```



根據方程式，為物件端點產生的色彩是材質色彩和淺色的組合。

下方兩個圖例顯示材質色彩 (灰色)，以及淺色 (鮮紅)。

![灰球體圖例](images/amb1.jpg)![紅色球體圖例](images/lightred.jpg)

下圖顯示產生的場景。 場景中唯一的物件為球體。 環境光線使用相同色彩照亮所有物件端點。 其不取決於頂點標準或光線方向。 如此一來，球體看起來像是 2D 圓形，因為物件表面周圍的陰影並無差別。

![使用環境光線的球體圖例](images/lighta.jpg)

若要讓物件看起來更逼真，請在環境光線之外套用光源擴散或反射光源。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[燈光數學](mathematics-of-lighting.md)
</dt> </dl>

 

 



