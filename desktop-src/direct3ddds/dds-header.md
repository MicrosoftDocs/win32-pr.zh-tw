---
title: 'DDS_HEADER 結構 (Dd. h) '
description: 描述 DDS 檔案標頭。
ms.assetid: 7f8bde30-0ff9-4bb9-b444-5c875e6a0865
keywords:
- DDS_HEADER 結構 DDS
topic_type:
- apiref
api_name:
- DDS_HEADER
api_location:
- Dds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d70fa0c4b05b6655ce0329cc73651ea21d4d808
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106974842"
---
# <a name="dds_header-structure"></a><span data-ttu-id="b3bbb-104">DDS \_ 標頭結構</span><span class="sxs-lookup"><span data-stu-id="b3bbb-104">DDS\_HEADER structure</span></span>

<span data-ttu-id="b3bbb-105">描述 DDS 檔案標頭。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-105">Describes a DDS file header.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3bbb-106">語法</span><span class="sxs-lookup"><span data-stu-id="b3bbb-106">Syntax</span></span>


```C++
typedef struct {
  DWORD           dwSize;
  DWORD           dwFlags;
  DWORD           dwHeight;
  DWORD           dwWidth;
  DWORD           dwPitchOrLinearSize;
  DWORD           dwDepth;
  DWORD           dwMipMapCount;
  DWORD           dwReserved1[11];
  DDS_PIXELFORMAT ddspf;
  DWORD           dwCaps;
  DWORD           dwCaps2;
  DWORD           dwCaps3;
  DWORD           dwCaps4;
  DWORD           dwReserved2;
} DDS_HEADER;
```



## <a name="members"></a><span data-ttu-id="b3bbb-107">成員</span><span class="sxs-lookup"><span data-stu-id="b3bbb-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="b3bbb-108">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="b3bbb-108">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="b3bbb-109">類型： **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3bbb-109">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3bbb-110">結構的大小。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-110">Size of structure.</span></span> <span data-ttu-id="b3bbb-111">此成員必須設定為124。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-111">This member must be set to 124.</span></span>

</dd> <dt>

<span data-ttu-id="b3bbb-112">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="b3bbb-112">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="b3bbb-113">類型： **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3bbb-113">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3bbb-114">旗標，指出哪些成員包含有效的資料。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-114">Flags to indicate which members contain valid data.</span></span>



