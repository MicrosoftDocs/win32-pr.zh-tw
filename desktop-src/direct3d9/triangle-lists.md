---
description: 三角形清單是隔離三角形的清單。 它們可能會或可能不會彼此接近。 三角形清單必須至少有 3 個頂點，而且頂點總數必須可被 3 整除。
ms.assetid: e5c3470f-361c-458a-a42a-3549c51d8794
title: 三角形清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 230cac9b4120d31821d70db022ab50d311d7b73e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106967026"
---
# <a name="triangle-lists"></a>三角形清單

三角形清單是隔離三角形的清單。 它們可能會或可能不會彼此接近。 三角形清單必須至少有 3 個頂點，而且頂點總數必須可被 3 整除。

使用三角形清單，建立由不相交項目所組成的物件。 例如，建立 3D 遊戲中力場牆的一個方式是指定小、未連接三角形的大型清單。 然後套用看起來會發出光到三角形清單的材質和紋理。 牆中每個三角形看起來會發光。 牆背後的場景透過三角形之間的縫隙變成部分可見，如玩家看向力場時可能的預期。

三角形清單也適用於建立有清晰邊緣並以 Gouraud Shading 呈現陰影的基本類型。 請參閱 [臉部和頂點的一般向量 (Direct3D 9) ](face-and-vertex-normal-vectors.md)。

下圖描述轉譯的三角形清單。

![轉譯三角形清單的圖例](images/trilist.png)

下列程式碼顯示如何建立這個三角形清單的頂點。


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



下列程式碼範例顯示如何使用 [**IDirect3DDevice9：:D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)，在 Direct3D 9 中轉譯此三角形清單。


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, 2 );
```



您也可以使用三角形的條紋來呈現未彼此連接的三角形。 若要這樣做，請指定退化三角形 (也就是清單中) 大小為零的三角形;這將會在兩個三角形之間建立一條線，而不會在轉譯期間出現。 例如，若只要轉譯前一個範例中的第一個和最後一個三角形，請使用下列頂點初始化頂點緩衝區：


```
CUSTOMVERTEX Vertices[] =
{
    {-5.0, -5.0, 0.0},
    { 0.0,  5.0, 0.0},
    { 5.0, -5.0, 0.0},
    { 5.0, -5.0, 0.0}, // degenerate triangle
    {10.0,  5.0, 0.0}, // degenerate triangle
    {10.0,  5.0, 0.0},
    {15.0, -5.0, 0.0},
    {20.0,  5.0, 0.0}
};
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[基本](primitives.md)
</dt> </dl>

 

 
