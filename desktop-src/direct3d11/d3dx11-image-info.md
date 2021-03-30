---
title: 'D3DX11_IMAGE_INFO 結構 (D3DX11tex .h) '
description: '請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 選擇性地提供材質載入器 Api 的資訊，以控制如何載入紋理。 |D3DX11_IMAGE_INFO 結構 (D3DX11tex .h) '
ms.assetid: 981f4f1d-7609-416a-8f92-c7223d8b2773
keywords:
- D3DX11_IMAGE_INFO 結構 Direct3D 11
- LPD3DX11_IMAGE_INFO 結構指標 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_IMAGE_INFO
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 927967f8e76d0147ccc264bcbdd773191a170ae7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974710"
---
# <a name="d3dx11_image_info-structure"></a>D3DX11 \_ 影像 \_ 資訊結構

> [!Note]  
> D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。

 

選擇性地提供材質載入器 Api 的資訊，以控制如何載入紋理。 \_任何這些參數的 D3DX11 預設值都會導致 D3DX 自動使用來源檔案的值。

## <a name="syntax"></a>語法


```C++
typedef struct D3DX11_IMAGE_INFO {
  UINT                     Width;
  UINT                     Height;
  UINT                     Depth;
  UINT                     ArraySize;
  UINT                     MipLevels;
  UINT                     MiscFlags;
  DXGI_FORMAT              Format;
  D3D11_RESOURCE_DIMENSION ResourceDimension;
  D3DX11_IMAGE_FILE_FORMAT ImageFileFormat;
} D3DX11_IMAGE_INFO, *LPD3DX11_IMAGE_INFO;
```



## <a name="members"></a>成員

<dl> <dt>

**寬度**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

材質的目標寬度。 如果材質的實際寬度大於或等於這個值，則紋理會向上或向下調整以符合此目標寬度。

</dd> <dt>

**高度**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

材質的目標高度。 如果紋理的實際高度大於或等於這個值，則紋理會向上或向下調整以符合此目標高度。

</dd> <dt>

**深度**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

材質的深度。 這僅適用于磁片區紋理。

</dd> <dt>

[陣列大小]
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

陣列中的項目數。

</dd> <dt>

**MipLevels**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

材質中 mipmap 層級的最大數目。 請參閱 [**D3D11 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv)中的備註。 使用0或 D3DX11 \_ 預設值，將會建立完整的 mipmap 鏈。

</dd> <dt>

**MiscFlags**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

使用 [**D3D11 \_ 資源 \_ 其他 \_ 旗**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) 標旗標指定的其他資源屬性。

</dd> <dt>

**格式**
</dt> <dd>

類型： **[ **DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

</dd> <dd>

一個 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 列舉，用來指定材質載入後的材質格式。

</dd> <dt>

**ResourceDimension**
</dt> <dd>

類型： **[ **D3D11 \_ 資源 \_ 維度**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension)**

</dd> <dd>

識別資源類型的 [**D3D11 \_ 資源 \_ 維度**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension) 值。

</dd> <dt>

**ImageFileFormat**
</dt> <dd>

類型： **[ **D3DX11 \_ 圖像 \_ 檔案 \_ 格式**](d3dx11-image-file-format.md)**

</dd> <dd>

用來識別影像格式的 [**D3DX11 \_ 圖像 \_ 檔案 \_ 格式**](d3dx11-image-file-format.md) 值。

</dd> </dl>

## <a name="remarks"></a>備註

此結構是由方法所使用，例如： [**D3DX11GetImageInfoFromFile**](d3dx11getimageinfofromfile.md)、 [**D3DX11GetImageInfoFromMemory**](d3dx11getimageinfofrommemory.md)或 [**D3DX11GetImageInfoFromResource**](d3dx11getimageinfofromresource.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX11tex。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 結構](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 

