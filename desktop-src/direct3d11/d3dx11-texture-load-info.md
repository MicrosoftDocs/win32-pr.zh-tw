---
title: 'D3DX11_TEXTURE_LOAD_INFO 結構 (D3DX11tex .h) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 描述用來從另一個材質載入紋理的參數。
ms.assetid: 2fe24752-d1bc-4666-bf0f-cc397394da56
keywords:
- D3DX11_TEXTURE_LOAD_INFO 結構 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_TEXTURE_LOAD_INFO
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ca893908f854b6b127d783af25cc2fb9bc5df6a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992311"
---
# <a name="d3dx11_texture_load_info-structure"></a>D3DX11 \_ 材質 \_ 載入 \_ 資訊結構

> [!Note]  
> D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。

 

描述用來從另一個材質載入紋理的參數。

## <a name="syntax"></a>語法


```C++
typedef struct _D3DX11_TEXTURE_LOAD_INFO {
  D3D11_BOX *pSrcBox;
  D3D11_BOX *pDstBox;
  UINT      SrcFirstMip;
  UINT      DstFirstMip;
  UINT      NumMips;
  UINT      SrcFirstElement;
  UINT      DstFirstElement;
  UINT      NumElements;
  UINT      Filter;
  UINT      MipFilter;
} D3DX11_TEXTURE_LOAD_INFO;
```



## <a name="members"></a>成員

<dl> <dt>

**pSrcBox**
</dt> <dd>

Type： **[ **D3D11 \_ BOX**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)\***

</dd> <dd>

來源材質方塊 (查看 [**D3D11 \_ box**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)) 。

</dd> <dt>

**pDstBox**
</dt> <dd>

Type： **[ **D3D11 \_ BOX**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)\***

</dd> <dd>

目的地材質方塊 (查看 [**D3D11 \_ box**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)) 。

</dd> <dt>

**SrcFirstMip**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

來源紋理 mipmap 層級，如需詳細資料，請參閱 [**D3D11CalcSubresource**](/windows/desktop/api/D3D11/nf-d3d11-d3d11calcsubresource) 。

</dd> <dt>

**DstFirstMip**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

目的地紋理 mipmap 層級，如需詳細資料，請參閱 [**D3D11CalcSubresource**](/windows/desktop/api/D3D11/nf-d3d11-d3d11calcsubresource) 。

</dd> <dt>

**NumMips**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

來源材質中的 mipmap 層級數目。

</dd> <dt>

**SrcFirstElement**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

來源材質的第一個元素。

</dd> <dt>

**DstFirstElement**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

目的地材質的第一個元素。

</dd> <dt>

**NumElements**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

要載入的元素數目。

</dd> <dt>

**Filter**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

重新取樣期間的篩選選項 (參閱 [**D3DX11 \_ 篩選 \_ 旗**](d3dx11-filter-flag.md) 標) 。

</dd> <dt>

**MipFilter**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

產生 mip 層級時的篩選選項 (參閱 [**D3DX11 \_ 篩選 \_ 旗**](d3dx11-filter-flag.md) 標) 。

</dd> </dl>

## <a name="remarks"></a>備註

呼叫 [**D3DX11LoadTextureFromTexture**](d3dx11loadtexturefromtexture.md)時，會使用此結構。

預設值是：


```
    pSrcBox = NULL;
    pDstBox = NULL;
    SrcFirstMip = 0;
    DstFirstMip = 0;
    NumMips = D3DX11_DEFAULT;
    SrcFirstElement = 0;
    DstFirstElement = 0;
    NumElements = D3DX11_DEFAULT;
    Filter = D3DX11_DEFAULT;
    MipFilter = D3DX11_DEFAULT;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX11tex。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 結構](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 

