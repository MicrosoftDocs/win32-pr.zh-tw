---
description: 下列 Guid 用於 DirectShow 中的事件追蹤。
ms.assetid: 438938fe-37e7-45d6-b49a-d96698307f25
title: '追蹤 Guid (PerfStruct .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_AUDIOBREAK
- GUID_DSHOW_CTL
- GUID_STREAMTRACE
- GUID_VIDEOREND
api_type:
- HeaderDef
api_location:
- PerfStruct.h
ms.openlocfilehash: 4b2f2a6a678c029d01d9bf55481837d81d48557e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990761"
---
# <a name="trace-guids"></a><span data-ttu-id="3cc9c-103">追蹤 Guid</span><span class="sxs-lookup"><span data-stu-id="3cc9c-103">Trace GUIDs</span></span>

<span data-ttu-id="3cc9c-104">下列 Guid 用於 DirectShow 中的事件追蹤。</span><span class="sxs-lookup"><span data-stu-id="3cc9c-104">The following GUIDs are used for event tracing in DirectShow.</span></span>



| <span data-ttu-id="3cc9c-105">GUID</span><span class="sxs-lookup"><span data-stu-id="3cc9c-105">GUID</span></span>                                                                                                                                                                   | <span data-ttu-id="3cc9c-106">Description</span><span class="sxs-lookup"><span data-stu-id="3cc9c-106">Description</span></span>                                                                                                                                                  |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_AUDIOBREAK"></span><span id="guid_audiobreak"></span><dl> <span data-ttu-id="3cc9c-107"><dt>**GUID \_ AUDIOBREAK**</dt></span><span class="sxs-lookup"><span data-stu-id="3cc9c-107"><dt>**GUID\_AUDIOBREAK**</dt></span></span> </dl>    | <span data-ttu-id="3cc9c-108">音訊中斷事件。</span><span class="sxs-lookup"><span data-stu-id="3cc9c-108">Audio break event.</span></span> <span data-ttu-id="3cc9c-109">此類型的事件會針對事件資料使用 [**PERFINFO \_ DSHOW \_ AUDIOBREAK**](perfinfo-dshow-audiobreak.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="3cc9c-109">Events of this type use the [**PERFINFO\_DSHOW\_AUDIOBREAK**](perfinfo-dshow-audiobreak.md) structure for event data.</span></span><br/>         |
| <span id="GUID_DSHOW_CTL"></span><span id="guid_dshow_ctl"></span><dl> <span data-ttu-id="3cc9c-110"><dt>**GUID \_ DSHOW \_ CTL**</dt></span><span class="sxs-lookup"><span data-stu-id="3cc9c-110"><dt>**GUID\_DSHOW\_CTL**</dt></span></span> </dl>      | <span data-ttu-id="3cc9c-111">DirectShow 事件提供者。</span><span class="sxs-lookup"><span data-stu-id="3cc9c-111">DirectShow event provider.</span></span><br/>                                                                                                                        |
| <span id="GUID_STREAMTRACE"></span><span id="guid_streamtrace"></span><dl> <span data-ttu-id="3cc9c-112"><dt>**GUID \_ STREAMTRACE**</dt></span><span class="sxs-lookup"><span data-stu-id="3cc9c-112"><dt>**GUID\_STREAMTRACE**</dt></span></span> </dl> | <span data-ttu-id="3cc9c-113">一般串流事件。</span><span class="sxs-lookup"><span data-stu-id="3cc9c-113">General streaming event.</span></span> <span data-ttu-id="3cc9c-114">此類型的事件會針對事件資料使用 [**PERFINFO \_ DSHOW \_ STREAMTRACE**](perfinfo-dshow-streamtrace.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="3cc9c-114">Events of this type use the [**PERFINFO\_DSHOW\_STREAMTRACE**](perfinfo-dshow-streamtrace.md) structure for event data.</span></span><br/> |
| <span id="GUID_VIDEOREND"></span><span id="guid_videorend"></span><dl> <span data-ttu-id="3cc9c-115"><dt>**GUID \_ VIDEOREND**</dt></span><span class="sxs-lookup"><span data-stu-id="3cc9c-115"><dt>**GUID\_VIDEOREND**</dt></span></span> </dl>       | <span data-ttu-id="3cc9c-116">影片呈現事件。</span><span class="sxs-lookup"><span data-stu-id="3cc9c-116">Video rendering event.</span></span> <span data-ttu-id="3cc9c-117">此類型的事件會針對事件資料使用 [**PERFINFO \_ DSHOW \_ AVREND**](perfinfo-dshow-avrend.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="3cc9c-117">Events of this type use the [**PERFINFO\_DSHOW\_AVREND**](perfinfo-dshow-avrend.md) structure for event data.</span></span><br/>             |



## <a name="requirements"></a><span data-ttu-id="3cc9c-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="3cc9c-118">Requirements</span></span>



| <span data-ttu-id="3cc9c-119">需求</span><span class="sxs-lookup"><span data-stu-id="3cc9c-119">Requirement</span></span> | <span data-ttu-id="3cc9c-120">值</span><span class="sxs-lookup"><span data-stu-id="3cc9c-120">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3cc9c-121">標頭</span><span class="sxs-lookup"><span data-stu-id="3cc9c-121">Header</span></span><br/> | <dl> <span data-ttu-id="3cc9c-122"><dt>PerfStruct。h</dt></span><span class="sxs-lookup"><span data-stu-id="3cc9c-122"><dt>PerfStruct.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cc9c-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3cc9c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cc9c-124">DirectShow 中的事件追蹤</span><span class="sxs-lookup"><span data-stu-id="3cc9c-124">Event Tracing in DirectShow</span></span>](event-tracing-in-directshow.md)
</dt> </dl>

 

 




