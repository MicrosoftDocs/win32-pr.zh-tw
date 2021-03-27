---
description: 此類別是 UDP/IP 事件的父類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 0fbecad2-0221-408e-9f43-859547efa803
title: UdpIp 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5116b5f97a4aa7e3bafa9da1c1208ce7ee9d5794
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512185"
---
# <a name="udpip-class"></a><span data-ttu-id="7b628-104">UdpIp 類別</span><span class="sxs-lookup"><span data-stu-id="7b628-104">UdpIp class</span></span>

<span data-ttu-id="7b628-105">此類別是 UDP/IP 事件的父類別。</span><span class="sxs-lookup"><span data-stu-id="7b628-105">This class is the parent class for UDP/IP events.</span></span>

<span data-ttu-id="7b628-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="7b628-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b628-107">語法</span><span class="sxs-lookup"><span data-stu-id="7b628-107">Syntax</span></span>

``` syntax
[Guid("{bf3a50c5-a9c9-4988-a005-2df0b7c80f80}"), EventVersion(2)]
class UdpIp : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="7b628-108">成員</span><span class="sxs-lookup"><span data-stu-id="7b628-108">Members</span></span>

<span data-ttu-id="7b628-109">**UdpIp** 類別不會定義任何成員。</span><span class="sxs-lookup"><span data-stu-id="7b628-109">The **UdpIp** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b628-110">備註</span><span class="sxs-lookup"><span data-stu-id="7b628-110">Remarks</span></span>

<span data-ttu-id="7b628-111">若要在 NT 核心記錄會話中啟用 UDP/IP 事件，請在呼叫 [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)函數時，于 [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)結構的 **EnableFlags** 成員中指定 **事件 \_ 追蹤 \_ 旗標 \_ 網路 \_ TCPIP** 旗標。</span><span class="sxs-lookup"><span data-stu-id="7b628-111">To enable UDP/IP events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_NETWORK\_TCPIP** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="7b628-112">事件追蹤取用者可以呼叫 [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) 函式，並將 [**UdpIpGuid**](nt-kernel-logger-constants.md) 指定為 *PGUID* 參數，以針對 UDP/IP 事件執行特殊處理。</span><span class="sxs-lookup"><span data-stu-id="7b628-112">Event trace consumers can implement special processing for UDP/IP events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**UdpIpGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="7b628-113">使用下列事件種類來識別使用事件時的實際網路 (UDP/IP) 事件。</span><span class="sxs-lookup"><span data-stu-id="7b628-113">Use the following event types to identify the actual network (UDP/IP) event when consuming events.</span></span>



| <span data-ttu-id="7b628-114">事件類型</span><span class="sxs-lookup"><span data-stu-id="7b628-114">Event type</span></span>                                                         | <span data-ttu-id="7b628-115">描述</span><span class="sxs-lookup"><span data-stu-id="7b628-115">Description</span></span>                                                                                                                         |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b628-116">**活動 \_追蹤 \_ 類型 \_ 接收** (事件種類值為 11) </span><span class="sxs-lookup"><span data-stu-id="7b628-116">**EVENT\_TRACE\_TYPE\_RECEIVE**(Event type value is 11)</span></span><br/> | <span data-ttu-id="7b628-117">IPv4 通訊協定的接收事件。</span><span class="sxs-lookup"><span data-stu-id="7b628-117">Receive event for IPv4 protocol.</span></span> <span data-ttu-id="7b628-118">[**UdpIp \_ TypeGroup1**](udpip-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="7b628-118">The [**UdpIp\_TypeGroup1**](udpip-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="7b628-119">**活動 \_追蹤 \_ 類型 \_ 傳送** (事件種類值為 10) </span><span class="sxs-lookup"><span data-stu-id="7b628-119">**EVENT\_TRACE\_TYPE\_SEND**(Event type value is 10)</span></span><br/>    | <span data-ttu-id="7b628-120">傳送 IPv4 通訊協定的事件。</span><span class="sxs-lookup"><span data-stu-id="7b628-120">Send event for IPv4 protocol.</span></span> <span data-ttu-id="7b628-121">[**UdpIp \_ TypeGroup1**](udpip-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="7b628-121">The [**UdpIp\_TypeGroup1**](udpip-typegroup1.md) MOF class defines the event data for this event.</span></span>    |
| <span data-ttu-id="7b628-122">事件種類值17</span><span class="sxs-lookup"><span data-stu-id="7b628-122">Event type value, 17</span></span>                                               | <span data-ttu-id="7b628-123">Fail 事件。</span><span class="sxs-lookup"><span data-stu-id="7b628-123">Fail event.</span></span> <span data-ttu-id="7b628-124">[**UdpIp \_ Fail**](udpip-fail.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="7b628-124">The [**UdpIp\_Fail**](udpip-fail.md) MOF class defines the event data for this event.</span></span>                                  |
| <span data-ttu-id="7b628-125">事件種類值，26</span><span class="sxs-lookup"><span data-stu-id="7b628-125">Event type value, 26</span></span>                                               | <span data-ttu-id="7b628-126">IPv6 通訊協定的傳送事件。</span><span class="sxs-lookup"><span data-stu-id="7b628-126">Send event for IPv6 protocol.</span></span> <span data-ttu-id="7b628-127">[**UdpIp \_ TypeGroup2**](udpip-typegroup2.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="7b628-127">The [**UdpIp\_TypeGroup2**](udpip-typegroup2.md) MOF class defines the event data for this event.</span></span>    |
| <span data-ttu-id="7b628-128">事件種類值，27</span><span class="sxs-lookup"><span data-stu-id="7b628-128">Event type value, 27</span></span>                                               | <span data-ttu-id="7b628-129">IPv6 通訊協定的接收事件。</span><span class="sxs-lookup"><span data-stu-id="7b628-129">Receive event for IPv6 protocol.</span></span> <span data-ttu-id="7b628-130">[**UdpIp \_ TypeGroup2**](udpip-typegroup2.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="7b628-130">The [**UdpIp\_TypeGroup2**](udpip-typegroup2.md) MOF class defines the event data for this event.</span></span> |



 

<span data-ttu-id="7b628-131">您可以使用 **ProcessId** 屬性，將網路事件追蹤至來源和目的地進程。</span><span class="sxs-lookup"><span data-stu-id="7b628-131">You can trace network events to a source and destination process using the **ProcessId** property.</span></span> <span data-ttu-id="7b628-132">由於部分網路事件是由個別的執行緒所記錄，因此您可能無法使用 [**事件 \_ 追蹤 \_ 標頭**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header)的 **ProcessId** 和 **ThreadId** 成員來識別產生網路活動的進程或執行緒。</span><span class="sxs-lookup"><span data-stu-id="7b628-132">Because some network events are logged by separate threads, you may not be able to use the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) to identify the process or thread that originated the network activities.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b628-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="7b628-133">Requirements</span></span>



| <span data-ttu-id="7b628-134">需求</span><span class="sxs-lookup"><span data-stu-id="7b628-134">Requirement</span></span> | <span data-ttu-id="7b628-135">值</span><span class="sxs-lookup"><span data-stu-id="7b628-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7b628-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7b628-136">Minimum supported client</span></span><br/> | <span data-ttu-id="7b628-137">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7b628-137">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7b628-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7b628-138">Minimum supported server</span></span><br/> | <span data-ttu-id="7b628-139">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7b628-139">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7b628-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7b628-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b628-141">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="7b628-141">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="7b628-142">**UdpIp \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="7b628-142">**UdpIp\_Fail**</span></span>](udpip-fail.md)
</dt> <dt>

[<span data-ttu-id="7b628-143">**UdpIp \_ TypeGroup1**</span><span class="sxs-lookup"><span data-stu-id="7b628-143">**UdpIp\_TypeGroup1**</span></span>](udpip-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="7b628-144">**UdpIp \_ TypeGroup2**</span><span class="sxs-lookup"><span data-stu-id="7b628-144">**UdpIp\_TypeGroup2**</span></span>](udpip-typegroup2.md)
</dt> <dt>

[<span data-ttu-id="7b628-145">**UdpIp \_ V0**</span><span class="sxs-lookup"><span data-stu-id="7b628-145">**UdpIp\_V0**</span></span>](udpip-v0.md)
</dt> <dt>

[<span data-ttu-id="7b628-146">**UdpIp \_ V1**</span><span class="sxs-lookup"><span data-stu-id="7b628-146">**UdpIp\_V1**</span></span>](udpip-v1.md)
</dt> </dl>

 

 
