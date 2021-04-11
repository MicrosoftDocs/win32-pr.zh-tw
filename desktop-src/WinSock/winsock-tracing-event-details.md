---
description: Winsock 網路事件追蹤詳細資料
ms.assetid: f0386bd3-15d0-45f3-82c9-365d1c9f59c5
title: Winsock 網路事件追蹤詳細資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 588363420aee9c3b04f4f8060bbd9c77b9cc3232
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194029"
---
# <a name="winsock-network-event-tracing-details"></a><span data-ttu-id="aa0fe-103">Winsock 網路事件追蹤詳細資料</span><span class="sxs-lookup"><span data-stu-id="aa0fe-103">Winsock Network Event Tracing Details</span></span>

<span data-ttu-id="aa0fe-104">以下將詳細說明每個可追蹤的 Winsock 網路事件，以及描述所記錄的參數和資訊。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-104">The following details each of the Winsock network events that can be traced and describes which parameters and information are logged.</span></span>

## <a name="socket-creation"></a><span data-ttu-id="aa0fe-105">通訊端建立</span><span class="sxs-lookup"><span data-stu-id="aa0fe-105">Socket Creation</span></span>

<span data-ttu-id="aa0fe-106">事件識別碼 = 1</span><span class="sxs-lookup"><span data-stu-id="aa0fe-106">Event ID = 1</span></span>

<span data-ttu-id="aa0fe-107">層級 = 4 (資訊) </span><span class="sxs-lookup"><span data-stu-id="aa0fe-107">Level = 4 (Information)</span></span>

<span data-ttu-id="aa0fe-108">下列 Winsock 事件會針對通訊端建立進行追蹤：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-108">The following Winsock events are traced for socket creation:</span></span>

-   <span data-ttu-id="aa0fe-109">由呼叫 [**通訊端**](/windows/desktop/api/Winsock2/nf-winsock2-socket) 或 [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) 函式所建立的通訊端控制碼。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-109">Socket handles created by calls to the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) or [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) functions.</span></span>
-   <span data-ttu-id="aa0fe-110">已接受接聽通訊端的通訊端控制碼。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-110">Accepted socket handles on listening sockets.</span></span>
-   <span data-ttu-id="aa0fe-111">呼叫 [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) 函數所建立的通訊端控制碼。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-111">Socket handles created by calls to the [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) function.</span></span>
-   <span data-ttu-id="aa0fe-112">呼叫 [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) 或 [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex) 函式時，會重複使用通訊端控制碼。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-112">Socket handles re-used by calls to the [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) or [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex) functions.</span></span>

<span data-ttu-id="aa0fe-113">針對通訊端建立事件，會記錄下列參數：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-113">The following parameters are logged for a socket creation event:</span></span>



| <span data-ttu-id="aa0fe-114">參數</span><span class="sxs-lookup"><span data-stu-id="aa0fe-114">Parameter</span></span>                                                                                                        | <span data-ttu-id="aa0fe-115">Description</span><span class="sxs-lookup"><span data-stu-id="aa0fe-115">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa0fe-116"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程</span><span class="sxs-lookup"><span data-stu-id="aa0fe-116"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                 | <span data-ttu-id="aa0fe-117">進程的核心 EPROCESS 結構位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-117">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="aa0fe-118"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點</span><span class="sxs-lookup"><span data-stu-id="aa0fe-118"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>             | <span data-ttu-id="aa0fe-119">當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-119">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="aa0fe-120"><span id="SocketType"></span><span id="sockettype"></span><span id="SOCKETTYPE"></span>SocketType</span><span class="sxs-lookup"><span data-stu-id="aa0fe-120"><span id="SocketType"></span><span id="sockettype"></span><span id="SOCKETTYPE"></span>SocketType</span></span><br/>     | <span data-ttu-id="aa0fe-121">通訊端的型別。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-121">The type of the socket.</span></span><br/>                                                     |
| <span data-ttu-id="aa0fe-122"><span id="Protocol"></span><span id="protocol"></span><span id="PROTOCOL"></span>協定</span><span class="sxs-lookup"><span data-stu-id="aa0fe-122"><span id="Protocol"></span><span id="protocol"></span><span id="PROTOCOL"></span>Protocol</span></span><br/>             | <span data-ttu-id="aa0fe-123">通訊端的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-123">The protocol of the socket.</span></span><br/>                                                 |
| <span data-ttu-id="aa0fe-124"><span id="UserModePid"></span><span id="usermodepid"></span><span id="USERMODEPID"></span>UserModePid</span><span class="sxs-lookup"><span data-stu-id="aa0fe-124"><span id="UserModePid"></span><span id="usermodepid"></span><span id="USERMODEPID"></span>UserModePid</span></span><br/> | <span data-ttu-id="aa0fe-125">建立通訊端的使用者模式處理序識別碼。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-125">The user-mode process ID that created the socket.</span></span><br/>                           |



 

## <a name="socket-bind"></a><span data-ttu-id="aa0fe-126">通訊端系結</span><span class="sxs-lookup"><span data-stu-id="aa0fe-126">Socket Bind</span></span>

<span data-ttu-id="aa0fe-127">事件識別碼 = 2 (IPv4) ，事件識別碼 = 3 (IPv6) </span><span class="sxs-lookup"><span data-stu-id="aa0fe-127">Event ID = 2 (IPv4), Event ID = 3 (IPv6)</span></span>

<span data-ttu-id="aa0fe-128">層級 = 4 (資訊) </span><span class="sxs-lookup"><span data-stu-id="aa0fe-128">Level = 4 (Information)</span></span>

<span data-ttu-id="aa0fe-129">以下是針對系結作業追蹤的 Winsock 事件：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-129">The following Winsock events are traced for a bind operation:</span></span>

-   <span data-ttu-id="aa0fe-130">通訊端控制碼的隱含或明確系結。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-130">Implicit or explicit binding of a socket handle.</span></span>

<span data-ttu-id="aa0fe-131">以下是針對系結事件記錄的參數：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-131">The following parameters are logged for a bind event:</span></span>



| <span data-ttu-id="aa0fe-132">參數</span><span class="sxs-lookup"><span data-stu-id="aa0fe-132">Parameter</span></span>                                                                                            | <span data-ttu-id="aa0fe-133">Description</span><span class="sxs-lookup"><span data-stu-id="aa0fe-133">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa0fe-134"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程</span><span class="sxs-lookup"><span data-stu-id="aa0fe-134"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="aa0fe-135">進程的核心 EPROCESS 結構位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-135">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="aa0fe-136"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點</span><span class="sxs-lookup"><span data-stu-id="aa0fe-136"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="aa0fe-137">當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-137">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="aa0fe-138"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>位址</span><span class="sxs-lookup"><span data-stu-id="aa0fe-138"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>     | <span data-ttu-id="aa0fe-139">本機 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-139">The local IP address.</span></span><br/>                                                       |
| <span data-ttu-id="aa0fe-140"><span id="Port"></span><span id="port"></span><span id="PORT"></span>港口</span><span class="sxs-lookup"><span data-stu-id="aa0fe-140"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                 | <span data-ttu-id="aa0fe-141">本機 IP 埠號碼。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-141">The local IP port number.</span></span><br/>                                                   |
| <span data-ttu-id="aa0fe-142"><span id="Status"></span><span id="status"></span><span id="STATUS"></span>地位</span><span class="sxs-lookup"><span data-stu-id="aa0fe-142"><span id="Status"></span><span id="status"></span><span id="STATUS"></span>Status</span></span><br/>         | <span data-ttu-id="aa0fe-143">針對系結作業傳回的狀態或錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-143">The status or error code returned for the bind operation.</span></span><br/>                   |



 

## <a name="failed-bind"></a><span data-ttu-id="aa0fe-144">失敗的系結</span><span class="sxs-lookup"><span data-stu-id="aa0fe-144">Failed Bind</span></span>

<span data-ttu-id="aa0fe-145">事件識別碼 = 40</span><span class="sxs-lookup"><span data-stu-id="aa0fe-145">Event ID = 40</span></span>

<span data-ttu-id="aa0fe-146">層級 = 4 (資訊) </span><span class="sxs-lookup"><span data-stu-id="aa0fe-146">Level = 4 (Information)</span></span>

<span data-ttu-id="aa0fe-147">針對失敗的系結作業，會追蹤下列 Winsock 事件：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-147">The following Winsock events are traced for a failed bind operation:</span></span>

-   <span data-ttu-id="aa0fe-148">失敗之通訊端控制碼的隱含或明確系結。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-148">Implicit or explicit binding of a socket handle that fails.</span></span>

<span data-ttu-id="aa0fe-149">針對失敗的系結事件，會記錄下列參數：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-149">The following parameters are logged for a failed bind event:</span></span>



| <span data-ttu-id="aa0fe-150">參數</span><span class="sxs-lookup"><span data-stu-id="aa0fe-150">Parameter</span></span>                                                                                            | <span data-ttu-id="aa0fe-151">Description</span><span class="sxs-lookup"><span data-stu-id="aa0fe-151">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa0fe-152"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程</span><span class="sxs-lookup"><span data-stu-id="aa0fe-152"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="aa0fe-153">進程的核心 EPROCESS 結構位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-153">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="aa0fe-154"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點</span><span class="sxs-lookup"><span data-stu-id="aa0fe-154"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="aa0fe-155">當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-155">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="aa0fe-156"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>錯誤</span><span class="sxs-lookup"><span data-stu-id="aa0fe-156"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="aa0fe-157">失敗系結作業傳回的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-157">The error code returned for the failing bind operation.</span></span><br/>                     |



 

## <a name="socket-connect"></a><span data-ttu-id="aa0fe-158">通訊端連接</span><span class="sxs-lookup"><span data-stu-id="aa0fe-158">Socket Connect</span></span>

<span data-ttu-id="aa0fe-159">事件識別碼 = 4 (IPv4) ，事件識別碼 = 5 (IPv6) </span><span class="sxs-lookup"><span data-stu-id="aa0fe-159">Event ID = 4 (IPv4), Event ID = 5 (IPv6)</span></span>

<span data-ttu-id="aa0fe-160">層級 = 4 (資訊) </span><span class="sxs-lookup"><span data-stu-id="aa0fe-160">Level = 4 (Information)</span></span>

<span data-ttu-id="aa0fe-161">下列 Winsock 事件會針對 connect 作業要求進行追蹤， (對 [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect)、 [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex)、 [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect)、 [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)或 [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) 函數的呼叫) ：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-161">The following Winsock events are traced for a connect operation request (a call to the [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect), [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist), or [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) function):</span></span>

-   <span data-ttu-id="aa0fe-162">將通訊端連接至連接導向或不需連線的通訊端的目的地。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-162">Connecting a socket to a destination for either a connection-oriented or a connectionless socket.</span></span>

<span data-ttu-id="aa0fe-163">下列參數會針對 connect 事件進行記錄：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-163">The following parameters are logged for a connect event:</span></span>



| <span data-ttu-id="aa0fe-164">參數</span><span class="sxs-lookup"><span data-stu-id="aa0fe-164">Parameter</span></span>                                                                                            | <span data-ttu-id="aa0fe-165">Description</span><span class="sxs-lookup"><span data-stu-id="aa0fe-165">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa0fe-166"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程</span><span class="sxs-lookup"><span data-stu-id="aa0fe-166"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="aa0fe-167">進程的核心 EPROCESS 結構位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-167">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="aa0fe-168"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點</span><span class="sxs-lookup"><span data-stu-id="aa0fe-168"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="aa0fe-169">當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-169">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="aa0fe-170"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>位址</span><span class="sxs-lookup"><span data-stu-id="aa0fe-170"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>     | <span data-ttu-id="aa0fe-171">遠端 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-171">The remote IP address.</span></span><br/>                                                      |
| <span data-ttu-id="aa0fe-172"><span id="Port"></span><span id="port"></span><span id="PORT"></span>港口</span><span class="sxs-lookup"><span data-stu-id="aa0fe-172"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                 | <span data-ttu-id="aa0fe-173">遠端 IP 埠號碼。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-173">The remote IP port number.</span></span><br/>                                                  |



 

## <a name="connect-completed"></a><span data-ttu-id="aa0fe-174">連接完成</span><span class="sxs-lookup"><span data-stu-id="aa0fe-174">Connect Completed</span></span>

