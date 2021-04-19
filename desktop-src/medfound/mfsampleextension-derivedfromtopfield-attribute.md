---
description: 指定 deinterlaced 的影片框架是否衍生自上方欄位或下方欄位。
ms.assetid: 3710ab94-afb3-44d3-a680-b4a716810ec1
title: 'MFSampleExtension_DerivedFromTopField 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f90a67edf0b08337748bc118b0aa4ff024ec0ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974610"
---
# <a name="mfsampleextension_derivedfromtopfield-attribute"></a><span data-ttu-id="e127f-103">MFSampleExtension \_ DerivedFromTopField 屬性</span><span class="sxs-lookup"><span data-stu-id="e127f-103">MFSampleExtension\_DerivedFromTopField attribute</span></span>

<span data-ttu-id="e127f-104">指定 deinterlaced 的影片框架是否衍生自上方欄位或下方欄位。</span><span class="sxs-lookup"><span data-stu-id="e127f-104">Specifies whether a deinterlaced video frame was derived from the upper field or the lower field.</span></span> <span data-ttu-id="e127f-105">這個屬性會套用至媒體範例。</span><span class="sxs-lookup"><span data-stu-id="e127f-105">This attribute applies to media samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="e127f-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="e127f-106">Data type</span></span>

<span data-ttu-id="e127f-107">**BOOL** 儲存為 **UINT32**</span><span class="sxs-lookup"><span data-stu-id="e127f-107">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="e127f-108">取得/設定</span><span class="sxs-lookup"><span data-stu-id="e127f-108">Get/set</span></span>

<span data-ttu-id="e127f-109">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="e127f-109">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="e127f-110">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="e127f-110">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="e127f-111">適用於</span><span class="sxs-lookup"><span data-stu-id="e127f-111">Applies to</span></span>

[<span data-ttu-id="e127f-112">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="e127f-112">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="e127f-113">備註</span><span class="sxs-lookup"><span data-stu-id="e127f-113">Remarks</span></span>

<span data-ttu-id="e127f-114">這個屬性僅適用于 deinterlaced 範例。</span><span class="sxs-lookup"><span data-stu-id="e127f-114">This attribute is valid for deinterlaced samples only.</span></span> <span data-ttu-id="e127f-115">如果框架是藉由插上其中一個欄位來 deinterlaced，則設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="e127f-115">Set this attribute if the frame was deinterlaced by interpolating one of the fields.</span></span>

<span data-ttu-id="e127f-116">如果值為 **TRUE**，則會從上方欄位中插入較低的欄位。</span><span class="sxs-lookup"><span data-stu-id="e127f-116">If the value is **TRUE**, the lower field was interpolated from the upper field.</span></span> <span data-ttu-id="e127f-117">如果值為 **FALSE**，則會從較低的欄位內插上上方欄位。</span><span class="sxs-lookup"><span data-stu-id="e127f-117">If the value is **FALSE**, the upper field was interpolated from the lower field.</span></span>

<span data-ttu-id="e127f-118">如果未設定屬性，則不會 deinterlaced 框架。</span><span class="sxs-lookup"><span data-stu-id="e127f-118">If the attribute is not set, the frame has not been deinterlaced.</span></span> <span data-ttu-id="e127f-119">框架是真實的漸進式框架，也就是交錯的框架。</span><span class="sxs-lookup"><span data-stu-id="e127f-119">The frame is either a true progressive frame, or it is an interlaced frame.</span></span>

<span data-ttu-id="e127f-120">這個屬性是參考資訊。</span><span class="sxs-lookup"><span data-stu-id="e127f-120">This attribute is informational.</span></span> <span data-ttu-id="e127f-121">軟體 deinterlacer 可以設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="e127f-121">A software deinterlacer could set this attribute.</span></span> <span data-ttu-id="e127f-122">如果設定此屬性，它會提供提示，讓您藉由卸載插入的掃描行來復原原始欄位。</span><span class="sxs-lookup"><span data-stu-id="e127f-122">If this attribute is set, it provides a hint that you can recover the original field by dropping the interpolated scan lines.</span></span> <span data-ttu-id="e127f-123">例如，如果屬性為 **TRUE**，您可以藉由卸載插入的下半部欄位來復原原始的上方欄位。</span><span class="sxs-lookup"><span data-stu-id="e127f-123">For example, if the attribute is **TRUE**, you can recover the original upper field by dropping the interpolated lower field.</span></span>

<span data-ttu-id="e127f-124">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="e127f-124">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e127f-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="e127f-125">Requirements</span></span>



| <span data-ttu-id="e127f-126">需求</span><span class="sxs-lookup"><span data-stu-id="e127f-126">Requirement</span></span> | <span data-ttu-id="e127f-127">值</span><span class="sxs-lookup"><span data-stu-id="e127f-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e127f-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e127f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e127f-129">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e127f-129">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="e127f-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e127f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e127f-131">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e127f-131">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="e127f-132">標頭</span><span class="sxs-lookup"><span data-stu-id="e127f-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="e127f-133"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="e127f-133"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e127f-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e127f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e127f-135">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="e127f-135">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e127f-136">範例屬性</span><span class="sxs-lookup"><span data-stu-id="e127f-136">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="e127f-137">媒體範例</span><span class="sxs-lookup"><span data-stu-id="e127f-137">Media Samples</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="e127f-138">影片交錯</span><span class="sxs-lookup"><span data-stu-id="e127f-138">Video Interlacing</span></span>](video-interlacing.md)
</dt> </dl>

 

 




