---
title: 藍牙和 connect
description: 藍牙使用 connect 函式連接到目標藍牙裝置，並使用先前建立的藍牙通訊端。
ms.assetid: f9ab3934-7698-4f5e-8194-cca86685a4f8
keywords:
- 藍牙藍牙
- 連接藍牙
- 藍牙並連接藍牙
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b631aabbcd44d009ba30b9deb486e92a22feaec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463617"
---
# <a name="bluetooth-and-connect"></a><span data-ttu-id="82015-106">藍牙和 connect</span><span class="sxs-lookup"><span data-stu-id="82015-106">Bluetooth and connect</span></span>

<span data-ttu-id="82015-107">藍牙使用 [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) 函式連接到目標藍牙裝置，並使用先前建立的藍牙通訊端。</span><span class="sxs-lookup"><span data-stu-id="82015-107">Bluetooth uses the [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) function to connect to a target Bluetooth device, using a previously created Bluetooth socket.</span></span> <span data-ttu-id="82015-108">**Connect** 函式的 *name* 參數，也就是 [**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)結構，必須指定目標藍牙裝置。</span><span class="sxs-lookup"><span data-stu-id="82015-108">The *name* parameter of the **connect** function, which is a [**SOCKADDR\_BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) structure, must specify a target Bluetooth device.</span></span> <span data-ttu-id="82015-109">使用兩種機制來識別目標裝置：</span><span class="sxs-lookup"><span data-stu-id="82015-109">Two mechanisms are used to identify the target device:</span></span>

-   <span data-ttu-id="82015-110">[**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)結構可以直接指定要求連接的埠號碼。</span><span class="sxs-lookup"><span data-stu-id="82015-110">The [**SOCKADDR\_BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) structure can directly specify the port number to which a connect is requested.</span></span> <span data-ttu-id="82015-111">這種機制要求應用程式在嘗試 [**連接**](/windows/desktop/api/winsock2/nf-winsock2-connect) 作業之前，先執行自己的 SDP 查詢。</span><span class="sxs-lookup"><span data-stu-id="82015-111">This mechanism requires the application to perform its own SDP queries prior to attempting a [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) operation.</span></span>
-   <span data-ttu-id="82015-112">[**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)結構可以指定要連接之服務的唯一服務類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="82015-112">The [**SOCKADDR\_BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) structure can specify the unique service class ID of the service to which it wants to connect.</span></span> <span data-ttu-id="82015-113">如果對等裝置有一個以上的埠對應至服務類別識別碼，則 [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) 函式呼叫會連接到第一個有效的服務。</span><span class="sxs-lookup"><span data-stu-id="82015-113">If the peer device has more than one port that corresponds to the service class ID, the [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) function call connects to the first valid service.</span></span> <span data-ttu-id="82015-114">在沒有先前的 SDP 查詢的情況下，可以使用此機制。</span><span class="sxs-lookup"><span data-stu-id="82015-114">This mechanism can be used without prior SDP queries.</span></span>

<span data-ttu-id="82015-115">搭配 [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect)函式使用 [**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)結構時，適用下列需求：</span><span class="sxs-lookup"><span data-stu-id="82015-115">When using the [**SOCKADDR\_BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) structure with the [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) function, the following requirements apply:</span></span>