<span data-ttu-id="aa0fe-175">事件識別碼 = 6</span><span class="sxs-lookup"><span data-stu-id="aa0fe-175">Event ID = 6</span></span>

<span data-ttu-id="aa0fe-176">層級 = 4 (資訊) </span><span class="sxs-lookup"><span data-stu-id="aa0fe-176">Level = 4 (Information)</span></span>

<span data-ttu-id="aa0fe-177">以下是針對 connect 完成追蹤的 Winsock 事件：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-177">The following Winsock events are traced for a connect completed:</span></span>

-   <span data-ttu-id="aa0fe-178">連接操作已完成。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-178">The connect operation is completed.</span></span>

<span data-ttu-id="aa0fe-179">已針對 connect completed 事件記錄下列參數：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-179">The following parameters are logged for a connect completed event:</span></span>



| <span data-ttu-id="aa0fe-180">參數</span><span class="sxs-lookup"><span data-stu-id="aa0fe-180">Parameter</span></span>                                                                                            | <span data-ttu-id="aa0fe-181">Description</span><span class="sxs-lookup"><span data-stu-id="aa0fe-181">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa0fe-182"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程</span><span class="sxs-lookup"><span data-stu-id="aa0fe-182"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="aa0fe-183">進程的核心 EPROCESS 結構位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-183">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="aa0fe-184"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點</span><span class="sxs-lookup"><span data-stu-id="aa0fe-184"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="aa0fe-185">當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-185">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="aa0fe-186"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>錯誤</span><span class="sxs-lookup"><span data-stu-id="aa0fe-186"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="aa0fe-187">針對連接作業傳回的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-187">The error code returned for the connect operation.</span></span><br/>                          |



 

## <a name="afd-initiated-abort"></a><span data-ttu-id="aa0fe-188">AFD-Initiated 中止</span><span class="sxs-lookup"><span data-stu-id="aa0fe-188">AFD-Initiated Abort</span></span>

<span data-ttu-id="aa0fe-189">事件識別碼 = 7</span><span class="sxs-lookup"><span data-stu-id="aa0fe-189">Event ID = 7</span></span>

<span data-ttu-id="aa0fe-190">層級 = 4 (資訊) </span><span class="sxs-lookup"><span data-stu-id="aa0fe-190">Level = 4 (Information)</span></span>

<span data-ttu-id="aa0fe-191">下列 Winsock 事件會針對 Winsock 起始的中止或取消作業進行追蹤：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-191">The following Winsock events are traced for Winsock-initiated aborts or cancel operations:</span></span>

-   <span data-ttu-id="aa0fe-192">因為未讀取的接收資料在關閉後緩衝，所以會中止。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-192">An abort due to unread receive data buffered after close.</span></span>
-   <span data-ttu-id="aa0fe-193">在呼叫 [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown)函式之後中止，並 *將參數設定* 為 SD RECEIVE，以及對導致 closesocket 函式的 \_ 呼叫擱置的接收資料。 [](/windows/desktop/api/winsock/nf-winsock-closesocket)</span><span class="sxs-lookup"><span data-stu-id="aa0fe-193">An abort after a call to the [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) function with the *how* parameter set to SD\_RECEIVE and a call to the [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) function with receive data pending.</span></span>
-   <span data-ttu-id="aa0fe-194">在嘗試排清端點失敗之後中止。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-194">An abort after a failed attempt to flush the endpoint.</span></span>
-   <span data-ttu-id="aa0fe-195">發生內部 Winsock 錯誤之後，就會中止。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-195">An abort after an internal Winsock error occurred.</span></span>
-   <span data-ttu-id="aa0fe-196">因為連接有錯誤，而應用程式先前要求在某些情況下中止連接，所以會中止。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-196">An abort due to a connection with errors and the application previously requested that the connection be aborted on certain circumstances.</span></span> <span data-ttu-id="aa0fe-197">這種情況的其中一個範例，就是將 timeout 設定為延遲的應用程式 \_ ，並在連線上仍有未認可的資料。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-197">One example of this case would be an application that set SO\_LINGER with a timeout of zero and there is still unacknowledged data on the connection.</span></span>
-   <span data-ttu-id="aa0fe-198">未完全與接受端點相關聯的連接上的中止。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-198">An abort on a connection not fully associated with accepting endpoint.</span></span>
-   <span data-ttu-id="aa0fe-199">在對 [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) 或 [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) 函式的呼叫失敗時中止。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-199">An abort on a failed call to the [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) or [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) function.</span></span>
-   <span data-ttu-id="aa0fe-200">因為接收作業失敗而中止。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-200">An abort due to a failed receive operation.</span></span>
-   <span data-ttu-id="aa0fe-201">由於隨插即用事件而中止。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-201">An abort due to a Plug and Play event.</span></span>
-   <span data-ttu-id="aa0fe-202">因為排清要求失敗而中止。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-202">An abort due to a failed flush request.</span></span>
-   <span data-ttu-id="aa0fe-203">因為快速的資料接收要求失敗而中止。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-203">An abort due to a failed expedited data receive request.</span></span>
-   <span data-ttu-id="aa0fe-204">因為傳送要求失敗而中止。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-204">An abort due to a failed send request.</span></span>
-   <span data-ttu-id="aa0fe-205">因為取消的傳送要求而中止。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-205">An abort due to canceled send request.</span></span>
-   <span data-ttu-id="aa0fe-206">因為已取消呼叫 [**TransmitPackets**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_transmitpackets) 函式而中止。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-206">An abort due to a canceled called to the [**TransmitPackets**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_transmitpackets) function.</span></span>

<span data-ttu-id="aa0fe-207">系統會針對 Winsock 起始的中止或取消作業記錄下列參數：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-207">The following parameters are logged for a Winsock-initiated abort or cancel operation:</span></span>



| <span data-ttu-id="aa0fe-208">參數</span><span class="sxs-lookup"><span data-stu-id="aa0fe-208">Parameter</span></span>                                                                                            | <span data-ttu-id="aa0fe-209">Description</span><span class="sxs-lookup"><span data-stu-id="aa0fe-209">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa0fe-210"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程</span><span class="sxs-lookup"><span data-stu-id="aa0fe-210"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="aa0fe-211">進程的核心 EPROCESS 結構位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-211">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="aa0fe-212"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點</span><span class="sxs-lookup"><span data-stu-id="aa0fe-212"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="aa0fe-213">當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-213">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="aa0fe-214"><span id="Reason"></span><span id="reason"></span><span id="REASON"></span>原因</span><span class="sxs-lookup"><span data-stu-id="aa0fe-214"><span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Reason</span></span><br/>         | <span data-ttu-id="aa0fe-215">中止或取消作業的原因。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-215">The reason for the abort or cancel operation.</span></span><br/>                               |



 

## <a name="transport-initiated-abort"></a><span data-ttu-id="aa0fe-216">Transport-Initiated 中止</span><span class="sxs-lookup"><span data-stu-id="aa0fe-216">Transport-Initiated Abort</span></span>

<span data-ttu-id="aa0fe-217">事件識別碼 = 8</span><span class="sxs-lookup"><span data-stu-id="aa0fe-217">Event ID = 8</span></span>

<span data-ttu-id="aa0fe-218">層級 = 4 (資訊) </span><span class="sxs-lookup"><span data-stu-id="aa0fe-218">Level = 4 (Information)</span></span>

<span data-ttu-id="aa0fe-219">下列 Winsock 事件會針對傳輸起始的中止或取消作業進行追蹤：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-219">The following Winsock events are traced for transport-initiated abort or cancel operations:</span></span>

-   <span data-ttu-id="aa0fe-220">由傳輸指示的重設。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-220">Reset indicated by the transport.</span></span>

<span data-ttu-id="aa0fe-221">系統會針對 Winsock 起始的中止或取消作業記錄下列參數：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-221">The following parameters are logged for a Winsock-initiated abort or cancel operation:</span></span>



| <span data-ttu-id="aa0fe-222">參數</span><span class="sxs-lookup"><span data-stu-id="aa0fe-222">Parameter</span></span>                                                                                            | <span data-ttu-id="aa0fe-223">Description</span><span class="sxs-lookup"><span data-stu-id="aa0fe-223">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa0fe-224"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程</span><span class="sxs-lookup"><span data-stu-id="aa0fe-224"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="aa0fe-225">進程的核心 EPROCESS 結構位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-225">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="aa0fe-226"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點</span><span class="sxs-lookup"><span data-stu-id="aa0fe-226"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="aa0fe-227">當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-227">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="aa0fe-228"><span id="Reason"></span><span id="reason"></span><span id="REASON"></span>原因</span><span class="sxs-lookup"><span data-stu-id="aa0fe-228"><span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Reason</span></span><br/>         | <span data-ttu-id="aa0fe-229">中止或取消作業的原因。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-229">The reason for the abort or cancel operation.</span></span><br/>                               |



 

## <a name="failed-send-request"></a><span data-ttu-id="aa0fe-230">傳送要求失敗</span><span class="sxs-lookup"><span data-stu-id="aa0fe-230">Failed Send Request</span></span>

<span data-ttu-id="aa0fe-231">事件識別碼 = 9</span><span class="sxs-lookup"><span data-stu-id="aa0fe-231">Event ID = 9</span></span>

<span data-ttu-id="aa0fe-232">層級 = 4 (資訊) </span><span class="sxs-lookup"><span data-stu-id="aa0fe-232">Level = 4 (Information)</span></span>

<span data-ttu-id="aa0fe-233">針對 [**傳送**](/windows/desktop/api/Winsock2/nf-winsock2-send) 或 [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) 要求的錯誤，會追蹤下列 Winsock 事件：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-233">The following Winsock events are traced for errors on [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) or [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) requests:</span></span>

-   <span data-ttu-id="aa0fe-234">失敗的 [**傳送**](/windows/desktop/api/Winsock2/nf-winsock2-send) 或 [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) 要求傳回的錯誤。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-234">Errors returned on failed [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) or [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) requests.</span></span>

<span data-ttu-id="aa0fe-235">下列參數會針對產生錯誤的傳送要求進行記錄：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-235">The following parameters are logged for a send requests that results in an error:</span></span>



| <span data-ttu-id="aa0fe-236">參數</span><span class="sxs-lookup"><span data-stu-id="aa0fe-236">Parameter</span></span>                                                                                            | <span data-ttu-id="aa0fe-237">Description</span><span class="sxs-lookup"><span data-stu-id="aa0fe-237">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa0fe-238"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程</span><span class="sxs-lookup"><span data-stu-id="aa0fe-238"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="aa0fe-239">進程的核心 EPROCESS 結構位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-239">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="aa0fe-240"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點</span><span class="sxs-lookup"><span data-stu-id="aa0fe-240"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="aa0fe-241">當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-241">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="aa0fe-242"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>錯誤</span><span class="sxs-lookup"><span data-stu-id="aa0fe-242"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="aa0fe-243">針對作業傳回的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-243">The error code returned for the operation.</span></span><br/>                                  |



 

## <a name="failed-wsasendmsg-request"></a><span data-ttu-id="aa0fe-244">失敗的 WsaSendMsg 要求</span><span class="sxs-lookup"><span data-stu-id="aa0fe-244">Failed WsaSendMsg Request</span></span>

<span data-ttu-id="aa0fe-245">事件識別碼 = 10</span><span class="sxs-lookup"><span data-stu-id="aa0fe-245">Event ID = 10</span></span>

<span data-ttu-id="aa0fe-246">層級 = 4 (資訊) </span><span class="sxs-lookup"><span data-stu-id="aa0fe-246">Level = 4 (Information)</span></span>

<span data-ttu-id="aa0fe-247">針對 [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) 要求的錯誤，會追蹤下列 Winsock 事件：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-247">The following Winsock events are traced for errors on [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) requests:</span></span>

-   <span data-ttu-id="aa0fe-248">失敗的 [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) 要求傳回的錯誤。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-248">Errors returned on failed [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) requests.</span></span>

<span data-ttu-id="aa0fe-249">下列參數會針對產生錯誤的傳送要求進行記錄：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-249">The following parameters are logged for a send requests that results in an error:</span></span>



