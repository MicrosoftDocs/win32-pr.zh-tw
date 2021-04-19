---
title: 'DDS_PIXELFORMAT 結構 (Dd. h) '
description: Surface 像素格式。
ms.assetid: 39c5e48d-cf20-4d77-80d5-a67f04de4883
keywords:
- DDS_PIXELFORMAT 結構 DDS
topic_type:
- apiref
api_name:
- DDS_PIXELFORMAT
api_location:
- Dds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fd909d62a1be212f9ed4ef9af243a27f28be818
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982197"
---
# <a name="dds_pixelformat-structure"></a><span data-ttu-id="868ea-104">DDS \_ PIXELFORMAT 結構</span><span class="sxs-lookup"><span data-stu-id="868ea-104">DDS\_PIXELFORMAT structure</span></span>

<span data-ttu-id="868ea-105">Surface 像素格式。</span><span class="sxs-lookup"><span data-stu-id="868ea-105">Surface pixel format.</span></span>

## <a name="syntax"></a><span data-ttu-id="868ea-106">語法</span><span class="sxs-lookup"><span data-stu-id="868ea-106">Syntax</span></span>


```C++
struct DDS_PIXELFORMAT {
  DWORD dwSize;
  DWORD dwFlags;
  DWORD dwFourCC;
  DWORD dwRGBBitCount;
  DWORD dwRBitMask;
  DWORD dwGBitMask;
  DWORD dwBBitMask;
  DWORD dwABitMask;
};
```



## <a name="members"></a><span data-ttu-id="868ea-107">成員</span><span class="sxs-lookup"><span data-stu-id="868ea-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="868ea-108">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="868ea-108">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="868ea-109">類型： **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="868ea-109">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="868ea-110">結構大小;設定為 32 (位元組) 。</span><span class="sxs-lookup"><span data-stu-id="868ea-110">Structure size; set to 32 (bytes).</span></span>

</dd> <dt>

<span data-ttu-id="868ea-111">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="868ea-111">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="868ea-112">類型： **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="868ea-112">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="868ea-113">指出介面中資料類型的值。</span><span class="sxs-lookup"><span data-stu-id="868ea-113">Values which indicate what type of data is in the surface.</span></span>



