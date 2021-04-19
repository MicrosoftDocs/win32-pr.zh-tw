---
description: 顯示模式屬性的相關資訊。
ms.assetid: df9d12b9-7acb-435b-9d54-0b095c871f0e
title: 'D3DDISPLAYMODEEX 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDISPLAYMODEEX
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 5906b6b23cc83e6d2379f0c5923b08b220285708
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976470"
---
# <a name="d3ddisplaymodeex-structure"></a>D3DDISPLAYMODEEX 結構

顯示模式屬性的相關資訊。

## <a name="syntax"></a>語法


```C++
typedef struct {
  UINT                Size;
  UINT                Width;
  UINT                Height;
  UINT                RefreshRate;
  D3DFORMAT           Format;
  D3DSCANLINEORDERING ScanLineOrdering;
} D3DDISPLAYMODEEX;
```



## <a name="members"></a>成員

<dl> <dt>

**大小**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

此結構的大小。 這應該一律設定為 sizeof (D3DDISPLAYMODEEX) 。

</dd> <dt>

**寬度**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

顯示模式的寬度。

</dd> <dt>

**高度**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

顯示模式的高度。

</dd> <dt>

**RefreshRate**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

顯示模式的更新速率。

</dd> <dt>

**格式**
</dt> <dd>

類型： **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

顯示模式的格式。 請參閱 [D3DFORMAT](d3dformat.md)。

</dd> <dt>

**ScanLineOrdering**
</dt> <dd>

類型： **[ **D3DSCANLINEORDERING**](./d3dscanlineordering.md)**

</dd> <dd>

指出 scanline 順序是漸進式或交錯式。 請參閱 [**D3DSCANLINEORDERING**](./d3dscanlineordering.md)。

</dd> </dl>

## <a name="remarks"></a>備註

此結構用於各種方法中，以建立和管理 Direct3D 9Ex 裝置 ([**IDirect3DDevice9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex)) 和 Swapchains ([**IDirect3DSwapChain9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dswapchain9ex)) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3d9types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 結構](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