| <span data-ttu-id="aa0fe-250">參數</span><span class="sxs-lookup"><span data-stu-id="aa0fe-250">Parameter</span></span>                                                                                            | <span data-ttu-id="aa0fe-251">Description</span><span class="sxs-lookup"><span data-stu-id="aa0fe-251">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa0fe-252"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程</span><span class="sxs-lookup"><span data-stu-id="aa0fe-252"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="aa0fe-253">進程的核心 EPROCESS 結構位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-253">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="aa0fe-254"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點</span><span class="sxs-lookup"><span data-stu-id="aa0fe-254"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="aa0fe-255">當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-255">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="aa0fe-256"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>錯誤</span><span class="sxs-lookup"><span data-stu-id="aa0fe-256"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="aa0fe-257">針對作業傳回的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-257">The error code returned for the operation.</span></span><br/>                                  |



 

## <a name="failed-recv-request"></a><span data-ttu-id="aa0fe-258">失敗的接收要求</span><span class="sxs-lookup"><span data-stu-id="aa0fe-258">Failed Recv Request</span></span>

<span data-ttu-id="aa0fe-259">事件識別碼 = 11</span><span class="sxs-lookup"><span data-stu-id="aa0fe-259">Event ID = 11</span></span>

<span data-ttu-id="aa0fe-260">層級 = 4 (資訊) </span><span class="sxs-lookup"><span data-stu-id="aa0fe-260">Level = 4 (Information)</span></span>

<span data-ttu-id="aa0fe-261">針對 [**接收**](/windows/desktop/api/winsock/nf-winsock-recv)、 [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)或 [**WSARecvEx**](/windows/win32/api/mswsock/nf-mswsock-wsarecvex) 要求的錯誤，會追蹤下列 Winsock 事件：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-261">The following Winsock events are traced for errors on [**recv**](/windows/desktop/api/winsock/nf-winsock-recv), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), or [**WSARecvEx**](/windows/win32/api/mswsock/nf-mswsock-wsarecvex) requests:</span></span>

-   <span data-ttu-id="aa0fe-262">失敗的接收要求傳回的錯誤。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-262">Errors returned on failed receive requests.</span></span>

<span data-ttu-id="aa0fe-263">下列參數會針對產生錯誤的傳送要求進行記錄：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-263">The following parameters are logged for a send requests that results in an error:</span></span>



| <span data-ttu-id="aa0fe-264">參數</span><span class="sxs-lookup"><span data-stu-id="aa0fe-264">Parameter</span></span>                                                                                            | <span data-ttu-id="aa0fe-265">Description</span><span class="sxs-lookup"><span data-stu-id="aa0fe-265">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa0fe-266"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程</span><span class="sxs-lookup"><span data-stu-id="aa0fe-266"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="aa0fe-267">進程的核心 EPROCESS 結構位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-267">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="aa0fe-268"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點</span><span class="sxs-lookup"><span data-stu-id="aa0fe-268"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="aa0fe-269">當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-269">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="aa0fe-270"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>錯誤</span><span class="sxs-lookup"><span data-stu-id="aa0fe-270"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="aa0fe-271">針對作業傳回的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-271">The error code returned for the operation.</span></span><br/>                                  |



 

## <a name="failed-recvfrom-request"></a><span data-ttu-id="aa0fe-272">失敗的 Recvfrom 要求</span><span class="sxs-lookup"><span data-stu-id="aa0fe-272">Failed Recvfrom Request</span></span>

<span data-ttu-id="aa0fe-273">事件識別碼 = 12</span><span class="sxs-lookup"><span data-stu-id="aa0fe-273">Event ID = 12</span></span>

<span data-ttu-id="aa0fe-274">層級 = 4 (資訊) </span><span class="sxs-lookup"><span data-stu-id="aa0fe-274">Level = 4 (Information)</span></span>

<span data-ttu-id="aa0fe-275">針對 [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) 或 [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) 要求的錯誤，會追蹤下列 Winsock 事件：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-275">The following Winsock events are traced for errors on [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) or [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) requests:</span></span>

-   <span data-ttu-id="aa0fe-276">失敗的 [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) 或 [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) 要求傳回的錯誤。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-276">Errors returned on failed [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) or [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) requests.</span></span>

<span data-ttu-id="aa0fe-277">系統會針對導致錯誤的 [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) 或 [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) 要求記錄下列參數：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-277">The following parameters are logged for a [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) or [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) request that results in an error:</span></span>



| <span data-ttu-id="aa0fe-278">參數</span><span class="sxs-lookup"><span data-stu-id="aa0fe-278">Parameter</span></span>                                                                                            | <span data-ttu-id="aa0fe-279">Description</span><span class="sxs-lookup"><span data-stu-id="aa0fe-279">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa0fe-280"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程</span><span class="sxs-lookup"><span data-stu-id="aa0fe-280"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="aa0fe-281">進程的核心 EPROCESS 結構位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-281">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="aa0fe-282"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點</span><span class="sxs-lookup"><span data-stu-id="aa0fe-282"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="aa0fe-283">當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-283">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="aa0fe-284"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>錯誤</span><span class="sxs-lookup"><span data-stu-id="aa0fe-284"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="aa0fe-285">針對作業傳回的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-285">The error code returned for the operation.</span></span><br/>                                  |



 

## <a name="socket-close"></a><span data-ttu-id="aa0fe-286">通訊端關閉</span><span class="sxs-lookup"><span data-stu-id="aa0fe-286">Socket Close</span></span>

<span data-ttu-id="aa0fe-287">事件識別碼 = 13</span><span class="sxs-lookup"><span data-stu-id="aa0fe-287">Event ID = 13</span></span>

<span data-ttu-id="aa0fe-288">層級 = 4 (資訊) </span><span class="sxs-lookup"><span data-stu-id="aa0fe-288">Level = 4 (Information)</span></span>

<span data-ttu-id="aa0fe-289">以下是針對通訊端關閉作業追蹤的 Winsock 事件：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-289">The following Winsock events are traced for socket close operations:</span></span>

-   <span data-ttu-id="aa0fe-290">通訊端控制碼已關閉。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-290">A socket handle is closed.</span></span>

<span data-ttu-id="aa0fe-291">通訊端關閉事件會記錄下列參數：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-291">The following parameters are logged for a socket close event:</span></span>



| <span data-ttu-id="aa0fe-292">參數</span><span class="sxs-lookup"><span data-stu-id="aa0fe-292">Parameter</span></span>                                                                                            | <span data-ttu-id="aa0fe-293">Description</span><span class="sxs-lookup"><span data-stu-id="aa0fe-293">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa0fe-294"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程</span><span class="sxs-lookup"><span data-stu-id="aa0fe-294"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="aa0fe-295">進程的核心 EPROCESS 結構位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-295">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="aa0fe-296"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點</span><span class="sxs-lookup"><span data-stu-id="aa0fe-296"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="aa0fe-297">當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-297">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="aa0fe-298"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>錯誤</span><span class="sxs-lookup"><span data-stu-id="aa0fe-298"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="aa0fe-299">通訊端關閉作業的傳回值。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-299">The return value for the socket close operation.</span></span><br/>                            |



 

## <a name="socket-cleanup"></a><span data-ttu-id="aa0fe-300">通訊端清除</span><span class="sxs-lookup"><span data-stu-id="aa0fe-300">Socket Cleanup</span></span>

<span data-ttu-id="aa0fe-301">事件識別碼 = 14</span><span class="sxs-lookup"><span data-stu-id="aa0fe-301">Event ID = 14</span></span>

<span data-ttu-id="aa0fe-302">層級 = 4 (資訊) </span><span class="sxs-lookup"><span data-stu-id="aa0fe-302">Level = 4 (Information)</span></span>

<span data-ttu-id="aa0fe-303">下列 Winsock 事件會針對通訊端清除 (關機) 作業進行追蹤：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-303">The following Winsock events are traced for socket cleanup (shutdown) operations:</span></span>

-   <span data-ttu-id="aa0fe-304">在通訊端上呼叫 [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) 函數。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-304">The [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) function is called on a socket.</span></span>
-   <span data-ttu-id="aa0fe-305">傳輸表示失敗的正常中斷連線。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-305">The transport indicates a failed graceful disconnect.</span></span>

<span data-ttu-id="aa0fe-306">下列參數會針對通訊端清除 (關機) 或通訊端關閉事件進行記錄：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-306">The following parameters are logged for a socket cleanup (shutdown) or socket close event:</span></span>



| <span data-ttu-id="aa0fe-307">參數</span><span class="sxs-lookup"><span data-stu-id="aa0fe-307">Parameter</span></span>                                                                                            | <span data-ttu-id="aa0fe-308">Description</span><span class="sxs-lookup"><span data-stu-id="aa0fe-308">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa0fe-309"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程</span><span class="sxs-lookup"><span data-stu-id="aa0fe-309"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="aa0fe-310">進程的核心 EPROCESS 結構位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-310">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="aa0fe-311"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點</span><span class="sxs-lookup"><span data-stu-id="aa0fe-311"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="aa0fe-312">當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-312">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="aa0fe-313"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>錯誤</span><span class="sxs-lookup"><span data-stu-id="aa0fe-313"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="aa0fe-314">通訊端清除 (關閉) 作業的傳回值。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-314">The return value for the socket cleanup (shutdown) operation.</span></span><br/>               |



 

## <a name="socket-accept"></a><span data-ttu-id="aa0fe-315">通訊端接受</span><span class="sxs-lookup"><span data-stu-id="aa0fe-315">Socket Accept</span></span>

<span data-ttu-id="aa0fe-316">事件識別碼 = 15 (IPv4) ，事件識別碼 = 16 (IPv6) </span><span class="sxs-lookup"><span data-stu-id="aa0fe-316">Event ID = 15 (IPv4), Event ID = 16 (IPv6)</span></span>

<span data-ttu-id="aa0fe-317">層級 = 4 (資訊) </span><span class="sxs-lookup"><span data-stu-id="aa0fe-317">Level = 4 (Information)</span></span>

<span data-ttu-id="aa0fe-318">針對 [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept)、 [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex)或 [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) 函數要求，會追蹤下列 Winsock 事件：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-318">The following Winsock events are traced for an [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex), or [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) function request:</span></span>

-   <span data-ttu-id="aa0fe-319">在通訊端控制碼上的 [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept)、 [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex)或 [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) 函數要求。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-319">An [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex), or [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) function request on a socket handle.</span></span>

<span data-ttu-id="aa0fe-320">下列參數會針對 accept 事件進行記錄：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-320">The following parameters are logged for an accept event:</span></span>



| <span data-ttu-id="aa0fe-321">參數</span><span class="sxs-lookup"><span data-stu-id="aa0fe-321">Parameter</span></span>                                                                                            | <span data-ttu-id="aa0fe-322">Description</span><span class="sxs-lookup"><span data-stu-id="aa0fe-322">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa0fe-323"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程</span><span class="sxs-lookup"><span data-stu-id="aa0fe-323"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="aa0fe-324">進程的核心 EPROCESS 結構位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-324">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="aa0fe-325"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點</span><span class="sxs-lookup"><span data-stu-id="aa0fe-325"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="aa0fe-326">當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-326">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="aa0fe-327"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>位址</span><span class="sxs-lookup"><span data-stu-id="aa0fe-327"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>     | <span data-ttu-id="aa0fe-328">遠端 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-328">The remote IP address.</span></span><br/>                                                      |
| <span data-ttu-id="aa0fe-329"><span id="Port"></span><span id="port"></span><span id="PORT"></span>港口</span><span class="sxs-lookup"><span data-stu-id="aa0fe-329"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                 | <span data-ttu-id="aa0fe-330">遠端 IP 埠號碼。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-330">The remote IP port number.</span></span><br/>                                                  |
| <span data-ttu-id="aa0fe-331"><span id="Status"></span><span id="status"></span><span id="STATUS"></span>地位</span><span class="sxs-lookup"><span data-stu-id="aa0fe-331"><span id="Status"></span><span id="status"></span><span id="STATUS"></span>Status</span></span><br/>         | <span data-ttu-id="aa0fe-332">針對接受操作傳回的狀態或錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-332">The status or error code returned for the accept operation.</span></span><br/>                 |



 

## <a name="accept-failed"></a><span data-ttu-id="aa0fe-333">接受失敗</span><span class="sxs-lookup"><span data-stu-id="aa0fe-333">Accept Failed</span></span>

<span data-ttu-id="aa0fe-334">事件識別碼 = 17</span><span class="sxs-lookup"><span data-stu-id="aa0fe-334">Event ID = 17</span></span>

