---
description: WIA \_ 原始 \_ 標頭結構會以裝置的原始資料格式來定義影像，並可讓應用程式在 Windows 映像取得 (WIA) 傳輸中使用原始格式。
ms.assetid: c7b50816-d596-4c62-a00e-cd8d6e303e42
title: 'WIA_RAW_HEADER 結構 (Wiadef .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_RAW_HEADER
api_type:
- HeaderDef
api_location:
- Wiadef.h
ms.openlocfilehash: 8da33f0b257168712f1b16fb7f940df5db862d3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966723"
---
# <a name="wia_raw_header-structure"></a><span data-ttu-id="968fe-103">WIA \_ 原始 \_ 標頭結構</span><span class="sxs-lookup"><span data-stu-id="968fe-103">WIA\_RAW\_HEADER structure</span></span>

<span data-ttu-id="968fe-104">**WIA \_ 原始 \_ 標頭** 結構會以裝置的原始資料格式來定義影像，並可讓應用程式在 WINDOWS 映射取得 (WIA) 傳輸中使用原始格式。</span><span class="sxs-lookup"><span data-stu-id="968fe-104">The **WIA\_RAW\_HEADER** structure defines an image in the RAW data format of a device and enables applications to use RAW format in Windows Image Acquisition (WIA) transfers.</span></span>

## <a name="syntax"></a><span data-ttu-id="968fe-105">語法</span><span class="sxs-lookup"><span data-stu-id="968fe-105">Syntax</span></span>


```C++
typedef struct _WIA_RAW_HEADER {
  DWORD Tag;
  DWORD Version;
  DWORD HeaderSize;
  DWORD XRes;
  DWORD YRes;
  DWORD XExtent;
  DWORD YExtent;
  DWORD BytesPerLine;
  DWORD BitsPerPixel;
  DWORD ChannelsPerPixel;
  DWORD DataType;
  BYTE  BitsPerChannel[8];
  DWORD Compression;
  DWORD PhotometricInterp;
  DWORD LineOrder;
  DWORD RawDataOffset;
  DWORD RawDataSize;
  DWORD PaletteOffset;
  DWORD PaletteSize;
} WIA_RAW_HEADER;
```



## <a name="members"></a><span data-ttu-id="968fe-106">成員</span><span class="sxs-lookup"><span data-stu-id="968fe-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="968fe-107">**Tag**</span><span class="sxs-lookup"><span data-stu-id="968fe-107">**Tag**</span></span>
</dt> <dd>

<span data-ttu-id="968fe-108">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="968fe-108">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="968fe-109">格式的名稱。</span><span class="sxs-lookup"><span data-stu-id="968fe-109">The name of the format.</span></span> <span data-ttu-id="968fe-110">這必須是常值 ' WRAW ' (四個單一位元組 ASCII 字元) 。</span><span class="sxs-lookup"><span data-stu-id="968fe-110">This must be the literal 'WRAW' (four single byte ASCII characters).</span></span>

</dd> <dt>

<span data-ttu-id="968fe-111">**版本**</span><span class="sxs-lookup"><span data-stu-id="968fe-111">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="968fe-112">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="968fe-112">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="968fe-113">原始格式的版本。</span><span class="sxs-lookup"><span data-stu-id="968fe-113">The version of the RAW format.</span></span> <span data-ttu-id="968fe-114">一律使用0x00010000。</span><span class="sxs-lookup"><span data-stu-id="968fe-114">Always use 0x00010000.</span></span>

</dd> <dt>

<span data-ttu-id="968fe-115">**HeaderSize**</span><span class="sxs-lookup"><span data-stu-id="968fe-115">**HeaderSize**</span></span>
</dt> <dd>

<span data-ttu-id="968fe-116">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="968fe-116">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="968fe-117">標頭中的有效位元組總數。</span><span class="sxs-lookup"><span data-stu-id="968fe-117">The total valid bytes in the header.</span></span>

</dd> <dt>

<span data-ttu-id="968fe-118">**XRes**</span><span class="sxs-lookup"><span data-stu-id="968fe-118">**XRes**</span></span>
</dt> <dd>

<span data-ttu-id="968fe-119">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="968fe-119">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="968fe-120">水平解析度 (單位為 DPI)。</span><span class="sxs-lookup"><span data-stu-id="968fe-120">The horizontal resolution in dots per inch.</span></span>

</dd> <dt>

<span data-ttu-id="968fe-121">**YRes**</span><span class="sxs-lookup"><span data-stu-id="968fe-121">**YRes**</span></span>
</dt> <dd>

<span data-ttu-id="968fe-122">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="968fe-122">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="968fe-123">垂直解析度 (單位為 DPI)。</span><span class="sxs-lookup"><span data-stu-id="968fe-123">The vertical resolution in dots per inch.</span></span>

</dd> <dt>

<span data-ttu-id="968fe-124">**範圍**</span><span class="sxs-lookup"><span data-stu-id="968fe-124">**XExtent**</span></span>
</dt> <dd>

