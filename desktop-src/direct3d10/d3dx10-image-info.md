---
description: D3DX10_IMAGE_INFO 結構-傳回影像檔案原始內容的描述。
ms.assetid: 40d89166-cc11-490d-867c-ae5db23a0784
title: 'D3DX10_IMAGE_INFO 結構 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_IMAGE_INFO
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 228ddf777217e9e61369b0a7fc3b3eb1ca012b1d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105476"
---
# <a name="d3dx10_image_info-structure"></a>D3DX10 \_ 影像 \_ 資訊結構

傳回影像檔案原始內容的描述。

## <a name="syntax"></a>語法


```C++
typedef struct D3DX10_IMAGE_INFO {
  UINT                     Width;
  UINT                     Height;
  UINT                     Depth;
  UINT                     ArraySize;
  UINT                     MipLevels;
  UINT                     MiscFlags;
  DXGI_FORMAT              Format;
  D3D10_RESOURCE_DIMENSION ResourceDimension;
  D3DX10_IMAGE_FILE_FORMAT ImageFileFormat;
} D3DX10_IMAGE_INFO, *LPD3DX10_IMAGE_INFO;
```



## <a name="members"></a>成員

<dl> <dt>

**寬度**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

原始影像的寬度（以圖元為單位）。

</dd> <dt>

**高度**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

原始影像的高度（以圖元為單位）。

</dd> <dt>

**深度**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

原始影像的深度（以圖元為單位）。

</dd> <dt>

[陣列大小]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

材質陣列的大小。 單一映射的 *ArraySize* 會是1。

</dd> <dt>

**MipLevels**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

原始影像中的 mipmap 層級數目。

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

從 [**DXGI \_ 格式**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) 列舉類型到最接近原始影像中資料的值。

</dd> <dt>

**ResourceDimension**
</dt> <dd>

類型： **[ **D3D10 \_ 資源 \_ 維度**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension)**

</dd> <dd>

表示儲存在檔案中的材質類型。 請參閱 [**D3D10 \_ 資源 \_ 維度**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension)。

</dd> <dt>

**ImageFileFormat**
</dt> <dd>

類型： **[ **D3DX10 \_ 圖像 \_ 檔案 \_ 格式**](d3dx10-image-file-format.md)**

</dd> <dd>

代表影像檔案的格式。 請參閱 [**D3DX10 \_ 影像檔案 \_ \_ 格式**](d3dx10-image-file-format.md)。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX10。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 結構](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