-   <span data-ttu-id="82015-116">**BtAddr** 成員必須是有效的遠端無線電位址。</span><span class="sxs-lookup"><span data-stu-id="82015-116">The **btAddr** member must be a valid remote radio address.</span></span>
-   <span data-ttu-id="82015-117">針對 **serviceClassId** 成員，如果埠成員為零，系統會嘗試使用 **serviceClassId** 來解析對應至服務的遠端埠。</span><span class="sxs-lookup"><span data-stu-id="82015-117">For the **serviceClassId** member, if the port member is zero, the system attempts to use **serviceClassId** to resolve the remote port corresponding to the service.</span></span> <span data-ttu-id="82015-118">服務類別是由藍牙規格定義的正規化128位 GUID。</span><span class="sxs-lookup"><span data-stu-id="82015-118">The service class is a normalized 128-bit GUID, defined by the Bluetooth specification.</span></span> <span data-ttu-id="82015-119">一般 Guid 是由藍牙指派的數位檔所定義。</span><span class="sxs-lookup"><span data-stu-id="82015-119">Common GUIDs are defined by the Bluetooth Assigned Numbers document.</span></span> <span data-ttu-id="82015-120">或者，您也可以針對特定領域的應用程式使用唯一的 GUID。</span><span class="sxs-lookup"><span data-stu-id="82015-120">Alternatively, a unique GUID may be used for a domain-specific application.</span></span>
-   <span data-ttu-id="82015-121">**埠** 成員必須是有效的遠端埠，如果指定了 **serviceClassId** 成員，則為零。</span><span class="sxs-lookup"><span data-stu-id="82015-121">The **port** member must be a valid remote port, or zero if the **serviceClassId** member is specified.</span></span>

<span data-ttu-id="82015-122">下表列出藍牙和 [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) 功能的結果碼。</span><span class="sxs-lookup"><span data-stu-id="82015-122">The following table lists the result codes for Bluetooth and the [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) function.</span></span>

