---
description: 媒體會話引發事件的大約時間。
ms.assetid: 58083bc8-59cc-4503-8fae-36fcd864921a
title: 'MF_SESSION_APPROX_EVENT_OCCURRENCE_TIME 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a31b1970c2c9d86384c12c50777a8cee55e3ffd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978246"
---
# <a name="mf_session_approx_event_occurrence_time-attribute"></a><span data-ttu-id="332a6-103">MF \_ 會話 \_ 大約 \_ 發生事件 \_ 發生 \_ 時間屬性</span><span class="sxs-lookup"><span data-stu-id="332a6-103">MF\_SESSION\_APPROX\_EVENT\_OCCURRENCE\_TIME attribute</span></span>

<span data-ttu-id="332a6-104">媒體會話引發事件的大約時間。</span><span class="sxs-lookup"><span data-stu-id="332a6-104">The approximate time when the Media Session raised an event.</span></span>

## <a name="data-type"></a><span data-ttu-id="332a6-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="332a6-105">Data type</span></span>

<span data-ttu-id="332a6-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="332a6-106">**UINT64**</span></span>

<span data-ttu-id="332a6-107">視為 **LONGLONG** 值。</span><span class="sxs-lookup"><span data-stu-id="332a6-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="332a6-108">備註</span><span class="sxs-lookup"><span data-stu-id="332a6-108">Remarks</span></span>

<span data-ttu-id="332a6-109">媒體會話中的某些事件有此屬性。</span><span class="sxs-lookup"><span data-stu-id="332a6-109">Some events from the Media Session have this attribute.</span></span> <span data-ttu-id="332a6-110">此值會提供引發事件時的大約呈現時間。</span><span class="sxs-lookup"><span data-stu-id="332a6-110">The value gives the approximate presentation time when the event was raised.</span></span>

<span data-ttu-id="332a6-111">這個屬性是帶正負號的值，雖然它會儲存為 **UINT64**。</span><span class="sxs-lookup"><span data-stu-id="332a6-111">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="332a6-112">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="332a6-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="332a6-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="332a6-113">Requirements</span></span>



| <span data-ttu-id="332a6-114">需求</span><span class="sxs-lookup"><span data-stu-id="332a6-114">Requirement</span></span> | <span data-ttu-id="332a6-115">值</span><span class="sxs-lookup"><span data-stu-id="332a6-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="332a6-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="332a6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="332a6-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="332a6-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="332a6-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="332a6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="332a6-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="332a6-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="332a6-120">標頭</span><span class="sxs-lookup"><span data-stu-id="332a6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="332a6-121"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="332a6-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="332a6-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="332a6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="332a6-123">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="332a6-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="332a6-124">事件屬性</span><span class="sxs-lookup"><span data-stu-id="332a6-124">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="332a6-125">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="332a6-125">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="332a6-126">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="332a6-126">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




