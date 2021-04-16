---
description: 三角形連環是一系列的連接三角形。
ms.assetid: 3923c570-47a4-4b53-a097-731981380ae0
title: 三角形條紋
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2766529a37b994e5fe30815ca6300476f06c7d4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104567450"
---
# <a name="triangle-strips"></a>三角形條紋

三角形連環是一系列的連接三角形。 因為是連接三角形，應用程式不需要重複指定每個三角形的所有三個頂點。 例如，您只需要七個頂點即可定義下列三角形連環。

![使用七個頂點的三角形連環的圖例](images/tristrip.png)

系統會使用頂點 v1、v2 及 v3 繪製第一個三角形；v2、v4 及 v3 繪製第二個三角形；v3、v4 及 v5 繪製第三個；v4、v6 及 v5 繪製第四個，以此類推。 請注意，第二個和第四個三角形的頂點失序，這是確保所有三角形都是以順時針方向繪製。

3D 場景中的大多數物件都是由三角形連環組成。 這是因為三角形連環可用於以有效率使用記憶體和處理時間的方式指定複雜物件。

下圖描述轉譯的三角形連環。

![轉譯三角形連環的圖例](images/tstrip2.png)

下列程式碼顯示如何建立這個三角形連環的頂點。


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



下列程式碼範例示範如何使用 [**IDirect3DDevice9：:D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)，在 Direct3D 9 中轉譯這個三角形的條紋。


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_TRIANGLESTRIP, 0, 4);
```



使用三角形帶狀轉譯未彼此連接的三角形。 若要這樣做，請指定退化三角形 (也就是在三角形清單中，其區域為零) 的三角形。 這會在兩個不會轉譯的三角形之間建立線條。 若只要轉譯前一個範例中的第一個和最後一個三角形，請修改頂點緩衝區，如下所示：


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

 

 