| <span data-ttu-id="868ea-114">旗標</span><span class="sxs-lookup"><span data-stu-id="868ea-114">Flag</span></span>              | <span data-ttu-id="868ea-115">描述</span><span class="sxs-lookup"><span data-stu-id="868ea-115">Description</span></span>                                                                                                                                                                                                                                | <span data-ttu-id="868ea-116">值</span><span class="sxs-lookup"><span data-stu-id="868ea-116">Value</span></span>   |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------|
| <span data-ttu-id="868ea-117">DDPF \_ ALPHAPIXELS</span><span class="sxs-lookup"><span data-stu-id="868ea-117">DDPF\_ALPHAPIXELS</span></span> | <span data-ttu-id="868ea-118">材質包含 Alpha 資料; **dwRGBAlphaBitMask** 包含有效的資料。</span><span class="sxs-lookup"><span data-stu-id="868ea-118">Texture contains alpha data; **dwRGBAlphaBitMask** contains valid data.</span></span>                                                                                                                                                                    | <span data-ttu-id="868ea-119">0x1</span><span class="sxs-lookup"><span data-stu-id="868ea-119">0x1</span></span>     |
| <span data-ttu-id="868ea-120">DDPF \_ ALPHA</span><span class="sxs-lookup"><span data-stu-id="868ea-120">DDPF\_ALPHA</span></span>       | <span data-ttu-id="868ea-121">用於 Alpha 通道的一些較舊的 DDS 檔 (dwRGBBitCount 包含 Alpha 通道 bitcount;dwABitMask 包含有效的資料) </span><span class="sxs-lookup"><span data-stu-id="868ea-121">Used in some older DDS files for alpha channel only uncompressed data (dwRGBBitCount contains the alpha channel bitcount; dwABitMask contains valid data)</span></span>                                                                                  | <span data-ttu-id="868ea-122">0x2</span><span class="sxs-lookup"><span data-stu-id="868ea-122">0x2</span></span>     |
| <span data-ttu-id="868ea-123">DDPF \_ FOURCC</span><span class="sxs-lookup"><span data-stu-id="868ea-123">DDPF\_FOURCC</span></span>      | <span data-ttu-id="868ea-124">材質包含壓縮的 RGB 資料; **dwFourCC** 包含有效的資料。</span><span class="sxs-lookup"><span data-stu-id="868ea-124">Texture contains compressed RGB data; **dwFourCC** contains valid data.</span></span>                                                                                                                                                                    | <span data-ttu-id="868ea-125">0x4</span><span class="sxs-lookup"><span data-stu-id="868ea-125">0x4</span></span>     |
| <span data-ttu-id="868ea-126">DDPF \_ RGB</span><span class="sxs-lookup"><span data-stu-id="868ea-126">DDPF\_RGB</span></span>         | <span data-ttu-id="868ea-127">材質包含未壓縮的 RGB 資料; **dwRGBBitCount** 和 RGB 遮罩 (**dwRBitMask**、 **dwGBitMask**、 **dwBBitMask**) 包含有效的資料。</span><span class="sxs-lookup"><span data-stu-id="868ea-127">Texture contains uncompressed RGB data; **dwRGBBitCount** and the RGB masks (**dwRBitMask**, **dwGBitMask**, **dwBBitMask**) contain valid data.</span></span>                                                                                           | <span data-ttu-id="868ea-128">0x40</span><span class="sxs-lookup"><span data-stu-id="868ea-128">0x40</span></span>    |
| <span data-ttu-id="868ea-129">DDPF \_ YUV</span><span class="sxs-lookup"><span data-stu-id="868ea-129">DDPF\_YUV</span></span>         | <span data-ttu-id="868ea-130">用在一些較舊的 DDS 檔中，用於 YUV 未壓縮的資料 (dwRGBBitCount 包含 YUV 位元數目;dwRBitMask 包含 Y 遮罩，dwGBitMask 包含 U 遮罩，dwBBitMask 包含 V 遮罩) </span><span class="sxs-lookup"><span data-stu-id="868ea-130">Used in some older DDS files for YUV uncompressed data (dwRGBBitCount contains the YUV bit count; dwRBitMask contains the Y mask, dwGBitMask contains the U mask, dwBBitMask contains the V mask)</span></span>                                          | <span data-ttu-id="868ea-131">0x200</span><span class="sxs-lookup"><span data-stu-id="868ea-131">0x200</span></span>   |
| <span data-ttu-id="868ea-132">DDPF \_ 亮度</span><span class="sxs-lookup"><span data-stu-id="868ea-132">DDPF\_LUMINANCE</span></span>   | <span data-ttu-id="868ea-133">用於某些較舊的 DDS 檔案，用於單一通道色彩未壓縮資料 (dwRGBBitCount 包含亮度通道位元數目;dwRBitMask 包含通道遮罩) 。</span><span class="sxs-lookup"><span data-stu-id="868ea-133">Used in some older DDS files for single channel color uncompressed data (dwRGBBitCount contains the luminance channel bit count; dwRBitMask contains the channel mask).</span></span> <span data-ttu-id="868ea-134">可以與 \_ 兩個通道 DDS 檔案的 DDPF ALPHAPIXELS 結合。</span><span class="sxs-lookup"><span data-stu-id="868ea-134">Can be combined with DDPF\_ALPHAPIXELS for a two channel DDS file.</span></span> | <span data-ttu-id="868ea-135">0x20000</span><span class="sxs-lookup"><span data-stu-id="868ea-135">0x20000</span></span> |



 

</dd> <dt>

<span data-ttu-id="868ea-136">**dwFourCC**</span><span class="sxs-lookup"><span data-stu-id="868ea-136">**dwFourCC**</span></span>
</dt> <dd>