| <span data-ttu-id="b3bbb-115">旗標</span><span class="sxs-lookup"><span data-stu-id="b3bbb-115">Flag</span></span>              | <span data-ttu-id="b3bbb-116">描述</span><span class="sxs-lookup"><span data-stu-id="b3bbb-116">Description</span></span>                                                  | <span data-ttu-id="b3bbb-117">值</span><span class="sxs-lookup"><span data-stu-id="b3bbb-117">Value</span></span>    |
|-------------------|--------------------------------------------------------------|----------|
| <span data-ttu-id="b3bbb-118">DDSD \_ 帽</span><span class="sxs-lookup"><span data-stu-id="b3bbb-118">DDSD\_CAPS</span></span>        | <span data-ttu-id="b3bbb-119">每個 dd 檔案都需要。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-119">Required in every .dds file.</span></span>                                 | <span data-ttu-id="b3bbb-120">0x1</span><span class="sxs-lookup"><span data-stu-id="b3bbb-120">0x1</span></span>      |
| <span data-ttu-id="b3bbb-121">DDSD \_ 高度</span><span class="sxs-lookup"><span data-stu-id="b3bbb-121">DDSD\_HEIGHT</span></span>      | <span data-ttu-id="b3bbb-122">每個 dd 檔案都需要。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-122">Required in every .dds file.</span></span>                                 | <span data-ttu-id="b3bbb-123">0x2</span><span class="sxs-lookup"><span data-stu-id="b3bbb-123">0x2</span></span>      |
| <span data-ttu-id="b3bbb-124">DDSD \_ 寬度</span><span class="sxs-lookup"><span data-stu-id="b3bbb-124">DDSD\_WIDTH</span></span>       | <span data-ttu-id="b3bbb-125">每個 dd 檔案都需要。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-125">Required in every .dds file.</span></span>                                 | <span data-ttu-id="b3bbb-126">0x4</span><span class="sxs-lookup"><span data-stu-id="b3bbb-126">0x4</span></span>      |
| <span data-ttu-id="b3bbb-127">DDSD \_ 音調</span><span class="sxs-lookup"><span data-stu-id="b3bbb-127">DDSD\_PITCH</span></span>       | <span data-ttu-id="b3bbb-128">針對未壓縮材質提供音調時需要。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-128">Required when pitch is provided for an uncompressed texture.</span></span> | <span data-ttu-id="b3bbb-129">0x8</span><span class="sxs-lookup"><span data-stu-id="b3bbb-129">0x8</span></span>      |
| <span data-ttu-id="b3bbb-130">DDSD \_ PIXELFORMAT</span><span class="sxs-lookup"><span data-stu-id="b3bbb-130">DDSD\_PIXELFORMAT</span></span> | <span data-ttu-id="b3bbb-131">每個 dd 檔案都需要。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-131">Required in every .dds file.</span></span>                                 | <span data-ttu-id="b3bbb-132">0x1000</span><span class="sxs-lookup"><span data-stu-id="b3bbb-132">0x1000</span></span>   |
| <span data-ttu-id="b3bbb-133">DDSD \_ MIPMAPCOUNT</span><span class="sxs-lookup"><span data-stu-id="b3bbb-133">DDSD\_MIPMAPCOUNT</span></span> | <span data-ttu-id="b3bbb-134">Mipmapped 材質中的必要項。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-134">Required in a mipmapped texture.</span></span>                             | <span data-ttu-id="b3bbb-135">0x20000</span><span class="sxs-lookup"><span data-stu-id="b3bbb-135">0x20000</span></span>  |
| <span data-ttu-id="b3bbb-136">DDSD \_ LINEARSIZE</span><span class="sxs-lookup"><span data-stu-id="b3bbb-136">DDSD\_LINEARSIZE</span></span>  | <span data-ttu-id="b3bbb-137">針對壓縮材質提供音調時需要。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-137">Required when pitch is provided for a compressed texture.</span></span>    | <span data-ttu-id="b3bbb-138">0x80000</span><span class="sxs-lookup"><span data-stu-id="b3bbb-138">0x80000</span></span>  |
| <span data-ttu-id="b3bbb-139">DDSD \_ 深度</span><span class="sxs-lookup"><span data-stu-id="b3bbb-139">DDSD\_DEPTH</span></span>       | <span data-ttu-id="b3bbb-140">深度材質中的必要項。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-140">Required in a depth texture.</span></span>                                 | <span data-ttu-id="b3bbb-141">0x800000</span><span class="sxs-lookup"><span data-stu-id="b3bbb-141">0x800000</span></span> |



 

> [!Note]  
> <span data-ttu-id="b3bbb-142">當您撰寫 dds 檔案時，您應該設定 DDSD \_ CAPS AND DDSD \_ PIXELFORMAT 旗標，而針對 mipmapped 紋理，您也應該設定 DDSD \_ MIPMAPCOUNT 旗標。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-142">When you write .dds files, you should set the DDSD\_CAPS and DDSD\_PIXELFORMAT flags, and for mipmapped textures you should also set the DDSD\_MIPMAPCOUNT flag.</span></span> <span data-ttu-id="b3bbb-143">但是，當您讀取的是 dds 檔案時，不應該依賴設定的 DDSD \_ CAPS、DDSD \_ PIXELFORMAT 和 DDSD \_ MIPMAPCOUNT 旗標，因為這類檔案的某些寫入器可能不會設定這些旗標。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-143">However, when you read a .dds file, you should not rely on the DDSD\_CAPS, DDSD\_PIXELFORMAT, and DDSD\_MIPMAPCOUNT flags being set because some writers of such a file might not set these flags.</span></span>

 

