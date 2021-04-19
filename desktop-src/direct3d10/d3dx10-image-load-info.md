---
description: 選擇性地提供材質載入器 Api 的資訊，以控制如何載入紋理。 \_任何這些參數的 D3DX10 預設值都會導致 D3DX 自動使用來源檔案的值。
ms.assetid: 8325d50e-a8a9-4ee2-87e2-e60fb3699af6
title: 'D3DX10_IMAGE_LOAD_INFO 結構 (D3DX10Tex .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_IMAGE_LOAD_INFO
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: 89e819e81c11842feaa6996e047f3cac3587792c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976738"
---
# <a name="d3dx10_image_load_info-structure"></a>D3DX10 \_ 映射 \_ 載入 \_ 資訊結構

選擇性地提供材質載入器 Api 的資訊，以控制如何載入紋理。 \_任何這些參數的 D3DX10 預設值都會導致 D3DX 自動使用來源檔案的值。

## <a name="syntax"></a>語法


```C++
typedef struct D3DX10_IMAGE_LOAD_INFO {
  UINT              Width;
  UINT              Height;
  UINT              Depth;
  UINT              FirstMipLevel;
  UINT              MipLevels;
  D3D10_USAGE       Usage;
  UINT              BindFlags;
  UINT              CpuAccessFlags;
  UINT              MiscFlags;
  DXGI_FORMAT       Format;
  UINT              Filter;
  UINT              MipFilter;
  D3DX10_IMAGE_INFO *pSrcInfo;
} D3DX10_IMAGE_LOAD_INFO, *LPD3DX10_IMAGE_LOAD_INFO;
```



## <a name="members"></a>成員

<dl> <dt>

**寬度**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

材質的目標寬度。 如果材質的實際寬度大於或等於這個值，則紋理會向上或向下調整以符合此目標寬度。

</dd> <dt>

**高度**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

材質的目標高度。 如果紋理的實際高度大於或等於這個值，則紋理會向上或向下調整以符合此目標高度。

</dd> <dt>

**深度**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

材質的深度。 這僅適用于磁片區紋理。

</dd> <dt>

**FirstMipLevel**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

材質的最高解析度 mipmap 層級。 如果大於0，則在載入紋理之後，FirstMipLevel 會對應至 mipmap 層級0。

</dd> <dt>

**MipLevels**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

材質將擁有的最大 mipmap 層級數目。 使用0或 D3DX10 \_ 預設值，將會建立完整的 mipmap 鏈。

</dd> <dt>

**使用量**
</dt> <dd>

類型： **[ **D3D10 \_ 使用** 方式](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)**

</dd> <dd>

材質資源的使用方式。 請參閱 [**D3D10 \_ 使用量**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)。

</dd> <dt>

**BindFlags**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

將允許紋理系結的管線階段。 請參閱 [**D3D10 \_ BIND \_ 旗**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag)標。

</dd> <dt>

**CpuAccessFlags**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Cpu 對材質資源將擁有的存取權限。 請參閱 [**D3D10 \_ CPU \_ 存取 \_ 旗**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag)標。

</dd> <dt>

**MiscFlags**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

其他資源屬性 (參閱 [**D3D10 \_ 資源 \_ 其他 \_ 旗**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag) 標) 。

</dd> <dt>

**格式**
</dt> <dd>

類型： **[ **DXGI \_ 格式**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**

</dd> <dd>

材質載入後將採用的格式。 請參閱 [**DXGI \_ 格式**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)。

</dd> <dt>

**Filter**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

只有在重新取樣) 時，才使用指定的篩選 (篩選材質。 請參閱 [**D3DX10 \_ 篩選 \_ 旗**](d3dx10-filter-flag.md)標。

</dd> <dt>

**MipFilter**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

只有在產生 mipmap) 時，才使用指定的篩選 (來篩選材質 mip 層級。 有效的值為 D3DX10 \_ filter \_ NONE、D3DX10 \_ FILTER \_ POINT、D3DX10 \_ filter \_ 線性或 D3DX10 \_ filter \_ 三角形。 請參閱 [**D3DX10 \_ 篩選 \_ 旗**](d3dx10-filter-flag.md)標。

</dd> <dt>

**pSrcInfo**
</dt> <dd>

類型： **[ **D3DX10 \_ 影像 \_ 資訊**](d3dx10-image-info.md)\***

</dd> <dd>

原始影像的相關資訊。 請參閱 [**D3DX10 \_ 影像 \_ 資訊**](d3dx10-image-info.md)。 可以使用 [**D3DX10GetImageInfoFromFile**](d3dx10getimageinfofromfile.md)、 [**D3DX10GetImageInfoFromMemory**](d3dx10getimageinfofrommemory.md)或 [**D3DX10GetImageInfoFromResource**](d3dx10getimageinfofromresource.md)取得。

</dd> </dl>

## <a name="remarks"></a>備註

在初始化結構時，您可以將任何成員設定為 D3DX10 \_ 預設值，而 D3DX 會在載入紋理時，使用來源材質的預設值將它初始化。

下列 Api 可以使用此結構：

-   建立資源，例如 [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) 和 [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md)。
-   建立資料處理器，例如 [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md) 或 [**D3DX10CreateAsyncShaderResourceViewProcessor**](d3dx10createasyncshaderresourceviewprocessor.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX10Tex。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 結構](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
