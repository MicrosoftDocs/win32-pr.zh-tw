---
description: 描述支援的影像檔案格式。 如需這些格式的說明，請參閱備註。
ms.assetid: 245a0052-f156-44ad-ab46-3677a818167e
title: 'D3DXIMAGE_FILEFORMAT 列舉 (D3dx9tex .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIMAGE_FILEFORMAT
api_type:
- HeaderDef
api_location:
- d3dx9tex.h
ms.openlocfilehash: 3b1195e7503ff32e92cdbafde941b811dcf86427
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322908"
---
# <a name="d3dximage_fileformat-enumeration"></a>D3DXIMAGE \_ >fileformat 列舉

描述支援的影像檔案格式。 如需這些格式的說明，請參閱備註。

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DXIMAGE_FILEFORMAT { 
  D3DXIFF_BMP          = 0,
  D3DXIFF_JPG          = 1,
  D3DXIFF_TGA          = 2,
  D3DXIFF_PNG          = 3,
  D3DXIFF_DDS          = 4,
  D3DXIFF_PPM          = 5,
  D3DXIFF_DIB          = 6,
  D3DXIFF_HDR          = 7,
  D3DXIFF_PFM          = 8,
  D3DXIFF_FORCE_DWORD  = 0x7fffffff
} D3DXIMAGE_FILEFORMAT, *LPD3DXIMAGE_FILEFORMAT;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DXIFF_BMP"></span><span id="d3dxiff_bmp"></span>**D3DXIFF \_ BMP**
</dt> <dd>

Windows 點陣圖 (BMP) 檔案格式。

</dd> <dt>

<span id="D3DXIFF_JPG"></span><span id="d3dxiff_jpg"></span>**D3DXIFF \_ JPG**
</dt> <dd>

聯合 Photographics 專家群組 (JPEG) 壓縮檔案格式。

</dd> <dt>

<span id="D3DXIFF_TGA"></span><span id="d3dxiff_tga"></span>**D3DXIFF \_ TGA**
</dt> <dd>

Truevision (Targa 或 TGA) 影像檔案格式。

</dd> <dt>

<span id="D3DXIFF_PNG"></span><span id="d3dxiff_png"></span>**D3DXIFF \_ PNG**
</dt> <dd>

可移植網狀圖形 (PNG) 檔案格式。

</dd> <dt>

<span id="D3DXIFF_DDS"></span><span id="d3dxiff_dds"></span>**D3DXIFF \_ DDS**
</dt> <dd>

DirectDraw 介面 (DDS) 檔案格式。

</dd> <dt>

<span id="D3DXIFF_PPM"></span><span id="d3dxiff_ppm"></span>**D3DXIFF \_ PPM**
</dt> <dd>

便攜 pixmap (PPM) 檔案格式。

</dd> <dt>

<span id="D3DXIFF_DIB"></span><span id="d3dxiff_dib"></span>**D3DXIFF \_ DIB**
</dt> <dd>

Windows 裝置獨立點陣圖 (DIB) 檔案格式。

</dd> <dt>

<span id="D3DXIFF_HDR"></span><span id="d3dxiff_hdr"></span>**D3DXIFF \_ HDR**
</dt> <dd>

高動態範圍 (HDR) 檔案格式。

</dd> <dt>

<span id="D3DXIFF_PFM"></span><span id="d3dxiff_pfm"></span>**D3DXIFF \_ PFM**
</dt> <dd>

便攜浮點數對應檔案格式。

</dd> <dt>

<span id="D3DXIFF_FORCE_DWORD"></span><span id="d3dxiff_force_dword"></span>**D3DXIFF \_ 強制 \_ DWORD**
</dt> <dd>

強制此列舉的大小編譯為32位。 如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。 不使用這個值。

</dd> </dl>

## <a name="remarks"></a>備註

以 D3DXLoadxxx 開頭的函式支援所有列出的格式。 以 D3DXSavexxx 開頭的函式支援所有列出的格式，除了 Truevision (. tga) 和便攜 pixmap ( ppm) 格式。

下表列出可用的輸入和輸出格式。



| 副檔名 | Description                                                                                                                                                                                                                                                                                                                                        |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| .bmp           | Windows 點陣圖格式。 包含標頭，其描述建立圖元矩形的裝置解析度、矩形的維度、位陣列的大小、邏輯調色板，以及定義點陣圖影像中圖元之間的關聯性，以及邏輯調色板中的專案之間的關聯性的位陣列。 |
| .dds           | DirectDraw 表面檔案格式。 儲存材質、磁片區材質和三層的環境對應、具有或不具有 mipmap 層級，以及具有或不含圖元壓縮。 請參閱 [DDS](../direct3ddds/dx-graphics-dds.md)。                                                                                                                                       |
| .dib           | Windows DIB。 包含與結構結合的位陣列，這些結構會指定點陣圖影像的寬度和高度、建立映射之裝置的色彩格式，以及用來建立該映射的裝置解析度。                                                                                                              |
| 。 hdr           | HDR 格式。 將每個圖元編碼為 RGBE 32 位色彩，紅色、綠色和藍色有8個位的尾數，以及共用的8位指數。 每個通道都會以執行長度編碼方式分別壓縮 (RLE) 。                                                                                                                                       |
| .jpg           | JPEG 標準。 指定24位 RGB 色彩和8位灰階標籤影像檔案格式的可變壓縮 (TIFF) 影像檔案。                                                                                                                                                                                                       |
| .pfm           | 便攜浮點數對應格式。 未經壓縮的原始浮點數影像格式。 檔案標頭會指定影像寬度、高度、單色或色彩，以及電腦文字順序。 圖元資料是以32位浮點數的形式儲存，每個圖元有3個值用於色彩，而一個值為單色的每個圖元。                                |
| .png           | PNG 格式。 使用非失真壓縮的非專屬點陣圖格式。                                                                                                                                                                                                                                                                            |
| ppm           | 可移植的 Pixmap 格式。 包含影像高度和寬度以及最大色彩元件值之彩色影像的二進位或 ASCII 檔案格式。                                                                                                                                                                                                 |
| .tga           | Targa 或 Truevision 圖形介面卡格式。 支援的深度為8、15、16、24和32位（包括8位灰階），並包含選擇性的色板資料、影像 (x、y) 原點和大小的資料，以及圖元資料。                                                                                                                               |



 

如需其中一些格式的詳細資訊，請參閱 [點陣圖類型](../gdiplus/-gdiplus-types-of-bitmaps-about.md) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9tex。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 列舉](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
