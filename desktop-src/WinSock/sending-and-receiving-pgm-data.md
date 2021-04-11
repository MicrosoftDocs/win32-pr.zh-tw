---
description: 傳送和接收 PGM 資料類似于在任何通訊端上傳送或接收資料。 以下段落所述的 PGM 有一些特定考慮。
ms.assetid: 51b447ad-b6da-424b-91df-e5be9ce225a5
title: 傳送和接收 PGM 資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab73999c33c97c6ba528552af6d746d54fb605df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115052"
---
# <a name="sending-and-receiving-pgm-data"></a><span data-ttu-id="c3351-104">傳送和接收 PGM 資料</span><span class="sxs-lookup"><span data-stu-id="c3351-104">Sending and Receiving PGM Data</span></span>

<span data-ttu-id="c3351-105">傳送和接收 PGM 資料類似于在任何通訊端上傳送或接收資料。</span><span class="sxs-lookup"><span data-stu-id="c3351-105">Sending and receiving PGM data is similar to sending or receiving data on any socket.</span></span> <span data-ttu-id="c3351-106">以下段落所述的 PGM 有一些特定考慮。</span><span class="sxs-lookup"><span data-stu-id="c3351-106">There are considerations specific to PGM, outlined in the following paragraphs.</span></span>

## <a name="sending-pgm-data"></a><span data-ttu-id="c3351-107">傳送 PGM 資料</span><span class="sxs-lookup"><span data-stu-id="c3351-107">Sending PGM Data</span></span>

<span data-ttu-id="c3351-108">建立了 PGM 傳送者會話之後，會使用各種 Windows 通訊端傳送函數傳送資料： [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send)、 [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto)、 [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend)和 [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto)。</span><span class="sxs-lookup"><span data-stu-id="c3351-108">Once a PGM sender session is created, data is sent using the various Windows Sockets send functions: [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send), [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto), [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend), and [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto).</span></span> <span data-ttu-id="c3351-109">由於 Windows 通訊端控制碼是檔案系統控制碼，因此 [**WriteFile**](/windows/win32/api/fileapi/nf-fileapi-writefile) 和 CRT 函數之類的其他函式也可以傳輸資料。</span><span class="sxs-lookup"><span data-stu-id="c3351-109">Since Windows Sockets handles are file system handles, other functions such as [**WriteFile**](/windows/win32/api/fileapi/nf-fileapi-writefile) and CRT functions can also transmit data.</span></span> <span data-ttu-id="c3351-110">下列程式碼片段說明 PGM 傳送者作業：</span><span class="sxs-lookup"><span data-stu-id="c3351-110">The following code snippet illustrates a PGM sender operation:</span></span>


```C++
LONG        error;
    //:
error = send (s, pSendBuffer, SendLength, 0);
if (error == SOCKET_ERROR)
{
    fprintf (stderr, "send() failed: Error = %d\n",
             WSAGetLastError());
}
```



<span data-ttu-id="c3351-111">使用訊息模式 (SOCK \_ RDM) 時，傳送函式的每個呼叫都會產生離散訊息，有時不是理想的情況; 應用程式可能會想要傳送具有多個呼叫的 2 mb 訊息來 [**傳送**](/windows/desktop/api/Winsock2/nf-winsock2-send)。</span><span class="sxs-lookup"><span data-stu-id="c3351-111">When using message mode (SOCK\_RDM), each call to a send function results in a discrete message, which sometimes isn't desirable; an application may want to send a 2 megabyte message with multiple calls to [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send).</span></span> <span data-ttu-id="c3351-112">在這種情況下，傳送者可以設定 [RM \_ 設定 \_ 訊息 \_ 界限](socket-options.md) 通訊端選項，以指出接在的訊息大小。</span><span class="sxs-lookup"><span data-stu-id="c3351-112">In such circumstances, the sender can set the [RM\_SET\_MESSAGE\_BOUNDARY](socket-options.md) socket option to indicate the size of the message that followings.</span></span>

