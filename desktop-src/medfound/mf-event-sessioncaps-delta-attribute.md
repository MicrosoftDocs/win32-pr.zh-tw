---
description: 包含旗標，這些旗標會根據目前的簡報，指出媒體會話中的哪些功能已變更。
ms.assetid: aa01d17f-f2ac-4504-b278-3edd90ab8a23
title: 'MF_EVENT_SESSIONCAPS_DELTA 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 284a31a8d3fc661c15e7de991972455468efbd40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386161"
---
# <a name="mf_event_sessioncaps_delta-attribute"></a><span data-ttu-id="c48ff-103">MF \_ 事件 \_ SESSIONCAPS \_ DELTA 屬性</span><span class="sxs-lookup"><span data-stu-id="c48ff-103">MF\_EVENT\_SESSIONCAPS\_DELTA attribute</span></span>

<span data-ttu-id="c48ff-104">包含旗標，這些旗標會根據目前的簡報，指出媒體會話中的哪些功能已變更。</span><span class="sxs-lookup"><span data-stu-id="c48ff-104">Contains flags that indicate which capabilities have changed in the Media Session, based on the current presentation.</span></span>

## <a name="data-type"></a><span data-ttu-id="c48ff-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="c48ff-105">Data type</span></span>

<span data-ttu-id="c48ff-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="c48ff-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="c48ff-107">備註</span><span class="sxs-lookup"><span data-stu-id="c48ff-107">Remarks</span></span>

<span data-ttu-id="c48ff-108">此屬性包含一個位元遮罩，指出哪些功能旗標已變更。</span><span class="sxs-lookup"><span data-stu-id="c48ff-108">This attribute contains a bitmask indicating which capabilities flags have changed.</span></span> <span data-ttu-id="c48ff-109">如需可能旗標的清單，請參閱 [**IMFMediaSession：： GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities)。</span><span class="sxs-lookup"><span data-stu-id="c48ff-109">For a list of possible flags, see [**IMFMediaSession::GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities).</span></span> <span data-ttu-id="c48ff-110">在位元遮罩中的位會設定為1，原因如下：</span><span class="sxs-lookup"><span data-stu-id="c48ff-110">Bits are set to 1 in the bitmask for any of the following reasons:</span></span>

-   <span data-ttu-id="c48ff-111">對應的功能位已從0變更為1。</span><span class="sxs-lookup"><span data-stu-id="c48ff-111">The corresponding capabilities bit changed from 0 to 1.</span></span>
-   <span data-ttu-id="c48ff-112">對應的功能位從1變更為0。</span><span class="sxs-lookup"><span data-stu-id="c48ff-112">The corresponding capabilities bit changed from 1 to 0.</span></span>
-   <span data-ttu-id="c48ff-113">對應的功能位保持為1，但功能的詳細資料已變更。</span><span class="sxs-lookup"><span data-stu-id="c48ff-113">The corresponding capabilities bit remained 1, but the details of the capability changed.</span></span> <span data-ttu-id="c48ff-114">例如，最大播放速率已變更。</span><span class="sxs-lookup"><span data-stu-id="c48ff-114">For example, the maximum playback rate changed.</span></span>

<span data-ttu-id="c48ff-115">這個屬性會與 [MESessionCapabilitiesChanged](mesessioncapabilitieschanged.md) 事件一起使用。</span><span class="sxs-lookup"><span data-stu-id="c48ff-115">This attribute is used with the [MESessionCapabilitiesChanged](mesessioncapabilitieschanged.md) event.</span></span>

<span data-ttu-id="c48ff-116">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="c48ff-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c48ff-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="c48ff-117">Requirements</span></span>



| <span data-ttu-id="c48ff-118">需求</span><span class="sxs-lookup"><span data-stu-id="c48ff-118">Requirement</span></span> | <span data-ttu-id="c48ff-119">值</span><span class="sxs-lookup"><span data-stu-id="c48ff-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c48ff-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c48ff-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c48ff-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c48ff-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c48ff-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c48ff-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c48ff-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c48ff-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c48ff-124">標頭</span><span class="sxs-lookup"><span data-stu-id="c48ff-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c48ff-125"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="c48ff-125"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c48ff-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c48ff-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c48ff-127">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="c48ff-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c48ff-128">事件屬性</span><span class="sxs-lookup"><span data-stu-id="c48ff-128">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="c48ff-129">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="c48ff-129">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="c48ff-130">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="c48ff-130">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




