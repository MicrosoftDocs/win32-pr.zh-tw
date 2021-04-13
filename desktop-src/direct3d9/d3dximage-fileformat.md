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
# <a name="d3dximage_fileformat-enumeration"></a><span data-ttu-id="dd675-104">D3DXIMAGE \_ >fileformat 列舉</span><span class="sxs-lookup"><span data-stu-id="dd675-104">D3DXIMAGE\_FILEFORMAT enumeration</span></span>

<span data-ttu-id="dd675-105">描述支援的影像檔案格式。</span><span class="sxs-lookup"><span data-stu-id="dd675-105">Describes the supported image file formats.</span></span> <span data-ttu-id="dd675-106">如需這些格式的說明，請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="dd675-106">See Remarks for descriptions of these formats.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd675-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd675-107">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="dd675-108">常數</span><span class="sxs-lookup"><span data-stu-id="dd675-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="dd675-109"><span id="D3DXIFF_BMP"></span><span id="d3dxiff_bmp"></span>**D3DXIFF \_ BMP**</span><span class="sxs-lookup"><span data-stu-id="dd675-109"><span id="D3DXIFF_BMP"></span><span id="d3dxiff_bmp"></span>**D3DXIFF\_BMP**</span></span>
</dt> <dd>

<span data-ttu-id="dd675-110">Windows 點陣圖 (BMP) 檔案格式。</span><span class="sxs-lookup"><span data-stu-id="dd675-110">Windows bitmap (BMP) file format.</span></span>

</dd> <dt>

<span data-ttu-id="dd675-111"><span id="D3DXIFF_JPG"></span><span id="d3dxiff_jpg"></span>**D3DXIFF \_ JPG**</span><span class="sxs-lookup"><span data-stu-id="dd675-111"><span id="D3DXIFF_JPG"></span><span id="d3dxiff_jpg"></span>**D3DXIFF\_JPG**</span></span>
</dt> <dd>

<span data-ttu-id="dd675-112">聯合 Photographics 專家群組 (JPEG) 壓縮檔案格式。</span><span class="sxs-lookup"><span data-stu-id="dd675-112">Joint Photographics Experts Group (JPEG) compressed file format.</span></span>

</dd> <dt>

<span data-ttu-id="dd675-113"><span id="D3DXIFF_TGA"></span><span id="d3dxiff_tga"></span>**D3DXIFF \_ TGA**</span><span class="sxs-lookup"><span data-stu-id="dd675-113"><span id="D3DXIFF_TGA"></span><span id="d3dxiff_tga"></span>**D3DXIFF\_TGA**</span></span>
</dt> <dd>

<span data-ttu-id="dd675-114">Truevision (Targa 或 TGA) 影像檔案格式。</span><span class="sxs-lookup"><span data-stu-id="dd675-114">Truevision (Targa, or TGA) image file format.</span></span>

</dd> <dt>

<span data-ttu-id="dd675-115"><span id="D3DXIFF_PNG"></span><span id="d3dxiff_png"></span>**D3DXIFF \_ PNG**</span><span class="sxs-lookup"><span data-stu-id="dd675-115"><span id="D3DXIFF_PNG"></span><span id="d3dxiff_png"></span>**D3DXIFF\_PNG**</span></span>
</dt> <dd>

<span data-ttu-id="dd675-116">可移植網狀圖形 (PNG) 檔案格式。</span><span class="sxs-lookup"><span data-stu-id="dd675-116">Portable Network Graphics (PNG) file format.</span></span>

</dd> <dt>

<span data-ttu-id="dd675-117"><span id="D3DXIFF_DDS"></span><span id="d3dxiff_dds"></span>**D3DXIFF \_ DDS**</span><span class="sxs-lookup"><span data-stu-id="dd675-117"><span id="D3DXIFF_DDS"></span><span id="d3dxiff_dds"></span>**D3DXIFF\_DDS**</span></span>
</dt> <dd>

<span data-ttu-id="dd675-118">DirectDraw 介面 (DDS) 檔案格式。</span><span class="sxs-lookup"><span data-stu-id="dd675-118">DirectDraw surface (DDS) file format.</span></span>

</dd> <dt>

