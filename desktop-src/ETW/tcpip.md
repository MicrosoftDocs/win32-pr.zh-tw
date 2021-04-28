---
description: TcpIp 類別-此類別是 TCP/IP 事件的父類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: f9d6ea8f-c777-4747-89f4-f389c6eeac35
title: TcpIp 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp
api_type:
- NA
api_location: ''
ms.openlocfilehash: abcd805b417451adf2122e7baf3310be101a35ff
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105726"
---
# <a name="tcpip-class"></a><span data-ttu-id="1a2ec-104">TcpIp 類別</span><span class="sxs-lookup"><span data-stu-id="1a2ec-104">TcpIp class</span></span>

<span data-ttu-id="1a2ec-105">這個類別是 TCP/IP 事件的父類別。</span><span class="sxs-lookup"><span data-stu-id="1a2ec-105">This class is the parent class for TCP/IP events.</span></span>

<span data-ttu-id="1a2ec-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="1a2ec-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a2ec-107">語法</span><span class="sxs-lookup"><span data-stu-id="1a2ec-107">Syntax</span></span>

``` syntax
[Guid("{9a280ac0-c8e0-11d1-84e2-00c04fb998a2}"), EventVersion(2)]
class TcpIp : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="1a2ec-108">成員</span><span class="sxs-lookup"><span data-stu-id="1a2ec-108">Members</span></span>

<span data-ttu-id="1a2ec-109">**TcpIp** 類別未定義任何成員。</span><span class="sxs-lookup"><span data-stu-id="1a2ec-109">The **TcpIp** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a2ec-110">備註</span><span class="sxs-lookup"><span data-stu-id="1a2ec-110">Remarks</span></span>

<span data-ttu-id="1a2ec-111">若要在 NT 核心記錄會話中啟用 TCP/IP 事件，請在呼叫 [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)函數時，于 [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)結構的 **EnableFlags** 成員中指定 **事件 \_ 追蹤 \_ 旗標 \_ 網路 \_ TCPIP** 旗標。</span><span class="sxs-lookup"><span data-stu-id="1a2ec-111">To enable TCP/IP events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_NETWORK\_TCPIP** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="1a2ec-112">事件追蹤取用者可以藉由呼叫 [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) 函式並將 [**TcpIpGuid**](nt-kernel-logger-constants.md) 指定為 *PGUID* 參數，來執行 tcp/ip 事件的特殊處理。</span><span class="sxs-lookup"><span data-stu-id="1a2ec-112">Event trace consumers can implement special processing for TCP/IP events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**TcpIpGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="1a2ec-113">使用事件時，請使用下列事件種類來識別實際的網路 (TCP/IP) 事件。</span><span class="sxs-lookup"><span data-stu-id="1a2ec-113">Use the following event types to identify the actual network (TCP/IP) event when consuming events.</span></span>



| <span data-ttu-id="1a2ec-114">事件類型</span><span class="sxs-lookup"><span data-stu-id="1a2ec-114">Event type</span></span>                                                            | <span data-ttu-id="1a2ec-115">描述</span><span class="sxs-lookup"><span data-stu-id="1a2ec-115">Description</span></span>                                                                                                                                                                                   |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a2ec-116">**活動 \_追蹤 \_ 類型 \_ 接受** (事件種類值為 15) </span><span class="sxs-lookup"><span data-stu-id="1a2ec-116">**EVENT\_TRACE\_TYPE\_ACCEPT**(Event type value is 15)</span></span><br/>     | <span data-ttu-id="1a2ec-117">接受 IPv4 通訊協定的事件。</span><span class="sxs-lookup"><span data-stu-id="1a2ec-117">Accept event for IPv4 protocol.</span></span> <span data-ttu-id="1a2ec-118">[**TcpIp \_ TypeGroup2**](tcpip-typegroup2.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="1a2ec-118">The [**TcpIp\_TypeGroup2**](tcpip-typegroup2.md) MOF class defines the event data for this event.</span></span>                                                            |
| <span data-ttu-id="1a2ec-119">**活動 \_追蹤 \_ 類型 \_ 連接** (事件種類值為 12) </span><span class="sxs-lookup"><span data-stu-id="1a2ec-119">**EVENT\_TRACE\_TYPE\_CONNECT**(Event type value is 12)</span></span><br/>    | <span data-ttu-id="1a2ec-120">IPv4 通訊協定的連接事件。</span><span class="sxs-lookup"><span data-stu-id="1a2ec-120">Connect event for IPv4 protocol.</span></span> <span data-ttu-id="1a2ec-121">[**TcpIp \_ TypeGroup2**](tcpip-typegroup2.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="1a2ec-121">The [**TcpIp\_TypeGroup2**](tcpip-typegroup2.md) MOF class defines the event data for this event.</span></span>                                                           |
| <span data-ttu-id="1a2ec-122">**活動 \_追蹤 \_ 類型 \_ 中斷** (事件種類值為 13) </span><span class="sxs-lookup"><span data-stu-id="1a2ec-122">**EVENT\_TRACE\_TYPE\_DISCONNECT**(Event type value is 13)</span></span><br/> | <span data-ttu-id="1a2ec-123">IPv4 通訊協定的中斷線上活動。</span><span class="sxs-lookup"><span data-stu-id="1a2ec-123">Disconnect event for IPv4 protocol.</span></span> <span data-ttu-id="1a2ec-124">[**TcpIp \_ TypeGroup1**](tcpip-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="1a2ec-124">The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                        |
| <span data-ttu-id="1a2ec-125">**活動 \_追蹤 \_ 類型 \_ 接收** (事件種類值為 11) </span><span class="sxs-lookup"><span data-stu-id="1a2ec-125">**EVENT\_TRACE\_TYPE\_RECEIVE**(Event type value is 11)</span></span><br/>    | <span data-ttu-id="1a2ec-126">IPv4 通訊協定的接收事件。</span><span class="sxs-lookup"><span data-stu-id="1a2ec-126">Receive event for IPv4 protocol.</span></span> <span data-ttu-id="1a2ec-127">[**TcpIp \_ TypeGroup1**](tcpip-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="1a2ec-127">The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                           |
| <span data-ttu-id="1a2ec-128">**活動 \_追蹤 \_ 類型 \_ 重新連接** (事件種類值為 16) </span><span class="sxs-lookup"><span data-stu-id="1a2ec-128">**EVENT\_TRACE\_TYPE\_RECONNECT**(Event type value is 16)</span></span><br/>  | <span data-ttu-id="1a2ec-129">IPv4 通訊協定的重新連接事件。</span><span class="sxs-lookup"><span data-stu-id="1a2ec-129">Reconnect event for IPv4 protocol.</span></span> <span data-ttu-id="1a2ec-130"> (連線嘗試失敗，並嘗試進行其他嘗試。 ) [**TcpIp \_ TypeGroup1**](tcpip-typegroup1.md) MOF 類別定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="1a2ec-130">(A connect attempt failed and another attempt is made.) The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="1a2ec-131">**活動 \_追蹤 \_ 類型重新 \_ 傳輸** (事件種類值為 14) </span><span class="sxs-lookup"><span data-stu-id="1a2ec-131">**EVENT\_TRACE\_TYPE\_RETRANSMIT**(Event type value is 14)</span></span><br/> | <span data-ttu-id="1a2ec-132">IPv4 通訊協定的重新傳輸事件。</span><span class="sxs-lookup"><span data-stu-id="1a2ec-132">Retransmit event for IPv4 protocol.</span></span> <span data-ttu-id="1a2ec-133">[**TcpIp \_ TypeGroup1**](tcpip-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="1a2ec-133">The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                        |
| <span data-ttu-id="1a2ec-134">**活動 \_追蹤 \_ 類型 \_ 傳送** (事件種類值為 10) </span><span class="sxs-lookup"><span data-stu-id="1a2ec-134">**EVENT\_TRACE\_TYPE\_SEND**(Event type value is 10)</span></span><br/>       | <span data-ttu-id="1a2ec-135">傳送 IPv4 通訊協定的事件。</span><span class="sxs-lookup"><span data-stu-id="1a2ec-135">Send event for IPv4 protocol.</span></span> <span data-ttu-id="1a2ec-136">[**TcpIp \_ SendIPV4**](tcpip-sendipv4.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="1a2ec-136">The [**TcpIp\_SendIPV4**](tcpip-sendipv4.md) MOF class defines the event data for this event.</span></span>                                                                  |
| <span data-ttu-id="1a2ec-137">事件種類值17</span><span class="sxs-lookup"><span data-stu-id="1a2ec-137">Event type value, 17</span></span>                                                  | <span data-ttu-id="1a2ec-138">Fail 事件。</span><span class="sxs-lookup"><span data-stu-id="1a2ec-138">Fail event.</span></span> <span data-ttu-id="1a2ec-139">[**TcpIp \_ 失敗**](tcpip-fail.md)MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="1a2ec-139">The [**TcpIp\_Fail**](tcpip-fail.md) MOF class defines the event data for this event.</span></span>                                                                                            |
| <span data-ttu-id="1a2ec-140">事件種類值，18</span><span class="sxs-lookup"><span data-stu-id="1a2ec-140">Event type value, 18</span></span>                                                  | <span data-ttu-id="1a2ec-141">IPv4 通訊協定的 TCP 複製事件。</span><span class="sxs-lookup"><span data-stu-id="1a2ec-141">TCP copy event for IPv4 protocol.</span></span> <span data-ttu-id="1a2ec-142">[**TcpIp \_ TypeGroup1**](tcpip-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="1a2ec-142">The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                          |
| <span data-ttu-id="1a2ec-143">事件種類值，26</span><span class="sxs-lookup"><span data-stu-id="1a2ec-143">Event type value, 26</span></span>                                                  | <span data-ttu-id="1a2ec-144">IPv6 通訊協定的傳送事件。</span><span class="sxs-lookup"><span data-stu-id="1a2ec-144">Send event for IPv6 protocol.</span></span> <span data-ttu-id="1a2ec-145">[**TcpIp \_ SendIPV6**](tcpip-sendipv6.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="1a2ec-145">The [**TcpIp\_SendIPV6**](tcpip-sendipv6.md) MOF class defines the event data for this event.</span></span>                                                                  |
| <span data-ttu-id="1a2ec-146">事件種類值，27</span><span class="sxs-lookup"><span data-stu-id="1a2ec-146">Event type value, 27</span></span>                                                  | <span data-ttu-id="1a2ec-147">IPv6 通訊協定的接收事件。</span><span class="sxs-lookup"><span data-stu-id="1a2ec-147">Receive event for IPv6 protocol.</span></span> <span data-ttu-id="1a2ec-148">[**TcpIp \_ TypeGroup3**](tcpip-typegroup3.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="1a2ec-148">The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span>                                                           |
| <span data-ttu-id="1a2ec-149">事件種類值28</span><span class="sxs-lookup"><span data-stu-id="1a2ec-149">Event type value, 28</span></span>                                                  | <span data-ttu-id="1a2ec-150">IPv6 通訊協定的連接事件。</span><span class="sxs-lookup"><span data-stu-id="1a2ec-150">Connect event for IPv6 protocol.</span></span> <span data-ttu-id="1a2ec-151">[**TcpIp \_ TypeGroup4**](tcpip-typegroup4.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="1a2ec-151">The [**TcpIp\_TypeGroup4**](tcpip-typegroup4.md) MOF class defines the event data for this event.</span></span>                                                           |
| <span data-ttu-id="1a2ec-152">事件種類值，29</span><span class="sxs-lookup"><span data-stu-id="1a2ec-152">Event type value, 29</span></span>                                                  | <span data-ttu-id="1a2ec-153">IPv6 通訊協定的中斷線上活動。</span><span class="sxs-lookup"><span data-stu-id="1a2ec-153">Disconnect event for IPv6 protocol.</span></span> <span data-ttu-id="1a2ec-154">[**TcpIp \_ TypeGroup3**](tcpip-typegroup3.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="1a2ec-154">The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span>                                                        |
| <span data-ttu-id="1a2ec-155">事件種類值30</span><span class="sxs-lookup"><span data-stu-id="1a2ec-155">Event type value, 30</span></span>                                                  | <span data-ttu-id="1a2ec-156">IPv6 通訊協定的重新傳輸事件。</span><span class="sxs-lookup"><span data-stu-id="1a2ec-156">Retransmit event for IPv6 protocol.</span></span> <span data-ttu-id="1a2ec-157">[**TcpIp \_ TypeGroup3**](tcpip-typegroup3.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="1a2ec-157">The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span>                                                        |
| <span data-ttu-id="1a2ec-158">事件種類值，31</span><span class="sxs-lookup"><span data-stu-id="1a2ec-158">Event type value, 31</span></span>                                                  | <span data-ttu-id="1a2ec-159">接受 IPv6 通訊協定的事件。</span><span class="sxs-lookup"><span data-stu-id="1a2ec-159">Accept event for IPv6 protocol.</span></span> <span data-ttu-id="1a2ec-160">[**TcpIp \_ TypeGroup4**](tcpip-typegroup4.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="1a2ec-160">The [**TcpIp\_TypeGroup4**](tcpip-typegroup4.md) MOF class defines the event data for this event.</span></span>                                                            |
| <span data-ttu-id="1a2ec-161">事件種類值，32</span><span class="sxs-lookup"><span data-stu-id="1a2ec-161">Event type value, 32</span></span>                                                  | <span data-ttu-id="1a2ec-162">IPv6 通訊協定的重新連接事件。</span><span class="sxs-lookup"><span data-stu-id="1a2ec-162">Reconnect event for IPv6 protocol.</span></span> <span data-ttu-id="1a2ec-163"> (連線嘗試失敗，並嘗試進行其他嘗試。 ) [**TcpIp \_ TypeGroup3**](tcpip-typegroup3.md) MOF 類別定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="1a2ec-163">(A connect attempt failed and another attempt is made.) The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="1a2ec-164">事件種類值，34</span><span class="sxs-lookup"><span data-stu-id="1a2ec-164">Event type value, 34</span></span>                                                  | <span data-ttu-id="1a2ec-165">IPv6 通訊協定的 TCP 複製事件。</span><span class="sxs-lookup"><span data-stu-id="1a2ec-165">TCP copy event for IPv6 protocol.</span></span> <span data-ttu-id="1a2ec-166">[**TcpIp \_ TypeGroup3**](tcpip-typegroup3.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="1a2ec-166">The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span>                                                          |



 

<span data-ttu-id="1a2ec-167">您可以使用 **ProcessId** 屬性，將網路事件追蹤至來源和目的地進程。</span><span class="sxs-lookup"><span data-stu-id="1a2ec-167">You can trace network events to a source and destination process using the **ProcessId** property.</span></span> <span data-ttu-id="1a2ec-168">由於部分網路事件是由個別的執行緒所記錄，因此您可能無法使用 [**事件 \_ 追蹤 \_ 標頭**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header)的 **ProcessId** 和 **ThreadId** 成員來識別產生網路活動的進程或執行緒。</span><span class="sxs-lookup"><span data-stu-id="1a2ec-168">Because some network events are logged by separate threads, you may not be able to use the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) to identify the process or thread that originated the network activities.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a2ec-169">規格需求</span><span class="sxs-lookup"><span data-stu-id="1a2ec-169">Requirements</span></span>



| <span data-ttu-id="1a2ec-170">需求</span><span class="sxs-lookup"><span data-stu-id="1a2ec-170">Requirement</span></span> | <span data-ttu-id="1a2ec-171">值</span><span class="sxs-lookup"><span data-stu-id="1a2ec-171">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1a2ec-172">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1a2ec-172">Minimum supported client</span></span><br/> | <span data-ttu-id="1a2ec-173">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1a2ec-173">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1a2ec-174">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1a2ec-174">Minimum supported server</span></span><br/> | <span data-ttu-id="1a2ec-175">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1a2ec-175">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1a2ec-176">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1a2ec-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a2ec-177">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="1a2ec-177">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="1a2ec-178">**TcpIp \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="1a2ec-178">**TcpIp\_Fail**</span></span>](tcpip-fail.md)
</dt> <dt>

[<span data-ttu-id="1a2ec-179">**TcpIp \_ SendIPV4**</span><span class="sxs-lookup"><span data-stu-id="1a2ec-179">**TcpIp\_SendIPV4**</span></span>](tcpip-sendipv4.md)
</dt> <dt>

[<span data-ttu-id="1a2ec-180">**TcpIp \_ SendIPV6**</span><span class="sxs-lookup"><span data-stu-id="1a2ec-180">**TcpIp\_SendIPV6**</span></span>](tcpip-sendipv6.md)
</dt> <dt>

[<span data-ttu-id="1a2ec-181">**TcpIp \_ TypeGroup1**</span><span class="sxs-lookup"><span data-stu-id="1a2ec-181">**TcpIp\_TypeGroup1**</span></span>](tcpip-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="1a2ec-182">**TcpIp \_ TypeGroup2**</span><span class="sxs-lookup"><span data-stu-id="1a2ec-182">**TcpIp\_TypeGroup2**</span></span>](tcpip-typegroup2.md)
</dt> <dt>

[<span data-ttu-id="1a2ec-183">**TcpIp \_ TypeGroup3**</span><span class="sxs-lookup"><span data-stu-id="1a2ec-183">**TcpIp\_TypeGroup3**</span></span>](tcpip-typegroup3.md)
</dt> <dt>

[<span data-ttu-id="1a2ec-184">**TcpIp \_ TypeGroup4**</span><span class="sxs-lookup"><span data-stu-id="1a2ec-184">**TcpIp\_TypeGroup4**</span></span>](tcpip-typegroup4.md)
</dt> <dt>

[<span data-ttu-id="1a2ec-185">**TcpIp \_ V0**</span><span class="sxs-lookup"><span data-stu-id="1a2ec-185">**TcpIp\_V0**</span></span>](tcpip-v0.md)
</dt> <dt>

[<span data-ttu-id="1a2ec-186">**TcpIp \_ V1**</span><span class="sxs-lookup"><span data-stu-id="1a2ec-186">**TcpIp\_V1**</span></span>](tcpip-v1.md)
</dt> </dl>

 

 
