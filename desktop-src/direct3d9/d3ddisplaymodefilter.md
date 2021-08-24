---
description: 指定要篩選出的顯示模式類型。
ms.assetid: 4a03d0f0-dec5-4209-8c99-b58cc13064f5
title: 'D3DDISPLAYMODEFILTER 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDISPLAYMODEFILTER
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: f59e2e095f7f0f1c6ee73fc940733e932efaef9af7ec05807ff1b38f35fe5189
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751058"
---
# <a name="d3ddisplaymodefilter-structure"></a>D3DDISPLAYMODEFILTER 結構

指定要篩選出的顯示模式類型。

## <a name="syntax"></a>語法


```C++
typedef struct {
  UINT                Size;
  D3DFORMAT           Format;
  D3DSCANLINEORDERING ScanLineOrdering;
} D3DDISPLAYMODEFILTER;
```



## <a name="members"></a>成員

<dl> <dt>

**大小**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

此結構的大小。 這應該一律設定為 sizeof (D3DDISPLAYMODEFILTER) 。

</dd> <dt>

**格式**
</dt> <dd>

類型： **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

要篩選出的顯示模式格式。請參閱 [D3DFORMAT](d3dformat.md)。

</dd> <dt>

**ScanLineOrdering**
</dt> <dd>

類型： **[ **D3DSCANLINEORDERING**](./d3dscanlineordering.md)**

</dd> <dd>

Scanline 順序是否為交錯式或漸進式。 請參閱 [**D3DSCANLINEORDERING**](./d3dscanlineordering.md)。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3d9types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 結構](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