<span data-ttu-id="b3bbb-144">Dds \_ 標頭 \_ 旗標 \_ 材質旗標（定義于 dd. h 中）是 DDSD \_ CAPS、DDSD \_ HEIGHT、DDSD \_ WIDTH 和 DDSD \_ PIXELFORMAT 旗標的位 or 組合。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-144">The DDS\_HEADER\_FLAGS\_TEXTURE flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSD\_CAPS, DDSD\_HEIGHT, DDSD\_WIDTH, and DDSD\_PIXELFORMAT flags.</span></span>

<span data-ttu-id="b3bbb-145">Dds \_ 標頭 \_ 旗標 \_ MIPMAP 旗標（定義于 dd. h）等於 DDSD \_ MIPMAPCOUNT 旗標。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-145">The DDS\_HEADER\_FLAGS\_MIPMAP flag, which is defined in Dds.h, is equal to the DDSD\_MIPMAPCOUNT flag.</span></span>

<span data-ttu-id="b3bbb-146">Dds \_ 標頭 \_ 旗標 \_ 磁片區旗標（定義于 dd. h）等於 DDSD \_ DEPTH 旗標。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-146">The DDS\_HEADER\_FLAGS\_VOLUME flag, which is defined in Dds.h, is equal to the DDSD\_DEPTH flag.</span></span>

<span data-ttu-id="b3bbb-147">Dds \_ 標頭 \_ 旗標 \_ 音調旗標（定義于 dd. h 中）等於 DDSD \_ 音調旗標。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-147">The DDS\_HEADER\_FLAGS\_PITCH flag, which is defined in Dds.h, is equal to the DDSD\_PITCH flag.</span></span>

<span data-ttu-id="b3bbb-148">Dds \_ 標頭 \_ 旗標 \_ LINEARSIZE 旗標（定義于 dd. h）等於 DDSD \_ LINEARSIZE 旗標。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-148">The DDS\_HEADER\_FLAGS\_LINEARSIZE flag, which is defined in Dds.h, is equal to the DDSD\_LINEARSIZE flag.</span></span>

</dd> <dt>

<span data-ttu-id="b3bbb-149">**dwHeight**</span><span class="sxs-lookup"><span data-stu-id="b3bbb-149">**dwHeight**</span></span>
</dt> <dd>

<span data-ttu-id="b3bbb-150">類型： **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3bbb-150">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3bbb-151">介面高度 (以圖元為單位) 。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-151">Surface height (in pixels).</span></span>

</dd> <dt>

<span data-ttu-id="b3bbb-152">**dwWidth**</span><span class="sxs-lookup"><span data-stu-id="b3bbb-152">**dwWidth**</span></span>
</dt> <dd>

<span data-ttu-id="b3bbb-153">類型： **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3bbb-153">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3bbb-154">介面寬度 (以圖元為單位) 。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-154">Surface width (in pixels).</span></span>

</dd> <dt>

<span data-ttu-id="b3bbb-155">**dwPitchOrLinearSize**</span><span class="sxs-lookup"><span data-stu-id="b3bbb-155">**dwPitchOrLinearSize**</span></span>
</dt> <dd>

<span data-ttu-id="b3bbb-156">類型： **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3bbb-156">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3bbb-157">未壓縮材質中每個掃描行的字元數或位元組數;針對壓縮材質的最上層材質中的總位元組數。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-157">The pitch or number of bytes per scan line in an uncompressed texture; the total number of bytes in the top level texture for a compressed texture.</span></span> <span data-ttu-id="b3bbb-158">如需如何計算推銷方式的詳細資訊，請參閱 [dds 程式設計指南](dx-graphics-dds-pguide.md)的 dds 檔案配置一節。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-158">For information about how to compute the pitch, see the DDS File Layout section of the [Programming Guide for DDS](dx-graphics-dds-pguide.md).</span></span>

</dd> <dt>

<span data-ttu-id="b3bbb-159">**dwDepth**</span><span class="sxs-lookup"><span data-stu-id="b3bbb-159">**dwDepth**</span></span>
</dt> <dd>

<span data-ttu-id="b3bbb-160">類型： **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3bbb-160">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3bbb-161">磁片區材質的深度 (（以圖元為單位）) ，否則未使用。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-161">Depth of a volume texture (in pixels), otherwise unused.</span></span>