<span data-ttu-id="c3351-113">如果傳送視窗已滿，就不會接受來自應用程式的新傳送，直到視窗前進為止。</span><span class="sxs-lookup"><span data-stu-id="c3351-113">If the send window is full, a new send from the application is not accepted until window has been advanced.</span></span> <span data-ttu-id="c3351-114">嘗試在非封鎖通訊端上傳送會因為 WSAEWOULDBLOCK 而失敗;封鎖通訊端只會封鎖，直到視窗前進到要求的資料可以緩衝和傳送的點為止。</span><span class="sxs-lookup"><span data-stu-id="c3351-114">Attempting to send on a non-blocking socket fails with WSAEWOULDBLOCK; a blocking socket simply blocks until the window advances to the point where the requested data can be buffered and sent.</span></span> <span data-ttu-id="c3351-115">在重迭的 i/o 中，除非視窗前進到足以容納新的資料，否則作業不會完成。</span><span class="sxs-lookup"><span data-stu-id="c3351-115">In overlapped I/O, the operation does not complete until the window advances enough to accommodate the new data.</span></span>

## <a name="receiving-pgm-data"></a><span data-ttu-id="c3351-116">接收 PGM 資料</span><span class="sxs-lookup"><span data-stu-id="c3351-116">Receiving PGM Data</span></span>

<span data-ttu-id="c3351-117">建立了 PGM 接收器會話 [**之後，會**](/windows/desktop/api/winsock/nf-winsock-recv)使用各種 Windows 通訊端接收函式來接收資料： receive、 [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom)、 [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)和 [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom)。</span><span class="sxs-lookup"><span data-stu-id="c3351-117">Once a PGM receiver session is created, data is received using the various Windows Sockets receive functions: [**recv**](/windows/desktop/api/winsock/nf-winsock-recv), [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), and [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom).</span></span> <span data-ttu-id="c3351-118">由於 Windows 通訊端控制碼也是檔案控制代碼，因此 [**ReadFile**](/windows/win32/api/fileapi/nf-fileapi-readfile) 和 CRT 函數也可以用來接收 PGM 會話資料。</span><span class="sxs-lookup"><span data-stu-id="c3351-118">Since Windows Sockets handles are also file handles, the [**ReadFile**](/windows/win32/api/fileapi/nf-fileapi-readfile) and CRT functions can also be used to receive PGM session data.</span></span> <span data-ttu-id="c3351-119">只要資料是依序，傳輸就會將資料轉送至接收者。</span><span class="sxs-lookup"><span data-stu-id="c3351-119">The transport forwards data up to the receiver as it arrives as long as the data is in sequence.</span></span> <span data-ttu-id="c3351-120">傳輸可保證傳回的資料是連續的，而且沒有重複的資料。</span><span class="sxs-lookup"><span data-stu-id="c3351-120">The transport guarantees that the data returned is contiguous and free of duplicates.</span></span> <span data-ttu-id="c3351-121">下列程式碼片段說明 PGM 接收作業：</span><span class="sxs-lookup"><span data-stu-id="c3351-121">The following code snippet illustrates a PGM receive operation:</span></span>


```C++
LONG        BytesRead;
    //:
BytesRead = recv (sockR, pTestBuffer, MaxBufferSize, 0);
if (BytesRead == 0)
{
    fprintf(stdout, "Session was terminated\n");
}
else if (BytesRead == SOCKET_ERROR)
{
    fprintf(stderr, "recv() failed: Error = %d\n",
            WSAGetLastError());
}
```



<span data-ttu-id="c3351-122">使用訊息模式 (SOCK \_ RDM) 時，傳輸會指出收到部分訊息時（不論是 WSAEMSGSIZE 錯誤），或在 \_ 從 [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) 和 [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) 函式傳回時設定 message 部分旗標。</span><span class="sxs-lookup"><span data-stu-id="c3351-122">When using message mode (SOCK\_RDM), the transport indicates when a partial message is received, either with the WSAEMSGSIZE error, or by setting the MSG\_PARTIAL flag upon return from the [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) and [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) functions.</span></span> <span data-ttu-id="c3351-123">當完整訊息的最後一個片段傳回給用戶端時，不會指出錯誤或旗標。</span><span class="sxs-lookup"><span data-stu-id="c3351-123">When the last fragment of the full message is returned to the client, the error or flag is not indicated.</span></span>

