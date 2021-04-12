---
description: 描述呈現介面。
ms.assetid: cffa1555-1fa2-427d-8bcb-da0e61d82152
title: 'D3DXRTS_DESC 結構 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXRTS_DESC
api_type:
- HeaderDef
api_location:
- d3dx9core.h
ms.openlocfilehash: 3a0b52f258956f7b62734ca97cc5d1bf5ed00ac3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946089"
---
# <a name="d3dxrts_desc-structure"></a>D3DXRTS \_ DESC 結構

描述呈現介面。

## <a name="syntax"></a>語法


```C++
typedef struct D3DXRTS_DESC {
  UINT      Width;
  UINT      Height;
  D3DFORMAT Format;
  BOOL      DepthStencil;
  D3DFORMAT DepthStencilFormat;
} D3DXRTS_DESC, *LPD3DXRTS_DESC;
```



## <a name="members"></a>成員

<dl> <dt>

**寬度**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

呈現介面的寬度（以圖元為單位）。

</dd> <dt>

**高度**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

轉譯介面的高度（以圖元為單位）。

</dd> <dt>

**格式**
</dt> <dd>

類型： **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

[D3DFORMAT](d3dformat.md)列舉型別的成員，描述呈現介面的像素格式。

</dd> <dt>

**DepthStencil**
</dt> <dd>

類型： **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

若 **為 TRUE**，表示呈現介面支援深度樣板表面;否則，此成員會設定為 **FALSE**。

</dd> <dt>

**DepthStencilFormat**
</dt> <dd>

類型： **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

如果 DepthStencil 設定為 **TRUE**，這個參數就是 [D3DFORMAT](d3dformat.md) 列舉型別的成員，它會描述呈現介面的深度樣板格式。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9core。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 結構](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**ID3DXRenderToSurface::GetDesc**](id3dxrendertosurface--getdesc.md)
</dt> </dl>

 

 