<span data-ttu-id="aa0fe-335">層級 = 4 (資訊) </span><span class="sxs-lookup"><span data-stu-id="aa0fe-335">Level = 4 (Information)</span></span>

<span data-ttu-id="aa0fe-336">針對失敗的接受作業，會追蹤下列 Winsock 事件：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-336">The following Winsock events are traced for a failed accept operation:</span></span>

-   <span data-ttu-id="aa0fe-337">通訊端控制碼上的 [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept)、 [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex)或 [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) 要求失敗。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-337">An [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex), or [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) request on a socket handle that fails.</span></span>

<span data-ttu-id="aa0fe-338">針對失敗的接受事件，會記錄下列參數：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-338">The following parameters are logged for a failed accept event:</span></span>



| <span data-ttu-id="aa0fe-339">參數</span><span class="sxs-lookup"><span data-stu-id="aa0fe-339">Parameter</span></span>                                                                                            | <span data-ttu-id="aa0fe-340">Description</span><span class="sxs-lookup"><span data-stu-id="aa0fe-340">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa0fe-341"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程</span><span class="sxs-lookup"><span data-stu-id="aa0fe-341"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="aa0fe-342">進程的核心 EPROCESS 結構位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-342">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="aa0fe-343"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點</span><span class="sxs-lookup"><span data-stu-id="aa0fe-343"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="aa0fe-344">當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-344">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="aa0fe-345"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>錯誤</span><span class="sxs-lookup"><span data-stu-id="aa0fe-345"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="aa0fe-346">針對失敗的接受作業傳回的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-346">The error code returned for the failing accept operation.</span></span><br/>                   |



 

## <a name="send-posted"></a><span data-ttu-id="aa0fe-347">傳送已張貼</span><span class="sxs-lookup"><span data-stu-id="aa0fe-347">Send Posted</span></span>

<span data-ttu-id="aa0fe-348">事件識別碼 = 18</span><span class="sxs-lookup"><span data-stu-id="aa0fe-348">Event ID = 18</span></span>

<span data-ttu-id="aa0fe-349">層級 = 5 (詳細資訊) </span><span class="sxs-lookup"><span data-stu-id="aa0fe-349">Level = 5 (Verbose)</span></span>

<span data-ttu-id="aa0fe-350">為了診斷使用者緩衝區損毀 (例如，當應用程式在另一個傳送或接收呼叫中重複使用相同的緩衝區時，當它仍在使用) 時，會在張貼到 Winsock 時記錄資料緩衝區，並在基礎傳輸完成時記錄資料緩衝區。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-350">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="aa0fe-351">針對通訊端傳送和接收緩衝區 post 作業，會追蹤下列 Winsock 事件：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-351">The following Winsock events are traced for socket send and receive buffer post operations:</span></span>

-   <span data-ttu-id="aa0fe-352">應用程式張貼傳送。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-352">An application posts a send.</span></span>
-   <span data-ttu-id="aa0fe-353">傳送作業完成至 Winsock。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-353">A send operation completes to Winsock.</span></span>

<span data-ttu-id="aa0fe-354">針對通訊端傳送作業，會記錄下列參數：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-354">The following parameters are logged for socket send operations:</span></span>



| <span data-ttu-id="aa0fe-355">參數</span><span class="sxs-lookup"><span data-stu-id="aa0fe-355">Parameter</span></span>                                                                                                            | <span data-ttu-id="aa0fe-356">Description</span><span class="sxs-lookup"><span data-stu-id="aa0fe-356">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa0fe-357"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程</span><span class="sxs-lookup"><span data-stu-id="aa0fe-357"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="aa0fe-358">進程的核心 EPROCESS 結構位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-358">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                          |
| <span data-ttu-id="aa0fe-359"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點</span><span class="sxs-lookup"><span data-stu-id="aa0fe-359"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="aa0fe-360">當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-360">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                     |
| <span data-ttu-id="aa0fe-361"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span><span class="sxs-lookup"><span data-stu-id="aa0fe-361"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span></span><br/>                 | <span data-ttu-id="aa0fe-362">布林值，指出是否使用快速路徑 i/o。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-362">A Boolean value that indicates if fast path I/O was used.</span></span><br/>                                                                       |
| <span data-ttu-id="aa0fe-363"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span><span class="sxs-lookup"><span data-stu-id="aa0fe-363"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span></span><br/>     | <span data-ttu-id="aa0fe-364">緩衝區計數。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-364">The buffer count.</span></span><br/>                                                                                                               |
| <span data-ttu-id="aa0fe-365"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>緩衝區</span><span class="sxs-lookup"><span data-stu-id="aa0fe-365"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="aa0fe-366">緩衝區的虛擬位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-366">The virtual address of the buffer.</span></span> <span data-ttu-id="aa0fe-367">針對連結的緩衝區，此參數是鏈中第一個緩衝區的虛擬位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-367">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/> |
| <span data-ttu-id="aa0fe-368"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="aa0fe-368"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="aa0fe-369">緩衝區的長度。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-369">The length of the buffer.</span></span> <span data-ttu-id="aa0fe-370">針對連結的緩衝區，此參數是鏈中所有緩衝區的總位元組數。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-370">For chained buffers, this parameter is the total number of bytes in all of the buffers in the chain.</span></span><br/>  |



 

<span data-ttu-id="aa0fe-371">當 FastPath 為 true 時，緩衝區陣列中第一個緩衝區的 usermode 位址會記錄在緩衝區參數中。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-371">When FastPath is true, the usermode address of the first buffer in the array of buffers is logged in the Buffer parameter.</span></span> <span data-ttu-id="aa0fe-372">當 FastPath 為 false 時，會在緩衝區參數中記錄 Winsock 核心緩衝區位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-372">When FastPath is false, the Winsock kernel buffer address is logged in the Buffer parameter.</span></span>

## <a name="receive-posted"></a><span data-ttu-id="aa0fe-373">已張貼接收</span><span class="sxs-lookup"><span data-stu-id="aa0fe-373">Receive Posted</span></span>

<span data-ttu-id="aa0fe-374">事件識別碼 = 19</span><span class="sxs-lookup"><span data-stu-id="aa0fe-374">Event ID = 19</span></span>

<span data-ttu-id="aa0fe-375">層級 = 5 (詳細資訊) </span><span class="sxs-lookup"><span data-stu-id="aa0fe-375">Level = 5 (Verbose)</span></span>

<span data-ttu-id="aa0fe-376">為了診斷使用者緩衝區損毀 (例如，當應用程式在另一個傳送或接收呼叫中重複使用相同的緩衝區時，當它仍在使用) 時，會在張貼到 Winsock 時記錄資料緩衝區，並在基礎傳輸完成時記錄資料緩衝區。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-376">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="aa0fe-377">針對通訊端接收緩衝區 post 作業，會追蹤下列 Winsock 事件：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-377">The following Winsock events are traced for socket receive buffer post operations:</span></span>

-   <span data-ttu-id="aa0fe-378">應用程式張貼接收。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-378">An application posts a receive.</span></span>
-   <span data-ttu-id="aa0fe-379">接收作業會完成至 Winsock。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-379">A receive operation completes to Winsock.</span></span>

<span data-ttu-id="aa0fe-380">針對通訊端接收作業，會記錄下列參數：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-380">The following parameters are logged for socket receive operations:</span></span>



| <span data-ttu-id="aa0fe-381">參數</span><span class="sxs-lookup"><span data-stu-id="aa0fe-381">Parameter</span></span>                                                                                                            | <span data-ttu-id="aa0fe-382">Description</span><span class="sxs-lookup"><span data-stu-id="aa0fe-382">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa0fe-383"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程</span><span class="sxs-lookup"><span data-stu-id="aa0fe-383"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="aa0fe-384">進程的核心 EPROCESS 結構位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-384">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                          |
| <span data-ttu-id="aa0fe-385"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點</span><span class="sxs-lookup"><span data-stu-id="aa0fe-385"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="aa0fe-386">當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-386">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                     |
| <span data-ttu-id="aa0fe-387"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span><span class="sxs-lookup"><span data-stu-id="aa0fe-387"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span></span><br/>                 | <span data-ttu-id="aa0fe-388">布林值，指出是否使用快速路徑 i/o。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-388">A Boolean value that indicates if fast path I/O was used.</span></span><br/>                                                                       |
| <span data-ttu-id="aa0fe-389"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span><span class="sxs-lookup"><span data-stu-id="aa0fe-389"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span></span><br/>     | <span data-ttu-id="aa0fe-390">緩衝區計數。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-390">The buffer count.</span></span><br/>                                                                                                               |
| <span data-ttu-id="aa0fe-391"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>緩衝區</span><span class="sxs-lookup"><span data-stu-id="aa0fe-391"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="aa0fe-392">緩衝區的虛擬位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-392">The virtual address of the buffer.</span></span> <span data-ttu-id="aa0fe-393">針對連結的緩衝區，此參數是鏈中第一個緩衝區的虛擬位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-393">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/> |
| <span data-ttu-id="aa0fe-394"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="aa0fe-394"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="aa0fe-395">緩衝區的長度。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-395">The length of the buffer.</span></span> <span data-ttu-id="aa0fe-396">針對連結的緩衝區，此參數是鏈中所有緩衝區的總位元組數。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-396">For chained buffers, this parameter is the total number of bytes in all of the buffers in the chain.</span></span><br/>  |



 

<span data-ttu-id="aa0fe-397">當 FastPath 為 true 時，緩衝區陣列中第一個緩衝區的 usermode 位址會記錄在緩衝區參數中。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-397">When FastPath is true, the usermode address of the first buffer in the array of buffers is logged in the Buffer parameter.</span></span> <span data-ttu-id="aa0fe-398">當 FastPath 為 false 時，會在緩衝區參數中記錄 Winsock 核心緩衝區位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-398">When FastPath is false, the Winsock kernel buffer address is logged in the Buffer parameter.</span></span>

## <a name="recvfrom-posted"></a><span data-ttu-id="aa0fe-399">張貼的 RecvFrom</span><span class="sxs-lookup"><span data-stu-id="aa0fe-399">RecvFrom Posted</span></span>

<span data-ttu-id="aa0fe-400">事件識別碼 = 20</span><span class="sxs-lookup"><span data-stu-id="aa0fe-400">Event ID = 20</span></span>

<span data-ttu-id="aa0fe-401">層級 = 5 (詳細資訊) </span><span class="sxs-lookup"><span data-stu-id="aa0fe-401">Level = 5 (Verbose)</span></span>

<span data-ttu-id="aa0fe-402">為了診斷使用者緩衝區損毀 (例如，當應用程式在另一個傳送或接收呼叫中重複使用相同的緩衝區時，當它仍在使用) 時，會在張貼到 Winsock 時記錄資料緩衝區，並在基礎傳輸完成時記錄資料緩衝區。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-402">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="aa0fe-403">針對通訊端上的 [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) 緩衝區 post 作業，會追蹤下列 Winsock 事件：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-403">The following Winsock events are traced for a [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) buffer post operation on a socket:</span></span>

-   <span data-ttu-id="aa0fe-404">應用程式會從作業張貼接收。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-404">An application posts a receive from operation.</span></span>

<span data-ttu-id="aa0fe-405">Recvfrom 作業會記錄下列參數：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-405">The following parameters are logged for the recvfrom operation:</span></span>