<span data-ttu-id="868ea-137">類型： **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="868ea-137">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="868ea-138">用來指定壓縮或自訂格式的四個字元的代碼。</span><span class="sxs-lookup"><span data-stu-id="868ea-138">Four-character codes for specifying compressed or custom formats.</span></span> <span data-ttu-id="868ea-139">可能的值包括： *DXT1*、 *DXT2*、 *DXT3*、 *DXT4* 或 *DXT5*。</span><span class="sxs-lookup"><span data-stu-id="868ea-139">Possible values include: *DXT1*, *DXT2*, *DXT3*, *DXT4*, or *DXT5*.</span></span> <span data-ttu-id="868ea-140">FourCC of DX10 指出 [**DDS \_ 標頭 \_ DXT10**](dds-header-dxt10.md) 擴充標頭的 prescense，而該結構的 dxgiFormat 成員表示 true 格式。</span><span class="sxs-lookup"><span data-stu-id="868ea-140">A FourCC of DX10 indicates the prescense of the [**DDS\_HEADER\_DXT10**](dds-header-dxt10.md) extended header, and the dxgiFormat member of that structure indicates the true format.</span></span> <span data-ttu-id="868ea-141">使用四個字元的程式碼時，dwFlags 必須包含 *DDPF \_ FOURCC*。</span><span class="sxs-lookup"><span data-stu-id="868ea-141">When using a four-character code, dwFlags must include *DDPF\_FOURCC*.</span></span>

</dd> <dt>

<span data-ttu-id="868ea-142">**dwRGBBitCount**</span><span class="sxs-lookup"><span data-stu-id="868ea-142">**dwRGBBitCount**</span></span>
</dt> <dd>

<span data-ttu-id="868ea-143">類型： **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="868ea-143">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="868ea-144">RGB (中可能包含 Alpha) 格式的位數。</span><span class="sxs-lookup"><span data-stu-id="868ea-144">Number of bits in an RGB (possibly including alpha) format.</span></span> <span data-ttu-id="868ea-145">在 **dwFlags** 包含 *DDPF \_ RGB*、 *DDPF \_ 亮度* 或 *DDPF \_ YUV* 時有效。</span><span class="sxs-lookup"><span data-stu-id="868ea-145">Valid when **dwFlags** includes *DDPF\_RGB*, *DDPF\_LUMINANCE*, or *DDPF\_YUV*.</span></span>

</dd> <dt>

<span data-ttu-id="868ea-146">**dwRBitMask**</span><span class="sxs-lookup"><span data-stu-id="868ea-146">**dwRBitMask**</span></span>
</dt> <dd>

<span data-ttu-id="868ea-147">類型： **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="868ea-147">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="868ea-148">用於讀取色彩資料的紅色 (或 lumiannce 或 Y) 遮罩。</span><span class="sxs-lookup"><span data-stu-id="868ea-148">Red (or lumiannce or Y) mask for reading color data.</span></span> <span data-ttu-id="868ea-149">例如，假設有 A8R8G8B8 格式，則會0x00ff0000 紅色遮罩。</span><span class="sxs-lookup"><span data-stu-id="868ea-149">For instance, given the A8R8G8B8 format, the red mask would be 0x00ff0000.</span></span>

</dd> <dt>

<span data-ttu-id="868ea-150">**dwGBitMask**</span><span class="sxs-lookup"><span data-stu-id="868ea-150">**dwGBitMask**</span></span>
</dt> <dd>

<span data-ttu-id="868ea-151">類型： **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="868ea-151">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="868ea-152">綠色 (或 U) 遮罩來讀取色彩資料。</span><span class="sxs-lookup"><span data-stu-id="868ea-152">Green (or U) mask for reading color data.</span></span> <span data-ttu-id="868ea-153">例如，假設有 A8R8G8B8 格式，則會0x0000ff00 綠色遮罩。</span><span class="sxs-lookup"><span data-stu-id="868ea-153">For instance, given the A8R8G8B8 format, the green mask would be 0x0000ff00.</span></span>

</dd> <dt>

<span data-ttu-id="868ea-154">**dwBBitMask**</span><span class="sxs-lookup"><span data-stu-id="868ea-154">**dwBBitMask**</span></span>
</dt> <dd>

<span data-ttu-id="868ea-155">類型： **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="868ea-155">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="868ea-156">用於讀取色彩資料的藍色 (或 V) 遮罩。</span><span class="sxs-lookup"><span data-stu-id="868ea-156">Blue (or V) mask for reading color data.</span></span> <span data-ttu-id="868ea-157">例如，假設有 A8R8G8B8 格式，則會0x000000ff 藍色遮罩。</span><span class="sxs-lookup"><span data-stu-id="868ea-157">For instance, given the A8R8G8B8 format, the blue mask would be 0x000000ff.</span></span>

