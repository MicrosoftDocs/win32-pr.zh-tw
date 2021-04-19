---
description: 線清單是隔離、直線段的清單。
ms.assetid: bb02b3d6-f30f-4f2b-8b40-a7e37faf524a
title: 行清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b27bd58ea2de6b5944b8511e99154c50f671439
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970505"
---
# <a name="line-lists"></a>行清單

線清單是隔離、直線段的清單。 在 3D 場景中加入冰雹或暴雨的這類工作適合使用線清單。 應用程式藉由填入頂點陣列來建立線清單。 請注意，線清單中的頂點數必須是大於或等於二的偶數。

下圖顯示呈現的線清單。

![線清單的圖例](images/linelst.png)

您可以將資料和紋理套用到線清單。 資料或紋理中的的色彩只會隨繪製線條出現，不會出現在線之間的任何點。

下列程式碼顯示如何建立這個線段的頂點。


```
struct CUSTOMVERTEX
{
    float x,y,z;
};

CUSTOMVERTEX Vertices[] = 
{
    {-5.0, -5.0, 0.0},
    { 0.0,  5.0, 0.0},
    { 5.0, -5.0, 0.0},
    {10.0,  5.0, 0.0},
    {15.0, -5.0, 0.0},
    {20.0,  5.0, 0.0}
};
```



下列程式碼範例顯示如何使用 [**IDirect3DDevice9：:D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)在 Direct3D 9 中轉譯行清單。


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_LINELIST, 0, 3 );
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[基本](primitives.md)
</dt> </dl>

 

 
