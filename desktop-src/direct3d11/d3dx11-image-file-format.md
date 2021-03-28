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
ms.openlocfilehash: 730ce59bb8a07f3fd8ef78bbeb27b4d01d198f7f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974713"
---
# <a name="d3dx11_image_file_format-enumeration"></a><span data-ttu-id="f89d0-106">D3DX11 \_ 圖像 \_ 檔案 \_ 格式列舉</span><span class="sxs-lookup"><span data-stu-id="f89d0-106">D3DX11\_IMAGE\_FILE\_FORMAT enumeration</span></span>

> [!Note]  
> <span data-ttu-id="f89d0-107">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="f89d0-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="f89d0-108">D3DX11Createxxx 和 D3DX11Savexxx 函數所支援的影像檔案格式。</span><span class="sxs-lookup"><span data-stu-id="f89d0-108">Image file formats supported by D3DX11Createxxx and D3DX11Savexxx functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="f89d0-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f89d0-109">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="f89d0-110">常數</span><span class="sxs-lookup"><span data-stu-id="f89d0-110">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f89d0-111"><span id="D3DX11_IFF_BMP"></span><span id="d3dx11_iff_bmp"></span>**D3DX11 \_ 如果 \_ BMP**</span><span class="sxs-lookup"><span data-stu-id="f89d0-111"><span id="D3DX11_IFF_BMP"></span><span id="d3dx11_iff_bmp"></span>**D3DX11\_IFF\_BMP**</span></span>
</dt> <dd>

<span data-ttu-id="f89d0-112">Windows 點陣圖 (BMP) 檔案格式。</span><span class="sxs-lookup"><span data-stu-id="f89d0-112">Windows bitmap (BMP) file format.</span></span> <span data-ttu-id="f89d0-113">包含標頭，其描述建立圖元矩形的裝置解析度、矩形的維度、位陣列的大小、邏輯調色板，以及定義點陣圖影像中圖元之間的關聯性，以及邏輯調色板中的專案之間的關聯性的位陣列。</span><span class="sxs-lookup"><span data-stu-id="f89d0-113">Contains a header that describes the resolution of the device on which the rectangle of pixels was created, the dimensions of the rectangle, the size of the array of bits, a logical palette, and an array of bits that defines the relationship between pixels in the bitmapped image and entries in the logical palette.</span></span> <span data-ttu-id="f89d0-114">此格式的副檔名是 .bmp。</span><span class="sxs-lookup"><span data-stu-id="f89d0-114">The file extension for this format is .bmp.</span></span>

</dd> <dt>

<span data-ttu-id="f89d0-115"><span id="D3DX11_IFF_JPG"></span><span id="d3dx11_iff_jpg"></span>**D3DX11 \_ 如果 \_ JPG**</span><span class="sxs-lookup"><span data-stu-id="f89d0-115"><span id="D3DX11_IFF_JPG"></span><span id="d3dx11_iff_jpg"></span>**D3DX11\_IFF\_JPG**</span></span>
</dt> <dd>

<span data-ttu-id="f89d0-116">聯合攝影專家群組 (JPEG) 壓縮檔案格式。</span><span class="sxs-lookup"><span data-stu-id="f89d0-116">Joint Photographic Experts Group (JPEG) compressed file format.</span></span> <span data-ttu-id="f89d0-117">指定24位 RGB 色彩和8位灰階標籤影像檔案格式的可變壓縮 (TIFF) 影像檔案。</span><span class="sxs-lookup"><span data-stu-id="f89d0-117">Specifies variable compression of 24-bit RGB color and 8-bit gray-scale Tagged Image File Format (TIFF) image document files.</span></span> <span data-ttu-id="f89d0-118">此格式的副檔名為 .jpg。</span><span class="sxs-lookup"><span data-stu-id="f89d0-118">The file extension for this format is .jpg.</span></span>

</dd> <dt>