<span data-ttu-id="c3351-124">當會話正常結束時，接收作業會失敗並出現 WSAEDISCON。</span><span class="sxs-lookup"><span data-stu-id="c3351-124">When the session is terminated gracefully, the receive operation fails with WSAEDISCON.</span></span> <span data-ttu-id="c3351-125">當傳輸中發生資料遺失時，PGM 會暫時緩衝出超出順序的封包，並嘗試復原遺失的資料。</span><span class="sxs-lookup"><span data-stu-id="c3351-125">When data loss occurs in the transport, PGM temporarily buffers the out-of-sequence packets and attempts to recover the lost data.</span></span> <span data-ttu-id="c3351-126">如果資料遺失無法復原，則接收作業會失敗並出現 WSAECONNRESET，且會話會終止。</span><span class="sxs-lookup"><span data-stu-id="c3351-126">If the data-loss is unrecoverable, the receive operation fail with WSAECONNRESET, and the session is terminated.</span></span> <span data-ttu-id="c3351-127">您可以根據各種條件重設會話，包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="c3351-127">The session can be reset due to a variety of conditions, including the following:</span></span>

-   <span data-ttu-id="c3351-128">接收器或傳入的連線速度太慢，無法跟上連入資料速率的步調。</span><span class="sxs-lookup"><span data-stu-id="c3351-128">The receiver or the incoming connection rate is too slow to keep pace with the incoming data rate.</span></span>
-   <span data-ttu-id="c3351-129">發生過多資料遺失，可能是因為暫時性的網路狀況，例如路由問題、網路不穩定等等。</span><span class="sxs-lookup"><span data-stu-id="c3351-129">Excessive data loss occurs, possibly due to transient network conditions, such as routing problems, network instability, and so forth.</span></span>
-   <span data-ttu-id="c3351-130">傳送者上發生無法復原的錯誤。</span><span class="sxs-lookup"><span data-stu-id="c3351-130">An unrecoverable error occurs on the sender.</span></span>
-   <span data-ttu-id="c3351-131">在本機電腦上發生過度的資源使用率，例如超過允許的內部緩衝區儲存空間上限，或遇到資源不足的狀況。</span><span class="sxs-lookup"><span data-stu-id="c3351-131">Excessive resource utilization occurs on the local computer, such as exceeding the maximum allowed internal buffer storage, or encountering an out-of-resources condition.</span></span>
-   <span data-ttu-id="c3351-132">發生資料一致性檢查錯誤。</span><span class="sxs-lookup"><span data-stu-id="c3351-132">A data consistency check error occurs.</span></span>
-   <span data-ttu-id="c3351-133">元件的 PGM 失敗取決於 TCP/IP 或 Windows 通訊端。</span><span class="sxs-lookup"><span data-stu-id="c3351-133">Failure in a component PGM depends on, such as TCP/IP or Windows Sockets.</span></span>

<span data-ttu-id="c3351-134">上述清單中的第一個和第二個專案，可能會導致接收者在資源耗盡之前或最後移至傳送者的視窗之外，執行過多的緩衝處理。</span><span class="sxs-lookup"><span data-stu-id="c3351-134">Both the first and second items in the above list could result in the receiver performing excessive buffering before running out of resources, or before ultimately moving beyond the sender's window.</span></span>

## <a name="terminating-a-pgm-session"></a><span data-ttu-id="c3351-135">終止 PGM 會話</span><span class="sxs-lookup"><span data-stu-id="c3351-135">Terminating A PGM Session</span></span>

<span data-ttu-id="c3351-136">PGM 傳送者或接收者可以藉由呼叫 [**導致 closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket)來停止傳送或接收資料。</span><span class="sxs-lookup"><span data-stu-id="c3351-136">The PGM sender or receiver can stop sending or receiving data by calling [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket).</span></span> <span data-ttu-id="c3351-137">接收者必須在接聽和接收通訊端上呼叫 **導致 closesocket** ，以防止控制碼流失。</span><span class="sxs-lookup"><span data-stu-id="c3351-137">The receiver must call **closesocket** on both the listening and receiving sockets to prevent handle leaks.</span></span> <span data-ttu-id="c3351-138">在呼叫 **導致 closesocket** 之前呼叫傳送者的 [**關機**](/windows/desktop/api/winsock/nf-winsock-shutdown)可確保傳送所有資料，並確保在傳送視窗前進超過最後一個資料序列之前，保留修復資料，即使應用程式本身終止也是如此。</span><span class="sxs-lookup"><span data-stu-id="c3351-138">Calling [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) on the sender before calling **closesocket** ensures all data gets sent, and ensures repair data is maintained until the send window advances past the last data sequence, even if the application itself terminates.</span></span>

 

 