| <span data-ttu-id="aa0fe-406">參數</span><span class="sxs-lookup"><span data-stu-id="aa0fe-406">Parameter</span></span>                                                                                                            | <span data-ttu-id="aa0fe-407">Description</span><span class="sxs-lookup"><span data-stu-id="aa0fe-407">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa0fe-408"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程</span><span class="sxs-lookup"><span data-stu-id="aa0fe-408"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="aa0fe-409">進程的核心 EPROCESS 結構位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-409">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                          |
| <span data-ttu-id="aa0fe-410"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點</span><span class="sxs-lookup"><span data-stu-id="aa0fe-410"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="aa0fe-411">當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-411">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                     |
| <span data-ttu-id="aa0fe-412"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span><span class="sxs-lookup"><span data-stu-id="aa0fe-412"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span></span><br/>                 | <span data-ttu-id="aa0fe-413">布林值，指出是否使用快速路徑 i/o。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-413">A Boolean value that indicates if fast path I/O was used.</span></span><br/>                                                                       |
| <span data-ttu-id="aa0fe-414"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span><span class="sxs-lookup"><span data-stu-id="aa0fe-414"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span></span><br/>     | <span data-ttu-id="aa0fe-415">緩衝區計數。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-415">The buffer count.</span></span><br/>                                                                                                               |
| <span data-ttu-id="aa0fe-416"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>緩衝區</span><span class="sxs-lookup"><span data-stu-id="aa0fe-416"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="aa0fe-417">緩衝區的虛擬位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-417">The virtual address of the buffer.</span></span> <span data-ttu-id="aa0fe-418">針對連結的緩衝區，此參數是鏈中第一個緩衝區的虛擬位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-418">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/> |
| <span data-ttu-id="aa0fe-419"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="aa0fe-419"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="aa0fe-420">緩衝區的長度。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-420">The length of the buffer.</span></span> <span data-ttu-id="aa0fe-421">針對連結的緩衝區，此參數是鏈中所有緩衝區的總位元組數。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-421">For chained buffers, this parameter is the total number of bytes in all of the buffers in the chain.</span></span><br/>  |



 

<span data-ttu-id="aa0fe-422">當 FastPath 為 true 時，緩衝區陣列中第一個緩衝區的 usermode 位址會記錄在緩衝區參數中。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-422">When FastPath is true, the usermode address of the first buffer in the array of buffers is logged in the Buffer parameter.</span></span> <span data-ttu-id="aa0fe-423">當 FastPath 為 false 時，會在緩衝區參數中記錄 Winsock 核心緩衝區位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-423">When FastPath is false, the Winsock kernel buffer address is logged in the Buffer parameter.</span></span>

## <a name="sendto-posted"></a><span data-ttu-id="aa0fe-424">SendTo 張貼</span><span class="sxs-lookup"><span data-stu-id="aa0fe-424">SendTo Posted</span></span>

<span data-ttu-id="aa0fe-425">事件識別碼 = 21 (IPv4) ，事件識別碼 = 22 (IPv6) </span><span class="sxs-lookup"><span data-stu-id="aa0fe-425">Event ID = 21 (IPv4), Event ID = 22 (IPv6)</span></span>

<span data-ttu-id="aa0fe-426">層級 = 5 (詳細資訊) </span><span class="sxs-lookup"><span data-stu-id="aa0fe-426">Level = 5 (Verbose)</span></span>

<span data-ttu-id="aa0fe-427">為了診斷使用者緩衝區損毀 (例如，當應用程式在另一個傳送或接收呼叫中重複使用相同的緩衝區時，當它仍在使用) 時，會在張貼到 Winsock 時記錄資料緩衝區，並在基礎傳輸完成時記錄資料緩衝區。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-427">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="aa0fe-428">針對通訊端上的 [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) 緩衝區 post 作業，會追蹤下列 Winsock 事件：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-428">The following Winsock events are traced for a [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) buffer post operation on a socket:</span></span>

-   <span data-ttu-id="aa0fe-429">應用程式張貼傳送的來源。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-429">An application posts a send from.</span></span>

<span data-ttu-id="aa0fe-430">針對 [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) 作業記錄下列參數：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-430">The following parameters are logged for the [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) operation:</span></span>



| <span data-ttu-id="aa0fe-431">參數</span><span class="sxs-lookup"><span data-stu-id="aa0fe-431">Parameter</span></span>                                                                                                            | <span data-ttu-id="aa0fe-432">Description</span><span class="sxs-lookup"><span data-stu-id="aa0fe-432">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa0fe-433"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程</span><span class="sxs-lookup"><span data-stu-id="aa0fe-433"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="aa0fe-434">進程的核心 EPROCESS 結構位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-434">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                          |
| <span data-ttu-id="aa0fe-435"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點</span><span class="sxs-lookup"><span data-stu-id="aa0fe-435"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="aa0fe-436">當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-436">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                     |
| <span data-ttu-id="aa0fe-437"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span><span class="sxs-lookup"><span data-stu-id="aa0fe-437"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span></span><br/>                 | <span data-ttu-id="aa0fe-438">布林值，指出是否使用快速路徑 i/o。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-438">A Boolean value that indicates if fast path I/O was used.</span></span><br/>                                                                       |
| <span data-ttu-id="aa0fe-439"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span><span class="sxs-lookup"><span data-stu-id="aa0fe-439"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span></span><br/>     | <span data-ttu-id="aa0fe-440">緩衝區計數。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-440">The buffer count.</span></span><br/>                                                                                                               |
| <span data-ttu-id="aa0fe-441"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>緩衝區</span><span class="sxs-lookup"><span data-stu-id="aa0fe-441"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="aa0fe-442">緩衝區的虛擬位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-442">The virtual address of the buffer.</span></span> <span data-ttu-id="aa0fe-443">針對連結的緩衝區，此參數是鏈中第一個緩衝區的虛擬位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-443">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/> |
| <span data-ttu-id="aa0fe-444"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="aa0fe-444"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="aa0fe-445">緩衝區的長度。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-445">The length of the buffer.</span></span> <span data-ttu-id="aa0fe-446">針對連結的緩衝區，此參數是鏈中所有緩衝區的總位元組數。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-446">For chained buffers, this parameter is the total number of bytes in all of the buffers in the chain.</span></span><br/>  |
| <span data-ttu-id="aa0fe-447"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>位址</span><span class="sxs-lookup"><span data-stu-id="aa0fe-447"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>                     | <span data-ttu-id="aa0fe-448">通訊端的遠端 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-448">The remote IP address of the socket.</span></span><br/>                                                                                            |
| <span data-ttu-id="aa0fe-449"><span id="Port"></span><span id="port"></span><span id="PORT"></span>港口</span><span class="sxs-lookup"><span data-stu-id="aa0fe-449"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                                 | <span data-ttu-id="aa0fe-450">通訊端的遠端 IP 埠號碼。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-450">The remote IP port number of the socket.</span></span><br/>                                                                                        |



 

<span data-ttu-id="aa0fe-451">當 FastPath 為 true 時，緩衝區陣列中第一個緩衝區的 usermode 位址會記錄在緩衝區參數中。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-451">When FastPath is true, the usermode address of the first buffer in the array of buffers is logged in the Buffer parameter.</span></span> <span data-ttu-id="aa0fe-452">當 FastPath 為 false 時，會在緩衝區參數中記錄 Winsock 核心緩衝區位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-452">When FastPath is false, the Winsock kernel buffer address is logged in the Buffer parameter.</span></span>

## <a name="recv-completed"></a><span data-ttu-id="aa0fe-453">已完成接收</span><span class="sxs-lookup"><span data-stu-id="aa0fe-453">Recv Completed</span></span>

<span data-ttu-id="aa0fe-454">事件識別碼 = 23</span><span class="sxs-lookup"><span data-stu-id="aa0fe-454">Event ID = 23</span></span>

<span data-ttu-id="aa0fe-455">層級 = 5 (詳細資訊) </span><span class="sxs-lookup"><span data-stu-id="aa0fe-455">Level = 5 (Verbose)</span></span>

<span data-ttu-id="aa0fe-456">為了診斷使用者緩衝區損毀 (例如，當應用程式在另一個傳送或接收呼叫中重複使用相同的緩衝區時，當它仍在使用) 時，會在張貼到 Winsock 時記錄資料緩衝區，並在基礎傳輸完成時記錄資料緩衝區。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-456">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="aa0fe-457">針對通訊端接收完成的作業，會追蹤下列 Winsock 事件：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-457">The following Winsock events are traced for socket receive completed operations:</span></span>

-   <span data-ttu-id="aa0fe-458">傳送作業會完成傳輸。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-458">A send operation completes to the transport.</span></span>
-   <span data-ttu-id="aa0fe-459">接收作業會完成傳輸。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-459">A receive operation completes to the transport.</span></span>

<span data-ttu-id="aa0fe-460">系統會針對傳送完成或接收完成記錄下列參數：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-460">The following parameters are logged for a send completed or receive completed:</span></span>



| <span data-ttu-id="aa0fe-461">參數</span><span class="sxs-lookup"><span data-stu-id="aa0fe-461">Parameter</span></span>                                                                                                            | <span data-ttu-id="aa0fe-462">Description</span><span class="sxs-lookup"><span data-stu-id="aa0fe-462">Description</span></span>                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa0fe-463"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程</span><span class="sxs-lookup"><span data-stu-id="aa0fe-463"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="aa0fe-464">進程的核心 EPROCESS 結構位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-464">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                                   |
| <span data-ttu-id="aa0fe-465"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點</span><span class="sxs-lookup"><span data-stu-id="aa0fe-465"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="aa0fe-466">當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-466">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                              |
| <span data-ttu-id="aa0fe-467"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>緩衝區</span><span class="sxs-lookup"><span data-stu-id="aa0fe-467"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="aa0fe-468">緩衝區的虛擬位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-468">The virtual address of the buffer.</span></span> <span data-ttu-id="aa0fe-469">針對連結的緩衝區，此參數是鏈中第一個緩衝區的虛擬位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-469">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/>          |
| <span data-ttu-id="aa0fe-470"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="aa0fe-470"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="aa0fe-471">收到的位元組緩衝區長度。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-471">The length of the buffer of bytes received.</span></span> <span data-ttu-id="aa0fe-472">針對連結的緩衝區，此參數是在鏈中的所有緩衝區內接收的位元組總數。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-472">For chained buffers, this parameter is the total bytes received in all buffers in the chain.</span></span><br/> |



 

## <a name="send-completed"></a><span data-ttu-id="aa0fe-473">傳送完成</span><span class="sxs-lookup"><span data-stu-id="aa0fe-473">Send Completed</span></span>

<span data-ttu-id="aa0fe-474">事件識別碼 = 24</span><span class="sxs-lookup"><span data-stu-id="aa0fe-474">Event ID = 24</span></span>

<span data-ttu-id="aa0fe-475">層級 = 5 (詳細資訊) </span><span class="sxs-lookup"><span data-stu-id="aa0fe-475">Level = 5 (Verbose)</span></span>

<span data-ttu-id="aa0fe-476">為了診斷使用者緩衝區損毀 (例如，當應用程式在另一個傳送或接收呼叫中重複使用相同的緩衝區時，當它仍在使用) 時，會在張貼到 Winsock 時記錄資料緩衝區，並在基礎傳輸完成時記錄資料緩衝區。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-476">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="aa0fe-477">針對通訊端傳送完成的作業，會追蹤下列 Winsock 事件：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-477">The following Winsock events are traced for socket send completed operations:</span></span>

-   <span data-ttu-id="aa0fe-478">傳送作業會完成傳輸。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-478">A send operation completes to the transport.</span></span>

<span data-ttu-id="aa0fe-479">系統會針對傳送完成記錄下列參數：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-479">The following parameters are logged for a send completed:</span></span>



| <span data-ttu-id="aa0fe-480">參數</span><span class="sxs-lookup"><span data-stu-id="aa0fe-480">Parameter</span></span>                                                                                                            | <span data-ttu-id="aa0fe-481">Description</span><span class="sxs-lookup"><span data-stu-id="aa0fe-481">Description</span></span>                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa0fe-482"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程</span><span class="sxs-lookup"><span data-stu-id="aa0fe-482"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="aa0fe-483">進程的核心 EPROCESS 結構位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-483">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                             |
| <span data-ttu-id="aa0fe-484"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點</span><span class="sxs-lookup"><span data-stu-id="aa0fe-484"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="aa0fe-485">當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-485">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                        |
| <span data-ttu-id="aa0fe-486"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>緩衝區</span><span class="sxs-lookup"><span data-stu-id="aa0fe-486"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="aa0fe-487">緩衝區的虛擬位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-487">The virtual address of the buffer.</span></span> <span data-ttu-id="aa0fe-488">針對連結的緩衝區，此參數是鏈中第一個緩衝區的虛擬位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-488">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/>    |
| <span data-ttu-id="aa0fe-489"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="aa0fe-489"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="aa0fe-490">傳送位元組緩衝區的長度。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-490">The length of the buffer of bytes sent.</span></span> <span data-ttu-id="aa0fe-491">針對連結的緩衝區，此參數是從鏈中的所有緩衝區傳送的位元組總數。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-491">For chained buffers, this parameter is the total bytes sent from all buffers in the chain.</span></span><br/> |



 

