---
description: 定義各種類型的介面格式。
ms.assetid: a222e3bb-310c-4019-93ee-6a2da2a46ded
title: 'D3DFORMAT (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DFORMAT
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 228884435322992b8c87d20a9f351161f945c43c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696683"
---
# <a name="d3dformat"></a><span data-ttu-id="1f1bf-103">D3DFORMAT</span><span class="sxs-lookup"><span data-stu-id="1f1bf-103">D3DFORMAT</span></span>

<span data-ttu-id="1f1bf-104">定義各種類型的介面格式。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-104">Defines the various types of surface formats.</span></span>

``` syntax
typedef enum _D3DFORMAT {
    D3DFMT_UNKNOWN              =  0,

    D3DFMT_R8G8B8               = 20,
    D3DFMT_A8R8G8B8             = 21,
    D3DFMT_X8R8G8B8             = 22,
    D3DFMT_R5G6B5               = 23,
    D3DFMT_X1R5G5B5             = 24,
    D3DFMT_A1R5G5B5             = 25,
    D3DFMT_A4R4G4B4             = 26,
    D3DFMT_R3G3B2               = 27,
    D3DFMT_A8                   = 28,
    D3DFMT_A8R3G3B2             = 29,
    D3DFMT_X4R4G4B4             = 30,
    D3DFMT_A2B10G10R10          = 31,
    D3DFMT_A8B8G8R8             = 32,
    D3DFMT_X8B8G8R8             = 33,
    D3DFMT_G16R16               = 34,
    D3DFMT_A2R10G10B10          = 35,
    D3DFMT_A16B16G16R16         = 36,

    D3DFMT_A8P8                 = 40,
    D3DFMT_P8                   = 41,

    D3DFMT_L8                   = 50,
    D3DFMT_A8L8                 = 51,
    D3DFMT_A4L4                 = 52,

    D3DFMT_V8U8                 = 60,
    D3DFMT_L6V5U5               = 61,
    D3DFMT_X8L8V8U8             = 62,
    D3DFMT_Q8W8V8U8             = 63,
    D3DFMT_V16U16               = 64,
    D3DFMT_A2W10V10U10          = 67,

    D3DFMT_UYVY                 = MAKEFOURCC('U', 'Y', 'V', 'Y'),
    D3DFMT_R8G8_B8G8            = MAKEFOURCC('R', 'G', 'B', 'G'),
    D3DFMT_YUY2                 = MAKEFOURCC('Y', 'U', 'Y', '2'),
    D3DFMT_G8R8_G8B8            = MAKEFOURCC('G', 'R', 'G', 'B'),
    D3DFMT_DXT1                 = MAKEFOURCC('D', 'X', 'T', '1'),
    D3DFMT_DXT2                 = MAKEFOURCC('D', 'X', 'T', '2'),
    D3DFMT_DXT3                 = MAKEFOURCC('D', 'X', 'T', '3'),
    D3DFMT_DXT4                 = MAKEFOURCC('D', 'X', 'T', '4'),
    D3DFMT_DXT5                 = MAKEFOURCC('D', 'X', 'T', '5'),

    D3DFMT_D16_LOCKABLE         = 70,
    D3DFMT_D32                  = 71,
    D3DFMT_D15S1                = 73,
    D3DFMT_D24S8                = 75,
    D3DFMT_D24X8                = 77,
    D3DFMT_D24X4S4              = 79,
    D3DFMT_D16                  = 80,

    D3DFMT_D32F_LOCKABLE        = 82,
    D3DFMT_D24FS8               = 83,

#if !defined(D3D_DISABLE_9EX)
    D3DFMT_D32_LOCKABLE         = 84,
    D3DFMT_S8_LOCKABLE          = 85,
#endif // !D3D_DISABLE_9EX

    D3DFMT_L16                  = 81,

    D3DFMT_VERTEXDATA           =100,
    D3DFMT_INDEX16              =101,
    D3DFMT_INDEX32              =102,

    D3DFMT_Q16W16V16U16         =110,

    D3DFMT_MULTI2_ARGB8         = MAKEFOURCC('M','E','T','1'),

    D3DFMT_R16F                 = 111,
    D3DFMT_G16R16F              = 112,
    D3DFMT_A16B16G16R16F        = 113,

    D3DFMT_R32F                 = 114,
    D3DFMT_G32R32F              = 115,
    D3DFMT_A32B32G32R32F        = 116,

    D3DFMT_CxV8U8               = 117,

#if !defined(D3D_DISABLE_9EX)
    D3DFMT_A1                   = 118,
    D3DFMT_A2B10G10R10_XR_BIAS  = 119,
    D3DFMT_BINARYBUFFER         = 199,
#endif // !D3D_DISABLE_9EX

    D3DFMT_FORCE_DWORD          =0x7fffffff
} D3DFORMAT;
```

## <a name="remarks"></a><span data-ttu-id="1f1bf-105">備註</span><span class="sxs-lookup"><span data-stu-id="1f1bf-105">Remarks</span></span>

<span data-ttu-id="1f1bf-106">有數種類型的格式：</span><span class="sxs-lookup"><span data-stu-id="1f1bf-106">There are several types of formats:</span></span>

