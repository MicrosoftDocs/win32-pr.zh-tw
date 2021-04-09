---
description: 媒體接收器轉譯新拓撲第一個樣本的呈現時間。
ms.assetid: 02a8c542-b519-495e-9fb2-8db2f5384db7
title: 'MF_EVENT_START_PRESENTATION_TIME_AT_OUTPUT 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a588bc6604deed6c6865cd8283390d28e3ffd49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850072"
---
# <a name="mf_event_start_presentation_time_at_output-attribute"></a><span data-ttu-id="ad18d-103">MF \_ 事件 \_ \_ \_ \_ 在 \_ 輸出屬性開始呈現時間</span><span class="sxs-lookup"><span data-stu-id="ad18d-103">MF\_EVENT\_START\_PRESENTATION\_TIME\_AT\_OUTPUT attribute</span></span>

<span data-ttu-id="ad18d-104">媒體接收器轉譯新拓撲第一個樣本的呈現時間。</span><span class="sxs-lookup"><span data-stu-id="ad18d-104">The presentation time at which the media sinks will render the first sample of the new topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="ad18d-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="ad18d-105">Data type</span></span>

<span data-ttu-id="ad18d-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="ad18d-106">**UINT64**</span></span>

<span data-ttu-id="ad18d-107">視為 **LONGLONG** 值。</span><span class="sxs-lookup"><span data-stu-id="ad18d-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad18d-108">備註</span><span class="sxs-lookup"><span data-stu-id="ad18d-108">Remarks</span></span>

<span data-ttu-id="ad18d-109">如果之前拓撲中的任何管線物件已緩衝處理資料，此值會稍微小於 [**MF \_ 事件 \_ 呈現 \_ 時間 \_ 位移**](mf-event-presentation-time-offset-attribute.md) 屬性中的值，因為接收必須轉譯緩衝的資料。</span><span class="sxs-lookup"><span data-stu-id="ad18d-109">If any pipeline objects in the previous topology buffered data, this value will be slightly less than the value in the [**MF\_EVENT\_PRESENTATION\_TIME\_OFFSET**](mf-event-presentation-time-offset-attribute.md) attribute, because the sinks must render the buffered data.</span></span>

<span data-ttu-id="ad18d-110">這個屬性是帶正負號的值，雖然它會儲存為 **UINT64**。</span><span class="sxs-lookup"><span data-stu-id="ad18d-110">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="ad18d-111">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="ad18d-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad18d-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="ad18d-112">Requirements</span></span>



| <span data-ttu-id="ad18d-113">需求</span><span class="sxs-lookup"><span data-stu-id="ad18d-113">Requirement</span></span> | <span data-ttu-id="ad18d-114">值</span><span class="sxs-lookup"><span data-stu-id="ad18d-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ad18d-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ad18d-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ad18d-116">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ad18d-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ad18d-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ad18d-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ad18d-118">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ad18d-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ad18d-119">標頭</span><span class="sxs-lookup"><span data-stu-id="ad18d-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad18d-120"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="ad18d-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad18d-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ad18d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad18d-122">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="ad18d-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ad18d-123">事件屬性</span><span class="sxs-lookup"><span data-stu-id="ad18d-123">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="ad18d-124">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="ad18d-124">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="ad18d-125">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="ad18d-125">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