<span data-ttu-id="f89d0-119"><span id="D3DX11_IFF_PNG"></span><span id="d3dx11_iff_png"></span>**D3DX11 \_ 如果 \_ PNG**</span><span class="sxs-lookup"><span data-stu-id="f89d0-119"><span id="D3DX11_IFF_PNG"></span><span id="d3dx11_iff_png"></span>**D3DX11\_IFF\_PNG**</span></span>
</dt> <dd>

<span data-ttu-id="f89d0-120">可移植網狀圖形 (PNG) 檔案格式。</span><span class="sxs-lookup"><span data-stu-id="f89d0-120">Portable Network Graphics (PNG) file format.</span></span> <span data-ttu-id="f89d0-121">使用非失真壓縮的非專屬點陣圖格式。</span><span class="sxs-lookup"><span data-stu-id="f89d0-121">A non-proprietary bitmap format using lossless compression.</span></span> <span data-ttu-id="f89d0-122">此格式的副檔名為 .png。</span><span class="sxs-lookup"><span data-stu-id="f89d0-122">The file extension for this format is .png.</span></span>

</dd> <dt>

<span data-ttu-id="f89d0-123"><span id="D3DX11_IFF_DDS"></span><span id="d3dx11_iff_dds"></span>**D3DX11 \_ 如果 \_ DDS**</span><span class="sxs-lookup"><span data-stu-id="f89d0-123"><span id="D3DX11_IFF_DDS"></span><span id="d3dx11_iff_dds"></span>**D3DX11\_IFF\_DDS**</span></span>
</dt> <dd>

<span data-ttu-id="f89d0-124">DirectDraw 介面 (DDS) 檔案格式。</span><span class="sxs-lookup"><span data-stu-id="f89d0-124">DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="f89d0-125">儲存材質、磁片區材質和三層的環境對應、具有或不具有 mipmap 層級，以及具有或不含圖元壓縮。</span><span class="sxs-lookup"><span data-stu-id="f89d0-125">Stores textures, volume textures, and cubic environment maps, with or without mipmap levels, and with or without pixel compression.</span></span> <span data-ttu-id="f89d0-126">此格式的副檔名為. dd。</span><span class="sxs-lookup"><span data-stu-id="f89d0-126">The file extension for this format is .dds.</span></span>

</dd> <dt>

<span data-ttu-id="f89d0-127"><span id="D3DX11_IFF_TIFF"></span><span id="d3dx11_iff_tiff"></span>**D3DX11 \_ 如果 \_ TIFF**</span><span class="sxs-lookup"><span data-stu-id="f89d0-127"><span id="D3DX11_IFF_TIFF"></span><span id="d3dx11_iff_tiff"></span>**D3DX11\_IFF\_TIFF**</span></span>
</dt> <dd>

<span data-ttu-id="f89d0-128">標記的影像檔案格式 (TIFF) 。</span><span class="sxs-lookup"><span data-stu-id="f89d0-128">Tagged Image File Format (TIFF).</span></span> <span data-ttu-id="f89d0-129">此格式的副檔名為 .tif 和 tiff。</span><span class="sxs-lookup"><span data-stu-id="f89d0-129">The file extensions for this format are .tif and .tiff.</span></span>

</dd> <dt>

<span data-ttu-id="f89d0-130"><span id="D3DX11_IFF_GIF"></span><span id="d3dx11_iff_gif"></span>**D3DX11 \_ 如果 \_ GIF**</span><span class="sxs-lookup"><span data-stu-id="f89d0-130"><span id="D3DX11_IFF_GIF"></span><span id="d3dx11_iff_gif"></span>**D3DX11\_IFF\_GIF**</span></span>
</dt> <dd>

<span data-ttu-id="f89d0-131">圖形交換格式 (GIF) 。</span><span class="sxs-lookup"><span data-stu-id="f89d0-131">Graphics Interchange Format (GIF).</span></span> <span data-ttu-id="f89d0-132">此格式的副檔名為 .gif。</span><span class="sxs-lookup"><span data-stu-id="f89d0-132">The file extension for this format is .gif.</span></span>

