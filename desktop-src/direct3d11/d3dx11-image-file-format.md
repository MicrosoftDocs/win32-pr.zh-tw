---
title: 'D3DX11_IMAGE_FILE_FORMAT 列舉 (D3DX11tex .h) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 D3DX11Createxxx 和 D3DX11Savexxx 函數所支援的影像檔案格式。
ms.assetid: 89fa9ab8-3be0-4dc5-a533-94edb01df36a
keywords:
- D3DX11_IMAGE_FILE_FORMAT 列舉 Direct3D 11
- LPD3DX11_IMAGE_FILE_FORMAT 列舉指標 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_IMAGE_FILE_FORMAT
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e34d3ab49987d499114c4b9eee695bfad02055fbbef785a955407e97843208f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118536962"
---
# <a name="d3dx11_image_file_format-enumeration"></a>D3DX11 \_ 圖像 \_ 檔案 \_ 格式列舉

> [!Note]  
> D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，不支援 Windows Store 應用程式。

 

D3DX11Createxxx 和 D3DX11Savexxx 函數所支援的影像檔案格式。

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DX11_IMAGE_FILE_FORMAT { 
  D3DX11_IFF_BMP          = 0,
  D3DX11_IFF_JPG          = 1,
  D3DX11_IFF_PNG          = 3,
  D3DX11_IFF_DDS          = 4,
  D3DX11_IFF_TIFF         = 10,
  D3DX11_IFF_GIF          = 11,
  D3DX11_IFF_WMP          = 12,
  D3DX11_IFF_FORCE_DWORD  = 0x7fffffff
} D3DX11_IMAGE_FILE_FORMAT, *LPD3DX11_IMAGE_FILE_FORMAT;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DX11_IFF_BMP"></span><span id="d3dx11_iff_bmp"></span>**D3DX11 \_ 如果 \_ BMP**
</dt> <dd>

Windows 點陣圖 (BMP) 檔案格式。 包含標頭，其描述建立圖元矩形的裝置解析度、矩形的維度、位陣列的大小、邏輯調色板，以及定義點陣圖影像中圖元之間的關聯性，以及邏輯調色板中的專案之間的關聯性的位陣列。 此格式的副檔名是 .bmp。

</dd> <dt>

<span id="D3DX11_IFF_JPG"></span><span id="d3dx11_iff_jpg"></span>**D3DX11 \_ 如果 \_ JPG**
</dt> <dd>

聯合攝影專家群組 (JPEG) 壓縮檔案格式。 指定24位 RGB 色彩和8位灰階標籤影像檔案格式的可變壓縮 (TIFF) 影像檔案。 此格式的副檔名是 .jpg。

</dd> <dt>

<span id="D3DX11_IFF_PNG"></span><span id="d3dx11_iff_png"></span>**D3DX11 \_ 如果 \_ PNG**
</dt> <dd>

可移植網狀圖形 (PNG) 檔案格式。 使用非失真壓縮的非專屬點陣圖格式。 此格式的副檔名是 .png。

</dd> <dt>

<span id="D3DX11_IFF_DDS"></span><span id="d3dx11_iff_dds"></span>**D3DX11 \_ 如果 \_ DDS**
</dt> <dd>

DirectDraw 介面 (DDS) 檔案格式。 儲存材質、磁片區材質和三層的環境對應、具有或不具有 mipmap 層級，以及具有或不含圖元壓縮。 此格式的副檔名為. dd。

</dd> <dt>

<span id="D3DX11_IFF_TIFF"></span><span id="d3dx11_iff_tiff"></span>**D3DX11 \_ 如果 \_ TIFF**
</dt> <dd>

標記的影像檔案格式 (TIFF) 。 此格式的副檔名為 .tif 和 tiff。

</dd> <dt>

<span id="D3DX11_IFF_GIF"></span><span id="d3dx11_iff_gif"></span>**D3DX11 \_ 如果 \_ GIF**
</dt> <dd>

圖形交換格式 (GIF) 。 此格式的副檔名是 .gif。

</dd> <dt>

<span id="D3DX11_IFF_WMP"></span><span id="d3dx11_iff_wmp"></span>**D3DX11 \_ 如果 \_ WMP**
</dt> <dd>

Windows (WMP) 的媒體相片格式。 這種格式也稱為 HD 相片和 JPEG XR。 此格式的副檔名為. hdp、. jxr 和. wdp。

若要正常運作， **D3DX11 \_ 如果 \_ WMP** 需要您初始化 COM。 因此，請先在您的應用程式中呼叫 [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) 或 [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) ，然後再呼叫 D3DX。

</dd> <dt>

<span id="D3DX11_IFF_FORCE_DWORD"></span><span id="d3dx11_iff_force_dword"></span>**D3DX11 \_ 如果 \_ FORCE \_ DWORD**
</dt> <dd>

強制此列舉的大小編譯為32位。 如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。 不使用這個值。

</dd> </dl>

## <a name="remarks"></a>備註

如需其中一些格式的詳細資訊，請參閱[GDI+) 的點陣圖類型 (](../gdiplus/-gdiplus-types-of-bitmaps-about.md) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX11tex。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 列舉](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

