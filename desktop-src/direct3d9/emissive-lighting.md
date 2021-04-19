---
description: 放射光源是以單一字詞描述。
ms.assetid: b6ccf274-a6c5-4b26-8c43-c857c2c24e0f
title: 放射 (Direct3D 9) 的照明
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19cb0566d2409fb68e5fbbdca1cc609c31120e95
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106966998"
---
# <a name="emissive-lighting-direct3d-9"></a>放射 (Direct3D 9) 的照明

放射光源是以單一字詞描述。

放射光源 = Cₑ

其中：



| 參數 | 預設值 | 類型          | Description     |
|-----------|---------------|---------------|-----------------|
| Cₑ        | (0,0,0,0)     | D3DCOLORVALUE | 放射色彩。 |



 

C ₑ的值為：

-   頂點 color1 （如果 EMISSIVEMATERIALSOURCE = D3DMCS \_ color1）和第一個頂點色彩是在頂點宣告中提供。
-   頂點 color2 （如果 EMISSIVEMATERIALSOURCE = D3DMCS \_ color2），而第二個頂點色彩則是在頂點宣告中提供。
-   材質放射色彩

> [!Note]  
> 如果使用任一個 EMISSIVEMATERIALSOURCE 選項，而且未提供頂點色彩，則會使用材質放射色彩。

 

## <a name="example"></a>範例

在此範例中，物件使用場景環境光線和材料環境色彩上色。 程式碼如下所示。


```
// create material
D3DMATERIAL9 mtrl;
ZeroMemory( &mtrl, sizeof(mtrl) );
mtrl.Emissive.r = 0.0f;
mtrl.Emissive.g = 0.75f;
mtrl.Emissive.b = 0.0f;
mtrl.Emissive.a = 0.0f;
m_pd3dDevice->SetMaterial( &mtrl );
m_pd3dDevice->SetRenderState(D3DRS_EMISSIVEMATERIALSOURCE, D3DMCS_MATERIAL);
```



根據公式，產生的物件頂點色彩為材質色彩。

下圖顯示材質色彩，也就是綠色。 放射光線使用相同色彩照亮所有物件端點。 其不取決於頂點標準或光線方向。 如此一來，球體看起來像是 2D 圓形，因為物件表面周圍的陰影並無差別。

![綠色球體圖例](images/lighte.jpg)

下圖顯示在上述範例中，放射光源如何與其他三種類型的燈光混合。 在球體右側，有綠色放射光線和紅色環境光線的混合。 在球體左側，綠色放射光線與紅色環境和擴散光線混合，產生紅色漸層。 反射強光中心為白色，在反射光線值驟然消失時會產生黃色光環，使得環境、擴散和放射光線值彼此混合而產生黃色。

![有放射光線的綠色球體圖](images/lightadse.jpg)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[燈光數學](mathematics-of-lighting.md)
</dt> </dl>

 

 