<span data-ttu-id="968fe-125">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="968fe-125">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="968fe-126">影像的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="968fe-126">The width of the image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="968fe-127">**YExtent**</span><span class="sxs-lookup"><span data-stu-id="968fe-127">**YExtent**</span></span>
</dt> <dd>

<span data-ttu-id="968fe-128">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="968fe-128">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="968fe-129">影像的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="968fe-129">The height of the image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="968fe-130">**BytesPerLine**</span><span class="sxs-lookup"><span data-stu-id="968fe-130">**BytesPerLine**</span></span>
</dt> <dd>

<span data-ttu-id="968fe-131">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="968fe-131">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="968fe-132">未壓縮影像行中的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="968fe-132">The number of bytes in a line of an uncompressed image.</span></span> <span data-ttu-id="968fe-133">當資料壓縮時使用0，表示每行的位元組數目未知。</span><span class="sxs-lookup"><span data-stu-id="968fe-133">Use 0 when the data is compressed to signal that the number of bytes per line is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="968fe-134">**BitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="968fe-134">**BitsPerPixel**</span></span>
</dt> <dd>

<span data-ttu-id="968fe-135">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="968fe-135">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="968fe-136">所有圖元通道的每個圖元的位元組總數。</span><span class="sxs-lookup"><span data-stu-id="968fe-136">The total number of bits per pixel for all the pixel's channels.</span></span>

</dd> <dt>

<span data-ttu-id="968fe-137">**ChannelsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="968fe-137">**ChannelsPerPixel**</span></span>
</dt> <dd>

<span data-ttu-id="968fe-138">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="968fe-138">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="968fe-139">圖元中的色彩聲道數目。</span><span class="sxs-lookup"><span data-stu-id="968fe-139">The number of color channels in a pixel.</span></span>

</dd> <dt>

<span data-ttu-id="968fe-140">**DataType**</span><span class="sxs-lookup"><span data-stu-id="968fe-140">**DataType**</span></span>
</dt> <dd>

<span data-ttu-id="968fe-141">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="968fe-141">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="968fe-142">影像的 WIA \_ IPA \_ 資料類型。</span><span class="sxs-lookup"><span data-stu-id="968fe-142">The WIA\_IPA\_DATATYPE of the image.</span></span> <span data-ttu-id="968fe-143">由於 WIA \_ IPA \_ 格式設定為 [WiaImgFmt \_ RAW]，這是應用程式所挑選的允許值清單。</span><span class="sxs-lookup"><span data-stu-id="968fe-143">Since WIA\_IPA\_FORMAT is set to WiaImgFmt\_RAW, this is a list of allowed values from which the application picks.</span></span>

</dd> <dt>

<span data-ttu-id="968fe-144">**BitsPerChannel \[ 8\]**</span><span class="sxs-lookup"><span data-stu-id="968fe-144">**BitsPerChannel\[8\]**</span></span>
</dt> <dd>

<span data-ttu-id="968fe-145">類型： **位元組**</span><span class="sxs-lookup"><span data-stu-id="968fe-145">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="968fe-146">通道中的位數，最大值為8。</span><span class="sxs-lookup"><span data-stu-id="968fe-146">The number of bits in a channel, up to a maximum of 8.</span></span>

</dd> <dt>

<span data-ttu-id="968fe-147">**壓縮**</span><span class="sxs-lookup"><span data-stu-id="968fe-147">**Compression**</span></span>
</dt> <dd>

<span data-ttu-id="968fe-148">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="968fe-148">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="968fe-149">WIA \_ IPA \_ 壓縮值，指定所使用的壓縮類型（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="968fe-149">A WIA\_IPA\_COMPRESSION value specifying the type of compression used, if any.</span></span>

</dd> <dt>

<span data-ttu-id="968fe-150">**PhotometricInterp**</span><span class="sxs-lookup"><span data-stu-id="968fe-150">**PhotometricInterp**</span></span>
</dt> <dd>

<span data-ttu-id="968fe-151">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="968fe-151">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="968fe-152">WIA \_ IPA \_ PHOTOMETRIC \_ INTERP 值，指定影像的 PHOTOMETRIC 轉譯。</span><span class="sxs-lookup"><span data-stu-id="968fe-152">A WIA\_IPA\_PHOTOMETRIC\_INTERP value specifying the photometric interpretation of the image.</span></span>

</dd> <dt>

<span data-ttu-id="968fe-153">**LineOrder**</span><span class="sxs-lookup"><span data-stu-id="968fe-153">**LineOrder**</span></span>
</dt> <dd>

<span data-ttu-id="968fe-154">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="968fe-154">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="968fe-155">代表影像行順序的值。</span><span class="sxs-lookup"><span data-stu-id="968fe-155">A value representing the image line order.</span></span> <span data-ttu-id="968fe-156">這一律是從 \_ \_ 上到下的 wia 行順序，或是從 \_ \_ \_ \_ \_ \_ 下 \_ 到 \_ 上的 wia 行順序。</span><span class="sxs-lookup"><span data-stu-id="968fe-156">This is always either WIA\_LINE\_ORDER\_TOP\_TO\_BOTTOM or WIA\_LINE\_ORDER\_BOTTOM\_TO\_TOP.</span></span>