## <a name="sendmsg-completed"></a><span data-ttu-id="aa0fe-492">SendMsg 已完成</span><span class="sxs-lookup"><span data-stu-id="aa0fe-492">SendMsg Completed</span></span>

<span data-ttu-id="aa0fe-493">事件識別碼 = 25</span><span class="sxs-lookup"><span data-stu-id="aa0fe-493">Event ID = 25</span></span>

<span data-ttu-id="aa0fe-494">層級 = 5 (詳細資訊) </span><span class="sxs-lookup"><span data-stu-id="aa0fe-494">Level = 5 (Verbose)</span></span>

<span data-ttu-id="aa0fe-495">為了診斷使用者緩衝區損毀 (例如，當應用程式在另一個傳送或接收呼叫中重複使用相同的緩衝區時，當它仍在使用) 時，會在張貼到 Winsock 時記錄資料緩衝區，並在基礎傳輸完成時記錄資料緩衝區。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-495">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="aa0fe-496">當通訊端上的 [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) 緩衝區 post 操作完成時，會追蹤下列 Winsock 事件：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-496">The following Winsock events are traced when a [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) buffer post operation completes on a socket:</span></span>

-   <span data-ttu-id="aa0fe-497">應用程式完成 [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) 作業。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-497">An application completes a [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) operation.</span></span>

<span data-ttu-id="aa0fe-498">[**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)完成時會記錄下列參數：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-498">The following parameters are logged for the [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) completion:</span></span>



| <span data-ttu-id="aa0fe-499">參數</span><span class="sxs-lookup"><span data-stu-id="aa0fe-499">Parameter</span></span>                                                                                                            | <span data-ttu-id="aa0fe-500">Description</span><span class="sxs-lookup"><span data-stu-id="aa0fe-500">Description</span></span>                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa0fe-501"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程</span><span class="sxs-lookup"><span data-stu-id="aa0fe-501"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="aa0fe-502">進程的核心 EPROCESS 結構位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-502">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                             |
| <span data-ttu-id="aa0fe-503"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點</span><span class="sxs-lookup"><span data-stu-id="aa0fe-503"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="aa0fe-504">當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-504">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                        |
| <span data-ttu-id="aa0fe-505"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span><span class="sxs-lookup"><span data-stu-id="aa0fe-505"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span></span><br/>     | <span data-ttu-id="aa0fe-506">緩衝區計數。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-506">The buffer count.</span></span><br/>                                                                                                                  |
| <span data-ttu-id="aa0fe-507"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>緩衝區</span><span class="sxs-lookup"><span data-stu-id="aa0fe-507"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="aa0fe-508">緩衝區的虛擬位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-508">The virtual address of the buffer.</span></span> <span data-ttu-id="aa0fe-509">針對連結的緩衝區，此參數是鏈中第一個緩衝區的虛擬位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-509">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/>    |
| <span data-ttu-id="aa0fe-510"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="aa0fe-510"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="aa0fe-511">傳送位元組緩衝區的長度。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-511">The length of the buffer of bytes sent.</span></span> <span data-ttu-id="aa0fe-512">針對連結的緩衝區，此參數是從鏈中的所有緩衝區傳送的位元組總數。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-512">For chained buffers, this parameter is the total bytes sent from all buffers in the chain.</span></span><br/> |
| <span data-ttu-id="aa0fe-513"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>位址</span><span class="sxs-lookup"><span data-stu-id="aa0fe-513"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>                     | <span data-ttu-id="aa0fe-514">通訊端的遠端 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-514">The remote IP address of the socket.</span></span><br/>                                                                                               |
| <span data-ttu-id="aa0fe-515"><span id="Port"></span><span id="port"></span><span id="PORT"></span>港口</span><span class="sxs-lookup"><span data-stu-id="aa0fe-515"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                                 | <span data-ttu-id="aa0fe-516">通訊端的遠端 IP 埠號碼。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-516">The remote IP port number of the socket.</span></span><br/>                                                                                           |



 

## <a name="recvfrom-completed"></a><span data-ttu-id="aa0fe-517">RecvFrom 已完成</span><span class="sxs-lookup"><span data-stu-id="aa0fe-517">RecvFrom Completed</span></span>

<span data-ttu-id="aa0fe-518">事件識別碼 = 26 (IPv4) ，事件識別碼 = 27 (IPv6) </span><span class="sxs-lookup"><span data-stu-id="aa0fe-518">Event ID = 26 (IPv4), Event ID = 27 (IPv6)</span></span>

<span data-ttu-id="aa0fe-519">層級 = 5 (詳細資訊) </span><span class="sxs-lookup"><span data-stu-id="aa0fe-519">Level = 5 (Verbose)</span></span>

<span data-ttu-id="aa0fe-520">為了診斷使用者緩衝區損毀 (例如，當應用程式在另一個傳送或接收呼叫中重複使用相同的緩衝區時，當它仍在使用) 時，會在張貼到 Winsock 時記錄資料緩衝區，並在基礎傳輸完成時記錄資料緩衝區。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-520">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="aa0fe-521">當通訊端上的 [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) 緩衝區 post 操作完成時，會追蹤下列 Winsock 事件：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-521">The following Winsock events are traced when a [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) buffer post operation completes on a socket:</span></span>

-   <span data-ttu-id="aa0fe-522">應用程式完成 [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) 作業。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-522">An application completes a [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) operation.</span></span>

<span data-ttu-id="aa0fe-523">[**Recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom)完成時會記錄下列參數：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-523">The following parameters are logged for the [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) completion:</span></span>



| <span data-ttu-id="aa0fe-524">參數</span><span class="sxs-lookup"><span data-stu-id="aa0fe-524">Parameter</span></span>                                                                                                            | <span data-ttu-id="aa0fe-525">Description</span><span class="sxs-lookup"><span data-stu-id="aa0fe-525">Description</span></span>                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa0fe-526"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程</span><span class="sxs-lookup"><span data-stu-id="aa0fe-526"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="aa0fe-527">進程的核心 EPROCESS 結構位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-527">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                                   |
| <span data-ttu-id="aa0fe-528"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點</span><span class="sxs-lookup"><span data-stu-id="aa0fe-528"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="aa0fe-529">當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-529">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                              |
| <span data-ttu-id="aa0fe-530"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span><span class="sxs-lookup"><span data-stu-id="aa0fe-530"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span></span><br/>     | <span data-ttu-id="aa0fe-531">緩衝區計數。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-531">The buffer count.</span></span><br/>                                                                                                                        |
| <span data-ttu-id="aa0fe-532"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>緩衝區</span><span class="sxs-lookup"><span data-stu-id="aa0fe-532"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="aa0fe-533">緩衝區的虛擬位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-533">The virtual address of the buffer.</span></span> <span data-ttu-id="aa0fe-534">針對連結的緩衝區，此參數是鏈中第一個緩衝區的虛擬位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-534">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/>          |
| <span data-ttu-id="aa0fe-535"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="aa0fe-535"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="aa0fe-536">收到的位元組緩衝區長度。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-536">The length of the buffer of bytes received.</span></span> <span data-ttu-id="aa0fe-537">針對連結的緩衝區，此參數是在鏈中的所有緩衝區內接收的位元組總數。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-537">For chained buffers, this parameter is the total bytes received in all buffers in the chain.</span></span><br/> |
| <span data-ttu-id="aa0fe-538"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>位址</span><span class="sxs-lookup"><span data-stu-id="aa0fe-538"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>                     | <span data-ttu-id="aa0fe-539">通訊端的遠端 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-539">The remote IP address of the socket.</span></span><br/>                                                                                                     |
| <span data-ttu-id="aa0fe-540"><span id="Port"></span><span id="port"></span><span id="PORT"></span>港口</span><span class="sxs-lookup"><span data-stu-id="aa0fe-540"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                                 | <span data-ttu-id="aa0fe-541">通訊端的遠端 IP 埠號碼。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-541">The remote IP port number of the socket.</span></span><br/>                                                                                                 |



 

## <a name="sendto-completed"></a><span data-ttu-id="aa0fe-542">SendTo 已完成</span><span class="sxs-lookup"><span data-stu-id="aa0fe-542">SendTo Completed</span></span>

<span data-ttu-id="aa0fe-543">事件識別碼 = 28</span><span class="sxs-lookup"><span data-stu-id="aa0fe-543">Event ID = 28</span></span>

<span data-ttu-id="aa0fe-544">層級 = 5 (詳細資訊) </span><span class="sxs-lookup"><span data-stu-id="aa0fe-544">Level = 5 (Verbose)</span></span>

<span data-ttu-id="aa0fe-545">為了診斷使用者緩衝區損毀 (例如，當應用程式在另一個傳送或接收呼叫中重複使用相同的緩衝區時，當它仍在使用) 時，會在張貼到 Winsock 時記錄資料緩衝區，並在基礎傳輸完成時記錄資料緩衝區。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-545">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="aa0fe-546">在通訊端上完成 [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) 緩衝區 post 作業時，會追蹤下列 Winsock 事件：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-546">The following Winsock events are traced when a [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) buffer post operation completes on a socket:</span></span>

-   <span data-ttu-id="aa0fe-547">應用程式完成 [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) 操作。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-547">An application completes a [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) operation.</span></span>

<span data-ttu-id="aa0fe-548">針對 [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) 完成記錄下列參數：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-548">The following parameters are logged for the [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) completion:</span></span>



| <span data-ttu-id="aa0fe-549">參數</span><span class="sxs-lookup"><span data-stu-id="aa0fe-549">Parameter</span></span>                                                                                                            | <span data-ttu-id="aa0fe-550">Description</span><span class="sxs-lookup"><span data-stu-id="aa0fe-550">Description</span></span>                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa0fe-551"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程</span><span class="sxs-lookup"><span data-stu-id="aa0fe-551"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="aa0fe-552">進程的核心 EPROCESS 結構位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-552">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                             |
| <span data-ttu-id="aa0fe-553"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點</span><span class="sxs-lookup"><span data-stu-id="aa0fe-553"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="aa0fe-554">當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-554">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                        |
| <span data-ttu-id="aa0fe-555"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span><span class="sxs-lookup"><span data-stu-id="aa0fe-555"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span></span><br/>     | <span data-ttu-id="aa0fe-556">緩衝區計數。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-556">The buffer count.</span></span><br/>                                                                                                                  |
| <span data-ttu-id="aa0fe-557"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>緩衝區</span><span class="sxs-lookup"><span data-stu-id="aa0fe-557"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="aa0fe-558">緩衝區的虛擬位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-558">The virtual address of the buffer.</span></span> <span data-ttu-id="aa0fe-559">針對連結的緩衝區，此參數是鏈中第一個緩衝區的虛擬位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-559">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/>    |
| <span data-ttu-id="aa0fe-560"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="aa0fe-560"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="aa0fe-561">傳送位元組緩衝區的長度。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-561">The length of the buffer of bytes sent.</span></span> <span data-ttu-id="aa0fe-562">針對連結的緩衝區，此參數是從鏈中的所有緩衝區傳送的位元組總數。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-562">For chained buffers, this parameter is the total bytes sent from all buffers in the chain.</span></span><br/> |
| <span data-ttu-id="aa0fe-563"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>位址</span><span class="sxs-lookup"><span data-stu-id="aa0fe-563"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>                     | <span data-ttu-id="aa0fe-564">通訊端的遠端 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-564">The remote IP address of the socket.</span></span><br/>                                                                                               |
| <span data-ttu-id="aa0fe-565"><span id="Port"></span><span id="port"></span><span id="PORT"></span>港口</span><span class="sxs-lookup"><span data-stu-id="aa0fe-565"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                                 | <span data-ttu-id="aa0fe-566">通訊端的遠端 IP 埠號碼。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-566">The remote IP port number of the socket.</span></span><br/>                                                                                           |



 

## <a name="socket-option-set"></a><span data-ttu-id="aa0fe-567">通訊端選項群組</span><span class="sxs-lookup"><span data-stu-id="aa0fe-567">Socket Option Set</span></span>

<span data-ttu-id="aa0fe-568">事件識別碼 = 29</span><span class="sxs-lookup"><span data-stu-id="aa0fe-568">Event ID = 29</span></span>

<span data-ttu-id="aa0fe-569">層級 = 5 (詳細資訊) </span><span class="sxs-lookup"><span data-stu-id="aa0fe-569">Level = 5 (Verbose)</span></span>

