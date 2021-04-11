---
description: 描述 ID3DXRenderToEnvMap 實例所使用的非畫面呈現目標。
ms.assetid: 805df4da-e882-4d54-bf2c-49cfcbc59ac6
title: 'D3DXRTE_DESC 結構 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXRTE_DESC
api_type:
- HeaderDef
api_location:
- d3dx9core.h
ms.openlocfilehash: 69a5957bc9338abac4441f65066a43efb7dabead
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196245"
---
# <a name="d3dxrte_desc-structure"></a>D3DXRTE \_ DESC 結構

描述 [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md)實例所使用的非畫面呈現目標。

## <a name="syntax"></a>語法


```C++
typedef struct D3DXRTE_DESC {
  UINT      Size;
  UINT      MipLevels;
  D3DFORMAT Format;
  BOOL      DepthStencil;
  D3DFORMAT DepthStencilFormat;
} D3DXRTE_DESC, *LPD3DXRTE_DESC;
```



## <a name="members"></a>成員

<dl> <dt>

**大小**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

寬度和高度（以圖元為單位）。

</dd> <dt>

**MipLevels**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

詳細資料層級 (」 LOD) 的最大值。

</dd> <dt>

**格式**
</dt> <dd>

類型： **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

色彩緩衝區格式。

</dd> <dt>

**DepthStencil**
</dt> <dd>

類型： **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

指出是否需要 z 緩衝區。

</dd> <dt>

**DepthStencilFormat**
</dt> <dd>

類型： **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

深度緩衝區的格式。

</dd> </dl>

## <a name="remarks"></a>備註

這個方法是用來傳回建立 [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md) 物件時所使用的建立參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9core。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 結構](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
