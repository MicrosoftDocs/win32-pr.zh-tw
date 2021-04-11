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
# <a name="d3dx10_image_file_format-enumeration"></a><span data-ttu-id="a43a4-103">D3DX10 \_ 圖像 \_ 檔案 \_ 格式列舉</span><span class="sxs-lookup"><span data-stu-id="a43a4-103">D3DX10\_IMAGE\_FILE\_FORMAT enumeration</span></span>

<span data-ttu-id="a43a4-104">D3DXCreatexxx 和 D3DX10Savexxx 函數所支援的影像檔案格式。</span><span class="sxs-lookup"><span data-stu-id="a43a4-104">Image file formats supported by D3DXCreatexxx and D3DX10Savexxx functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="a43a4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a43a4-105">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="a43a4-106">常數</span><span class="sxs-lookup"><span data-stu-id="a43a4-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a43a4-107"><span id="D3DX10_IFF_BMP"></span><span id="d3dx10_iff_bmp"></span>**D3DX10 \_ 如果 \_ BMP**</span><span class="sxs-lookup"><span data-stu-id="a43a4-107"><span id="D3DX10_IFF_BMP"></span><span id="d3dx10_iff_bmp"></span>**D3DX10\_IFF\_BMP**</span></span>
</dt> <dd>

<span data-ttu-id="a43a4-108">Windows 點陣圖 (BMP) 檔案格式。</span><span class="sxs-lookup"><span data-stu-id="a43a4-108">Windows bitmap (BMP) file format.</span></span> <span data-ttu-id="a43a4-109">包含標頭，其描述建立圖元矩形的裝置解析度、矩形的維度、位陣列的大小、邏輯調色板，以及定義點陣圖影像中圖元之間的關聯性，以及邏輯調色板中的專案之間的關聯性的位陣列。</span><span class="sxs-lookup"><span data-stu-id="a43a4-109">Contains a header that describes the resolution of the device on which the rectangle of pixels was created, the dimensions of the rectangle, the size of the array of bits, a logical palette, and an array of bits that defines the relationship between pixels in the bitmapped image and entries in the logical palette.</span></span> <span data-ttu-id="a43a4-110">此格式的副檔名是 .bmp。</span><span class="sxs-lookup"><span data-stu-id="a43a4-110">The file extension for this format is .bmp.</span></span>

</dd> <dt>

<span data-ttu-id="a43a4-111"><span id="D3DX10_IFF_JPG"></span><span id="d3dx10_iff_jpg"></span>**D3DX10 \_ 如果 \_ JPG**</span><span class="sxs-lookup"><span data-stu-id="a43a4-111"><span id="D3DX10_IFF_JPG"></span><span id="d3dx10_iff_jpg"></span>**D3DX10\_IFF\_JPG**</span></span>
</dt> <dd>

<span data-ttu-id="a43a4-112">聯合攝影專家群組 (JPEG) 壓縮檔案格式。</span><span class="sxs-lookup"><span data-stu-id="a43a4-112">Joint Photographic Experts Group (JPEG) compressed file format.</span></span> <span data-ttu-id="a43a4-113">指定24位 RGB 色彩和8位灰階標籤影像檔案格式的可變壓縮 (TIFF) 影像檔案。</span><span class="sxs-lookup"><span data-stu-id="a43a4-113">Specifies variable compression of 24-bit RGB color and 8-bit gray-scale Tagged Image File Format (TIFF) image document files.</span></span> <span data-ttu-id="a43a4-114">此格式的副檔名為 .jpg。</span><span class="sxs-lookup"><span data-stu-id="a43a4-114">The file extension for this format is .jpg.</span></span>

</dd> <dt>

<span data-ttu-id="a43a4-115"><span id="D3DX10_IFF_PNG"></span><span id="d3dx10_iff_png"></span>**D3DX10 \_ 如果 \_ PNG**</span><span class="sxs-lookup"><span data-stu-id="a43a4-115"><span id="D3DX10_IFF_PNG"></span><span id="d3dx10_iff_png"></span>**D3DX10\_IFF\_PNG**</span></span>
</dt> <dd>

