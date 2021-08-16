---
description: 描述用來從另一個材質載入紋理的參數。
ms.assetid: dee693ce-afa7-479b-a76a-00816e30d5cf
title: 'D3DX10_TEXTURE_LOAD_INFO 結構 (D3DX10Tex .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_TEXTURE_LOAD_INFO
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: 144475b4b4967ff0a1fd130a658b8276af5d8897cc043000d150417aa01b227e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753468"
---
# <a name="d3dx10_texture_load_info-structure"></a>D3DX10 \_ 材質 \_ 載入 \_ 資訊結構

描述用來從另一個材質載入紋理的參數。

## <a name="syntax"></a>語法


```C++
typedef struct _D3DX10_TEXTURE_LOAD_INFO {
  D3D10_BOX *pSrcBox;
  D3D10_BOX *pDstBox;
  UINT      SrcFirstMip;
  UINT      DstFirstMip;
  UINT      NumMips;
  UINT      SrcFirstElement;
  UINT      DstFirstElement;
  UINT      NumElements;
  UINT      Filter;
  UINT      MipFilter;
} D3DX10_TEXTURE_LOAD_INFO;
```



## <a name="members"></a>成員

<dl> <dt>

**pSrcBox**
</dt> <dd>

Type： **[ **D3D10 \_ BOX**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)\***

</dd> <dd>

來源材質方塊 (查看 [**D3D10 \_ box**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)) 。

</dd> <dt>

**pDstBox**
</dt> <dd>

Type： **[ **D3D10 \_ BOX**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)\***

</dd> <dd>

目的地材質方塊 (查看 [**D3D10 \_ box**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)) 。

</dd> <dt>

**SrcFirstMip**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

來源紋理 mipmap 層級，如需詳細資料，請參閱 [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource) 。

</dd> <dt>

**DstFirstMip**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

目的地紋理 mipmap 層級，如需詳細資料，請參閱 [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource) 。

</dd> <dt>

**NumMips**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

來源材質中的 mipmap 層級數目。

</dd> <dt>

**SrcFirstElement**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

來源材質的第一個元素。

</dd> <dt>

**DstFirstElement**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

目的地材質的第一個元素。

</dd> <dt>

**NumElements**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

要載入的元素數目。

</dd> <dt>

**Filter**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

重新取樣期間的篩選選項 (參閱 [**D3DX10 \_ 篩選 \_ 旗**](d3dx10-filter-flag.md) 標) 。

</dd> <dt>

**MipFilter**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

產生 mip 層級時的篩選選項 (參閱 [**D3DX10 \_ 篩選 \_ 旗**](d3dx10-filter-flag.md) 標) 。

</dd> </dl>

## <a name="remarks"></a>備註

呼叫 [**D3DX10LoadTextureFromTexture**](d3dx10loadtexturefromtexture.md)時，會使用此結構。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX10Tex。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 結構](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