<span data-ttu-id="aa0fe-570">每當應用程式變更特定通訊端選項值和 Ioctls 時，就會記錄新的值。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-570">Whenever an application changes certain socket option values and Ioctls, the new values will be logged.</span></span> <span data-ttu-id="aa0fe-571">記錄的選項可以用來診斷應用程式中的效能不佳或奇怪的行為。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-571">The options logged can be used to diagnose poor performance or strange behavior in applications.</span></span> <span data-ttu-id="aa0fe-572">下列 Winsock 事件會針對某些通訊端選項和 Ioctls 進行追蹤：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-572">The following Winsock events are traced for certain socket options and Ioctls:</span></span>

-   <span data-ttu-id="aa0fe-573">\_SNDBUF 變更。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-573">SO\_SNDBUF changes.</span></span>
-   <span data-ttu-id="aa0fe-574">\_RCVBUF 變更。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-574">SO\_RCVBUF changes.</span></span>
-   <span data-ttu-id="aa0fe-575">FIONBIO</span><span class="sxs-lookup"><span data-stu-id="aa0fe-575">FIONBIO</span></span>
-   <span data-ttu-id="aa0fe-576">SIO \_ 啟用 \_ 迴圈 \_ 佇列</span><span class="sxs-lookup"><span data-stu-id="aa0fe-576">SIO\_ENABLE\_CIRCULAR\_QUEUEING</span></span>
-   <span data-ttu-id="aa0fe-577">SIO \_ UDP \_ CONNRESET</span><span class="sxs-lookup"><span data-stu-id="aa0fe-577">SIO\_UDP\_CONNRESET</span></span>
-   <span data-ttu-id="aa0fe-578">\_OOBINLINE</span><span class="sxs-lookup"><span data-stu-id="aa0fe-578">SO\_OOBINLINE</span></span>

<span data-ttu-id="aa0fe-579">針對會變更上述任何值的 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 和 [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) 函式呼叫，會記錄下列參數：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-579">The following parameters are logged for [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) and [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) function calls that change any of the above values:</span></span>



| <span data-ttu-id="aa0fe-580">參數</span><span class="sxs-lookup"><span data-stu-id="aa0fe-580">Parameter</span></span>                                                                                            | <span data-ttu-id="aa0fe-581">Description</span><span class="sxs-lookup"><span data-stu-id="aa0fe-581">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa0fe-582"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程</span><span class="sxs-lookup"><span data-stu-id="aa0fe-582"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="aa0fe-583">進程的核心 EPROCESS 結構位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-583">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="aa0fe-584"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點</span><span class="sxs-lookup"><span data-stu-id="aa0fe-584"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="aa0fe-585">當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-585">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="aa0fe-586"><span id="Option"></span><span id="option"></span><span id="OPTION"></span>選項</span><span class="sxs-lookup"><span data-stu-id="aa0fe-586"><span id="Option"></span><span id="option"></span><span id="OPTION"></span>Option</span></span><br/>         | <span data-ttu-id="aa0fe-587">已變更的通訊端選項或 Ioctl。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-587">The socket option or Ioctl that is changed.</span></span> <br/>                                |
| <span data-ttu-id="aa0fe-588"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>價值</span><span class="sxs-lookup"><span data-stu-id="aa0fe-588"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span><br/>             | <span data-ttu-id="aa0fe-589">通訊端選項或 Ioctl 的新值。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-589">The new value for the socket option or Ioctl.</span></span> <br/>                              |



 

## <a name="selectpoll-posted"></a><span data-ttu-id="aa0fe-590">選取/輪詢已張貼</span><span class="sxs-lookup"><span data-stu-id="aa0fe-590">Select/Poll Posted</span></span>

<span data-ttu-id="aa0fe-591">事件識別碼 = 30</span><span class="sxs-lookup"><span data-stu-id="aa0fe-591">Event ID = 30</span></span>

<span data-ttu-id="aa0fe-592">層級 = 5 (詳細資訊) </span><span class="sxs-lookup"><span data-stu-id="aa0fe-592">Level = 5 (Verbose)</span></span>

<span data-ttu-id="aa0fe-593">當應用程式呼叫 [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) 或 [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) 函式時，會追蹤下列 Winsock 事件：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-593">The following Winsock events are traced when an application calls the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) function:</span></span>

-   <span data-ttu-id="aa0fe-594">應用程式張貼 [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) 或 [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) 要求。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-594">Application posts a [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) request.</span></span>

<span data-ttu-id="aa0fe-595">針對 [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) 或 [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) 事件記錄下列參數：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-595">The following parameters are logged for [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) events:</span></span>



| <span data-ttu-id="aa0fe-596">參數</span><span class="sxs-lookup"><span data-stu-id="aa0fe-596">Parameter</span></span>                                                                                                        | <span data-ttu-id="aa0fe-597">Description</span><span class="sxs-lookup"><span data-stu-id="aa0fe-597">Description</span></span>                                                                                                    |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa0fe-598"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程</span><span class="sxs-lookup"><span data-stu-id="aa0fe-598"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                 | <span data-ttu-id="aa0fe-599">擁有的處理序識別碼。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-599">The owning process ID.</span></span><br/>                                                                              |
| <span data-ttu-id="aa0fe-600"><span id="HandleCount"></span><span id="handlecount"></span><span id="HANDLECOUNT"></span>HandleCount</span><span class="sxs-lookup"><span data-stu-id="aa0fe-600"><span id="HandleCount"></span><span id="handlecount"></span><span id="HANDLECOUNT"></span>HandleCount</span></span><br/> | <span data-ttu-id="aa0fe-601">應用程式所傳入的控制碼數目 (只有在起始事件) 上才有效。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-601">The number of handles passed in by the application (only valid on the initiating event).</span></span><br/>            |
| <span data-ttu-id="aa0fe-602"><span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>超時</span><span class="sxs-lookup"><span data-stu-id="aa0fe-602"><span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>Timeout</span></span><br/>                 | <span data-ttu-id="aa0fe-603">[**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select)或 [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll)函數等候的最長時間。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-603">The maximum time for the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) function to wait.</span></span><br/> |



 

## <a name="selectpoll-completed"></a><span data-ttu-id="aa0fe-604">選取/輪詢已完成</span><span class="sxs-lookup"><span data-stu-id="aa0fe-604">Select/Poll Completed</span></span>

<span data-ttu-id="aa0fe-605">事件識別碼 = 31</span><span class="sxs-lookup"><span data-stu-id="aa0fe-605">Event ID = 31</span></span>

<span data-ttu-id="aa0fe-606">層級 = 5 (詳細資訊) </span><span class="sxs-lookup"><span data-stu-id="aa0fe-606">Level = 5 (Verbose)</span></span>

<span data-ttu-id="aa0fe-607">當應用程式呼叫 [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) 或 [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) 函式時，會追蹤下列 Winsock 事件：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-607">The following Winsock events are traced when an application calls the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) function:</span></span>

-   <span data-ttu-id="aa0fe-608">Winsock 完成 [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) 或 [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) 呼叫。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-608">Winsock completes a [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) call.</span></span>

<span data-ttu-id="aa0fe-609">當 [**選取**](/windows/desktop/api/Winsock2/nf-winsock2-select) 或 [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) 操作完成時，會記錄下列參數：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-609">The following parameters are logged when a [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) operation completes:</span></span>



| <span data-ttu-id="aa0fe-610">參數</span><span class="sxs-lookup"><span data-stu-id="aa0fe-610">Parameter</span></span>                                                                                            | <span data-ttu-id="aa0fe-611">Description</span><span class="sxs-lookup"><span data-stu-id="aa0fe-611">Description</span></span>                                                                                                    |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa0fe-612"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程</span><span class="sxs-lookup"><span data-stu-id="aa0fe-612"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="aa0fe-613">進程的核心 EPROCESS 結構位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-613">The kernel EPROCESS structure address for the process.</span></span><br/>                                              |
| <span data-ttu-id="aa0fe-614"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點</span><span class="sxs-lookup"><span data-stu-id="aa0fe-614"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="aa0fe-615">當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-615">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                         |
| <span data-ttu-id="aa0fe-616"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>錯誤</span><span class="sxs-lookup"><span data-stu-id="aa0fe-616"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="aa0fe-617">針對 [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) 或 [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) 作業傳回的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-617">The error code returned for the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) operation.</span></span><br/> |



 

## <a name="wsaeventselect"></a><span data-ttu-id="aa0fe-618">WSAEventSelect</span><span class="sxs-lookup"><span data-stu-id="aa0fe-618">WSAEventSelect</span></span>

<span data-ttu-id="aa0fe-619">事件識別碼 = 32</span><span class="sxs-lookup"><span data-stu-id="aa0fe-619">Event ID = 32</span></span>

<span data-ttu-id="aa0fe-620">層級 = 5 (詳細資訊) </span><span class="sxs-lookup"><span data-stu-id="aa0fe-620">Level = 5 (Verbose)</span></span>

<span data-ttu-id="aa0fe-621">當應用程式呼叫 [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) 函式時，會追蹤下列 Winsock 事件：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-621">The following Winsock events are traced when an application calls the [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) function:</span></span>

-   <span data-ttu-id="aa0fe-622">記錄在 [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) 函式中傳遞的事件遮罩。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-622">Log the event mask passed in the [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) function.</span></span>

<span data-ttu-id="aa0fe-623">[**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect)函式呼叫會記錄下列參數：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-623">The following parameters are logged for [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) function calls:</span></span>



| <span data-ttu-id="aa0fe-624">參數</span><span class="sxs-lookup"><span data-stu-id="aa0fe-624">Parameter</span></span>                                                                                                | <span data-ttu-id="aa0fe-625">Description</span><span class="sxs-lookup"><span data-stu-id="aa0fe-625">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa0fe-626"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程</span><span class="sxs-lookup"><span data-stu-id="aa0fe-626"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>         | <span data-ttu-id="aa0fe-627">進程的核心 EPROCESS 結構位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-627">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="aa0fe-628"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點</span><span class="sxs-lookup"><span data-stu-id="aa0fe-628"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>     | <span data-ttu-id="aa0fe-629">當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-629">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="aa0fe-630"><span id="EventMask"></span><span id="eventmask"></span><span id="EVENTMASK"></span>EventMask</span><span class="sxs-lookup"><span data-stu-id="aa0fe-630"><span id="EventMask"></span><span id="eventmask"></span><span id="EVENTMASK"></span>EventMask</span></span><br/> | <span data-ttu-id="aa0fe-631">事件遮罩的值。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-631">The value for the event mask.</span></span> <br/>                                              |



 

## <a name="dropped-datagram"></a><span data-ttu-id="aa0fe-632">丟棄的資料包</span><span class="sxs-lookup"><span data-stu-id="aa0fe-632">Dropped Datagram</span></span>

<span data-ttu-id="aa0fe-633">事件識別碼 = 33 (IPv4) ，事件識別碼 = 34 (IPv6) </span><span class="sxs-lookup"><span data-stu-id="aa0fe-633">Event ID = 33 (IPv4), Event ID = 34 (IPv6)</span></span>

<span data-ttu-id="aa0fe-634">層級 = 5 (詳細資訊) </span><span class="sxs-lookup"><span data-stu-id="aa0fe-634">Level = 5 (Verbose)</span></span>

<span data-ttu-id="aa0fe-635">為了協助診斷資料包應用程式周圍的問題，會追蹤下列 Winsock 事件：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-635">To help diagnose issues around datagram applications, the following Winsock events are traced:</span></span>

-   <span data-ttu-id="aa0fe-636">當資料包送出，而它被捨棄時，沒有足夠的緩衝區空間。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-636">When a datagram arrives and it is dropped do to insufficient buffer space.</span></span>
-   <span data-ttu-id="aa0fe-637">在連接的資料包中，如果資料從連接的目的地以外的來源進行。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-637">On a connected datagram, if data arrives from a source other than connected destination.</span></span>

<span data-ttu-id="aa0fe-638">已針對捨棄的資料包記錄下列參數：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-638">The following parameters are logged for dropped datagrams:</span></span>