<span data-ttu-id="a43a4-116">可移植網狀圖形 (PNG) 檔案格式。</span><span class="sxs-lookup"><span data-stu-id="a43a4-116">Portable Network Graphics (PNG) file format.</span></span> <span data-ttu-id="a43a4-117">使用非失真壓縮的非專屬點陣圖格式。</span><span class="sxs-lookup"><span data-stu-id="a43a4-117">A non-proprietary bitmap format using lossless compression.</span></span> <span data-ttu-id="a43a4-118">此格式的副檔名為 .png。</span><span class="sxs-lookup"><span data-stu-id="a43a4-118">The file extension for this format is .png.</span></span>

</dd> <dt>

<span data-ttu-id="a43a4-119"><span id="D3DX10_IFF_DDS"></span><span id="d3dx10_iff_dds"></span>**D3DX10 \_ 如果 \_ DDS**</span><span class="sxs-lookup"><span data-stu-id="a43a4-119"><span id="D3DX10_IFF_DDS"></span><span id="d3dx10_iff_dds"></span>**D3DX10\_IFF\_DDS**</span></span>
</dt> <dd>

<span data-ttu-id="a43a4-120">DirectDraw 介面 (DDS) 檔案格式。</span><span class="sxs-lookup"><span data-stu-id="a43a4-120">DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="a43a4-121">儲存材質、磁片區材質和三層的環境對應、具有或不具有 mipmap 層級，以及具有或不含圖元壓縮。</span><span class="sxs-lookup"><span data-stu-id="a43a4-121">Stores textures, volume textures, and cubic environment maps, with or without mipmap levels, and with or without pixel compression.</span></span> <span data-ttu-id="a43a4-122">此格式的副檔名為. dd。</span><span class="sxs-lookup"><span data-stu-id="a43a4-122">The file extension for this format is .dds.</span></span>

</dd> <dt>

<span data-ttu-id="a43a4-123"><span id="D3DX10_IFF_TIFF"></span><span id="d3dx10_iff_tiff"></span>**D3DX10 \_ 如果 \_ TIFF**</span><span class="sxs-lookup"><span data-stu-id="a43a4-123"><span id="D3DX10_IFF_TIFF"></span><span id="d3dx10_iff_tiff"></span>**D3DX10\_IFF\_TIFF**</span></span>
</dt> <dd>

<span data-ttu-id="a43a4-124">標記的影像檔案格式 (TIFF) 。</span><span class="sxs-lookup"><span data-stu-id="a43a4-124">Tagged Image File Format (TIFF).</span></span> <span data-ttu-id="a43a4-125">此格式的副檔名為 .tif 和 tiff。</span><span class="sxs-lookup"><span data-stu-id="a43a4-125">The file extensions for this format are .tif and .tiff.</span></span>

</dd> <dt>

<span data-ttu-id="a43a4-126"><span id="D3DX10_IFF_GIF"></span><span id="d3dx10_iff_gif"></span>**D3DX10 \_ 如果 \_ GIF**</span><span class="sxs-lookup"><span data-stu-id="a43a4-126"><span id="D3DX10_IFF_GIF"></span><span id="d3dx10_iff_gif"></span>**D3DX10\_IFF\_GIF**</span></span>
</dt> <dd>

<span data-ttu-id="a43a4-127">圖形交換格式 (GIF) 。此格式的副檔名為 .gif。</span><span class="sxs-lookup"><span data-stu-id="a43a4-127">Graphics Interchange Format (GIF).The file extension for this format is .gif.</span></span>

</dd> <dt>

<span data-ttu-id="a43a4-128"><span id="D3DX10_IFF_WMP"></span><span id="d3dx10_iff_wmp"></span>**D3DX10 \_ 如果 \_ WMP**</span><span class="sxs-lookup"><span data-stu-id="a43a4-128"><span id="D3DX10_IFF_WMP"></span><span id="d3dx10_iff_wmp"></span>**D3DX10\_IFF\_WMP**</span></span>
</dt> <dd>

