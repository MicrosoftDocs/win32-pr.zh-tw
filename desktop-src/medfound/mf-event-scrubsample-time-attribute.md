---
description: 在清除時轉譯之樣本的呈現時間。
ms.assetid: 6ce52cf5-014b-49a2-abf7-2c9cc5340a42
title: 'MF_EVENT_SCRUBSAMPLE_TIME 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de7c4fb1a8015367fa3d48edb066cdb135983926
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943788"
---
# <a name="mf_event_scrubsample_time-attribute"></a><span data-ttu-id="b1dc7-103">MF \_ 事件 \_ SCRUBSAMPLE \_ 時間屬性</span><span class="sxs-lookup"><span data-stu-id="b1dc7-103">MF\_EVENT\_SCRUBSAMPLE\_TIME attribute</span></span>

<span data-ttu-id="b1dc7-104">在清除時轉譯之樣本的呈現時間。</span><span class="sxs-lookup"><span data-stu-id="b1dc7-104">Presentation time for a sample that was rendered while scrubbing.</span></span>

## <a name="data-type"></a><span data-ttu-id="b1dc7-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="b1dc7-105">Data type</span></span>

<span data-ttu-id="b1dc7-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="b1dc7-106">**UINT64**</span></span>

<span data-ttu-id="b1dc7-107">視為 **LONGLONG** 值。</span><span class="sxs-lookup"><span data-stu-id="b1dc7-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1dc7-108">備註</span><span class="sxs-lookup"><span data-stu-id="b1dc7-108">Remarks</span></span>

<span data-ttu-id="b1dc7-109">這個屬性會與 [MEStreamSinkScrubSampleComplete](mestreamsinkscrubsamplecomplete.md) 事件一起使用。</span><span class="sxs-lookup"><span data-stu-id="b1dc7-109">This attribute is used with the [MEStreamSinkScrubSampleComplete](mestreamsinkscrubsamplecomplete.md) event.</span></span>

<span data-ttu-id="b1dc7-110">這個屬性是帶正負號的值，雖然它會儲存為 **UINT64**。</span><span class="sxs-lookup"><span data-stu-id="b1dc7-110">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="b1dc7-111">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="b1dc7-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1dc7-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="b1dc7-112">Requirements</span></span>



| <span data-ttu-id="b1dc7-113">需求</span><span class="sxs-lookup"><span data-stu-id="b1dc7-113">Requirement</span></span> | <span data-ttu-id="b1dc7-114">值</span><span class="sxs-lookup"><span data-stu-id="b1dc7-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b1dc7-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b1dc7-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b1dc7-116">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b1dc7-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b1dc7-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b1dc7-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b1dc7-118">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b1dc7-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b1dc7-119">標頭</span><span class="sxs-lookup"><span data-stu-id="b1dc7-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1dc7-120"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="b1dc7-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1dc7-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b1dc7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1dc7-122">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="b1dc7-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b1dc7-123">事件屬性</span><span class="sxs-lookup"><span data-stu-id="b1dc7-123">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="b1dc7-124">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="b1dc7-124">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="b1dc7-125">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="b1dc7-125">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




