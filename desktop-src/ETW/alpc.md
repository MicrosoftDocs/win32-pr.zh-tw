---
description: 這個類別是 advanced local procedure 呼叫事件的父類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 5380fada-50e7-4eb2-8549-6d738a56d2cd
title: ALPC 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2a4b09a8bab9280de8fb4c91368f5d6d93f7944a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972236"
---
# <a name="alpc-class"></a><span data-ttu-id="93a9c-104">ALPC 類別</span><span class="sxs-lookup"><span data-stu-id="93a9c-104">ALPC class</span></span>

<span data-ttu-id="93a9c-105">這個類別是 advanced local procedure 呼叫事件的父類別。</span><span class="sxs-lookup"><span data-stu-id="93a9c-105">This class is the parent class for advanced local procedure call events.</span></span>

<span data-ttu-id="93a9c-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="93a9c-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="93a9c-107">語法</span><span class="sxs-lookup"><span data-stu-id="93a9c-107">Syntax</span></span>

``` syntax
[Guid("{45d8cccd-539f-4b72-a8b7-5c683142609a}")]
class ALPC : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="93a9c-108">成員</span><span class="sxs-lookup"><span data-stu-id="93a9c-108">Members</span></span>

<span data-ttu-id="93a9c-109">**ALPC** 類別未定義任何成員。</span><span class="sxs-lookup"><span data-stu-id="93a9c-109">The **ALPC** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="93a9c-110">備註</span><span class="sxs-lookup"><span data-stu-id="93a9c-110">Remarks</span></span>

<span data-ttu-id="93a9c-111">若要在 NT 核心記錄會話中啟用 advanced local procedure 呼叫事件，請在呼叫 [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)函數時，于 [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)結構的 **EnableFlags** 成員中指定 **事件 \_ 追蹤 \_ 旗標 \_ ALPC** 旗標。</span><span class="sxs-lookup"><span data-stu-id="93a9c-111">To enable advanced local procedure call events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_ALPC** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="93a9c-112">事件追蹤取用者可以呼叫 [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) 函式，並將 [**ALPCGuid**](nt-kernel-logger-constants.md) 指定為 *PGUID* 參數，以針對 ALPC 事件執行特殊處理。</span><span class="sxs-lookup"><span data-stu-id="93a9c-112">Event trace consumers can implement special processing for ALPC events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**ALPCGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="93a9c-113">使用事件時，請使用下列事件種類來識別實際的 ALPC 事件。</span><span class="sxs-lookup"><span data-stu-id="93a9c-113">Use the following event types to identify the actual ALPC event when consuming events.</span></span>



| <span data-ttu-id="93a9c-114">事件類型</span><span class="sxs-lookup"><span data-stu-id="93a9c-114">Event type</span></span>           | <span data-ttu-id="93a9c-115">描述</span><span class="sxs-lookup"><span data-stu-id="93a9c-115">Description</span></span>                                                                                                                                         |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93a9c-116">事件種類值，33</span><span class="sxs-lookup"><span data-stu-id="93a9c-116">Event type value, 33</span></span> | <span data-ttu-id="93a9c-117">傳送訊息事件。</span><span class="sxs-lookup"><span data-stu-id="93a9c-117">Send message event.</span></span> <span data-ttu-id="93a9c-118">[**ALPC \_ 傳送 \_ 訊息**](alpc-send-message.md)MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="93a9c-118">The [**ALPC\_Send\_Message**](alpc-send-message.md) MOF class defines the event data for this event.</span></span>                           |
| <span data-ttu-id="93a9c-119">事件種類值，34</span><span class="sxs-lookup"><span data-stu-id="93a9c-119">Event type value, 34</span></span> | <span data-ttu-id="93a9c-120">接收訊息事件。</span><span class="sxs-lookup"><span data-stu-id="93a9c-120">Receive message event.</span></span> <span data-ttu-id="93a9c-121">[**ALPC \_ 接收 \_ 訊息**](alpc-receive-message.md)MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="93a9c-121">The [**ALPC\_Receive\_Message**](alpc-receive-message.md) MOF class defines the event data for this event.</span></span>                  |
| <span data-ttu-id="93a9c-122">事件種類值，35</span><span class="sxs-lookup"><span data-stu-id="93a9c-122">Event type value, 35</span></span> | <span data-ttu-id="93a9c-123">等候回復事件。</span><span class="sxs-lookup"><span data-stu-id="93a9c-123">Wait for reply event.</span></span> <span data-ttu-id="93a9c-124">[**ALPC \_ 等候 \_ \_ 回復**](alpc-wait-for-reply.md)MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="93a9c-124">The [**ALPC\_Wait\_For\_Reply**](alpc-wait-for-reply.md) MOF class defines the event data for this event.</span></span>                    |
| <span data-ttu-id="93a9c-125">事件種類值，36</span><span class="sxs-lookup"><span data-stu-id="93a9c-125">Event type value, 36</span></span> | <span data-ttu-id="93a9c-126">等候新的訊息事件。</span><span class="sxs-lookup"><span data-stu-id="93a9c-126">Wait for new message event.</span></span> <span data-ttu-id="93a9c-127">[**ALPC \_ 等候 \_ \_ 新 \_ 訊息**](alpc-wait-for-new-message.md)MOF 類別定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="93a9c-127">The [**ALPC\_Wait\_For\_New\_Message**](alpc-wait-for-new-message.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="93a9c-128">事件種類值，37</span><span class="sxs-lookup"><span data-stu-id="93a9c-128">Event type value, 37</span></span> | <span data-ttu-id="93a9c-129">停止等候事件。</span><span class="sxs-lookup"><span data-stu-id="93a9c-129">Stop waiting event.</span></span> <span data-ttu-id="93a9c-130">[**ALPC \_ Unwait**](alpc-unwait.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="93a9c-130">The [**ALPC\_Unwait**](alpc-unwait.md) MOF class defines the event data for this event.</span></span>                                        |



 

## <a name="requirements"></a><span data-ttu-id="93a9c-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="93a9c-131">Requirements</span></span>



| <span data-ttu-id="93a9c-132">需求</span><span class="sxs-lookup"><span data-stu-id="93a9c-132">Requirement</span></span> | <span data-ttu-id="93a9c-133">值</span><span class="sxs-lookup"><span data-stu-id="93a9c-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="93a9c-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="93a9c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="93a9c-135">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="93a9c-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="93a9c-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="93a9c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="93a9c-137">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="93a9c-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