| <span data-ttu-id="aa0fe-639">參數</span><span class="sxs-lookup"><span data-stu-id="aa0fe-639">Parameter</span></span>                                                                                                    | <span data-ttu-id="aa0fe-640">Description</span><span class="sxs-lookup"><span data-stu-id="aa0fe-640">Description</span></span>                                                                            |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa0fe-641"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程</span><span class="sxs-lookup"><span data-stu-id="aa0fe-641"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>             | <span data-ttu-id="aa0fe-642">進程的核心 EPROCESS 結構位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-642">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="aa0fe-643"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點</span><span class="sxs-lookup"><span data-stu-id="aa0fe-643"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>         | <span data-ttu-id="aa0fe-644">當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-644">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="aa0fe-645"><span id="PacketSize"></span><span id="packetsize"></span><span id="PACKETSIZE"></span>PacketSize</span><span class="sxs-lookup"><span data-stu-id="aa0fe-645"><span id="PacketSize"></span><span id="packetsize"></span><span id="PACKETSIZE"></span>PacketSize</span></span><br/> | <span data-ttu-id="aa0fe-646">丟棄的封包大小。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-646">The size of the packet that was dropped.</span></span> <br/>                                   |
| <span data-ttu-id="aa0fe-647"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>位址</span><span class="sxs-lookup"><span data-stu-id="aa0fe-647"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>             | <span data-ttu-id="aa0fe-648">封包來源的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-648">The IP address of the source of the packet.</span></span> <br/>                                |
| <span data-ttu-id="aa0fe-649"><span id="Port"></span><span id="port"></span><span id="PORT"></span>港口</span><span class="sxs-lookup"><span data-stu-id="aa0fe-649"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                         | <span data-ttu-id="aa0fe-650">封包來源的 IP 埠號碼。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-650">The IP port number of the source of the packet.</span></span><br/>                             |
| <span data-ttu-id="aa0fe-651"><span id="Reason"></span><span id="reason"></span><span id="REASON"></span>原因</span><span class="sxs-lookup"><span data-stu-id="aa0fe-651"><span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Reason</span></span><br/>                 | <span data-ttu-id="aa0fe-652">丟棄封包的錯誤碼或原因。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-652">The error code or reason the packet was dropped.</span></span><br/>                            |



 

## <a name="connection-indicated"></a><span data-ttu-id="aa0fe-653">指出的連接</span><span class="sxs-lookup"><span data-stu-id="aa0fe-653">Connection Indicated</span></span>

<span data-ttu-id="aa0fe-654">事件識別碼 = 35 (IPv4) ，事件識別碼 = 36 (IPv6) </span><span class="sxs-lookup"><span data-stu-id="aa0fe-654">Event ID = 35 (IPv4), Event ID = 36 (IPv6)</span></span>

<span data-ttu-id="aa0fe-655">層級 = 5 (詳細資訊) </span><span class="sxs-lookup"><span data-stu-id="aa0fe-655">Level = 5 (Verbose)</span></span>

<span data-ttu-id="aa0fe-656">針對連接指出的作業，會追蹤下列 Winsock 事件：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-656">The following Winsock events are traced for connection indicated operations:</span></span>

-   <span data-ttu-id="aa0fe-657">應用程式會收到連接要求。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-657">An application receives a connection request.</span></span>

<span data-ttu-id="aa0fe-658">系統會針對從傳輸事件指出的連接記錄下列參數：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-658">The following parameters are logged for connections indicated from transport events:</span></span>



| <span data-ttu-id="aa0fe-659">參數</span><span class="sxs-lookup"><span data-stu-id="aa0fe-659">Parameter</span></span>                                                                                            | <span data-ttu-id="aa0fe-660">Description</span><span class="sxs-lookup"><span data-stu-id="aa0fe-660">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa0fe-661"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程</span><span class="sxs-lookup"><span data-stu-id="aa0fe-661"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="aa0fe-662">進程的核心 EPROCESS 結構位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-662">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="aa0fe-663"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點</span><span class="sxs-lookup"><span data-stu-id="aa0fe-663"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="aa0fe-664">當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-664">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="aa0fe-665"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>位址</span><span class="sxs-lookup"><span data-stu-id="aa0fe-665"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>     | <span data-ttu-id="aa0fe-666">遠端 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-666">The remote IP address.</span></span> <br/>                                                     |
| <span data-ttu-id="aa0fe-667"><span id="Port"></span><span id="port"></span><span id="PORT"></span>港口</span><span class="sxs-lookup"><span data-stu-id="aa0fe-667"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                 | <span data-ttu-id="aa0fe-668">遠端 IP 埠號碼。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-668">The remote IP port number.</span></span><br/>                                                  |



 

## <a name="data-indicated"></a><span data-ttu-id="aa0fe-669">指出的資料</span><span class="sxs-lookup"><span data-stu-id="aa0fe-669">Data Indicated</span></span>

<span data-ttu-id="aa0fe-670">事件識別碼 = 37</span><span class="sxs-lookup"><span data-stu-id="aa0fe-670">Event ID = 37</span></span>

<span data-ttu-id="aa0fe-671">層級 = 5 (詳細資訊) </span><span class="sxs-lookup"><span data-stu-id="aa0fe-671">Level = 5 (Verbose)</span></span>

<span data-ttu-id="aa0fe-672">針對資料指出的作業，會追蹤下列 Winsock 事件：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-672">The following Winsock events are traced for data indicated operations:</span></span>

-   <span data-ttu-id="aa0fe-673">應用程式會接收連接的通訊端上的資料。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-673">An application receives data on a connected socket.</span></span>

<span data-ttu-id="aa0fe-674">系統會針對從傳輸事件指出的資料記錄下列參數：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-674">The following parameters are logged for data indicated from transport events:</span></span>



| <span data-ttu-id="aa0fe-675">參數</span><span class="sxs-lookup"><span data-stu-id="aa0fe-675">Parameter</span></span>                                                                                                                        | <span data-ttu-id="aa0fe-676">Description</span><span class="sxs-lookup"><span data-stu-id="aa0fe-676">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa0fe-677"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程</span><span class="sxs-lookup"><span data-stu-id="aa0fe-677"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                                 | <span data-ttu-id="aa0fe-678">擁有的處理序識別碼。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-678">The owning process ID.</span></span><br/>                                                      |
| <span data-ttu-id="aa0fe-679"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點</span><span class="sxs-lookup"><span data-stu-id="aa0fe-679"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                             | <span data-ttu-id="aa0fe-680">當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-680">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="aa0fe-681"><span id="Bytes_Indicated"></span><span id="bytes_indicated"></span><span id="BYTES_INDICATED"></span>指出的位元組</span><span class="sxs-lookup"><span data-stu-id="aa0fe-681"><span id="Bytes_Indicated"></span><span id="bytes_indicated"></span><span id="BYTES_INDICATED"></span>Bytes Indicated</span></span><br/> | <span data-ttu-id="aa0fe-682">在通訊端上收到的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-682">The number of bytes received on the socket.</span></span><br/>                                 |



 

## <a name="data-indicated-from-transport"></a><span data-ttu-id="aa0fe-683">從傳輸指出的資料</span><span class="sxs-lookup"><span data-stu-id="aa0fe-683">Data Indicated from Transport</span></span>

<span data-ttu-id="aa0fe-684">事件識別碼 = 38 (IPv4) ，事件識別碼 = 39 (IPv6) </span><span class="sxs-lookup"><span data-stu-id="aa0fe-684">Event ID = 38 (IPv4), Event ID = 39 (IPv6)</span></span>

<span data-ttu-id="aa0fe-685">層級 = 5 (詳細資訊) </span><span class="sxs-lookup"><span data-stu-id="aa0fe-685">Level = 5 (Verbose)</span></span>

<span data-ttu-id="aa0fe-686">針對傳輸作業所指出的資料，會追蹤下列 Winsock 事件：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-686">The following Winsock events are traced for data indicated from transport operations:</span></span>

-   <span data-ttu-id="aa0fe-687">應用程式會張貼接收要求並接收資料。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-687">An application posts a receive request and receives data.</span></span>

<span data-ttu-id="aa0fe-688">系統會針對從傳輸事件指出的資料記錄下列參數：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-688">The following parameters are logged for data indicated from transport events:</span></span>



| <span data-ttu-id="aa0fe-689">參數</span><span class="sxs-lookup"><span data-stu-id="aa0fe-689">Parameter</span></span>                                                                                                                        | <span data-ttu-id="aa0fe-690">Description</span><span class="sxs-lookup"><span data-stu-id="aa0fe-690">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa0fe-691"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程</span><span class="sxs-lookup"><span data-stu-id="aa0fe-691"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                                 | <span data-ttu-id="aa0fe-692">進程的核心 EPROCESS 結構位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-692">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="aa0fe-693"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點</span><span class="sxs-lookup"><span data-stu-id="aa0fe-693"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                             | <span data-ttu-id="aa0fe-694">當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-694">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="aa0fe-695"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>位址</span><span class="sxs-lookup"><span data-stu-id="aa0fe-695"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>                                 | <span data-ttu-id="aa0fe-696">遠端 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-696">The remote IP address.</span></span> <br/>                                                     |
| <span data-ttu-id="aa0fe-697"><span id="Port"></span><span id="port"></span><span id="PORT"></span>港口</span><span class="sxs-lookup"><span data-stu-id="aa0fe-697"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                                             | <span data-ttu-id="aa0fe-698">遠端 IP 埠號碼。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-698">The remote IP port number.</span></span><br/>                                                  |
| <span data-ttu-id="aa0fe-699"><span id="Bytes_Indicated"></span><span id="bytes_indicated"></span><span id="BYTES_INDICATED"></span>指出的位元組</span><span class="sxs-lookup"><span data-stu-id="aa0fe-699"><span id="Bytes_Indicated"></span><span id="bytes_indicated"></span><span id="BYTES_INDICATED"></span>Bytes Indicated</span></span><br/> | <span data-ttu-id="aa0fe-700">在通訊端上收到的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-700">The number of bytes received on the socket.</span></span><br/>                                 |



 

## <a name="disconnect-indicated-from-transport"></a><span data-ttu-id="aa0fe-701">從傳輸指出中斷連線</span><span class="sxs-lookup"><span data-stu-id="aa0fe-701">Disconnect Indicated from Transport</span></span>

<span data-ttu-id="aa0fe-702">事件識別碼 = 41</span><span class="sxs-lookup"><span data-stu-id="aa0fe-702">Event ID = 41</span></span>

<span data-ttu-id="aa0fe-703">層級 = 5 (詳細資訊) </span><span class="sxs-lookup"><span data-stu-id="aa0fe-703">Level = 5 (Verbose)</span></span>

<span data-ttu-id="aa0fe-704">針對中斷連接指出的作業，會追蹤下列 Winsock 事件：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-704">The following Winsock events are traced for disconnect indicated operations:</span></span>

-   <span data-ttu-id="aa0fe-705">應用程式會收到中斷連接指示。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-705">An application receives a disconnect indication.</span></span>

<span data-ttu-id="aa0fe-706">從傳輸事件指出的中斷連接會記錄下列參數：</span><span class="sxs-lookup"><span data-stu-id="aa0fe-706">The following parameters are logged for disconnect indicated from transport events:</span></span>



| <span data-ttu-id="aa0fe-707">參數</span><span class="sxs-lookup"><span data-stu-id="aa0fe-707">Parameter</span></span>                                                                                            | <span data-ttu-id="aa0fe-708">Description</span><span class="sxs-lookup"><span data-stu-id="aa0fe-708">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa0fe-709"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程</span><span class="sxs-lookup"><span data-stu-id="aa0fe-709"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="aa0fe-710">進程的核心 EPROCESS 結構位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-710">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="aa0fe-711"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點</span><span class="sxs-lookup"><span data-stu-id="aa0fe-711"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="aa0fe-712">當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。</span><span class="sxs-lookup"><span data-stu-id="aa0fe-712">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="aa0fe-713">相關主題</span><span class="sxs-lookup"><span data-stu-id="aa0fe-713">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa0fe-714">Winsock 追蹤的控制權</span><span class="sxs-lookup"><span data-stu-id="aa0fe-714">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="aa0fe-715">Winsock 追蹤</span><span class="sxs-lookup"><span data-stu-id="aa0fe-715">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="aa0fe-716">Winsock 目錄變更追蹤詳細資料</span><span class="sxs-lookup"><span data-stu-id="aa0fe-716">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> <dt>

[<span data-ttu-id="aa0fe-717">Winsock 追蹤層級</span><span class="sxs-lookup"><span data-stu-id="aa0fe-717">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> </dl>

 

 
