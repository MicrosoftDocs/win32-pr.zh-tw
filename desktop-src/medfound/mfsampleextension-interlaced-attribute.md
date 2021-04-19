---
description: 指出影片框架是否為交錯式或漸進式。
ms.assetid: 3cb80e75-e803-493b-a22d-e485e77b5177
title: 'MFSampleExtension_Interlaced 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43a273b548192ac52da8604eb36fde5ec0e9fcf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974569"
---
# <a name="mfsampleextension_interlaced-attribute"></a><span data-ttu-id="fe25b-103">MFSampleExtension \_ 交錯屬性</span><span class="sxs-lookup"><span data-stu-id="fe25b-103">MFSampleExtension\_Interlaced attribute</span></span>

<span data-ttu-id="fe25b-104">指出影片框架是否為交錯式或漸進式。</span><span class="sxs-lookup"><span data-stu-id="fe25b-104">Indicates whether a video frame is interlaced or progressive.</span></span> <span data-ttu-id="fe25b-105">若 **為 TRUE**，則框架為交錯式。</span><span class="sxs-lookup"><span data-stu-id="fe25b-105">If **TRUE**, the frame is interlaced.</span></span> <span data-ttu-id="fe25b-106">如果 **為 FALSE**，則表示框架為漸進式。</span><span class="sxs-lookup"><span data-stu-id="fe25b-106">If **FALSE**, the frame is progressive.</span></span> <span data-ttu-id="fe25b-107">如果未設定，則媒體類型會描述交錯。</span><span class="sxs-lookup"><span data-stu-id="fe25b-107">If not set, the media type describes the interlacing.</span></span> <span data-ttu-id="fe25b-108">這個屬性會套用至媒體範例。</span><span class="sxs-lookup"><span data-stu-id="fe25b-108">This attribute applies to media samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="fe25b-109">資料類型</span><span class="sxs-lookup"><span data-stu-id="fe25b-109">Data type</span></span>

<span data-ttu-id="fe25b-110">**BOOL** 儲存為 **UINT32**</span><span class="sxs-lookup"><span data-stu-id="fe25b-110">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="fe25b-111">取得/設定</span><span class="sxs-lookup"><span data-stu-id="fe25b-111">Get/set</span></span>

<span data-ttu-id="fe25b-112">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="fe25b-112">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="fe25b-113">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="fe25b-113">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="fe25b-114">適用於</span><span class="sxs-lookup"><span data-stu-id="fe25b-114">Applies to</span></span>

[<span data-ttu-id="fe25b-115">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="fe25b-115">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="fe25b-116">備註</span><span class="sxs-lookup"><span data-stu-id="fe25b-116">Remarks</span></span>

<span data-ttu-id="fe25b-117">若為包含混合漸進和交錯框架的影片內容，請將媒體類型設定為交錯式，並在每個框架上使用此屬性，以指出框架是漸進式或交錯式。</span><span class="sxs-lookup"><span data-stu-id="fe25b-117">For video content that contains mixed progressive and interlaced frames, set the media type to interlaced and use this attribute on each frame to indicate whether the frame is progressive or interlaced.</span></span>

<span data-ttu-id="fe25b-118">若為完全交錯的影片內容，請將媒體類型設定為交錯式並省略這個屬性，或在每個範例上將它設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="fe25b-118">For video content that is entirely interlaced, set the media type to interlaced and omit this attribute, or set it to **TRUE** on every sample.</span></span>

<span data-ttu-id="fe25b-119">若為完全漸進的影片內容，請將媒體類型設定為漸進式並省略這個屬性，或在每個範例上將它設定為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="fe25b-119">For video content that is entirely progressive, set the media type to progressive and omit this attribute, or set it to **FALSE** on every sample.</span></span>

<span data-ttu-id="fe25b-120">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="fe25b-120">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe25b-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="fe25b-121">Requirements</span></span>



| <span data-ttu-id="fe25b-122">需求</span><span class="sxs-lookup"><span data-stu-id="fe25b-122">Requirement</span></span> | <span data-ttu-id="fe25b-123">值</span><span class="sxs-lookup"><span data-stu-id="fe25b-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fe25b-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fe25b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="fe25b-125">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fe25b-125">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="fe25b-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fe25b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="fe25b-127">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fe25b-127">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="fe25b-128">標頭</span><span class="sxs-lookup"><span data-stu-id="fe25b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe25b-129"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="fe25b-129"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe25b-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fe25b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe25b-131">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="fe25b-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="fe25b-132">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="fe25b-132">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="fe25b-133">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="fe25b-133">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="fe25b-134">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="fe25b-134">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[<span data-ttu-id="fe25b-135">範例屬性</span><span class="sxs-lookup"><span data-stu-id="fe25b-135">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="fe25b-136">媒體範例</span><span class="sxs-lookup"><span data-stu-id="fe25b-136">Media Samples</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="fe25b-137">影片交錯</span><span class="sxs-lookup"><span data-stu-id="fe25b-137">Video Interlacing</span></span>](video-interlacing.md)
</dt> </dl>

 

 