| <span data-ttu-id="82015-123">錯誤/錯誤\#</span><span class="sxs-lookup"><span data-stu-id="82015-123">Error/error\#</span></span>                    | <span data-ttu-id="82015-124">Description</span><span class="sxs-lookup"><span data-stu-id="82015-124">Description</span></span>                                                                        |
|----------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="82015-125">WSAEISCONN10056</span><span class="sxs-lookup"><span data-stu-id="82015-125">WSAEISCONN10056</span></span><br/>       | <span data-ttu-id="82015-126">針對已連接的通訊端呼叫的 [**連接**](/windows/desktop/api/winsock2/nf-winsock2-connect) 函數。</span><span class="sxs-lookup"><span data-stu-id="82015-126">The [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) function called for already connected socket.</span></span> |
| <span data-ttu-id="82015-127">WSAEACCES10013</span><span class="sxs-lookup"><span data-stu-id="82015-127">WSAEACCES10013</span></span><br/>        | <span data-ttu-id="82015-128">連接應用程式要求的驗證，但驗證失敗。</span><span class="sxs-lookup"><span data-stu-id="82015-128">Connecting application requested authentication, but authentication failed.</span></span>        |
| <span data-ttu-id="82015-129">WSAENOBUFS10055</span><span class="sxs-lookup"><span data-stu-id="82015-129">WSAENOBUFS10055</span></span><br/>       | <span data-ttu-id="82015-130">無法復原的記憶體不足錯誤。</span><span class="sxs-lookup"><span data-stu-id="82015-130">Unrecoverable out-of-memory error.</span></span>                                                 |
| <span data-ttu-id="82015-131">WSAEADDRINUSE10048</span><span class="sxs-lookup"><span data-stu-id="82015-131">WSAEADDRINUSE10048</span></span><br/>    | <span data-ttu-id="82015-132">要求的埠/頻道號碼正在使用中。</span><span class="sxs-lookup"><span data-stu-id="82015-132">The port/channel number requested is in use.</span></span>                                       |
| <span data-ttu-id="82015-133">WSAETIMEDOUT10060</span><span class="sxs-lookup"><span data-stu-id="82015-133">WSAETIMEDOUT10060</span></span><br/>     | <span data-ttu-id="82015-134">I/o 在藍牙無線電層級超時， (頁面 \_ 超時) 。</span><span class="sxs-lookup"><span data-stu-id="82015-134">The I/O timed out at the Bluetooth radio level (PAGE\_TIMEOUT).</span></span>                    |
| <span data-ttu-id="82015-135">WSAEDISCON10101</span><span class="sxs-lookup"><span data-stu-id="82015-135">WSAEDISCON10101</span></span><br/>       | <span data-ttu-id="82015-136">遠端對等互連的 RFCOMM 通道已中斷連線。</span><span class="sxs-lookup"><span data-stu-id="82015-136">The RFCOMM channel disconnected by remote peer.</span></span>                                    |
| <span data-ttu-id="82015-137">WSAECONNRESET10054</span><span class="sxs-lookup"><span data-stu-id="82015-137">WSAECONNRESET10054</span></span><br/>    | <span data-ttu-id="82015-138">RFCOMM 多重傳送器 (會話) 由遠端對等互連中斷連線。</span><span class="sxs-lookup"><span data-stu-id="82015-138">The RFCOMM multiplexor (session) disconnected by remote peer.</span></span>                      |
| <span data-ttu-id="82015-139">WSAECONNABORTED10053</span><span class="sxs-lookup"><span data-stu-id="82015-139">WSAECONNABORTED10053</span></span><br/>  | <span data-ttu-id="82015-140">應用程式關閉通訊端。</span><span class="sxs-lookup"><span data-stu-id="82015-140">Socket shut down by application.</span></span>                                                   |
| <span data-ttu-id="82015-141">WSAENETUNREACH10051</span><span class="sxs-lookup"><span data-stu-id="82015-141">WSAENETUNREACH10051</span></span><br/>   | <span data-ttu-id="82015-142">L2CAP 或 Bluetooth 無線電層級以外的錯誤。</span><span class="sxs-lookup"><span data-stu-id="82015-142">Error other than time-out at L2CAP or Bluetooth radio level.</span></span>                       |
| <span data-ttu-id="82015-143">WSAEHOSTDOWN10064</span><span class="sxs-lookup"><span data-stu-id="82015-143">WSAEHOSTDOWN10064</span></span><br/>     | <span data-ttu-id="82015-144">RFCOMM 收到 DM 回應。</span><span class="sxs-lookup"><span data-stu-id="82015-144">The RFCOMM received DM response.</span></span>                                                   |
| <span data-ttu-id="82015-145">WSAENETDOWN10050</span><span class="sxs-lookup"><span data-stu-id="82015-145">WSAENETDOWN10050</span></span><br/>      | <span data-ttu-id="82015-146">未預期的網路錯誤。</span><span class="sxs-lookup"><span data-stu-id="82015-146">Unexpected network error.</span></span>                                                          |
| <span data-ttu-id="82015-147">WSAESHUTDOWN10058</span><span class="sxs-lookup"><span data-stu-id="82015-147">WSAESHUTDOWN10058</span></span><br/>     | <span data-ttu-id="82015-148">遠端對等互連的 L2CAP 通道已中斷連線。</span><span class="sxs-lookup"><span data-stu-id="82015-148">The L2CAP channel disconnected by remote peer.</span></span>                                     |
| <span data-ttu-id="82015-149">WSAEADDRNOTAVAIL10049</span><span class="sxs-lookup"><span data-stu-id="82015-149">WSAEADDRNOTAVAIL10049</span></span><br/> | <span data-ttu-id="82015-150">藍牙埠/通道或裝置位址無效。</span><span class="sxs-lookup"><span data-stu-id="82015-150">Bluetooth port/channel or device address not valid.</span></span>                                |
| <span data-ttu-id="82015-151">WSAEINVAL10022</span><span class="sxs-lookup"><span data-stu-id="82015-151">WSAEINVAL10022</span></span><br/>        | <span data-ttu-id="82015-152">隨插即用、驅動程式堆疊事件或其他錯誤導致失敗。</span><span class="sxs-lookup"><span data-stu-id="82015-152">Plug and Play, driver-stack event, or other error caused failure.</span></span>                  |



 

## <a name="related-topics"></a><span data-ttu-id="82015-153">相關主題</span><span class="sxs-lookup"><span data-stu-id="82015-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82015-154">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="82015-154">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="82015-155">**連線**</span><span class="sxs-lookup"><span data-stu-id="82015-155">**connect**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[<span data-ttu-id="82015-156">**SOCKADDR \_ BTH**</span><span class="sxs-lookup"><span data-stu-id="82015-156">**SOCKADDR\_BTH**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> </dl>

 

