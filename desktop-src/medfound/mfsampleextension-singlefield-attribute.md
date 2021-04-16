---
description: 指定影片範例是否包含單一欄位或兩個交錯欄位。 這個屬性會套用至媒體範例。
ms.assetid: 550619be-2042-4a2c-9ad2-728474835255
title: 'MFSampleExtension_SingleField 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 217d7c43a9777982485ba350d259a59a518e26c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512612"
---
# <a name="mfsampleextension_singlefield-attribute"></a><span data-ttu-id="2857c-104">MFSampleExtension \_ SingleField 屬性</span><span class="sxs-lookup"><span data-stu-id="2857c-104">MFSampleExtension\_SingleField attribute</span></span>

<span data-ttu-id="2857c-105">指定影片範例是否包含單一欄位或兩個交錯欄位。</span><span class="sxs-lookup"><span data-stu-id="2857c-105">Specifies whether a video sample contains a single field or two interleaved fields.</span></span> <span data-ttu-id="2857c-106">這個屬性會套用至媒體範例。</span><span class="sxs-lookup"><span data-stu-id="2857c-106">This attribute applies to media samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="2857c-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="2857c-107">Data type</span></span>

<span data-ttu-id="2857c-108">**BOOL** 儲存為 **UINT32**</span><span class="sxs-lookup"><span data-stu-id="2857c-108">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="2857c-109">取得/設定</span><span class="sxs-lookup"><span data-stu-id="2857c-109">Get/set</span></span>

<span data-ttu-id="2857c-110">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="2857c-110">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="2857c-111">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="2857c-111">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="2857c-112">適用於</span><span class="sxs-lookup"><span data-stu-id="2857c-112">Applies to</span></span>

[<span data-ttu-id="2857c-113">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="2857c-113">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="2857c-114">備註</span><span class="sxs-lookup"><span data-stu-id="2857c-114">Remarks</span></span>

<span data-ttu-id="2857c-115">如果值為 **TRUE**，此範例就會包含一個欄位。</span><span class="sxs-lookup"><span data-stu-id="2857c-115">If the value is **TRUE**, the sample contains one field.</span></span> <span data-ttu-id="2857c-116">如果值為 **FALSE** 或未設定屬性，則範例包含完整的框架。</span><span class="sxs-lookup"><span data-stu-id="2857c-116">If the value is **FALSE** or the attribute is not set, the sample contains a complete frame.</span></span> <span data-ttu-id="2857c-117">如果交錯式或漸進式框架， (兩個欄位。 ) </span><span class="sxs-lookup"><span data-stu-id="2857c-117">(Two fields if interlaced, or a progressive frame.)</span></span>

<span data-ttu-id="2857c-118">如果媒體類型是漸進式框架或交錯的欄位，這個屬性必須為 **FALSE** 或保持未設定。</span><span class="sxs-lookup"><span data-stu-id="2857c-118">If the media type is progressive frames or interleaved fields, this attribute must be **FALSE** or left unset.</span></span>

<span data-ttu-id="2857c-119">如果媒體類型是單一欄位，則此屬性必須為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="2857c-119">If the media type is single field, this attribute must be **TRUE**.</span></span> <span data-ttu-id="2857c-120">設定範例上的 [**MFSampleExtension \_ BottomFieldFirst**](mfsampleextension-bottomfieldfirst-attribute.md) 屬性，以指出它是上方欄位或較低的欄位。</span><span class="sxs-lookup"><span data-stu-id="2857c-120">Set the [**MFSampleExtension\_BottomFieldFirst**](mfsampleextension-bottomfieldfirst-attribute.md) attribute on the sample to indicate whether it is the upper field or the lower field.</span></span>

<span data-ttu-id="2857c-121">目前增強型影片轉譯器 (EVR) 不支援在交錯式框架和單一欄位之間切換的內容。</span><span class="sxs-lookup"><span data-stu-id="2857c-121">Currently the enhanced video renderer (EVR) does not support content that switches between interlaced frames and single fields.</span></span>

<span data-ttu-id="2857c-122">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="2857c-122">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="2857c-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="2857c-123">Requirements</span></span>



| <span data-ttu-id="2857c-124">需求</span><span class="sxs-lookup"><span data-stu-id="2857c-124">Requirement</span></span> | <span data-ttu-id="2857c-125">值</span><span class="sxs-lookup"><span data-stu-id="2857c-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2857c-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2857c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2857c-127">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2857c-127">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="2857c-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2857c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2857c-129">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2857c-129">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="2857c-130">標頭</span><span class="sxs-lookup"><span data-stu-id="2857c-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="2857c-131"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="2857c-131"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2857c-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2857c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2857c-133">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="2857c-133">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="2857c-134">範例屬性</span><span class="sxs-lookup"><span data-stu-id="2857c-134">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="2857c-135">媒體範例</span><span class="sxs-lookup"><span data-stu-id="2857c-135">Media Samples</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="2857c-136">影片交錯</span><span class="sxs-lookup"><span data-stu-id="2857c-136">Video Interlacing</span></span>](video-interlacing.md)
</dt> </dl>

 

 




