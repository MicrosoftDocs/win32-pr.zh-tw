---
description: 指定是否要重複交錯框架中的第一個欄位。 這個屬性會套用至媒體範例。
ms.assetid: c469f418-fa23-443f-8012-0d548ee98c17
title: 'MFSampleExtension_RepeatFirstField 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0af10157c280a3e48ed8f415529534fc97fd5cc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114404"
---
# <a name="mfsampleextension_repeatfirstfield-attribute"></a><span data-ttu-id="8b0b5-104">MFSampleExtension \_ RepeatFirstField 屬性</span><span class="sxs-lookup"><span data-stu-id="8b0b5-104">MFSampleExtension\_RepeatFirstField attribute</span></span>

<span data-ttu-id="8b0b5-105">指定是否要重複交錯框架中的第一個欄位。</span><span class="sxs-lookup"><span data-stu-id="8b0b5-105">Specifies whether to repeat the first field in an interlaced frame.</span></span> <span data-ttu-id="8b0b5-106">這個屬性會套用至媒體範例。</span><span class="sxs-lookup"><span data-stu-id="8b0b5-106">This attribute applies to media samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="8b0b5-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="8b0b5-107">Data type</span></span>

<span data-ttu-id="8b0b5-108">**BOOL** 儲存為 **UINT32**</span><span class="sxs-lookup"><span data-stu-id="8b0b5-108">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="8b0b5-109">取得/設定</span><span class="sxs-lookup"><span data-stu-id="8b0b5-109">Get/set</span></span>

<span data-ttu-id="8b0b5-110">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="8b0b5-110">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="8b0b5-111">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="8b0b5-111">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="8b0b5-112">適用於</span><span class="sxs-lookup"><span data-stu-id="8b0b5-112">Applies to</span></span>

