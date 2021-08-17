---
description: 帶狀線是包含連接的帶狀線的基本類型。
ms.assetid: 73905718-a4c6-4f73-beef-4cccac7eea8c
title: 行條紋
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd8ba98518cac542a9b8272e4f96494889ef24f269744626aa24e882c7af509
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118799627"
---
# <a name="line-strips"></a>行條紋

帶狀線是包含連接的帶狀線的基本類型。 您的應用程式可使用帶狀線建立未閉合之多邊形。 封閉的多邊形是用線段將其最後一個頂點連接到第一個頂點的多邊形。 如果您的應用程式讓多邊形以帶狀線為主，不保證頂點為共面。

下圖顯示呈現的帶狀線。

![帶狀線的圖例](images/linstrip.gif)

下列程式碼顯示如何建立這個帶狀線的頂點。


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



下列程式碼範例示範如何使用 [**IDirect3DDevice9：:D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 在 Direct3D 9 中轉譯行帶。


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_LINESTRIP, 0, 5 );
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[基本](primitives.md)
</dt> </dl>

 

 
