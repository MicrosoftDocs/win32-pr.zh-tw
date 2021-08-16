---
description: 此常數是網格之頂點宣告子的最大數目。
ms.assetid: 234e99a2-1907-4065-b03b-fb9e8d6812ab
title: 'MAX_FVF_DECL_SIZE 列舉 (D3dx9mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MAX_FVF_DECL_SIZE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 52ac939cc77bbd87dbecffc07253f0fadc5cbbdaa48e07f938f163c453c21e14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118798794"
---
# <a name="max_fvf_decl_size-enumeration"></a>最大 \_ FVF \_ DECL \_ 大小列舉

此常數是網格之頂點宣告子的最大數目。

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  MAX_FVF_DECL_SIZE  = MAXD3DDECLLENGTH + 1
} MAX_FVF_DECL_SIZE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="MAX_FVF_DECL_SIZE"></span><span id="max_fvf_decl_size"></span>**最大 \_ FVF \_ DECL \_ 大小**
</dt> <dd>

頂點宣告中的元素數目上限。 額外的 (+ 1) 適用于 [**D3DDECL \_ END**](d3ddecl-end.md)。

</dd> </dl>

## <a name="remarks"></a>備註

MAXD3DDECLLENGTH 定義為最多 64 (請參閱 d3d9types) 。 這不包含 "end" 標記頂點元素。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9mesh。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 列舉](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[**ID3DXBaseMesh**](id3dxbasemesh.md)
</dt> <dt>

[**GetDeclaration**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexdeclaration9-getdeclaration)
</dt> <dt>

[**D3DXDeclaratorFromFVF**](d3dxdeclaratorfromfvf.md)
</dt> <dt>

[**ID3DXSkinInfo**](id3dxskininfo.md)
</dt> </dl>

 

 