[<span data-ttu-id="8b0b5-113">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="8b0b5-113">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="8b0b5-114">備註</span><span class="sxs-lookup"><span data-stu-id="8b0b5-114">Remarks</span></span>

<span data-ttu-id="8b0b5-115">如果值為 **FALSE** 或未設定屬性，則不會重複第一個欄位。</span><span class="sxs-lookup"><span data-stu-id="8b0b5-115">If the value is **FALSE** or the attribute is not set, the first field is not repeated.</span></span> <span data-ttu-id="8b0b5-116">如果值為 **TRUE**，則會重複第一個欄位。</span><span class="sxs-lookup"><span data-stu-id="8b0b5-116">If the value is **TRUE**, the first field is repeated.</span></span> <span data-ttu-id="8b0b5-117">只有當下列條件成立時，值 **true** 才有效：</span><span class="sxs-lookup"><span data-stu-id="8b0b5-117">The value **TRUE** is valid only when the following conditions are true:</span></span>

-   <span data-ttu-id="8b0b5-118">媒體類型為混合交錯和漸進式。</span><span class="sxs-lookup"><span data-stu-id="8b0b5-118">The media type is mixed interlaced and progressive.</span></span> <span data-ttu-id="8b0b5-119"> (媒體類型上的 [**MF \_ MT \_ 交錯 \_ 模式**](mf-mt-interlace-mode-attribute.md) 屬性屬性為 **MFVideoInterlace \_ MixedInterlaceOrProgressive**。 ) </span><span class="sxs-lookup"><span data-stu-id="8b0b5-119">(The [**MF\_MT\_INTERLACE\_MODE**](mf-mt-interlace-mode-attribute.md) attribute attribute on the media type is **MFVideoInterlace\_MixedInterlaceOrProgressive**.)</span></span>
-   <span data-ttu-id="8b0b5-120">框架是漸進式的，而範例上的 [**MFSampleExtension \_ 交錯**](mfsampleextension-interlaced-attribute.md) 屬性是 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="8b0b5-120">The frame is progressive and the [**MFSampleExtension\_Interlaced**](mfsampleextension-interlaced-attribute.md) attribute on the sample is **TRUE**.</span></span>
-   <span data-ttu-id="8b0b5-121">範例上會設定 [**MFSampleExtension \_ BottomFieldFirst**](mfsampleextension-bottomfieldfirst-attribute.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="8b0b5-121">The [**MFSampleExtension\_BottomFieldFirst**](mfsampleextension-bottomfieldfirst-attribute.md) attribute is set on the sample.</span></span> <span data-ttu-id="8b0b5-122">值可以是 **TRUE** 或 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="8b0b5-122">The value can be **TRUE** or **FALSE**.</span></span> <span data-ttu-id="8b0b5-123">欄位的排序是由這個屬性所決定。</span><span class="sxs-lookup"><span data-stu-id="8b0b5-123">The ordering of the fields is determined by this attribute.</span></span>

<span data-ttu-id="8b0b5-124">這個屬性是用於3:2 的下拉。</span><span class="sxs-lookup"><span data-stu-id="8b0b5-124">This attribute is used for 3:2 pulldown.</span></span> <span data-ttu-id="8b0b5-125">下表顯示欄位顯示的順序。</span><span class="sxs-lookup"><span data-stu-id="8b0b5-125">The following table shows the order in which fields are displayed.</span></span>



| <span data-ttu-id="8b0b5-126">MFSampleExtension \_ RepeatFirstField</span><span class="sxs-lookup"><span data-stu-id="8b0b5-126">MFSampleExtension\_RepeatFirstField</span></span> | <span data-ttu-id="8b0b5-127">MFSampleExtension \_ BottomFieldFirst</span><span class="sxs-lookup"><span data-stu-id="8b0b5-127">MFSampleExtension\_BottomFieldFirst</span></span> | <span data-ttu-id="8b0b5-128">欄位順序</span><span class="sxs-lookup"><span data-stu-id="8b0b5-128">Field order</span></span>         |
|-------------------------------------|-------------------------------------|---------------------|
| <span data-ttu-id="8b0b5-129">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="8b0b5-129">**TRUE**</span></span>                            | <span data-ttu-id="8b0b5-130">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="8b0b5-130">**TRUE**</span></span>                            | <span data-ttu-id="8b0b5-131">Lower、upper、lower</span><span class="sxs-lookup"><span data-stu-id="8b0b5-131">Lower, upper, lower</span></span> |
| <span data-ttu-id="8b0b5-132">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="8b0b5-132">**TRUE**</span></span>                            | <span data-ttu-id="8b0b5-133">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="8b0b5-133">**FALSE**</span></span>                           | <span data-ttu-id="8b0b5-134">Upper、lower、upper</span><span class="sxs-lookup"><span data-stu-id="8b0b5-134">Upper, lower, upper</span></span> |
| <span data-ttu-id="8b0b5-135">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="8b0b5-135">**FALSE**</span></span>                           | <span data-ttu-id="8b0b5-136">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="8b0b5-136">**TRUE**</span></span>                            | <span data-ttu-id="8b0b5-137">Lower、upper</span><span class="sxs-lookup"><span data-stu-id="8b0b5-137">Lower, upper</span></span>        |
| <span data-ttu-id="8b0b5-138">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="8b0b5-138">**FALSE**</span></span>                           | <span data-ttu-id="8b0b5-139">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="8b0b5-139">**FALSE**</span></span>                           | <span data-ttu-id="8b0b5-140">Upper、lower</span><span class="sxs-lookup"><span data-stu-id="8b0b5-140">Upper, lower</span></span>        |



 

<span data-ttu-id="8b0b5-141">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="8b0b5-141">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b0b5-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="8b0b5-142">Requirements</span></span>



| <span data-ttu-id="8b0b5-143">需求</span><span class="sxs-lookup"><span data-stu-id="8b0b5-143">Requirement</span></span> | <span data-ttu-id="8b0b5-144">值</span><span class="sxs-lookup"><span data-stu-id="8b0b5-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8b0b5-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8b0b5-145">Minimum supported client</span></span><br/> | <span data-ttu-id="8b0b5-146">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8b0b5-146">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="8b0b5-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8b0b5-147">Minimum supported server</span></span><br/> | <span data-ttu-id="8b0b5-148">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8b0b5-148">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="8b0b5-149">標頭</span><span class="sxs-lookup"><span data-stu-id="8b0b5-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b0b5-150"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="8b0b5-150"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b0b5-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8b0b5-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b0b5-152">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="8b0b5-152">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8b0b5-153">範例屬性</span><span class="sxs-lookup"><span data-stu-id="8b0b5-153">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="8b0b5-154">媒體範例</span><span class="sxs-lookup"><span data-stu-id="8b0b5-154">Media Samples</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="8b0b5-155">影片交錯</span><span class="sxs-lookup"><span data-stu-id="8b0b5-155">Video Interlacing</span></span>](video-interlacing.md)
</dt> </dl>

 

 