</dd> <dt>

<span data-ttu-id="868ea-158">**dwABitMask**</span><span class="sxs-lookup"><span data-stu-id="868ea-158">**dwABitMask**</span></span>
</dt> <dd>

<span data-ttu-id="868ea-159">類型： **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="868ea-159">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="868ea-160">用來讀取 Alpha 資料的 Alpha 遮罩。</span><span class="sxs-lookup"><span data-stu-id="868ea-160">Alpha mask for reading alpha data.</span></span> <span data-ttu-id="868ea-161">dwFlags 必須包含 *DDPF \_ ALPHAPIXELS* 或 *DDPF \_ ALPHA*。</span><span class="sxs-lookup"><span data-stu-id="868ea-161">dwFlags must include *DDPF\_ALPHAPIXELS* or *DDPF\_ALPHA*.</span></span> <span data-ttu-id="868ea-162">例如，假設有 A8R8G8B8 格式，則會 0xff000000 Alpha 遮罩。</span><span class="sxs-lookup"><span data-stu-id="868ea-162">For instance, given the A8R8G8B8 format, the alpha mask would be 0xff000000.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="868ea-163">備註</span><span class="sxs-lookup"><span data-stu-id="868ea-163">Remarks</span></span>

<span data-ttu-id="868ea-164">若要儲存像浮點數資料等 DXGI 格式，請使用 DDPF FOURCC 的 **dwFlags** ， \_ 並將 **DwFourCC** 設定為 ' d '、' X '、' 1 '、' 0 '。</span><span class="sxs-lookup"><span data-stu-id="868ea-164">To store DXGI formats such as floating-point data, use a **dwFlags** of DDPF\_FOURCC and set **dwFourCC** to 'D','X','1','0'.</span></span> <span data-ttu-id="868ea-165">使用 [**DDS \_ 標頭 \_ DXT10**](dds-header-dxt10.md) 延伸模組標頭將 DXGI 格式儲存在 **dxgiFormat** 成員中。</span><span class="sxs-lookup"><span data-stu-id="868ea-165">Use the [**DDS\_HEADER\_DXT10**](dds-header-dxt10.md) extension header to store the DXGI format in the **dxgiFormat** member.</span></span>

<span data-ttu-id="868ea-166">請注意， **dwFlags** 具有 DDPF \_ FOURCC 且 **dwFourCC** 值直接設定為 D3DFORMAT 或 DXGI \_ 格式列舉值的 DDS 檔案有非標準的變體。</span><span class="sxs-lookup"><span data-stu-id="868ea-166">Note that there are non-standard variants of DDS files where **dwFlags** has DDPF\_FOURCC and the **dwFourCC** value is set directly to a D3DFORMAT or DXGI\_FORMAT enumeration value.</span></span> <span data-ttu-id="868ea-167">\_您無法使用這個非標準配置來區分 D3DFORMAT 與 DXGI 格式值，因此建議改用 DX10 延伸模組標頭。</span><span class="sxs-lookup"><span data-stu-id="868ea-167">It is not possible to disambiguate the D3DFORMAT versus DXGI\_FORMAT values using this non-standard scheme, so the DX10 extension header is recommended instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="868ea-168">規格需求</span><span class="sxs-lookup"><span data-stu-id="868ea-168">Requirements</span></span>



| <span data-ttu-id="868ea-169">需求</span><span class="sxs-lookup"><span data-stu-id="868ea-169">Requirement</span></span> | <span data-ttu-id="868ea-170">值</span><span class="sxs-lookup"><span data-stu-id="868ea-170">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="868ea-171">標頭</span><span class="sxs-lookup"><span data-stu-id="868ea-171">Header</span></span><br/> | <dl> <span data-ttu-id="868ea-172"><dt>Dd. h</dt></span><span class="sxs-lookup"><span data-stu-id="868ea-172"><dt>Dds.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="868ea-173">另請參閱</span><span class="sxs-lookup"><span data-stu-id="868ea-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="868ea-174">DDS 的參考</span><span class="sxs-lookup"><span data-stu-id="868ea-174">Reference for DDS</span></span>](dx-graphics-dds-reference.md)
</dt> </dl>

 