</dd> <dt>

<span data-ttu-id="968fe-157">**RawDataOffset**</span><span class="sxs-lookup"><span data-stu-id="968fe-157">**RawDataOffset**</span></span>
</dt> <dd>

<span data-ttu-id="968fe-158">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="968fe-158">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="968fe-159">原始影像資料的位置（以位元組為單位），從標頭結尾的位置或調色板結束的位置開始。</span><span class="sxs-lookup"><span data-stu-id="968fe-159">The position of the raw image data in bytes, starting from position where the header ends or the position where the palette ends.</span></span>

</dd> <dt>

<span data-ttu-id="968fe-160">**RawDataSize**</span><span class="sxs-lookup"><span data-stu-id="968fe-160">**RawDataSize**</span></span>
</dt> <dd>

<span data-ttu-id="968fe-161">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="968fe-161">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="968fe-162">原始影像資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="968fe-162">The size, in bytes, of the raw image data.</span></span>

</dd> <dt>

<span data-ttu-id="968fe-163">**PaletteOffset**</span><span class="sxs-lookup"><span data-stu-id="968fe-163">**PaletteOffset**</span></span>
</dt> <dd>

<span data-ttu-id="968fe-164">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="968fe-164">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="968fe-165">元件的位置，以位元組為單位，從標頭結尾的位置或資料結束的位置開始。</span><span class="sxs-lookup"><span data-stu-id="968fe-165">The position of the palette in bytes, starting from the position where the header ends or the position where the data ends.</span></span> <span data-ttu-id="968fe-166"> (如果沒有任何調色板，則此值為0。 ) </span><span class="sxs-lookup"><span data-stu-id="968fe-166">(This value is 0, if there is no palette.)</span></span>

</dd> <dt>

<span data-ttu-id="968fe-167">**PaletteSize**</span><span class="sxs-lookup"><span data-stu-id="968fe-167">**PaletteSize**</span></span>
</dt> <dd>

<span data-ttu-id="968fe-168">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="968fe-168">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="968fe-169">調色板資料表的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="968fe-169">The size, in bytes, of the palette table.</span></span> <span data-ttu-id="968fe-170"> (如果沒有任何調色板，則為0。 ) </span><span class="sxs-lookup"><span data-stu-id="968fe-170">(This is 0, if there is no palette.)</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="968fe-171">備註</span><span class="sxs-lookup"><span data-stu-id="968fe-171">Remarks</span></span>

<span data-ttu-id="968fe-172">因為這不是檔案格式，所以請針對 WIA \_ IPA \_ 副檔名屬性使用空字串 \_ 。</span><span class="sxs-lookup"><span data-stu-id="968fe-172">Because this is not a file format, use an empty string for the WIA\_IPA\_FILE\_EXTENSION property.</span></span>

<span data-ttu-id="968fe-173">選擇區和資料可能會以任何順序出現。</span><span class="sxs-lookup"><span data-stu-id="968fe-173">The palette and the data can come in either order.</span></span>

<span data-ttu-id="968fe-174">**RawDataSize** 不包含標頭或調色板。</span><span class="sxs-lookup"><span data-stu-id="968fe-174">**RawDataSize** does not include either the header or the palette.</span></span> <span data-ttu-id="968fe-175">使用此欄位來確認是否已成功傳送映射。</span><span class="sxs-lookup"><span data-stu-id="968fe-175">Use this field to verify that the transfer of the image has been successful.</span></span>

<span data-ttu-id="968fe-176">**PaletteSize** 是位元組，而不是調色板中的專案數。</span><span class="sxs-lookup"><span data-stu-id="968fe-176">**PaletteSize** is bytes, not the number of entries in the palette.</span></span>

## <a name="requirements"></a><span data-ttu-id="968fe-177">規格需求</span><span class="sxs-lookup"><span data-stu-id="968fe-177">Requirements</span></span>



| <span data-ttu-id="968fe-178">需求</span><span class="sxs-lookup"><span data-stu-id="968fe-178">Requirement</span></span> | <span data-ttu-id="968fe-179">值</span><span class="sxs-lookup"><span data-stu-id="968fe-179">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="968fe-180">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="968fe-180">Minimum supported client</span></span><br/> | <span data-ttu-id="968fe-181">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="968fe-181">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="968fe-182">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="968fe-182">Minimum supported server</span></span><br/> | <span data-ttu-id="968fe-183">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="968fe-183">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="968fe-184">標頭</span><span class="sxs-lookup"><span data-stu-id="968fe-184">Header</span></span><br/>                   | <dl> <span data-ttu-id="968fe-185"><dt>Wiadef。h</dt></span><span class="sxs-lookup"><span data-stu-id="968fe-185"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




