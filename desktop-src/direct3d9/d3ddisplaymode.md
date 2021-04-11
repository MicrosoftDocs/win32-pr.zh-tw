---
description: 描述顯示模式。
ms.assetid: e83c03ee-2067-45c9-8fd8-8c4db5558df4
title: 'D3DDISPLAYMODE 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDISPLAYMODE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 8bf73899742f02a9682a3a27319768db894fd682
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116193"
---
# <a name="d3ddisplaymode-structure"></a>D3DDISPLAYMODE 結構

描述顯示模式。

## <a name="syntax"></a>語法


```C++
typedef struct D3DDISPLAYMODE {
  UINT      Width;
  UINT      Height;
  UINT      RefreshRate;
  D3DFORMAT Format;
} D3DDISPLAYMODE, *LPD3DDISPLAYMODE;
```



## <a name="members"></a>成員

<dl> <dt>

**寬度**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

螢幕寬度（以圖元為單位）。

</dd> <dt>

**高度**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

螢幕高度（以圖元為單位）。

</dd> <dt>

**RefreshRate**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

重新整理頻率。 值為0表示介面卡預設值。

</dd> <dt>

**格式**
</dt> <dd>

類型： **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

[D3DFORMAT](d3dformat.md)列舉型別的成員，描述顯示模式的介面格式。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 結構](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes)
</dt> <dt>

[**GetAdapterDisplayMode**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapterdisplaymode)
</dt> <dt>

[**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode)
</dt> </dl>

 

 