<span data-ttu-id="a43a4-129">Windows Media Photo 格式 (WMP) 。</span><span class="sxs-lookup"><span data-stu-id="a43a4-129">Windows Media Photo format (WMP).</span></span> <span data-ttu-id="a43a4-130">這種格式也稱為 HD 相片和 JPEG XR。</span><span class="sxs-lookup"><span data-stu-id="a43a4-130">This format is also known as HD Photo and JPEG XR.</span></span> <span data-ttu-id="a43a4-131">此格式的副檔名為. hdp、. jxr 和. wdp。</span><span class="sxs-lookup"><span data-stu-id="a43a4-131">The file extensions for this format are .hdp, .jxr, and .wdp.</span></span>

<span data-ttu-id="a43a4-132">若要正常運作， **D3DX10 \_ 如果 \_ WMP** 需要您初始化 COM。</span><span class="sxs-lookup"><span data-stu-id="a43a4-132">To work properly, **D3DX10\_IFF\_WMP** requires that you initialize COM.</span></span> <span data-ttu-id="a43a4-133">因此，請先在您的應用程式中呼叫 [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) 或 [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) ，然後再呼叫 D3DX。</span><span class="sxs-lookup"><span data-stu-id="a43a4-133">Therefore, call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) or [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) in your application before you call D3DX.</span></span>

</dd> <dt>

<span data-ttu-id="a43a4-134"><span id="D3DX10_IFF_FORCE_DWORD"></span><span id="d3dx10_iff_force_dword"></span>**D3DX10 \_ 如果 \_ FORCE \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="a43a4-134"><span id="D3DX10_IFF_FORCE_DWORD"></span><span id="d3dx10_iff_force_dword"></span>**D3DX10\_IFF\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="a43a4-135">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="a43a4-135">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="a43a4-136">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="a43a4-136">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="a43a4-137">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="a43a4-137">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a43a4-138">備註</span><span class="sxs-lookup"><span data-stu-id="a43a4-138">Remarks</span></span>

<span data-ttu-id="a43a4-139">如需其中一些格式的詳細資訊，請參閱 [點陣圖的類型 (GDI +) ](../gdiplus/-gdiplus-types-of-bitmaps-about.md) 。</span><span class="sxs-lookup"><span data-stu-id="a43a4-139">See [Types of Bitmaps (GDI+)](../gdiplus/-gdiplus-types-of-bitmaps-about.md) for more information on some of these formats.</span></span>

<span data-ttu-id="a43a4-140">D3DX10 利用 Windows 影像處理元件來執行大部分支援的點陣圖檔案類型。</span><span class="sxs-lookup"><span data-stu-id="a43a4-140">D3DX10 makes use of the Windows Imaging Component to implement the majority of the supported bitmap file types.</span></span> <span data-ttu-id="a43a4-141">如需其他資訊，請參閱 [Windows 影像處理元件總覽](https://msdn.microsoft.com/library/ms737408.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="a43a4-141">See [Windows Imaging Component Overview](https://msdn.microsoft.com/library/ms737408.aspx) for additional information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a43a4-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="a43a4-142">Requirements</span></span>



| <span data-ttu-id="a43a4-143">需求</span><span class="sxs-lookup"><span data-stu-id="a43a4-143">Requirement</span></span> | <span data-ttu-id="a43a4-144">值</span><span class="sxs-lookup"><span data-stu-id="a43a4-144">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a43a4-145">標頭</span><span class="sxs-lookup"><span data-stu-id="a43a4-145">Header</span></span><br/> | <dl> <span data-ttu-id="a43a4-146"><dt>D3DX10Tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="a43a4-146"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a43a4-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a43a4-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a43a4-148">D3DX 列舉</span><span class="sxs-lookup"><span data-stu-id="a43a4-148">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 