<span data-ttu-id="dd675-119"><span id="D3DXIFF_PPM"></span><span id="d3dxiff_ppm"></span>**D3DXIFF \_ PPM**</span><span class="sxs-lookup"><span data-stu-id="dd675-119"><span id="D3DXIFF_PPM"></span><span id="d3dxiff_ppm"></span>**D3DXIFF\_PPM**</span></span>
</dt> <dd>

<span data-ttu-id="dd675-120">便攜 pixmap (PPM) 檔案格式。</span><span class="sxs-lookup"><span data-stu-id="dd675-120">Portable pixmap (PPM) file format.</span></span>

</dd> <dt>

<span data-ttu-id="dd675-121"><span id="D3DXIFF_DIB"></span><span id="d3dxiff_dib"></span>**D3DXIFF \_ DIB**</span><span class="sxs-lookup"><span data-stu-id="dd675-121"><span id="D3DXIFF_DIB"></span><span id="d3dxiff_dib"></span>**D3DXIFF\_DIB**</span></span>
</dt> <dd>

<span data-ttu-id="dd675-122">Windows 裝置獨立點陣圖 (DIB) 檔案格式。</span><span class="sxs-lookup"><span data-stu-id="dd675-122">Windows device-independent bitmap (DIB) file format.</span></span>

</dd> <dt>

<span data-ttu-id="dd675-123"><span id="D3DXIFF_HDR"></span><span id="d3dxiff_hdr"></span>**D3DXIFF \_ HDR**</span><span class="sxs-lookup"><span data-stu-id="dd675-123"><span id="D3DXIFF_HDR"></span><span id="d3dxiff_hdr"></span>**D3DXIFF\_HDR**</span></span>
</dt> <dd>

<span data-ttu-id="dd675-124">高動態範圍 (HDR) 檔案格式。</span><span class="sxs-lookup"><span data-stu-id="dd675-124">High dynamic range (HDR) file format.</span></span>

</dd> <dt>

<span data-ttu-id="dd675-125"><span id="D3DXIFF_PFM"></span><span id="d3dxiff_pfm"></span>**D3DXIFF \_ PFM**</span><span class="sxs-lookup"><span data-stu-id="dd675-125"><span id="D3DXIFF_PFM"></span><span id="d3dxiff_pfm"></span>**D3DXIFF\_PFM**</span></span>
</dt> <dd>

<span data-ttu-id="dd675-126">便攜浮點數對應檔案格式。</span><span class="sxs-lookup"><span data-stu-id="dd675-126">Portable float map file format.</span></span>

</dd> <dt>

<span data-ttu-id="dd675-127"><span id="D3DXIFF_FORCE_DWORD"></span><span id="d3dxiff_force_dword"></span>**D3DXIFF \_ 強制 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="dd675-127"><span id="D3DXIFF_FORCE_DWORD"></span><span id="d3dxiff_force_dword"></span>**D3DXIFF\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="dd675-128">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="dd675-128">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="dd675-129">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="dd675-129">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="dd675-130">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="dd675-130">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dd675-131">備註</span><span class="sxs-lookup"><span data-stu-id="dd675-131">Remarks</span></span>

<span data-ttu-id="dd675-132">以 D3DXLoadxxx 開頭的函式支援所有列出的格式。</span><span class="sxs-lookup"><span data-stu-id="dd675-132">Functions that begin with D3DXLoadxxx support all of the formats listed.</span></span> <span data-ttu-id="dd675-133">以 D3DXSavexxx 開頭的函式支援所有列出的格式，除了 Truevision (. tga) 和便攜 pixmap ( ppm) 格式。</span><span class="sxs-lookup"><span data-stu-id="dd675-133">Functions that begin with D3DXSavexxx support all of the formats listed except the Truevision (.tga) and portable pixmap (.ppm) formats.</span></span>

<span data-ttu-id="dd675-134">下表列出可用的輸入和輸出格式。</span><span class="sxs-lookup"><span data-stu-id="dd675-134">The following table lists the available input and output formats.</span></span>