</dd> <dt>

<span data-ttu-id="b3bbb-162">**dwMipMapCount**</span><span class="sxs-lookup"><span data-stu-id="b3bbb-162">**dwMipMapCount**</span></span>
</dt> <dd>

<span data-ttu-id="b3bbb-163">類型： **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3bbb-163">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3bbb-164">Mipmap 層級的數目，否則未使用。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-164">Number of mipmap levels, otherwise unused.</span></span>

</dd> <dt>

<span data-ttu-id="b3bbb-165">**dwReserved1 \[ 11\]**</span><span class="sxs-lookup"><span data-stu-id="b3bbb-165">**dwReserved1\[11\]**</span></span>
</dt> <dd>

<span data-ttu-id="b3bbb-166">類型： **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3bbb-166">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3bbb-167">未使用的。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-167">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="b3bbb-168">**ddspf**</span><span class="sxs-lookup"><span data-stu-id="b3bbb-168">**ddspf**</span></span>
</dt> <dd>

<span data-ttu-id="b3bbb-169">類型： **[ **DDS \_ PIXELFORMAT**](dds-pixelformat.md)**</span><span class="sxs-lookup"><span data-stu-id="b3bbb-169">Type: **[**DDS\_PIXELFORMAT**](dds-pixelformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b3bbb-170">像素格式 (查看 [**DDS \_ PIXELFORMAT**](dds-pixelformat.md)) 。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-170">The pixel format (see [**DDS\_PIXELFORMAT**](dds-pixelformat.md)).</span></span>

</dd> <dt>

<span data-ttu-id="b3bbb-171">**dwCaps**</span><span class="sxs-lookup"><span data-stu-id="b3bbb-171">**dwCaps**</span></span>
</dt> <dd>

<span data-ttu-id="b3bbb-172">類型： **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3bbb-172">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3bbb-173">指定所儲存之表面的複雜度。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-173">Specifies the complexity of the surfaces stored.</span></span>



| <span data-ttu-id="b3bbb-174">旗標</span><span class="sxs-lookup"><span data-stu-id="b3bbb-174">Flag</span></span>             | <span data-ttu-id="b3bbb-175">描述</span><span class="sxs-lookup"><span data-stu-id="b3bbb-175">Description</span></span>                                                                                                                              | <span data-ttu-id="b3bbb-176">值</span><span class="sxs-lookup"><span data-stu-id="b3bbb-176">Value</span></span>    |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------|----------|
| <span data-ttu-id="b3bbb-177">DDSCAPS \_ 複雜</span><span class="sxs-lookup"><span data-stu-id="b3bbb-177">DDSCAPS\_COMPLEX</span></span> | <span data-ttu-id="b3bbb-178">參數必須用於包含多個介面 (mipmap、三層環境對應或 mipmapped 磁片區材質) 的任何檔案。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-178">Optional; must be used on any file that contains more than one surface (a mipmap, a cubic environment map, or mipmapped volume texture).</span></span> | <span data-ttu-id="b3bbb-179">0x8</span><span class="sxs-lookup"><span data-stu-id="b3bbb-179">0x8</span></span>      |
| <span data-ttu-id="b3bbb-180">DDSCAPS \_ MIPMAP</span><span class="sxs-lookup"><span data-stu-id="b3bbb-180">DDSCAPS\_MIPMAP</span></span>  | <span data-ttu-id="b3bbb-181">參數應用於 mipmap。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-181">Optional; should be used for a mipmap.</span></span>                                                                                                   | <span data-ttu-id="b3bbb-182">0x400000</span><span class="sxs-lookup"><span data-stu-id="b3bbb-182">0x400000</span></span> |
| <span data-ttu-id="b3bbb-183">DDSCAPS \_ 材質</span><span class="sxs-lookup"><span data-stu-id="b3bbb-183">DDSCAPS\_TEXTURE</span></span> | <span data-ttu-id="b3bbb-184">必要</span><span class="sxs-lookup"><span data-stu-id="b3bbb-184">Required</span></span>                                                                                                                                 | <span data-ttu-id="b3bbb-185">0x1000</span><span class="sxs-lookup"><span data-stu-id="b3bbb-185">0x1000</span></span>   |



 

> [!Note]  
> <span data-ttu-id="b3bbb-186">當您撰寫 dds 檔案時，您應該設定 DDSCAPS \_ 材質旗標，而針對多個表面，您也應該設定 DDSCAPS \_ 複雜旗標。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-186">When you write .dds files, you should set the DDSCAPS\_TEXTURE flag, and for multiple surfaces you should also set the DDSCAPS\_COMPLEX flag.</span></span> <span data-ttu-id="b3bbb-187">但是，當您讀取的是 dds 檔案時，不應該依賴 DDSCAPS \_ 材質和 DDSCAPS \_ 複雜旗標，因為這類檔案的某些寫入器可能不會設定這些旗標。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-187">However, when you read a .dds file, you should not rely on the DDSCAPS\_TEXTURE and DDSCAPS\_COMPLEX flags being set because some writers of such a file might not set these flags.</span></span>

 

<span data-ttu-id="b3bbb-188">Dds \_ 介面 \_ 旗標 \_ MIPMAP 旗標是在 dds 中定義，它是 DDSCAPS \_ COMPLEX 和 DDSCAPS MIPMAP 旗標的位 or 組合 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-188">The DDS\_SURFACE\_FLAGS\_MIPMAP flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSCAPS\_COMPLEX and DDSCAPS\_MIPMAP flags.</span></span>

<span data-ttu-id="b3bbb-189">Dds \_ 介面 \_ 旗標 \_ 材質旗標（定義于 dd. h 中）等於 DDSCAPS \_ 材質旗標。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-189">The DDS\_SURFACE\_FLAGS\_TEXTURE flag, which is defined in Dds.h, is equal to the DDSCAPS\_TEXTURE flag.</span></span>

<span data-ttu-id="b3bbb-190">Dds \_ 介面 \_ 旗標 \_ 立方體貼圖旗標（定義于 dd. h）等於 DDSCAPS \_ 複雜旗標。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-190">The DDS\_SURFACE\_FLAGS\_CUBEMAP flag, which is defined in Dds.h, is equal to the DDSCAPS\_COMPLEX flag.</span></span>

</dd> <dt>

<span data-ttu-id="b3bbb-191">**dwCaps2**</span><span class="sxs-lookup"><span data-stu-id="b3bbb-191">**dwCaps2**</span></span>
</dt> <dd>

<span data-ttu-id="b3bbb-192">類型： **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3bbb-192">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3bbb-193">所儲存之表面的其他詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-193">Additional detail about the surfaces stored.</span></span>



| <span data-ttu-id="b3bbb-194">旗標</span><span class="sxs-lookup"><span data-stu-id="b3bbb-194">Flag</span></span>                         | <span data-ttu-id="b3bbb-195">描述</span><span class="sxs-lookup"><span data-stu-id="b3bbb-195">Description</span></span>                                            | <span data-ttu-id="b3bbb-196">值</span><span class="sxs-lookup"><span data-stu-id="b3bbb-196">Value</span></span>    |
|------------------------------|--------------------------------------------------------|----------|
| <span data-ttu-id="b3bbb-197">DDSCAPS2 \_ 立方體貼圖</span><span class="sxs-lookup"><span data-stu-id="b3bbb-197">DDSCAPS2\_CUBEMAP</span></span>            | <span data-ttu-id="b3bbb-198">Cube 對應的必要參數。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-198">Required for a cube map.</span></span>                               | <span data-ttu-id="b3bbb-199">0x200</span><span class="sxs-lookup"><span data-stu-id="b3bbb-199">0x200</span></span>    |
| <span data-ttu-id="b3bbb-200">DDSCAPS2 \_ 立方體貼圖 \_ POSITIVEX</span><span class="sxs-lookup"><span data-stu-id="b3bbb-200">DDSCAPS2\_CUBEMAP\_POSITIVEX</span></span> | <span data-ttu-id="b3bbb-201">當這些介面儲存在 cube 對應中時，這是必要的。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-201">Required when these surfaces are stored in a cube map.</span></span> | <span data-ttu-id="b3bbb-202">0x400</span><span class="sxs-lookup"><span data-stu-id="b3bbb-202">0x400</span></span>    |
| <span data-ttu-id="b3bbb-203">DDSCAPS2 \_ 立方體貼圖 \_ NEGATIVEX</span><span class="sxs-lookup"><span data-stu-id="b3bbb-203">DDSCAPS2\_CUBEMAP\_NEGATIVEX</span></span> | <span data-ttu-id="b3bbb-204">當這些介面儲存在 cube 對應中時，這是必要的。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-204">Required when these surfaces are stored in a cube map.</span></span> | <span data-ttu-id="b3bbb-205">0x800</span><span class="sxs-lookup"><span data-stu-id="b3bbb-205">0x800</span></span>    |
| <span data-ttu-id="b3bbb-206">DDSCAPS2 \_ 立方體貼圖 \_ POSITIVEY</span><span class="sxs-lookup"><span data-stu-id="b3bbb-206">DDSCAPS2\_CUBEMAP\_POSITIVEY</span></span> | <span data-ttu-id="b3bbb-207">當這些介面儲存在 cube 對應中時，這是必要的。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-207">Required when these surfaces are stored in a cube map.</span></span> | <span data-ttu-id="b3bbb-208">0x1000</span><span class="sxs-lookup"><span data-stu-id="b3bbb-208">0x1000</span></span>   |
| <span data-ttu-id="b3bbb-209">DDSCAPS2 \_ 立方體貼圖 \_ NEGATIVEY</span><span class="sxs-lookup"><span data-stu-id="b3bbb-209">DDSCAPS2\_CUBEMAP\_NEGATIVEY</span></span> | <span data-ttu-id="b3bbb-210">當這些介面儲存在 cube 對應中時，這是必要的。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-210">Required when these surfaces are stored in a cube map.</span></span> | <span data-ttu-id="b3bbb-211">0x2000</span><span class="sxs-lookup"><span data-stu-id="b3bbb-211">0x2000</span></span>   |
| <span data-ttu-id="b3bbb-212">DDSCAPS2 \_ 立方體貼圖 \_ POSITIVEZ</span><span class="sxs-lookup"><span data-stu-id="b3bbb-212">DDSCAPS2\_CUBEMAP\_POSITIVEZ</span></span> | <span data-ttu-id="b3bbb-213">當這些介面儲存在 cube 對應中時，這是必要的。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-213">Required when these surfaces are stored in a cube map.</span></span> | <span data-ttu-id="b3bbb-214">0x4000</span><span class="sxs-lookup"><span data-stu-id="b3bbb-214">0x4000</span></span>   |
| <span data-ttu-id="b3bbb-215">DDSCAPS2 \_ 立方體貼圖 \_ NEGATIVEZ</span><span class="sxs-lookup"><span data-stu-id="b3bbb-215">DDSCAPS2\_CUBEMAP\_NEGATIVEZ</span></span> | <span data-ttu-id="b3bbb-216">當這些介面儲存在 cube 對應中時，這是必要的。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-216">Required when these surfaces are stored in a cube map.</span></span> | <span data-ttu-id="b3bbb-217">0x8000</span><span class="sxs-lookup"><span data-stu-id="b3bbb-217">0x8000</span></span>   |
| <span data-ttu-id="b3bbb-218">DDSCAPS2 \_ 磁片區</span><span class="sxs-lookup"><span data-stu-id="b3bbb-218">DDSCAPS2\_VOLUME</span></span>             | <span data-ttu-id="b3bbb-219">磁片區材質的必要參數。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-219">Required for a volume texture.</span></span>                         | <span data-ttu-id="b3bbb-220">0x200000</span><span class="sxs-lookup"><span data-stu-id="b3bbb-220">0x200000</span></span> |



 

<span data-ttu-id="b3bbb-221">Dds \_ 立方體貼圖 \_ POSITIVEX 旗標是在 dds 中定義，它是 DDSCAPS2 \_ 立方體貼圖和 DDSCAPS2 \_ 立方體貼圖 POSITIVEX 旗標的位 or 組合 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-221">The DDS\_CUBEMAP\_POSITIVEX flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSCAPS2\_CUBEMAP and DDSCAPS2\_CUBEMAP\_POSITIVEX flags.</span></span>

<span data-ttu-id="b3bbb-222">Dds \_ 立方體貼圖 \_ NEGATIVEX 旗標是在 dds 中定義，它是 DDSCAPS2 \_ 立方體貼圖和 DDSCAPS2 \_ 立方體貼圖 NEGATIVEX 旗標的位 or 組合 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-222">The DDS\_CUBEMAP\_NEGATIVEX flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSCAPS2\_CUBEMAP and DDSCAPS2\_CUBEMAP\_NEGATIVEX flags.</span></span>

<span data-ttu-id="b3bbb-223">Dds \_ 立方體貼圖 \_ POSITIVEY 旗標是在 dds 中定義，它是 DDSCAPS2 \_ 立方體貼圖和 DDSCAPS2 \_ 立方體貼圖 POSITIVEY 旗標的位 or 組合 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-223">The DDS\_CUBEMAP\_POSITIVEY flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSCAPS2\_CUBEMAP and DDSCAPS2\_CUBEMAP\_POSITIVEY flags.</span></span>

<span data-ttu-id="b3bbb-224">Dds \_ 立方體貼圖 \_ NEGATIVEY 旗標是在 dds 中定義，它是 DDSCAPS2 \_ 立方體貼圖和 DDSCAPS2 \_ 立方體貼圖 NEGATIVEY 旗標的位 or 組合 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-224">The DDS\_CUBEMAP\_NEGATIVEY flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSCAPS2\_CUBEMAP and DDSCAPS2\_CUBEMAP\_NEGATIVEY flags.</span></span>

<span data-ttu-id="b3bbb-225">Dds \_ 立方體貼圖 \_ POSITIVEZ 旗標是在 dds 中定義，它是 DDSCAPS2 \_ 立方體貼圖和 DDSCAPS2 \_ 立方體貼圖 POSITIVEZ 旗標的位 or 組合 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-225">The DDS\_CUBEMAP\_POSITIVEZ flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSCAPS2\_CUBEMAP and DDSCAPS2\_CUBEMAP\_POSITIVEZ flags.</span></span>

<span data-ttu-id="b3bbb-226">Dds \_ 立方體貼圖 \_ NEGATIVEZ 旗標是在 dds 中定義，它是 DDSCAPS2 \_ 立方體貼圖和 DDSCAPS2 \_ 立方體貼圖 NEGATIVEZ 旗標的位 or 組合 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-226">The DDS\_CUBEMAP\_NEGATIVEZ flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSCAPS2\_CUBEMAP and DDSCAPS2\_CUBEMAP\_NEGATIVEZ flags.</span></span>

<span data-ttu-id="b3bbb-227">Dds \_ 立方體貼圖 \_ ALLFACES 旗標（定義于 dd. h 中）是 dds \_ 立方體貼圖 \_ POSITIVEX、DDS \_ 立方體貼圖 \_ NEGATIVEX、dds \_ 立方體貼圖 \_ POSITIVEY、DDS \_ 立方體貼圖 \_ NEGATIVEY、dds \_ 立方體貼圖 \_ POSITIVEZ 和 DDSCAPS2 \_ 立方體貼圖 \_ NEGATIVEZ 旗標的位 or 組合。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-227">The DDS\_CUBEMAP\_ALLFACES flag, which is defined in Dds.h, is a bitwise-OR combination of the DDS\_CUBEMAP\_POSITIVEX, DDS\_CUBEMAP\_NEGATIVEX, DDS\_CUBEMAP\_POSITIVEY, DDS\_CUBEMAP\_NEGATIVEY, DDS\_CUBEMAP\_POSITIVEZ, and DDSCAPS2\_CUBEMAP\_NEGATIVEZ flags.</span></span>

<span data-ttu-id="b3bbb-228">Dds \_ 旗標 \_ 磁片區旗標（定義于 dd. h）等於 DDSCAPS2 \_ VOLUME 旗標。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-228">The DDS\_FLAGS\_VOLUME flag, which is defined in Dds.h, is equal to the DDSCAPS2\_VOLUME flag.</span></span>

> [!Note]  
> <span data-ttu-id="b3bbb-229">雖然 Direct3D 9 支援部分 cube 對應，Direct3D 10、10.1 和11都需要您定義全部六個立方體圖的臉部 (也就是說，您必須設定 DDS \_ 立方體貼圖 \_ ALLFACES) 。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-229">Although Direct3D 9 supports partial cube-maps, Direct3D 10, 10.1, and 11 require that you define all six cube-map faces (that is, you must set DDS\_CUBEMAP\_ALLFACES).</span></span>

 

</dd> <dt>

<span data-ttu-id="b3bbb-230">**dwCaps3**</span><span class="sxs-lookup"><span data-stu-id="b3bbb-230">**dwCaps3**</span></span>
</dt> <dd>

<span data-ttu-id="b3bbb-231">類型： **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3bbb-231">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3bbb-232">未使用的。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-232">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="b3bbb-233">**dwCaps4**</span><span class="sxs-lookup"><span data-stu-id="b3bbb-233">**dwCaps4**</span></span>
</dt> <dd>

<span data-ttu-id="b3bbb-234">類型： **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3bbb-234">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3bbb-235">未使用的。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-235">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="b3bbb-236">**dwReserved2**</span><span class="sxs-lookup"><span data-stu-id="b3bbb-236">**dwReserved2**</span></span>
</dt> <dd>

<span data-ttu-id="b3bbb-237">類型： **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3bbb-237">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3bbb-238">未使用的。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-238">Unused.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b3bbb-239">備註</span><span class="sxs-lookup"><span data-stu-id="b3bbb-239">Remarks</span></span>

<span data-ttu-id="b3bbb-240">針對包含有效資料之結構的成員，包含 **dwFlags** 中的旗標。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-240">Include flags in **dwFlags** for the members of the structure that contain valid data.</span></span>

<span data-ttu-id="b3bbb-241">搭配使用此結構與 [**dds \_ 標頭 \_ DXT10**](dds-header-dxt10.md) ，將資源陣列儲存在 dds 檔案中。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-241">Use this structure in combination with a [**DDS\_HEADER\_DXT10**](dds-header-dxt10.md) to store a resource array in a DDS file.</span></span> <span data-ttu-id="b3bbb-242">如需詳細資訊，請參閱 [材質陣列](dx-graphics-dds-pguide.md)。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-242">For more information, see [texture arrays](dx-graphics-dds-pguide.md).</span></span>

<span data-ttu-id="b3bbb-243">**DDS \_標頭** 與 DIRECTDRAW DDSURFACEDESC2 結構完全相同，但沒有 directdraw 相依性。</span><span class="sxs-lookup"><span data-stu-id="b3bbb-243">**DDS\_HEADER** is identical to the DirectDraw DDSURFACEDESC2 structure without DirectDraw dependencies.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3bbb-244">規格需求</span><span class="sxs-lookup"><span data-stu-id="b3bbb-244">Requirements</span></span>



| <span data-ttu-id="b3bbb-245">需求</span><span class="sxs-lookup"><span data-stu-id="b3bbb-245">Requirement</span></span> | <span data-ttu-id="b3bbb-246">值</span><span class="sxs-lookup"><span data-stu-id="b3bbb-246">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b3bbb-247">標頭</span><span class="sxs-lookup"><span data-stu-id="b3bbb-247">Header</span></span><br/> | <dl> <span data-ttu-id="b3bbb-248"><dt>Dd. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3bbb-248"><dt>Dds.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3bbb-249">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b3bbb-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3bbb-250">DDS 的參考</span><span class="sxs-lookup"><span data-stu-id="b3bbb-250">Reference for DDS</span></span>](dx-graphics-dds-reference.md)
</dt> </dl>

 

