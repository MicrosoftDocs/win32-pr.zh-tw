---
description: 當媒體來源要求新的播放速率時，這個屬性會指定來源是否也要求 thinning。 如需 thinning 的定義，請參閱關於速率控制。
ms.assetid: 42b6d0b3-e5af-4a48-969c-53628d1b7c31
title: 'MF_EVENT_DO_THINNING 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a08807413881a13789c50dbf2d063693e7e4539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943544"
---
# <a name="mf_event_do_thinning-attribute"></a><span data-ttu-id="bf0ae-104">MF \_ 事件 \_ DO \_ THINNING 屬性</span><span class="sxs-lookup"><span data-stu-id="bf0ae-104">MF\_EVENT\_DO\_THINNING attribute</span></span>

<span data-ttu-id="bf0ae-105">當媒體來源要求新的播放速率時，這個屬性會指定來源是否也要求 thinning。</span><span class="sxs-lookup"><span data-stu-id="bf0ae-105">When a media source requests a new playback rate, this attribute specifies whether the source also requests thinning.</span></span> <span data-ttu-id="bf0ae-106">如需 thinning 的定義，請參閱 [關於速率控制](about-rate-control.md)。</span><span class="sxs-lookup"><span data-stu-id="bf0ae-106">For a definition of thinning, see [About Rate Control](about-rate-control.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="bf0ae-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="bf0ae-107">Data type</span></span>

<span data-ttu-id="bf0ae-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="bf0ae-108">**UINT32**</span></span>

<span data-ttu-id="bf0ae-109">視為布林值。</span><span class="sxs-lookup"><span data-stu-id="bf0ae-109">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf0ae-110">備註</span><span class="sxs-lookup"><span data-stu-id="bf0ae-110">Remarks</span></span>

<span data-ttu-id="bf0ae-111">這個屬性會與 [MESourceRateChangeRequested](mesourceratechangerequested.md) 事件一起使用。</span><span class="sxs-lookup"><span data-stu-id="bf0ae-111">This attribute is used with the [MESourceRateChangeRequested](mesourceratechangerequested.md) event.</span></span> <span data-ttu-id="bf0ae-112">如果值為 **TRUE**，表示媒體來源要求切換至 thinned 播放。</span><span class="sxs-lookup"><span data-stu-id="bf0ae-112">If the value is **TRUE**, the media source is requesting a switch to thinned playback.</span></span>

<span data-ttu-id="bf0ae-113">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="bf0ae-113">The default value is **FALSE**.</span></span>

<span data-ttu-id="bf0ae-114">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="bf0ae-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf0ae-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="bf0ae-115">Requirements</span></span>



| <span data-ttu-id="bf0ae-116">需求</span><span class="sxs-lookup"><span data-stu-id="bf0ae-116">Requirement</span></span> | <span data-ttu-id="bf0ae-117">值</span><span class="sxs-lookup"><span data-stu-id="bf0ae-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bf0ae-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bf0ae-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bf0ae-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bf0ae-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="bf0ae-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bf0ae-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bf0ae-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bf0ae-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bf0ae-122">標頭</span><span class="sxs-lookup"><span data-stu-id="bf0ae-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf0ae-123"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="bf0ae-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf0ae-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bf0ae-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf0ae-125">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="bf0ae-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="bf0ae-126">事件屬性</span><span class="sxs-lookup"><span data-stu-id="bf0ae-126">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="bf0ae-127">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="bf0ae-127">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="bf0ae-128">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="bf0ae-128">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




