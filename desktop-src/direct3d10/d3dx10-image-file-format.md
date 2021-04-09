---
description: D3DXCreatexxx 和 D3DX10Savexxx 函數所支援的影像檔案格式。
ms.assetid: 39602f3c-5c91-4667-96d0-c3bdba712d88
title: 'D3DX10_IMAGE_FILE_FORMAT 列舉 (D3DX10Tex .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_IMAGE_FILE_FORMAT
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: fba878a40f510cc5e76256161255e01deaa7ee04
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696784"
---
# <a name="d3dx10_image_file_format-enumeration"></a>D3DX10 \_ 圖像 \_ 檔案 \_ 格式列舉

D3DXCreatexxx 和 D3DX10Savexxx 函數所支援的影像檔案格式。

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DX10_IMAGE_FILE_FORMAT { 
  D3DX10_IFF_BMP          = 0,
  D3DX10_IFF_JPG          = 1,
  D3DX10_IFF_PNG          = 3,
  D3DX10_IFF_DDS          = 4,
  D3DX10_IFF_TIFF         = 10,
  D3DX10_IFF_GIF          = 11,
  D3DX10_IFF_WMP          = 12,
  D3DX10_IFF_FORCE_DWORD  = 0x7fffffff
} D3DX10_IMAGE_FILE_FORMAT, *LPD3DX10_IMAGE_FILE_FORMAT;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DX10_IFF_BMP"></span><span id="d3dx10_iff_bmp"></span>**D3DX10 \_ 如果 \_ BMP**
</dt> <dd>

Windows 點陣圖 (BMP) 檔案格式。 包含標頭，其描述建立圖元矩形的裝置解析度、矩形的維度、位陣列的大小、邏輯調色板，以及定義點陣圖影像中圖元之間的關聯性，以及邏輯調色板中的專案之間的關聯性的位陣列。 此格式的副檔名是 .bmp。

</dd> <dt>

<span id="D3DX10_IFF_JPG"></span><span id="d3dx10_iff_jpg"></span>**D3DX10 \_ 如果 \_ JPG**
</dt> <dd>

聯合攝影專家群組 (JPEG) 壓縮檔案格式。 指定24位 RGB 色彩和8位灰階標籤影像檔案格式的可變壓縮 (TIFF) 影像檔案。 此格式的副檔名為 .jpg。

</dd> <dt>

<span id="D3DX10_IFF_PNG"></span><span id="d3dx10_iff_png"></span>**D3DX10 \_ 如果 \_ PNG**
</dt> <dd>

可移植網狀圖形 (PNG) 檔案格式。 使用非失真壓縮的非專屬點陣圖格式。 此格式的副檔名為 .png。

</dd> <dt>

<span id="D3DX10_IFF_DDS"></span><span id="d3dx10_iff_dds"></span>**D3DX10 \_ 如果 \_ DDS**
</dt> <dd>

DirectDraw 介面 (DDS) 檔案格式。 儲存材質、磁片區材質和三層的環境對應、具有或不具有 mipmap 層級，以及具有或不含圖元壓縮。 此格式的副檔名為. dd。

</dd> <dt>

<span id="D3DX10_IFF_TIFF"></span><span id="d3dx10_iff_tiff"></span>**D3DX10 \_ 如果 \_ TIFF**
</dt> <dd>

標記的影像檔案格式 (TIFF) 。 此格式的副檔名為 .tif 和 tiff。

</dd> <dt>

<span id="D3DX10_IFF_GIF"></span><span id="d3dx10_iff_gif"></span>**D3DX10 \_ 如果 \_ GIF**
</dt> <dd>

圖形交換格式 (GIF) 。此格式的副檔名為 .gif。

</dd> <dt>

<span id="D3DX10_IFF_WMP"></span><span id="d3dx10_iff_wmp"></span>**D3DX10 \_ 如果 \_ WMP**
</dt> <dd>

Windows Media Photo 格式 (WMP) 。 這種格式也稱為 HD 相片和 JPEG XR。 此格式的副檔名為. hdp、. jxr 和. wdp。

若要正常運作， **D3DX10 \_ 如果 \_ WMP** 需要您初始化 COM。 因此，請先在您的應用程式中呼叫 [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) 或 [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) ，然後再呼叫 D3DX。

</dd> <dt>

<span id="D3DX10_IFF_FORCE_DWORD"></span><span id="d3dx10_iff_force_dword"></span>**D3DX10 \_ 如果 \_ FORCE \_ DWORD**
</dt> <dd>

強制此列舉的大小編譯為32位。 如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。 不使用這個值。

</dd> </dl>

## <a name="remarks"></a>備註

如需其中一些格式的詳細資訊，請參閱 [點陣圖的類型 (GDI +) ](../gdiplus/-gdiplus-types-of-bitmaps-about.md) 。

D3DX10 利用 Windows 影像處理元件來執行大部分支援的點陣圖檔案類型。 如需其他資訊，請參閱 [Windows 影像處理元件總覽](https://msdn.microsoft.com/library/ms737408.aspx) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX10Tex。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 列舉](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 