</dd> <dt>

<span data-ttu-id="f89d0-133"><span id="D3DX11_IFF_WMP"></span><span id="d3dx11_iff_wmp"></span>**D3DX11 \_ 如果 \_ WMP**</span><span class="sxs-lookup"><span data-stu-id="f89d0-133"><span id="D3DX11_IFF_WMP"></span><span id="d3dx11_iff_wmp"></span>**D3DX11\_IFF\_WMP**</span></span>
</dt> <dd>

<span data-ttu-id="f89d0-134">Windows Media Photo 格式 (WMP) 。</span><span class="sxs-lookup"><span data-stu-id="f89d0-134">Windows Media Photo format (WMP).</span></span> <span data-ttu-id="f89d0-135">這種格式也稱為 HD 相片和 JPEG XR。</span><span class="sxs-lookup"><span data-stu-id="f89d0-135">This format is also known as HD Photo and JPEG XR.</span></span> <span data-ttu-id="f89d0-136">此格式的副檔名為. hdp、. jxr 和. wdp。</span><span class="sxs-lookup"><span data-stu-id="f89d0-136">The file extensions for this format are .hdp, .jxr, and .wdp.</span></span>

<span data-ttu-id="f89d0-137">若要正常運作， **D3DX11 \_ 如果 \_ WMP** 需要您初始化 COM。</span><span class="sxs-lookup"><span data-stu-id="f89d0-137">To work properly, **D3DX11\_IFF\_WMP** requires that you initialize COM.</span></span> <span data-ttu-id="f89d0-138">因此，請先在您的應用程式中呼叫 [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) 或 [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) ，然後再呼叫 D3DX。</span><span class="sxs-lookup"><span data-stu-id="f89d0-138">Therefore, call [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) or [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) in your application before you call D3DX.</span></span>

</dd> <dt>

<span data-ttu-id="f89d0-139"><span id="D3DX11_IFF_FORCE_DWORD"></span><span id="d3dx11_iff_force_dword"></span>**D3DX11 \_ 如果 \_ FORCE \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="f89d0-139"><span id="D3DX11_IFF_FORCE_DWORD"></span><span id="d3dx11_iff_force_dword"></span>**D3DX11\_IFF\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="f89d0-140">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="f89d0-140">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="f89d0-141">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="f89d0-141">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="f89d0-142">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="f89d0-142">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f89d0-143">備註</span><span class="sxs-lookup"><span data-stu-id="f89d0-143">Remarks</span></span>

<span data-ttu-id="f89d0-144">如需其中一些格式的詳細資訊，請參閱 [點陣圖的類型 (GDI +) ](../gdiplus/-gdiplus-types-of-bitmaps-about.md) 。</span><span class="sxs-lookup"><span data-stu-id="f89d0-144">See [Types of Bitmaps (GDI+)](../gdiplus/-gdiplus-types-of-bitmaps-about.md) for more information on some of these formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="f89d0-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="f89d0-145">Requirements</span></span>



| <span data-ttu-id="f89d0-146">需求</span><span class="sxs-lookup"><span data-stu-id="f89d0-146">Requirement</span></span> | <span data-ttu-id="f89d0-147">值</span><span class="sxs-lookup"><span data-stu-id="f89d0-147">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f89d0-148">標頭</span><span class="sxs-lookup"><span data-stu-id="f89d0-148">Header</span></span><br/> | <dl> <span data-ttu-id="f89d0-149"><dt>D3DX11tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="f89d0-149"><dt>D3DX11tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f89d0-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f89d0-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f89d0-151">D3DX 列舉</span><span class="sxs-lookup"><span data-stu-id="f89d0-151">D3DX Enumerations</span></span>](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