-   [<span data-ttu-id="1f1bf-107">背景緩衝區或顯示格式</span><span class="sxs-lookup"><span data-stu-id="1f1bf-107">BackBuffer or Display Formats</span></span>](#backbuffer-or-display-formats)
-   [<span data-ttu-id="1f1bf-108">緩衝區格式</span><span class="sxs-lookup"><span data-stu-id="1f1bf-108">Buffer Formats</span></span>](#buffer-formats)
-   [<span data-ttu-id="1f1bf-109">DXTn 壓縮的材質格式</span><span class="sxs-lookup"><span data-stu-id="1f1bf-109">DXTn Compressed Texture Formats</span></span>](#dxtn-compressed-texture-formats)
-   [<span data-ttu-id="1f1bf-110">浮點數格式</span><span class="sxs-lookup"><span data-stu-id="1f1bf-110">Floating-Point Formats</span></span>](#floating-point-formats)
-   [<span data-ttu-id="1f1bf-111">FOURCC 格式</span><span class="sxs-lookup"><span data-stu-id="1f1bf-111">FOURCC Formats</span></span>](#fourcc-formats)
-   [<span data-ttu-id="1f1bf-112">IEEE 格式</span><span class="sxs-lookup"><span data-stu-id="1f1bf-112">IEEE Formats</span></span>](#ieee-formats)
-   [<span data-ttu-id="1f1bf-113">混合格式</span><span class="sxs-lookup"><span data-stu-id="1f1bf-113">Mixed Formats</span></span>](#mixed-formats)
-   [<span data-ttu-id="1f1bf-114">簽署格式</span><span class="sxs-lookup"><span data-stu-id="1f1bf-114">Signed Formats</span></span>](#signed-formats)
-   [<span data-ttu-id="1f1bf-115">不帶正負號的格式</span><span class="sxs-lookup"><span data-stu-id="1f1bf-115">Unsigned Formats</span></span>](#unsigned-formats)
-   [<span data-ttu-id="1f1bf-116">其他</span><span class="sxs-lookup"><span data-stu-id="1f1bf-116">Other</span></span>](#other)

<span data-ttu-id="1f1bf-117">所有格式都會從左至右列出，最重要的位到最不重要的位。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-117">All formats are listed from left to right, most-significant bit to least-significant bit.</span></span> <span data-ttu-id="1f1bf-118">例如， **D3DFORMAT \_ ARGB** 是從最重要的位 channel A (Alpha) ，到最小的位頻道 B (blue) 進行排序。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-118">For example, **D3DFORMAT\_ARGB** is ordered from the most-significant bit channel A (alpha), to the least-significant bit channel B (blue).</span></span> <span data-ttu-id="1f1bf-119">當您遍歷介面資料時，資料會儲存在記憶體中，從最小到最大的位到最大的位，這表示記憶體中的通道順序是從最 (blue) 到最高有效位 (Alpha) 。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-119">When traversing surface data, the data is stored in memory from least-significant bit to most-significant bit, which means that the channel order in memory is from least-significant bit (blue) to most-significant bit (alpha).</span></span>

<span data-ttu-id="1f1bf-120">包含未定義通道的格式預設值 (G16R16、A8 等) 為1。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-120">The default value for formats that contain undefined channels (G16R16, A8, and so on) is 1.</span></span> <span data-ttu-id="1f1bf-121">唯一的例外是 A8 格式，它會針對三個色頻初始化為000。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-121">The only exception is the A8 format, which is initialized to 000 for the three color channels.</span></span>

<span data-ttu-id="1f1bf-122">位的順序是從最重要的位元組開始，因此 D3DFMT \_ A8L8 表示這個2位元組格式的高位元組是 Alpha。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-122">The order of the bits is from the most significant byte first, so D3DFMT\_A8L8 indicates that the high byte of this 2-byte format is alpha.</span></span> <span data-ttu-id="1f1bf-123">**D3DFMT \_D16** 表示16位整數值和應用程式可鎖定的介面。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-123">**D3DFMT\_D16** indicates a 16-bit integer value and an application-lockable surface.</span></span>

<span data-ttu-id="1f1bf-124">已選擇像素格式來啟用硬體廠商定義延伸格式的運算式，以及包含妥善建立的 FOURCC 方法。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-124">Pixel formats have been chosen to enable the expression of hardware-vendor-defined extension formats, as well as to include the well-established FOURCC method.</span></span> <span data-ttu-id="1f1bf-125">Direct3D 執行時間所瞭解的一組格式是由 D3DFORMAT 所定義。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-125">The set of formats understood by the Direct3D runtime is defined by D3DFORMAT.</span></span>

<span data-ttu-id="1f1bf-126">請注意，這些格式是由獨立硬體廠商 (Ihv) 所提供，且不會列出許多 FOURCC 碼。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-126">Note that formats are supplied by independent hardware vendors (IHVs) and many FOURCC codes are not listed.</span></span> <span data-ttu-id="1f1bf-127">此列舉中的格式是唯一的，因為它們是由執行時間獲批准，這表示參考轉譯器將在所有這些類型上運作。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-127">The formats in this enumeration are unique in that they are sanctioned by the runtime, meaning that the reference rasterizer will operate on all these types.</span></span> <span data-ttu-id="1f1bf-128">個別的 Ihv 會以卡片作為基礎來支援 IHV 提供的格式。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-128">IHV-supplied formats will be supported by the individual IHVs on a card-by-card basis.</span></span>

### <a name="backbuffer-or-display-formats"></a><span data-ttu-id="1f1bf-129">背景緩衝區或顯示格式</span><span class="sxs-lookup"><span data-stu-id="1f1bf-129">BackBuffer or Display Formats</span></span>

<span data-ttu-id="1f1bf-130">這些格式是背景緩衝區或顯示器唯一有效的格式。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-130">These formats are the only valid formats for a back buffer or a display.</span></span>



| <span data-ttu-id="1f1bf-131">格式</span><span class="sxs-lookup"><span data-stu-id="1f1bf-131">Format</span></span>      | <span data-ttu-id="1f1bf-132">背景緩衝區</span><span class="sxs-lookup"><span data-stu-id="1f1bf-132">Back buffer</span></span> | <span data-ttu-id="1f1bf-133">顯示</span><span class="sxs-lookup"><span data-stu-id="1f1bf-133">Display</span></span>                   |
|-------------|-------------|---------------------------|
| <span data-ttu-id="1f1bf-134">A2R10G10B10</span><span class="sxs-lookup"><span data-stu-id="1f1bf-134">A2R10G10B10</span></span> | <span data-ttu-id="1f1bf-135">x</span><span class="sxs-lookup"><span data-stu-id="1f1bf-135">x</span></span>           | <span data-ttu-id="1f1bf-136">x (全螢幕模式僅) </span><span class="sxs-lookup"><span data-stu-id="1f1bf-136">x (full-screen mode only)</span></span> |
| <span data-ttu-id="1f1bf-137">A8R8G8B8</span><span class="sxs-lookup"><span data-stu-id="1f1bf-137">A8R8G8B8</span></span>    | <span data-ttu-id="1f1bf-138">x</span><span class="sxs-lookup"><span data-stu-id="1f1bf-138">x</span></span>           |                           |
| <span data-ttu-id="1f1bf-139">X8R8G8B8</span><span class="sxs-lookup"><span data-stu-id="1f1bf-139">X8R8G8B8</span></span>    | <span data-ttu-id="1f1bf-140">x</span><span class="sxs-lookup"><span data-stu-id="1f1bf-140">x</span></span>           | <span data-ttu-id="1f1bf-141">x</span><span class="sxs-lookup"><span data-stu-id="1f1bf-141">x</span></span>                         |
| <span data-ttu-id="1f1bf-142">A1R5G5B5</span><span class="sxs-lookup"><span data-stu-id="1f1bf-142">A1R5G5B5</span></span>    | <span data-ttu-id="1f1bf-143">x</span><span class="sxs-lookup"><span data-stu-id="1f1bf-143">x</span></span>           |                           |
| <span data-ttu-id="1f1bf-144">X1R5G5B5</span><span class="sxs-lookup"><span data-stu-id="1f1bf-144">X1R5G5B5</span></span>    | <span data-ttu-id="1f1bf-145">x</span><span class="sxs-lookup"><span data-stu-id="1f1bf-145">x</span></span>           | <span data-ttu-id="1f1bf-146">x</span><span class="sxs-lookup"><span data-stu-id="1f1bf-146">x</span></span>                         |
| <span data-ttu-id="1f1bf-147">R5G6B5</span><span class="sxs-lookup"><span data-stu-id="1f1bf-147">R5G6B5</span></span>      | <span data-ttu-id="1f1bf-148">x</span><span class="sxs-lookup"><span data-stu-id="1f1bf-148">x</span></span>           | <span data-ttu-id="1f1bf-149">x</span><span class="sxs-lookup"><span data-stu-id="1f1bf-149">x</span></span>                         |



 

### <a name="buffer-formats"></a><span data-ttu-id="1f1bf-150">緩衝區格式</span><span class="sxs-lookup"><span data-stu-id="1f1bf-150">Buffer Formats</span></span>

<span data-ttu-id="1f1bf-151">深度、樣板、頂點和索引緩衝區各有獨特的格式。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-151">Depth, stencil, vertex, and index buffers each have unique formats.</span></span>



| <span data-ttu-id="1f1bf-152">緩衝區旗標</span><span class="sxs-lookup"><span data-stu-id="1f1bf-152">Buffer flags</span></span>               | <span data-ttu-id="1f1bf-153">值</span><span class="sxs-lookup"><span data-stu-id="1f1bf-153">Value</span></span> | <span data-ttu-id="1f1bf-154">格式</span><span class="sxs-lookup"><span data-stu-id="1f1bf-154">Format</span></span>                                                                                                                                        |
|----------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f1bf-155">**D3DFMT \_ D16 的 \_ 鎖定**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-155">**D3DFMT\_D16\_LOCKABLE**</span></span>  | <span data-ttu-id="1f1bf-156">70</span><span class="sxs-lookup"><span data-stu-id="1f1bf-156">70</span></span>    | <span data-ttu-id="1f1bf-157">16位 z-緩衝區位深度。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-157">16-bit z-buffer bit depth.</span></span>                                                                                                                    |
| <span data-ttu-id="1f1bf-158">**D3DFMT \_ D32**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-158">**D3DFMT\_D32**</span></span>            | <span data-ttu-id="1f1bf-159">71</span><span class="sxs-lookup"><span data-stu-id="1f1bf-159">71</span></span>    | <span data-ttu-id="1f1bf-160">32位 z-緩衝區位深度。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-160">32-bit z-buffer bit depth.</span></span>                                                                                                                    |
| <span data-ttu-id="1f1bf-161">**D3DFMT \_ D15S1**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-161">**D3DFMT\_D15S1**</span></span>          | <span data-ttu-id="1f1bf-162">73</span><span class="sxs-lookup"><span data-stu-id="1f1bf-162">73</span></span>    | <span data-ttu-id="1f1bf-163">16位 z-緩衝區位深度，其中15個位保留給深度通道，1位則保留供樣板通道之用。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-163">16-bit z-buffer bit depth where 15 bits are reserved for the depth channel and 1 bit is reserved for the stencil channel.</span></span>                     |
| <span data-ttu-id="1f1bf-164">**D3DFMT \_ D24S8**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-164">**D3DFMT\_D24S8**</span></span>          | <span data-ttu-id="1f1bf-165">75</span><span class="sxs-lookup"><span data-stu-id="1f1bf-165">75</span></span>    | <span data-ttu-id="1f1bf-166">32位 z-使用24位作為深度通道的緩衝區位深度，以及8個位的樣板通道。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-166">32-bit z-buffer bit depth using 24 bits for the depth channel and 8 bits for the stencil channel.</span></span>                                             |
| <span data-ttu-id="1f1bf-167">**D3DFMT \_ D24X8**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-167">**D3DFMT\_D24X8**</span></span>          | <span data-ttu-id="1f1bf-168">77</span><span class="sxs-lookup"><span data-stu-id="1f1bf-168">77</span></span>    | <span data-ttu-id="1f1bf-169">針對深度通道使用24位的32位 z-緩衝區位深度。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-169">32-bit z-buffer bit depth using 24 bits for the depth channel.</span></span>                                                                                |
| <span data-ttu-id="1f1bf-170">**D3DFMT \_ D24X4S4**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-170">**D3DFMT\_D24X4S4**</span></span>        | <span data-ttu-id="1f1bf-171">79</span><span class="sxs-lookup"><span data-stu-id="1f1bf-171">79</span></span>    | <span data-ttu-id="1f1bf-172">32位 z-使用24位作為深度通道的緩衝區位深度，以及適用于樣板通道的4個位。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-172">32-bit z-buffer bit depth using 24 bits for the depth channel and 4 bits for the stencil channel.</span></span>                                             |
| <span data-ttu-id="1f1bf-173">**D3DFMT \_ D32F 的 \_ 鎖定**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-173">**D3DFMT\_D32F\_LOCKABLE**</span></span> | <span data-ttu-id="1f1bf-174">82</span><span class="sxs-lookup"><span data-stu-id="1f1bf-174">82</span></span>    | <span data-ttu-id="1f1bf-175">可鎖定的格式，其中的深度值會以標準 IEEE 浮點數表示。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-175">A lockable format where the depth value is represented as a standard IEEE floating-point number.</span></span>                                              |
| <span data-ttu-id="1f1bf-176">**D3DFMT \_ D24FS8**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-176">**D3DFMT\_D24FS8**</span></span>         | <span data-ttu-id="1f1bf-177">83</span><span class="sxs-lookup"><span data-stu-id="1f1bf-177">83</span></span>    | <span data-ttu-id="1f1bf-178">不可鎖定的格式，包含24位的深度 (24 位浮點數格式-20e4) 和8位的樣板。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-178">A non-lockable format that contains 24 bits of depth (in a 24-bit floating point format - 20e4) and 8 bits of stencil.</span></span>                        |
| <span data-ttu-id="1f1bf-179">**D3DFMT \_ D32 的 \_ 鎖定**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-179">**D3DFMT\_D32\_LOCKABLE**</span></span>  | <span data-ttu-id="1f1bf-180">84</span><span class="sxs-lookup"><span data-stu-id="1f1bf-180">84</span></span>    | <span data-ttu-id="1f1bf-181">鎖定的32位深度緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-181">A lockable 32-bit depth buffer.</span></span> <span data-ttu-id="1f1bf-182">**Direct3d 9 與 Direct3d 9Ex 之間的差異：** 此旗標僅適用于 Direct3D 9Ex。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-182">**Differences between Direct3D 9 and Direct3D 9Ex:** This flag is available in Direct3D 9Ex only.</span></span><br/>  |
| <span data-ttu-id="1f1bf-183">**D3DFMT \_ S8 的 \_ 鎖定**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-183">**D3DFMT\_S8\_LOCKABLE**</span></span>   | <span data-ttu-id="1f1bf-184">85</span><span class="sxs-lookup"><span data-stu-id="1f1bf-184">85</span></span>    | <span data-ttu-id="1f1bf-185">鎖定的8位樣板緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-185">A lockable 8-bit stencil buffer.</span></span> <span data-ttu-id="1f1bf-186">**Direct3d 9 與 Direct3d 9Ex 之間的差異：** 此旗標僅適用于 Direct3D 9Ex。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-186">**Differences between Direct3D 9 and Direct3D 9Ex:** This flag is available in Direct3D 9Ex only.</span></span><br/> |
| <span data-ttu-id="1f1bf-187">**D3DFMT \_ D16**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-187">**D3DFMT\_D16**</span></span>            | <span data-ttu-id="1f1bf-188">80</span><span class="sxs-lookup"><span data-stu-id="1f1bf-188">80</span></span>    | <span data-ttu-id="1f1bf-189">16位 z-緩衝區位深度。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-189">16-bit z-buffer bit depth.</span></span>                                                                                                                    |
| <span data-ttu-id="1f1bf-190">**D3DFMT \_ VERTEXDATA**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-190">**D3DFMT\_VERTEXDATA**</span></span>     | <span data-ttu-id="1f1bf-191">100</span><span class="sxs-lookup"><span data-stu-id="1f1bf-191">100</span></span>   | <span data-ttu-id="1f1bf-192">描述頂點緩衝區介面。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-192">Describes a vertex buffer surface.</span></span>                                                                                                            |
| <span data-ttu-id="1f1bf-193">**D3DFMT \_ INDEX16**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-193">**D3DFMT\_INDEX16**</span></span>        | <span data-ttu-id="1f1bf-194">101</span><span class="sxs-lookup"><span data-stu-id="1f1bf-194">101</span></span>   | <span data-ttu-id="1f1bf-195">16位索引緩衝區位深度。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-195">16-bit index buffer bit depth.</span></span>                                                                                                                |
| <span data-ttu-id="1f1bf-196">**D3DFMT \_ INDEX32**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-196">**D3DFMT\_INDEX32**</span></span>        | <span data-ttu-id="1f1bf-197">102</span><span class="sxs-lookup"><span data-stu-id="1f1bf-197">102</span></span>   | <span data-ttu-id="1f1bf-198">32位索引緩衝區位深度。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-198">32-bit index buffer bit depth.</span></span>                                                                                                                |



 

<span data-ttu-id="1f1bf-199">除了 D3DFMT D16 可鎖定以外的所有深度樣板格式 \_ \_ ，都表示每圖元都沒有特定的位順序，而驅動程式可以取用超過指定位數的每深度通道 (但不能使用樣板通道) 。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-199">All depth-stencil formats except D3DFMT\_D16\_LOCKABLE indicate no particular bit ordering per pixel, and the driver is allowed to consume more than the indicated number of bits-per-depth channel (but not stencil channel).</span></span>

### <a name="dxtn-compressed-texture-formats"></a><span data-ttu-id="1f1bf-200">DXTn 壓縮的材質格式</span><span class="sxs-lookup"><span data-stu-id="1f1bf-200">DXTn Compressed Texture Formats</span></span>

<span data-ttu-id="1f1bf-201">這些旗標用於壓縮的材質：</span><span class="sxs-lookup"><span data-stu-id="1f1bf-201">These flags are used for compressed textures:</span></span>



| <span data-ttu-id="1f1bf-202">DXTn 壓縮的材質旗標</span><span class="sxs-lookup"><span data-stu-id="1f1bf-202">DXTn Compressed Texture flags</span></span> | <span data-ttu-id="1f1bf-203">值</span><span class="sxs-lookup"><span data-stu-id="1f1bf-203">Value</span></span>                          | <span data-ttu-id="1f1bf-204">格式</span><span class="sxs-lookup"><span data-stu-id="1f1bf-204">Format</span></span>                          |
|-------------------------------|--------------------------------|---------------------------------|
| <span data-ttu-id="1f1bf-205">**D3DFMT \_ DXT1**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-205">**D3DFMT\_DXT1**</span></span>              | <span data-ttu-id="1f1bf-206">MAKEFOURCC ( ' D '、' X '、' T '、' 1 ' ) </span><span class="sxs-lookup"><span data-stu-id="1f1bf-206">MAKEFOURCC('D', 'X', 'T', '1')</span></span> | <span data-ttu-id="1f1bf-207">DXT1 壓縮材質格式</span><span class="sxs-lookup"><span data-stu-id="1f1bf-207">DXT1 compression texture format</span></span> |
| <span data-ttu-id="1f1bf-208">**D3DFMT \_ DXT2**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-208">**D3DFMT\_DXT2**</span></span>              | <span data-ttu-id="1f1bf-209">MAKEFOURCC ( ' D '、' X '、' T '、' 2 ' ) </span><span class="sxs-lookup"><span data-stu-id="1f1bf-209">MAKEFOURCC('D', 'X', 'T', '2')</span></span> | <span data-ttu-id="1f1bf-210">DXT2 壓縮材質格式</span><span class="sxs-lookup"><span data-stu-id="1f1bf-210">DXT2 compression texture format</span></span> |
| <span data-ttu-id="1f1bf-211">**D3DFMT \_ DXT3**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-211">**D3DFMT\_DXT3**</span></span>              | <span data-ttu-id="1f1bf-212">MAKEFOURCC ( ' D '、' X '、' T '、' 3 ' ) </span><span class="sxs-lookup"><span data-stu-id="1f1bf-212">MAKEFOURCC('D', 'X', 'T', '3')</span></span> | <span data-ttu-id="1f1bf-213">DXT3 壓縮材質格式</span><span class="sxs-lookup"><span data-stu-id="1f1bf-213">DXT3 compression texture format</span></span> |
| <span data-ttu-id="1f1bf-214">**D3DFMT \_ DXT4**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-214">**D3DFMT\_DXT4**</span></span>              | <span data-ttu-id="1f1bf-215">MAKEFOURCC ( ' D '、' X '、' T '、' 4 ' ) </span><span class="sxs-lookup"><span data-stu-id="1f1bf-215">MAKEFOURCC('D', 'X', 'T', '4')</span></span> | <span data-ttu-id="1f1bf-216">DXT4 壓縮材質格式</span><span class="sxs-lookup"><span data-stu-id="1f1bf-216">DXT4 compression texture format</span></span> |
| <span data-ttu-id="1f1bf-217">**D3DFMT \_ DXT5**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-217">**D3DFMT\_DXT5**</span></span>              | <span data-ttu-id="1f1bf-218">MAKEFOURCC ( ' D '、' X '、' T '、' 5 ' ) </span><span class="sxs-lookup"><span data-stu-id="1f1bf-218">MAKEFOURCC('D', 'X', 'T', '5')</span></span> | <span data-ttu-id="1f1bf-219">DXT5 壓縮材質格式</span><span class="sxs-lookup"><span data-stu-id="1f1bf-219">DXT5 compression texture format</span></span> |



 

<span data-ttu-id="1f1bf-220">除非介面尺寸是4的倍數，否則執行時間不會允許應用程式使用 DXTn 格式來建立介面。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-220">The runtime will not allow an application to create a surface using a DXTn format unless the surface dimensions are multiples of 4.</span></span> <span data-ttu-id="1f1bf-221">這適用于螢幕外-一般表面、轉譯目標、2D 材質、立方體材質和音量材質。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-221">This applies to offscreen-plain surfaces, render targets, 2D textures, cube textures, and volume textures.</span></span>

### <a name="floating-point-formats"></a><span data-ttu-id="1f1bf-222">Floating-Point 格式</span><span class="sxs-lookup"><span data-stu-id="1f1bf-222">Floating-Point Formats</span></span>

<span data-ttu-id="1f1bf-223">這些旗標用於浮點介面格式。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-223">These flags are used for floating-point surface formats.</span></span> <span data-ttu-id="1f1bf-224">這些16位的每一通道格式也稱為 s10e5 格式。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-224">These 16-bits-per-channel formats are also known as s10e5 formats.</span></span>



| <span data-ttu-id="1f1bf-225">浮點數旗標</span><span class="sxs-lookup"><span data-stu-id="1f1bf-225">Floating-point flags</span></span>      | <span data-ttu-id="1f1bf-226">值</span><span class="sxs-lookup"><span data-stu-id="1f1bf-226">Value</span></span> | <span data-ttu-id="1f1bf-227">格式</span><span class="sxs-lookup"><span data-stu-id="1f1bf-227">Format</span></span>                                                                                   |
|---------------------------|-------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f1bf-228">**D3DFMT \_ R16F**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-228">**D3DFMT\_R16F**</span></span>          | <span data-ttu-id="1f1bf-229">111</span><span class="sxs-lookup"><span data-stu-id="1f1bf-229">111</span></span>   | <span data-ttu-id="1f1bf-230">適用于紅色通道的16位浮點數格式使用16位。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-230">16-bit float format using 16 bits for the red channel.</span></span>                                   |
| <span data-ttu-id="1f1bf-231">**D3DFMT \_ G16R16F**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-231">**D3DFMT\_G16R16F**</span></span>       | <span data-ttu-id="1f1bf-232">112</span><span class="sxs-lookup"><span data-stu-id="1f1bf-232">112</span></span>   | <span data-ttu-id="1f1bf-233">適用于紅色通道的32位浮點數格式和16位的綠色通道。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-233">32-bit float format using 16 bits for the red channel and 16 bits for the green channel.</span></span> |
| <span data-ttu-id="1f1bf-234">**D3DFMT \_ A16B16G16R16F**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-234">**D3DFMT\_A16B16G16R16F**</span></span> | <span data-ttu-id="1f1bf-235">113</span><span class="sxs-lookup"><span data-stu-id="1f1bf-235">113</span></span>   | <span data-ttu-id="1f1bf-236">針對每個通道使用16個位的64位 float 格式 (Alpha、blue、綠、red) 。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-236">64-bit float format using 16 bits for the each channel (alpha, blue, green, red).</span></span>        |



 

### <a name="fourcc-formats"></a><span data-ttu-id="1f1bf-237">FOURCC 格式</span><span class="sxs-lookup"><span data-stu-id="1f1bf-237">FOURCC Formats</span></span>

<span data-ttu-id="1f1bf-238">FOURCC 格式的資料是壓縮的資料。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-238">Data in a FOURCC format is compressed data.</span></span>

### <a name="makefourcc"></a><span data-ttu-id="1f1bf-239">MAKEFOURCC</span><span class="sxs-lookup"><span data-stu-id="1f1bf-239">MAKEFOURCC</span></span>

<span data-ttu-id="1f1bf-240">產生四個字元的程式碼的宏如下：</span><span class="sxs-lookup"><span data-stu-id="1f1bf-240">A macro for generating four-character codes follows:</span></span>

``` syntax
#define MAKEFOURCC(ch0, ch1, ch2, ch3)                              \
                ((DWORD)(BYTE)(ch0) | ((DWORD)(BYTE)(ch1) << 8) |   \
                ((DWORD)(BYTE)(ch2) << 16) | ((DWORD)(BYTE)(ch3) << 24 ))
```

<span data-ttu-id="1f1bf-241">以下是已定義的 FOURCC 格式：</span><span class="sxs-lookup"><span data-stu-id="1f1bf-241">Here are the defined FOURCC formats:</span></span>



| <span data-ttu-id="1f1bf-242">FOURCC 旗標</span><span class="sxs-lookup"><span data-stu-id="1f1bf-242">FOURCC flags</span></span>              | <span data-ttu-id="1f1bf-243">值</span><span class="sxs-lookup"><span data-stu-id="1f1bf-243">Value</span></span>                          | <span data-ttu-id="1f1bf-244">格式</span><span class="sxs-lookup"><span data-stu-id="1f1bf-244">Format</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f1bf-245">**D3DFMT \_ MULTI2 \_ ARGB8**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-245">**D3DFMT\_MULTI2\_ARGB8**</span></span> | <span data-ttu-id="1f1bf-246">MAKEFOURCC ( '、' E '、' T '、' 1 ' ) </span><span class="sxs-lookup"><span data-stu-id="1f1bf-246">MAKEFOURCC('M','E','T','1')</span></span>    | <span data-ttu-id="1f1bf-247">未壓縮的 MultiElement 材質 () </span><span class="sxs-lookup"><span data-stu-id="1f1bf-247">MultiElement texture (not compressed)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="1f1bf-248">**D3DFMT \_ G8R8 \_ G8B8**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-248">**D3DFMT\_G8R8\_G8B8**</span></span>    | <span data-ttu-id="1f1bf-249">MAKEFOURCC ( ' G '、' R '、' G '、' B ' ) </span><span class="sxs-lookup"><span data-stu-id="1f1bf-249">MAKEFOURCC('G', 'R', 'G', 'B')</span></span> | <span data-ttu-id="1f1bf-250">16位的壓縮 RGB 格式，類似于 YUY2 (Y0U0、Y1V0、Y2U2 等等) 。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-250">A 16-bit packed RGB format analogous to YUY2 (Y0U0, Y1V0, Y2U2, and so on).</span></span> <span data-ttu-id="1f1bf-251">它需要圖元配對，才能正確地表示色彩值。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-251">It requires a pixel pair in order to properly represent the color value.</span></span> <span data-ttu-id="1f1bf-252">配對中的第一個圖元包含8位的綠色 (（高8位) ）和8位的紅色 (（低8個位) ）。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-252">The first pixel in the pair contains 8 bits of green (in the high 8 bits) and 8 bits of red (in the low 8 bits).</span></span> <span data-ttu-id="1f1bf-253">第二個圖元包含8位的綠色 (（高8位）) 和低8個位) 中的8位藍色 (。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-253">The second pixel contains 8 bits of green (in the high 8 bits) and 8 bits of blue (in the low 8 bits).</span></span> <span data-ttu-id="1f1bf-254">這兩個圖元一起共用 red 和 blue 元件，而每個圖元都有唯一的綠色元件 (G0R0、G1B0、G2R2 等) 。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-254">Together, the two pixels share the red and blue components, while each has a unique green component (G0R0, G1B0, G2R2, and so on).</span></span> <span data-ttu-id="1f1bf-255">當查閱圖元著色器時，紋理取樣器不會將色彩正規化;它們維持在 0.0 f 到 255.0 f 的範圍內。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-255">The texture sampler does not normalize the colors when looking up into a pixel shader; they remain in the range of 0.0f to 255.0f.</span></span> <span data-ttu-id="1f1bf-256">這適用于所有可程式化的圖元著色器模型。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-256">This is true for all programmable pixel shader models.</span></span> <span data-ttu-id="1f1bf-257">針對固定函式圖元著色器，硬體應該正規化為0到 1. f 範圍，並基本上將它視為 YUY2 材質。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-257">For the fixed function pixel shader, the hardware should normalize to the 0.f to 1.f range and essentially treat it as the YUY2 texture.</span></span> <span data-ttu-id="1f1bf-258">公開此格式的硬體必須將 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) 的 PixelShader1xMaxValue 成員設定為能夠處理該範圍的值。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-258">Hardware that exposes this format must have the PixelShader1xMaxValue member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) set to a value capable of handling that range.</span></span> |
| <span data-ttu-id="1f1bf-259">**D3DFMT \_ R8G8 \_ B8G8**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-259">**D3DFMT\_R8G8\_B8G8**</span></span>    | <span data-ttu-id="1f1bf-260">MAKEFOURCC ( ' R '、' G '、' B '、' G ' ) </span><span class="sxs-lookup"><span data-stu-id="1f1bf-260">MAKEFOURCC('R', 'G', 'B', 'G')</span></span> | <span data-ttu-id="1f1bf-261">16位的壓縮 RGB 格式，類似于 UYVY (U0Y0、V0Y1、U2Y2 等等) 。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-261">A 16-bit packed RGB format analogous to UYVY (U0Y0, V0Y1, U2Y2, and so on).</span></span> <span data-ttu-id="1f1bf-262">它需要圖元配對，才能正確地表示色彩值。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-262">It requires a pixel pair in order to properly represent the color value.</span></span> <span data-ttu-id="1f1bf-263">配對中的第一個圖元包含8位的綠色 (的低8位) 和高8個位) 中的8位紅色 (。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-263">The first pixel in the pair contains 8 bits of green (in the low 8 bits) and 8 bits of red (in the high 8 bits).</span></span> <span data-ttu-id="1f1bf-264">第二個圖元包含8位的綠色 (的低8位) 和高8個位) 中的8位藍色 (。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-264">The second pixel contains 8 bits of green (in the low 8 bits) and 8 bits of blue (in the high 8 bits).</span></span> <span data-ttu-id="1f1bf-265">這兩個圖元一起共用 red 和 blue 元件，而每個圖元都有唯一的綠色元件 (R0G0、B0G1、R2G2 等) 。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-265">Together, the two pixels share the red and blue components, while each has a unique green component (R0G0, B0G1, R2G2, and so on).</span></span> <span data-ttu-id="1f1bf-266">當查閱圖元著色器時，紋理取樣器不會將色彩正規化;它們維持在 0.0 f 到 255.0 f 的範圍內。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-266">The texture sampler does not normalize the colors when looking up into a pixel shader; they remain in the range of 0.0f to 255.0f.</span></span> <span data-ttu-id="1f1bf-267">這適用于所有可程式化的圖元著色器模型。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-267">This is true for all programmable pixel shader models.</span></span> <span data-ttu-id="1f1bf-268">針對固定函式圖元著色器，硬體應該正規化為0到 1. f 範圍，並基本上將它視為 YUY2 材質。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-268">For the fixed function pixel shader, the hardware should normalize to the 0.f to 1.f range and essentially treat it as the YUY2 texture.</span></span> <span data-ttu-id="1f1bf-269">公開此格式的硬體必須將 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) 的 PixelShader1xMaxValue 成員設定為能夠處理該範圍的值。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-269">Hardware that exposes this format must have PixelShader1xMaxValue member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) set to a value capable of handling that range.</span></span>     |
| <span data-ttu-id="1f1bf-270">**D3DFMT \_ UYVY**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-270">**D3DFMT\_UYVY**</span></span>          | <span data-ttu-id="1f1bf-271">MAKEFOURCC ( ' U '、' Y '、' V '、' Y ' ) </span><span class="sxs-lookup"><span data-stu-id="1f1bf-271">MAKEFOURCC('U', 'Y', 'V', 'Y')</span></span> | <span data-ttu-id="1f1bf-272">UYVY 格式 (PC98 合規性) </span><span class="sxs-lookup"><span data-stu-id="1f1bf-272">UYVY format (PC98 compliance)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="1f1bf-273">**D3DFMT \_ YUY2**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-273">**D3DFMT\_YUY2**</span></span>          | <span data-ttu-id="1f1bf-274">MAKEFOURCC ( ' Y '、' U '、' Y '、' 2 ' ) </span><span class="sxs-lookup"><span data-stu-id="1f1bf-274">MAKEFOURCC('Y', 'U', 'Y', '2')</span></span> | <span data-ttu-id="1f1bf-275">YUY2 格式 (PC98 合規性) </span><span class="sxs-lookup"><span data-stu-id="1f1bf-275">YUY2 format (PC98 compliance)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



 

### <a name="ieee-formats"></a><span data-ttu-id="1f1bf-276">IEEE 格式</span><span class="sxs-lookup"><span data-stu-id="1f1bf-276">IEEE Formats</span></span>

<span data-ttu-id="1f1bf-277">這些旗標用於浮點介面格式。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-277">These flags are used for floating-point surface formats.</span></span> <span data-ttu-id="1f1bf-278">這些32位的每一通道格式也稱為 s23e8 格式。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-278">These 32-bits-per-channel formats are also known as s23e8 formats.</span></span>



| <span data-ttu-id="1f1bf-279">浮點數旗標</span><span class="sxs-lookup"><span data-stu-id="1f1bf-279">Floating-point flags</span></span>      | <span data-ttu-id="1f1bf-280">值</span><span class="sxs-lookup"><span data-stu-id="1f1bf-280">Value</span></span> | <span data-ttu-id="1f1bf-281">格式</span><span class="sxs-lookup"><span data-stu-id="1f1bf-281">Format</span></span>                                                                                   |
|---------------------------|-------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f1bf-282">**D3DFMT \_ R32F**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-282">**D3DFMT\_R32F**</span></span>          | <span data-ttu-id="1f1bf-283">114</span><span class="sxs-lookup"><span data-stu-id="1f1bf-283">114</span></span>   | <span data-ttu-id="1f1bf-284">使用32位作為紅色通道的32位浮點數格式。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-284">32-bit float format using 32 bits for the red channel.</span></span>                                   |
| <span data-ttu-id="1f1bf-285">**D3DFMT \_ G32R32F**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-285">**D3DFMT\_G32R32F**</span></span>       | <span data-ttu-id="1f1bf-286">115</span><span class="sxs-lookup"><span data-stu-id="1f1bf-286">115</span></span>   | <span data-ttu-id="1f1bf-287">適用于紅色通道的64位浮點數32格式，以及綠色通道的32位。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-287">64-bit float format using 32 bits for the red channel and 32 bits for the green channel.</span></span> |
| <span data-ttu-id="1f1bf-288">**D3DFMT \_ A32B32G32R32F**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-288">**D3DFMT\_A32B32G32R32F**</span></span> | <span data-ttu-id="1f1bf-289">116</span><span class="sxs-lookup"><span data-stu-id="1f1bf-289">116</span></span>   | <span data-ttu-id="1f1bf-290">針對每個通道使用32位的128位 float 格式 (Alpha、blue、綠、red) 。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-290">128-bit float format using 32 bits for the each channel (alpha, blue, green, red).</span></span>       |



 

### <a name="mixed-formats"></a><span data-ttu-id="1f1bf-291">混合格式</span><span class="sxs-lookup"><span data-stu-id="1f1bf-291">Mixed Formats</span></span>

<span data-ttu-id="1f1bf-292">混合格式的資料可以包含未簽署資料和已簽署資料的組合。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-292">Data in mixed formats can contain a combination of unsigned data and signed data.</span></span>



| <span data-ttu-id="1f1bf-293">混合格式旗標</span><span class="sxs-lookup"><span data-stu-id="1f1bf-293">Mixed format flags</span></span>      | <span data-ttu-id="1f1bf-294">值</span><span class="sxs-lookup"><span data-stu-id="1f1bf-294">Value</span></span> | <span data-ttu-id="1f1bf-295">格式</span><span class="sxs-lookup"><span data-stu-id="1f1bf-295">Format</span></span>                                                                                         |
|-------------------------|-------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f1bf-296">**D3DFMT \_ L6V5U5**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-296">**D3DFMT\_L6V5U5**</span></span>      | <span data-ttu-id="1f1bf-297">61</span><span class="sxs-lookup"><span data-stu-id="1f1bf-297">61</span></span>    | <span data-ttu-id="1f1bf-298">16位的 [使用亮度的亮度]、[亮度] 為 [亮度] 的亮度，以及 v 和您的5位。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-298">16-bit bump-map format with luminance using 6 bits for luminance, and 5 bits each for v and u.</span></span> |
| <span data-ttu-id="1f1bf-299">**D3DFMT \_ X8L8V8U8**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-299">**D3DFMT\_X8L8V8U8**</span></span>    | <span data-ttu-id="1f1bf-300">62</span><span class="sxs-lookup"><span data-stu-id="1f1bf-300">62</span></span>    | <span data-ttu-id="1f1bf-301">使用每個通道8位的亮度的32位凹凸對應格式。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-301">32-bit bump-map format with luminance using 8 bits for each channel.</span></span>                           |
| <span data-ttu-id="1f1bf-302">**D3DFMT \_ A2W10V10U10**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-302">**D3DFMT\_A2W10V10U10**</span></span> | <span data-ttu-id="1f1bf-303">67</span><span class="sxs-lookup"><span data-stu-id="1f1bf-303">67</span></span>    | <span data-ttu-id="1f1bf-304">32位的凹凸地圖格式，每個都使用2位來表示 w、v 和您的 Alpha 和10位。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-304">32-bit bump-map format using 2 bits for alpha and 10 bits each for w, v, and u.</span></span>                |



 

### <a name="signed-formats"></a><span data-ttu-id="1f1bf-305">簽署格式</span><span class="sxs-lookup"><span data-stu-id="1f1bf-305">Signed Formats</span></span>

<span data-ttu-id="1f1bf-306">採用帶正負號格式的資料可以是正數和負數。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-306">Data in a signed format can be both positive and negative.</span></span> <span data-ttu-id="1f1bf-307">簽署格式使用 (U) 、 (V) 、 (W) 和 (Q) 資料的組合。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-307">Signed formats use combinations of (U), (V), (W), and (Q) data.</span></span>



| <span data-ttu-id="1f1bf-308">帶正負號的格式旗標</span><span class="sxs-lookup"><span data-stu-id="1f1bf-308">Signed format flags</span></span>      | <span data-ttu-id="1f1bf-309">值</span><span class="sxs-lookup"><span data-stu-id="1f1bf-309">Value</span></span> | <span data-ttu-id="1f1bf-310">格式</span><span class="sxs-lookup"><span data-stu-id="1f1bf-310">Format</span></span>                                                                                                    |
|--------------------------|-------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f1bf-311">**D3DFMT \_ V8U8**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-311">**D3DFMT\_V8U8**</span></span>         | <span data-ttu-id="1f1bf-312">60</span><span class="sxs-lookup"><span data-stu-id="1f1bf-312">60</span></span>    | <span data-ttu-id="1f1bf-313">適用于您和 v 資料的16位凹凸地圖格式使用8個位。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-313">16-bit bump-map format using 8 bits each for u and v data.</span></span>                                                |
| <span data-ttu-id="1f1bf-314">**D3DFMT \_ Q8W8V8U8**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-314">**D3DFMT\_Q8W8V8U8**</span></span>     | <span data-ttu-id="1f1bf-315">63</span><span class="sxs-lookup"><span data-stu-id="1f1bf-315">63</span></span>    | <span data-ttu-id="1f1bf-316">每個通道使用8個位的32位凹凸對應格式。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-316">32-bit bump-map format using 8 bits for each channel.</span></span>                                                     |
| <span data-ttu-id="1f1bf-317">**D3DFMT \_ V16U16**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-317">**D3DFMT\_V16U16**</span></span>       | <span data-ttu-id="1f1bf-318">64</span><span class="sxs-lookup"><span data-stu-id="1f1bf-318">64</span></span>    | <span data-ttu-id="1f1bf-319">使用每個通道16個位的32位凹凸對應格式。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-319">32-bit bump-map format using 16 bits for each channel.</span></span>                                                    |
| <span data-ttu-id="1f1bf-320">**D3DFMT \_ Q16W16V16U16**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-320">**D3DFMT\_Q16W16V16U16**</span></span> | <span data-ttu-id="1f1bf-321">110</span><span class="sxs-lookup"><span data-stu-id="1f1bf-321">110</span></span>   | <span data-ttu-id="1f1bf-322">使用每個元件16個位的64位凹凸對應格式。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-322">64-bit bump-map format using 16 bits for each component.</span></span>                                                  |
| <span data-ttu-id="1f1bf-323">**D3DFMT \_ CxV8U8**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-323">**D3DFMT\_CxV8U8**</span></span>       | <span data-ttu-id="1f1bf-324">117</span><span class="sxs-lookup"><span data-stu-id="1f1bf-324">117</span></span>   | <span data-ttu-id="1f1bf-325">16位的一般壓縮格式。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-325">16-bit normal compression format.</span></span> <span data-ttu-id="1f1bf-326">紋理取樣器會計算來自： C = sqrt (1-U ²) 的 C 通道。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-326">The texture sampler computes the C channel from: C = sqrt(1 - U² - V²).</span></span> |



 

### <a name="unsigned-formats"></a><span data-ttu-id="1f1bf-327">不帶正負號的格式</span><span class="sxs-lookup"><span data-stu-id="1f1bf-327">Unsigned Formats</span></span>

<span data-ttu-id="1f1bf-328">不帶正負號格式的資料必須是正數。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-328">Data in an unsigned format must be positive.</span></span> <span data-ttu-id="1f1bf-329">不帶正負號的格式會使用 (R) ed 的組合、 (G) reen、 (B) ， () lpha、 (L) uminance，以及 (P) alette 資料。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-329">Unsigned formats use combinations of (R)ed, (G)reen, (B)lue, (A)lpha, (L)uminance, and (P)alette data.</span></span> <span data-ttu-id="1f1bf-330">因為資料是用來為調色板建立索引，所以調色板資料也稱為色彩索引資料。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-330">Palette data is also referred to as color indexed data because the data is used to index a color palette.</span></span>



| <span data-ttu-id="1f1bf-331">未簽署的格式旗標</span><span class="sxs-lookup"><span data-stu-id="1f1bf-331">Unsigned format flags</span></span>             | <span data-ttu-id="1f1bf-332">值</span><span class="sxs-lookup"><span data-stu-id="1f1bf-332">Value</span></span> | <span data-ttu-id="1f1bf-333">格式</span><span class="sxs-lookup"><span data-stu-id="1f1bf-333">Format</span></span>                                                                                                                                                                    |
|-----------------------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f1bf-334">**D3DFMT \_ R8G8B8**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-334">**D3DFMT\_R8G8B8**</span></span>                | <span data-ttu-id="1f1bf-335">20</span><span class="sxs-lookup"><span data-stu-id="1f1bf-335">20</span></span>    | <span data-ttu-id="1f1bf-336">24位 RGB 像素格式，每個通道8個位。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-336">24-bit RGB pixel format with 8 bits per channel.</span></span>                                                                                                                          |
| <span data-ttu-id="1f1bf-337">**D3DFMT \_ A8R8G8B8**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-337">**D3DFMT\_A8R8G8B8**</span></span>              | <span data-ttu-id="1f1bf-338">21</span><span class="sxs-lookup"><span data-stu-id="1f1bf-338">21</span></span>    | <span data-ttu-id="1f1bf-339">使用 Alpha 的32位 ARGB 像素格式，每個通道使用8個位。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-339">32-bit ARGB pixel format with alpha, using 8 bits per channel.</span></span>                                                                                                            |
| <span data-ttu-id="1f1bf-340">**D3DFMT \_ X8R8G8B8**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-340">**D3DFMT\_X8R8G8B8**</span></span>              | <span data-ttu-id="1f1bf-341">22</span><span class="sxs-lookup"><span data-stu-id="1f1bf-341">22</span></span>    | <span data-ttu-id="1f1bf-342">32位 RGB 像素格式，其中會為每個色彩保留8個位。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-342">32-bit RGB pixel format, where 8 bits are reserved for each color.</span></span>                                                                                                        |
| <span data-ttu-id="1f1bf-343">**D3DFMT \_ R5G6B5**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-343">**D3DFMT\_R5G6B5**</span></span>                | <span data-ttu-id="1f1bf-344">23</span><span class="sxs-lookup"><span data-stu-id="1f1bf-344">23</span></span>    | <span data-ttu-id="1f1bf-345">16位 RGB 像素格式，5位代表紅色，6位表示綠色，5位表示藍色。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-345">16-bit RGB pixel format with 5 bits for red, 6 bits for green, and 5 bits for blue.</span></span>                                                                                       |
| <span data-ttu-id="1f1bf-346">**D3DFMT \_ X1R5G5B5**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-346">**D3DFMT\_X1R5G5B5**</span></span>              | <span data-ttu-id="1f1bf-347">24</span><span class="sxs-lookup"><span data-stu-id="1f1bf-347">24</span></span>    | <span data-ttu-id="1f1bf-348">16位的像素格式，其中5個位會保留給每個色彩。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-348">16-bit pixel format where 5 bits are reserved for each color.</span></span>                                                                                                             |
| <span data-ttu-id="1f1bf-349">**D3DFMT \_ A1R5G5B5**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-349">**D3DFMT\_A1R5G5B5**</span></span>              | <span data-ttu-id="1f1bf-350">25</span><span class="sxs-lookup"><span data-stu-id="1f1bf-350">25</span></span>    | <span data-ttu-id="1f1bf-351">16位的像素格式，其中每個色彩都會保留5個位，而1位則保留給 Alpha。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-351">16-bit pixel format where 5 bits are reserved for each color and 1 bit is reserved for alpha.</span></span>                                                                             |
| <span data-ttu-id="1f1bf-352">**D3DFMT \_ A4R4G4B4**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-352">**D3DFMT\_A4R4G4B4**</span></span>              | <span data-ttu-id="1f1bf-353">26</span><span class="sxs-lookup"><span data-stu-id="1f1bf-353">26</span></span>    | <span data-ttu-id="1f1bf-354">16位 ARGB 像素格式，每個通道使用4個位。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-354">16-bit ARGB pixel format with 4 bits for each channel.</span></span>                                                                                                                    |
| <span data-ttu-id="1f1bf-355">**D3DFMT \_ R3G3B2**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-355">**D3DFMT\_R3G3B2**</span></span>                | <span data-ttu-id="1f1bf-356">27</span><span class="sxs-lookup"><span data-stu-id="1f1bf-356">27</span></span>    | <span data-ttu-id="1f1bf-357">8位 RGB 材質格式，使用3位的紅色，3位表示綠色，2位表示藍色。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-357">8-bit RGB texture format using 3 bits for red, 3 bits for green, and 2 bits for blue.</span></span>                                                                                     |
| <span data-ttu-id="1f1bf-358">**D3DFMT \_ A8**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-358">**D3DFMT\_A8**</span></span>                    | <span data-ttu-id="1f1bf-359">28</span><span class="sxs-lookup"><span data-stu-id="1f1bf-359">28</span></span>    | <span data-ttu-id="1f1bf-360">僅限8位 Alpha。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-360">8-bit alpha only.</span></span>                                                                                                                                                         |
| <span data-ttu-id="1f1bf-361">**D3DFMT \_ A8R3G3B2**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-361">**D3DFMT\_A8R3G3B2**</span></span>              | <span data-ttu-id="1f1bf-362">29</span><span class="sxs-lookup"><span data-stu-id="1f1bf-362">29</span></span>    | <span data-ttu-id="1f1bf-363">16位 ARGB 材質格式使用8位的 Alpha，每個都有3個位，紅色和綠色，2位表示藍色。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-363">16-bit ARGB texture format using 8 bits for alpha, 3 bits each for red and green, and 2 bits for blue.</span></span>                                                                    |
| <span data-ttu-id="1f1bf-364">**D3DFMT \_ X4R4G4B4**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-364">**D3DFMT\_X4R4G4B4**</span></span>              | <span data-ttu-id="1f1bf-365">30</span><span class="sxs-lookup"><span data-stu-id="1f1bf-365">30</span></span>    | <span data-ttu-id="1f1bf-366">針對每個色彩使用4個位的16位 RGB 像素格式。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-366">16-bit RGB pixel format using 4 bits for each color.</span></span>                                                                                                                      |
| <span data-ttu-id="1f1bf-367">**D3DFMT \_ A2B10G10R10**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-367">**D3DFMT\_A2B10G10R10**</span></span>           | <span data-ttu-id="1f1bf-368">31</span><span class="sxs-lookup"><span data-stu-id="1f1bf-368">31</span></span>    | <span data-ttu-id="1f1bf-369">針對每個色彩使用10個位的32位像素格式，以及 Alpha 的2位。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-369">32-bit pixel format using 10 bits for each color and 2 bits for alpha.</span></span>                                                                                                    |
| <span data-ttu-id="1f1bf-370">**D3DFMT \_ A8B8G8R8**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-370">**D3DFMT\_A8B8G8R8**</span></span>              | <span data-ttu-id="1f1bf-371">32</span><span class="sxs-lookup"><span data-stu-id="1f1bf-371">32</span></span>    | <span data-ttu-id="1f1bf-372">使用 Alpha 的32位 ARGB 像素格式，每個通道使用8個位。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-372">32-bit ARGB pixel format with alpha, using 8 bits per channel.</span></span>                                                                                                            |
| <span data-ttu-id="1f1bf-373">**D3DFMT \_ X8B8G8R8**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-373">**D3DFMT\_X8B8G8R8**</span></span>              | <span data-ttu-id="1f1bf-374">33</span><span class="sxs-lookup"><span data-stu-id="1f1bf-374">33</span></span>    | <span data-ttu-id="1f1bf-375">32位 RGB 像素格式，其中會為每個色彩保留8個位。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-375">32-bit RGB pixel format, where 8 bits are reserved for each color.</span></span>                                                                                                        |
| <span data-ttu-id="1f1bf-376">**D3DFMT \_ G16R16**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-376">**D3DFMT\_G16R16**</span></span>                | <span data-ttu-id="1f1bf-377">34</span><span class="sxs-lookup"><span data-stu-id="1f1bf-377">34</span></span>    | <span data-ttu-id="1f1bf-378">每個使用16個位的32位像素格式，以綠色和紅色表示。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-378">32-bit pixel format using 16 bits each for green and red.</span></span>                                                                                                                 |
| <span data-ttu-id="1f1bf-379">**D3DFMT \_ A2R10G10B10**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-379">**D3DFMT\_A2R10G10B10**</span></span>           | <span data-ttu-id="1f1bf-380">35</span><span class="sxs-lookup"><span data-stu-id="1f1bf-380">35</span></span>    | <span data-ttu-id="1f1bf-381">使用每個紅色、綠色和藍色10個位的32位像素格式，以及 Alpha 的2位。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-381">32-bit pixel format using 10 bits each for red, green, and blue, and 2 bits for alpha.</span></span>                                                                                    |
| <span data-ttu-id="1f1bf-382">**D3DFMT \_ A16B16G16R16**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-382">**D3DFMT\_A16B16G16R16**</span></span>          | <span data-ttu-id="1f1bf-383">36</span><span class="sxs-lookup"><span data-stu-id="1f1bf-383">36</span></span>    | <span data-ttu-id="1f1bf-384">每個元件使用16個位的64位像素格式。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-384">64-bit pixel format using 16 bits for each component.</span></span>                                                                                                                     |
| <span data-ttu-id="1f1bf-385">**D3DFMT \_ A8P8**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-385">**D3DFMT\_A8P8**</span></span>                  | <span data-ttu-id="1f1bf-386">40</span><span class="sxs-lookup"><span data-stu-id="1f1bf-386">40</span></span>    | <span data-ttu-id="1f1bf-387">8位色彩，以8位 Alpha 來編制索引。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-387">8-bit color indexed with 8 bits of alpha.</span></span>                                                                                                                                 |
| <span data-ttu-id="1f1bf-388">**D3DFMT \_ P8**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-388">**D3DFMT\_P8**</span></span>                    | <span data-ttu-id="1f1bf-389">41</span><span class="sxs-lookup"><span data-stu-id="1f1bf-389">41</span></span>    | <span data-ttu-id="1f1bf-390">8位色彩已編制索引。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-390">8-bit color indexed.</span></span>                                                                                                                                                      |
| <span data-ttu-id="1f1bf-391">**D3DFMT 的 \_ L8**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-391">**D3DFMT\_L8**</span></span>                    | <span data-ttu-id="1f1bf-392">50</span><span class="sxs-lookup"><span data-stu-id="1f1bf-392">50</span></span>    | <span data-ttu-id="1f1bf-393">僅限8位的亮度。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-393">8-bit luminance only.</span></span>                                                                                                                                                     |
| <span data-ttu-id="1f1bf-394">**D3DFMT \_ l16 也**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-394">**D3DFMT\_L16**</span></span>                   | <span data-ttu-id="1f1bf-395">81</span><span class="sxs-lookup"><span data-stu-id="1f1bf-395">81</span></span>    | <span data-ttu-id="1f1bf-396">僅限16位的亮度。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-396">16-bit luminance only.</span></span>                                                                                                                                                    |
| <span data-ttu-id="1f1bf-397">**D3DFMT \_ A8L8**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-397">**D3DFMT\_A8L8**</span></span>                  | <span data-ttu-id="1f1bf-398">51</span><span class="sxs-lookup"><span data-stu-id="1f1bf-398">51</span></span>    | <span data-ttu-id="1f1bf-399">16位使用8位，每個都用於 Alpha 和亮度。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-399">16-bit using 8 bits each for alpha and luminance.</span></span>                                                                                                                         |
| <span data-ttu-id="1f1bf-400">**D3DFMT \_ A4L4**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-400">**D3DFMT\_A4L4**</span></span>                  | <span data-ttu-id="1f1bf-401">52</span><span class="sxs-lookup"><span data-stu-id="1f1bf-401">52</span></span>    | <span data-ttu-id="1f1bf-402">8位，每個都使用4個位作為 Alpha 和亮度。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-402">8-bit using 4 bits each for alpha and luminance.</span></span>                                                                                                                          |
| <span data-ttu-id="1f1bf-403">**D3DFMT \_ A1**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-403">**D3DFMT\_A1**</span></span>                    | <span data-ttu-id="1f1bf-404">118</span><span class="sxs-lookup"><span data-stu-id="1f1bf-404">118</span></span>   | <span data-ttu-id="1f1bf-405">1位單色。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-405">1-bit monochrome.</span></span> <span data-ttu-id="1f1bf-406">**Direct3d 9 與 Direct3d 9Ex 之間的差異：** 此旗標僅適用于 Direct3D 9Ex。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-406">**Differences between Direct3D 9 and Direct3D 9Ex:** This flag is available in Direct3D 9Ex only.</span></span><br/>                                            |
| <span data-ttu-id="1f1bf-407">**D3DFMT \_ A2B10G10R10 \_ XR \_ 偏差**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-407">**D3DFMT\_A2B10G10R10\_XR\_BIAS**</span></span> | <span data-ttu-id="1f1bf-408">119</span><span class="sxs-lookup"><span data-stu-id="1f1bf-408">119</span></span>   | <span data-ttu-id="1f1bf-409">2.8-偏差固定點。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-409">2.8-biased fixed point.</span></span> <span data-ttu-id="1f1bf-410">**Direct3d 9 與 Direct3d 9Ex 之間的差異：** 此旗標僅適用于 Direct3D 9Ex。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-410">**Differences between Direct3D 9 and Direct3D 9Ex:** This flag is available in Direct3D 9Ex only.</span></span><br/>                                      |
| <span data-ttu-id="1f1bf-411">**D3DFMT \_ BINARYBUFFER**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-411">**D3DFMT\_BINARYBUFFER**</span></span>          | <span data-ttu-id="1f1bf-412">199</span><span class="sxs-lookup"><span data-stu-id="1f1bf-412">199</span></span>   | <span data-ttu-id="1f1bf-413">二進位格式，表示資料沒有任何固有型別。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-413">Binary format indicating that the data has no inherent type.</span></span> <span data-ttu-id="1f1bf-414">**Direct3d 9 與 Direct3d 9Ex 之間的差異：** 此旗標僅適用于 Direct3D 9Ex。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-414">**Differences between Direct3D 9 and Direct3D 9Ex:** This flag is available in Direct3D 9Ex only.</span></span><br/> |



 

### <a name="other"></a><span data-ttu-id="1f1bf-415">其他</span><span class="sxs-lookup"><span data-stu-id="1f1bf-415">Other</span></span>

<span data-ttu-id="1f1bf-416">此旗標用於未定義的格式。</span><span class="sxs-lookup"><span data-stu-id="1f1bf-416">This flag is used for undefined formats.</span></span>



| <span data-ttu-id="1f1bf-417">其他旗標</span><span class="sxs-lookup"><span data-stu-id="1f1bf-417">Other flags</span></span>         | <span data-ttu-id="1f1bf-418">值</span><span class="sxs-lookup"><span data-stu-id="1f1bf-418">Value</span></span> | <span data-ttu-id="1f1bf-419">格式</span><span class="sxs-lookup"><span data-stu-id="1f1bf-419">Format</span></span>                    |
|---------------------|-------|---------------------------|
| <span data-ttu-id="1f1bf-420">**D3DFMT \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="1f1bf-420">**D3DFMT\_UNKNOWN**</span></span> | <span data-ttu-id="1f1bf-421">0</span><span class="sxs-lookup"><span data-stu-id="1f1bf-421">0</span></span>     | <span data-ttu-id="1f1bf-422">介面格式不明</span><span class="sxs-lookup"><span data-stu-id="1f1bf-422">Surface format is unknown</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="1f1bf-423">規格需求</span><span class="sxs-lookup"><span data-stu-id="1f1bf-423">Requirements</span></span>



| <span data-ttu-id="1f1bf-424">需求</span><span class="sxs-lookup"><span data-stu-id="1f1bf-424">Requirement</span></span> | <span data-ttu-id="1f1bf-425">值</span><span class="sxs-lookup"><span data-stu-id="1f1bf-425">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f1bf-426">標頭</span><span class="sxs-lookup"><span data-stu-id="1f1bf-426">Header</span></span><br/> | <dl> <span data-ttu-id="1f1bf-427"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="1f1bf-427"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f1bf-428">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1f1bf-428">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f1bf-429">Direct3D 列舉</span><span class="sxs-lookup"><span data-stu-id="1f1bf-429">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