| <span data-ttu-id="dd675-135">副檔名</span><span class="sxs-lookup"><span data-stu-id="dd675-135">File Extension</span></span> | <span data-ttu-id="dd675-136">Description</span><span class="sxs-lookup"><span data-stu-id="dd675-136">Description</span></span>                                                                                                                                                                                                                                                                                                                                        |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd675-137">.bmp</span><span class="sxs-lookup"><span data-stu-id="dd675-137">.bmp</span></span>           | <span data-ttu-id="dd675-138">Windows 點陣圖格式。</span><span class="sxs-lookup"><span data-stu-id="dd675-138">Windows bitmap format.</span></span> <span data-ttu-id="dd675-139">包含標頭，其描述建立圖元矩形的裝置解析度、矩形的維度、位陣列的大小、邏輯調色板，以及定義點陣圖影像中圖元之間的關聯性，以及邏輯調色板中的專案之間的關聯性的位陣列。</span><span class="sxs-lookup"><span data-stu-id="dd675-139">Contains a header that describes the resolution of the device on which the rectangle of pixels was created, the dimensions of the rectangle, the size of the array of bits, a logical palette, and an array of bits that defines the relationship between pixels in the bitmapped image and entries in the logical palette.</span></span> |
| <span data-ttu-id="dd675-140">.dds</span><span class="sxs-lookup"><span data-stu-id="dd675-140">.dds</span></span>           | <span data-ttu-id="dd675-141">DirectDraw 表面檔案格式。</span><span class="sxs-lookup"><span data-stu-id="dd675-141">DirectDraw Surface file format.</span></span> <span data-ttu-id="dd675-142">儲存材質、磁片區材質和三層的環境對應、具有或不具有 mipmap 層級，以及具有或不含圖元壓縮。</span><span class="sxs-lookup"><span data-stu-id="dd675-142">Stores textures, volume textures, and cubic environment maps, with or without mipmap levels, and with or without pixel compression.</span></span> <span data-ttu-id="dd675-143">請參閱 [DDS](../direct3ddds/dx-graphics-dds.md)。</span><span class="sxs-lookup"><span data-stu-id="dd675-143">See [DDS](../direct3ddds/dx-graphics-dds.md).</span></span>                                                                                                                                       |
| <span data-ttu-id="dd675-144">.dib</span><span class="sxs-lookup"><span data-stu-id="dd675-144">.dib</span></span>           | <span data-ttu-id="dd675-145">Windows DIB。</span><span class="sxs-lookup"><span data-stu-id="dd675-145">Windows DIB.</span></span> <span data-ttu-id="dd675-146">包含與結構結合的位陣列，這些結構會指定點陣圖影像的寬度和高度、建立映射之裝置的色彩格式，以及用來建立該映射的裝置解析度。</span><span class="sxs-lookup"><span data-stu-id="dd675-146">Contains an array of bits combined with structures that specify width and height of the bitmapped image, color format of the device where the image was created, and resolution of the device used to create that image.</span></span>                                                                                                              |
| <span data-ttu-id="dd675-147">。 hdr</span><span class="sxs-lookup"><span data-stu-id="dd675-147">.hdr</span></span>           | <span data-ttu-id="dd675-148">HDR 格式。</span><span class="sxs-lookup"><span data-stu-id="dd675-148">HDR format.</span></span> <span data-ttu-id="dd675-149">將每個圖元編碼為 RGBE 32 位色彩，紅色、綠色和藍色有8個位的尾數，以及共用的8位指數。</span><span class="sxs-lookup"><span data-stu-id="dd675-149">Encodes each pixel as an RGBE 32-bit color, with 8 bits of mantissa for red, green, and blue, and a shared 8-bit exponent.</span></span> <span data-ttu-id="dd675-150">每個通道都會以執行長度編碼方式分別壓縮 (RLE) 。</span><span class="sxs-lookup"><span data-stu-id="dd675-150">Each channel is separately compressed with run-length encoding (RLE).</span></span>                                                                                                                                       |
| <span data-ttu-id="dd675-151">.jpg</span><span class="sxs-lookup"><span data-stu-id="dd675-151">.jpg</span></span>           | <span data-ttu-id="dd675-152">JPEG 標準。</span><span class="sxs-lookup"><span data-stu-id="dd675-152">JPEG standard.</span></span> <span data-ttu-id="dd675-153">指定24位 RGB 色彩和8位灰階標籤影像檔案格式的可變壓縮 (TIFF) 影像檔案。</span><span class="sxs-lookup"><span data-stu-id="dd675-153">Specifies variable compression of 24-bit RGB color and 8-bit gray-scale Tagged Image File Format (TIFF) image document files.</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="dd675-154">.pfm</span><span class="sxs-lookup"><span data-stu-id="dd675-154">.pfm</span></span>           | <span data-ttu-id="dd675-155">便攜浮點數對應格式。</span><span class="sxs-lookup"><span data-stu-id="dd675-155">Portable float map format.</span></span> <span data-ttu-id="dd675-156">未經壓縮的原始浮點數影像格式。</span><span class="sxs-lookup"><span data-stu-id="dd675-156">A raw floating point image format, without any compression.</span></span> <span data-ttu-id="dd675-157">檔案標頭會指定影像寬度、高度、單色或色彩，以及電腦文字順序。</span><span class="sxs-lookup"><span data-stu-id="dd675-157">The file header specifies image width, height, monochrome or color, and machine word order.</span></span> <span data-ttu-id="dd675-158">圖元資料是以32位浮點數的形式儲存，每個圖元有3個值用於色彩，而一個值為單色的每個圖元。</span><span class="sxs-lookup"><span data-stu-id="dd675-158">Pixel data is stored as 32-bit floating point values, with 3 values per pixel for color, and one value per pixel for monochrome.</span></span>                                |
| <span data-ttu-id="dd675-159">.png</span><span class="sxs-lookup"><span data-stu-id="dd675-159">.png</span></span>           | <span data-ttu-id="dd675-160">PNG 格式。</span><span class="sxs-lookup"><span data-stu-id="dd675-160">PNG format.</span></span> <span data-ttu-id="dd675-161">使用非失真壓縮的非專屬點陣圖格式。</span><span class="sxs-lookup"><span data-stu-id="dd675-161">A non-proprietary bitmap format using lossless compression.</span></span>                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="dd675-162">ppm</span><span class="sxs-lookup"><span data-stu-id="dd675-162">.ppm</span></span>           | <span data-ttu-id="dd675-163">可移植的 Pixmap 格式。</span><span class="sxs-lookup"><span data-stu-id="dd675-163">Portable Pixmap format.</span></span> <span data-ttu-id="dd675-164">包含影像高度和寬度以及最大色彩元件值之彩色影像的二進位或 ASCII 檔案格式。</span><span class="sxs-lookup"><span data-stu-id="dd675-164">A binary or ASCII file format for color images that includes image height and width and the maximum color component value.</span></span>                                                                                                                                                                                                 |
| <span data-ttu-id="dd675-165">.tga</span><span class="sxs-lookup"><span data-stu-id="dd675-165">.tga</span></span>           | <span data-ttu-id="dd675-166">Targa 或 Truevision 圖形介面卡格式。</span><span class="sxs-lookup"><span data-stu-id="dd675-166">Targa or Truevision Graphics Adapter format.</span></span> <span data-ttu-id="dd675-167">支援的深度為8、15、16、24和32位（包括8位灰階），並包含選擇性的色板資料、影像 (x、y) 原點和大小的資料，以及圖元資料。</span><span class="sxs-lookup"><span data-stu-id="dd675-167">Supports depths of 8, 15, 16, 24, and 32 bits, including 8-bit gray scale, and contains optional color palette data, image (x, y) origin and size data, and pixel data.</span></span>                                                                                                                               |



 

<span data-ttu-id="dd675-168">如需其中一些格式的詳細資訊，請參閱 [點陣圖類型](../gdiplus/-gdiplus-types-of-bitmaps-about.md) 。</span><span class="sxs-lookup"><span data-stu-id="dd675-168">See [Types of Bitmaps](../gdiplus/-gdiplus-types-of-bitmaps-about.md) for more information on some of these formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd675-169">規格需求</span><span class="sxs-lookup"><span data-stu-id="dd675-169">Requirements</span></span>



| <span data-ttu-id="dd675-170">需求</span><span class="sxs-lookup"><span data-stu-id="dd675-170">Requirement</span></span> | <span data-ttu-id="dd675-171">值</span><span class="sxs-lookup"><span data-stu-id="dd675-171">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dd675-172">標頭</span><span class="sxs-lookup"><span data-stu-id="dd675-172">Header</span></span><br/> | <dl> <span data-ttu-id="dd675-173"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="dd675-173"><dt>D3dx9tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd675-174">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dd675-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd675-175">D3DX 列舉</span><span class="sxs-lookup"><span data-stu-id="dd675-175">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
