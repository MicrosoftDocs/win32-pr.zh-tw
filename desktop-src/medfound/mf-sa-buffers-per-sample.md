---
description: 指定影片範例配置器為每個影片範例建立的緩衝區數目。
ms.assetid: A782BF8A-822A-407D-A30A-F2045BBB0BC0
title: 'MF_SA_BUFFERS_PER_SAMPLE 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d658ae72c53d986b364b2b6a3f405ae0052ea3fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691264"
---
# <a name="mf_sa_buffers_per_sample-attribute"></a><span data-ttu-id="68a4e-103">\_ \_ 每個範例的 MF SA 緩衝區 \_ \_ 屬性</span><span class="sxs-lookup"><span data-stu-id="68a4e-103">MF\_SA\_BUFFERS\_PER\_SAMPLE attribute</span></span>

<span data-ttu-id="68a4e-104">指定影片範例配置器為每個影片範例建立的緩衝區數目。</span><span class="sxs-lookup"><span data-stu-id="68a4e-104">Specifies how many buffers the video-sample allocator creates for each video sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="68a4e-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="68a4e-105">Data type</span></span>

<span data-ttu-id="68a4e-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="68a4e-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="68a4e-107">備註</span><span class="sxs-lookup"><span data-stu-id="68a4e-107">Remarks</span></span>

<span data-ttu-id="68a4e-108">如果您使用 [**IMFVideoSampleAllocatorEx**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex) 介面來配置影片範例，則可以使用此屬性來建立包含多個緩衝區的影片範例。</span><span class="sxs-lookup"><span data-stu-id="68a4e-108">If you use the [**IMFVideoSampleAllocatorEx**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex) interface to allocate video samples, you can use this attribute to create video samples that contain multiple buffers.</span></span> <span data-ttu-id="68a4e-109">例如，如果屬性值為2，配置器會為每個影片範例建立兩個影片緩衝區。</span><span class="sxs-lookup"><span data-stu-id="68a4e-109">For example, if the attribute value is 2, the allocator creates two video buffers for each video sample.</span></span> <span data-ttu-id="68a4e-110">在 [**IMFVideoSampleAllocatorEx：： InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex)方法的 *pAttributes* 參數中設定屬性。</span><span class="sxs-lookup"><span data-stu-id="68a4e-110">Set the attribute in the *pAttributes* parameter of the [**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) method.</span></span>

<span data-ttu-id="68a4e-111">預設值為 1。</span><span class="sxs-lookup"><span data-stu-id="68a4e-111">The default value is 1.</span></span> <span data-ttu-id="68a4e-112">如果未設定屬性，配置器會建立包含每個樣本單一緩衝區的影片範例。</span><span class="sxs-lookup"><span data-stu-id="68a4e-112">If the attribute is not set, the allocator creates video samples that contain a single buffer per sample.</span></span>

<span data-ttu-id="68a4e-113">這個屬性主要適用于在下列情況下，媒體基礎轉換 (MFTs 支援身歷聲3D 輸出的) ：</span><span class="sxs-lookup"><span data-stu-id="68a4e-113">This attribute is primarily intended for Media Foundation transforms (MFTs) that support stereo 3D output, in the following situation:</span></span>

-   <span data-ttu-id="68a4e-114">MFT 支援 Microsoft DirectX Graphic Infrastructure (DXGI) 。</span><span class="sxs-lookup"><span data-stu-id="68a4e-114">The MFT supports Microsoft DirectX Graphics Infrastructure (DXGI).</span></span>
-   <span data-ttu-id="68a4e-115">MFT 會配置自己的輸出範例。</span><span class="sxs-lookup"><span data-stu-id="68a4e-115">The MFT allocates its own output samples.</span></span>
-   <span data-ttu-id="68a4e-116">MFT 會使用 [**IMFVideoSampleAllocatorEx**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex) 介面來配置輸出範例。</span><span class="sxs-lookup"><span data-stu-id="68a4e-116">The MFT uses the [**IMFVideoSampleAllocatorEx**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex) interface to allocate the output samples.</span></span>
-   <span data-ttu-id="68a4e-117">3D 影片格式會針對每個視圖使用不同的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="68a4e-117">The 3D video format uses a separate buffer for each view.</span></span>

<span data-ttu-id="68a4e-118">如果上述所有準則都成立，則在每個 view) 中，MFT 應該將屬性值設定為 2 (一個緩衝區。</span><span class="sxs-lookup"><span data-stu-id="68a4e-118">If all of these criteria are true, the MFT should set the attribute value to 2 (one buffer per view).</span></span>

## <a name="requirements"></a><span data-ttu-id="68a4e-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="68a4e-119">Requirements</span></span>



| <span data-ttu-id="68a4e-120">需求</span><span class="sxs-lookup"><span data-stu-id="68a4e-120">Requirement</span></span> | <span data-ttu-id="68a4e-121">值</span><span class="sxs-lookup"><span data-stu-id="68a4e-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="68a4e-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="68a4e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="68a4e-123">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="68a4e-123">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="68a4e-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="68a4e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="68a4e-125">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="68a4e-125">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="68a4e-126">標頭</span><span class="sxs-lookup"><span data-stu-id="68a4e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="68a4e-127"><dt>Mftransform。h</dt></span><span class="sxs-lookup"><span data-stu-id="68a4e-127"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68a4e-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="68a4e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68a4e-129">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="68a4e-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




