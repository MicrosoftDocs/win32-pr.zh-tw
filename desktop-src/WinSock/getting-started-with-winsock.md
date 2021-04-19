---
description: 以下是開始使用 Windows 通訊端程式設計的逐步指南。
ms.assetid: 905cd5bc-44af-4d3f-841a-9e9a2700a785
title: 使用 Winsock 開始使用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43751663a637fafb2eec453a48c329ff8e4499f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972414"
---
# <a name="getting-started-with-winsock"></a><span data-ttu-id="47d6a-103">使用 Winsock 開始使用</span><span class="sxs-lookup"><span data-stu-id="47d6a-103">Getting Started with Winsock</span></span>

<span data-ttu-id="47d6a-104">以下是開始使用 Windows 通訊端程式設計的逐步指南。</span><span class="sxs-lookup"><span data-stu-id="47d6a-104">The following is a step-by-step guide to getting started with Windows Sockets programming.</span></span> <span data-ttu-id="47d6a-105">其設計目的是要讓您瞭解基本的 Winsock 函數和資料結構，以及它們如何一起運作。</span><span class="sxs-lookup"><span data-stu-id="47d6a-105">It is designed to provide an understanding of basic Winsock functions and data structures, and how they work together.</span></span>

<span data-ttu-id="47d6a-106">用於說明的用戶端和伺服器應用程式是非常基本的用戶端和伺服器。</span><span class="sxs-lookup"><span data-stu-id="47d6a-106">The client and server application that is used for illustration is a very basic client and server.</span></span> <span data-ttu-id="47d6a-107">Microsoft Windows 軟體開發套件 (SDK) 隨附的範例包含更先進的程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="47d6a-107">More advanced code examples are included in the samples included with the Microsoft Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="47d6a-108">用戶端和伺服器應用程式的前幾個步驟都相同。</span><span class="sxs-lookup"><span data-stu-id="47d6a-108">The first few steps are the same for both client and server applications.</span></span>

-   [<span data-ttu-id="47d6a-109">關於伺服器和用戶端</span><span class="sxs-lookup"><span data-stu-id="47d6a-109">About Servers and Clients</span></span>](about-clients-and-servers.md)
-   [<span data-ttu-id="47d6a-110">建立基本 Winsock 應用程式</span><span class="sxs-lookup"><span data-stu-id="47d6a-110">Creating a Basic Winsock Application</span></span>](creating-a-basic-winsock-application.md)
-   [<span data-ttu-id="47d6a-111">初始化 Winsock</span><span class="sxs-lookup"><span data-stu-id="47d6a-111">Initializing Winsock</span></span>](initializing-winsock.md)

<span data-ttu-id="47d6a-112">下列各節說明建立 Winsock 用戶端應用程式的其餘步驟。</span><span class="sxs-lookup"><span data-stu-id="47d6a-112">The following sections describe the remaining steps for creating a Winsock client application.</span></span>

-   [<span data-ttu-id="47d6a-113">建立用戶端的通訊端</span><span class="sxs-lookup"><span data-stu-id="47d6a-113">Creating a Socket for the Client</span></span>](creating-a-socket-for-the-client.md)
-   [<span data-ttu-id="47d6a-114">連接至通訊端</span><span class="sxs-lookup"><span data-stu-id="47d6a-114">Connecting to a Socket</span></span>](connecting-to-a-socket.md)
-   [<span data-ttu-id="47d6a-115">在用戶端上傳送和接收資料</span><span class="sxs-lookup"><span data-stu-id="47d6a-115">Sending and Receiving Data on the Client</span></span>](sending-and-receiving-data-on-the-client.md)
-   [<span data-ttu-id="47d6a-116">中斷用戶端連線</span><span class="sxs-lookup"><span data-stu-id="47d6a-116">Disconnecting the Client</span></span>](disconnecting-the-client.md)

<span data-ttu-id="47d6a-117">下列各節說明建立 Winsock 伺服器應用程式的其餘步驟。</span><span class="sxs-lookup"><span data-stu-id="47d6a-117">The following sections describe the remaining steps for creating a Winsock server application.</span></span>

-   [<span data-ttu-id="47d6a-118">建立伺服器的通訊端</span><span class="sxs-lookup"><span data-stu-id="47d6a-118">Creating a Socket for the Server</span></span>](creating-a-socket-for-the-server.md)
-   [<span data-ttu-id="47d6a-119">系結通訊端</span><span class="sxs-lookup"><span data-stu-id="47d6a-119">Binding a Socket</span></span>](binding-a-socket.md)
-   [<span data-ttu-id="47d6a-120">在通訊端上接聽</span><span class="sxs-lookup"><span data-stu-id="47d6a-120">Listening on a Socket</span></span>](listening-on-a-socket.md)
-   [<span data-ttu-id="47d6a-121">接受連接</span><span class="sxs-lookup"><span data-stu-id="47d6a-121">Accepting a Connection</span></span>](accepting-a-connection.md)
-   [<span data-ttu-id="47d6a-122">接收和傳送伺服器上的資料</span><span class="sxs-lookup"><span data-stu-id="47d6a-122">Receiving and Sending Data on the Server</span></span>](receiving-and-sending-data-on-the-server.md)
-   [<span data-ttu-id="47d6a-123">中斷伺服器的連線</span><span class="sxs-lookup"><span data-stu-id="47d6a-123">Disconnecting the Server</span></span>](disconnecting-the-server.md)

<span data-ttu-id="47d6a-124">這些基本範例的完整原始程式碼。</span><span class="sxs-lookup"><span data-stu-id="47d6a-124">The complete source code for these basic examples.</span></span>

-   [<span data-ttu-id="47d6a-125">執行 Winsock 用戶端和伺服器程式碼範例</span><span class="sxs-lookup"><span data-stu-id="47d6a-125">Running the Winsock Client and Server Code Sample</span></span>](finished-server-and-client-code.md)
-   [<span data-ttu-id="47d6a-126">完成 Winsock 用戶端程式代碼</span><span class="sxs-lookup"><span data-stu-id="47d6a-126">Complete Winsock Client Code</span></span>](complete-client-code.md)
-   [<span data-ttu-id="47d6a-127">完整的 Winsock 伺服器程式碼</span><span class="sxs-lookup"><span data-stu-id="47d6a-127">Complete Winsock Server Code</span></span>](complete-server-code.md)

## <a name="advanced-winsock-samples"></a><span data-ttu-id="47d6a-128">Advanced Winsock 範例</span><span class="sxs-lookup"><span data-stu-id="47d6a-128">Advanced Winsock Samples</span></span>

<span data-ttu-id="47d6a-129">Windows SDK 包含數個更先進的 Winsock 用戶端和伺服器範例。</span><span class="sxs-lookup"><span data-stu-id="47d6a-129">Several more advanced Winsock client and server samples are included with the Windows SDK.</span></span> <span data-ttu-id="47d6a-130">根據預設，Windows 7 的 Windows SDK 會在下列目錄中安裝 Winsock 範例原始程式碼：</span><span class="sxs-lookup"><span data-stu-id="47d6a-130">By default, the Winsock sample source code is installed in the following directory by the Windows SDK for Windows 7:</span></span>

<span data-ttu-id="47d6a-131">*C： \\ Program Files \\ Microsoft sdk \\ Windows \\ 7.0 \\ 範例 \\ NetDs \\ winsock*</span><span class="sxs-lookup"><span data-stu-id="47d6a-131">*C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\NetDs\\winsock*</span></span>

<span data-ttu-id="47d6a-132">在舊版的 Windows SDK 上，上述路徑中的版本號碼會變更。</span><span class="sxs-lookup"><span data-stu-id="47d6a-132">On earlier versions of the Windows SDK, the version number in the above path would change.</span></span> <span data-ttu-id="47d6a-133">例如，Windows Vista 的 Windows SDK 會在下列預設目錄中安裝 Winsock 範例原始程式碼。</span><span class="sxs-lookup"><span data-stu-id="47d6a-133">For example, the Winsock sample source code is installed in the following default directory by the Windows SDK for Windows Vista</span></span>

<span data-ttu-id="47d6a-134">*C： \\ Program Files \\ Microsoft sdk \\ Windows \\ v 6.0 \\ 範例 \\ NetDs \\ winsock*</span><span class="sxs-lookup"><span data-stu-id="47d6a-134">*C:\\Program Files\\Microsoft SDKs\\Windows\\v6.0\\Samples\\NetDs\\winsock*</span></span>

<span data-ttu-id="47d6a-135">以下是在下列目錄中，依序從較高到較低效能的順序列出的更先進範例：</span><span class="sxs-lookup"><span data-stu-id="47d6a-135">The more advanced samples listed below in order from higher to lower performance are found in the following directories:</span></span>

-   <span data-ttu-id="47d6a-136">Iocp</span><span class="sxs-lookup"><span data-stu-id="47d6a-136">iocp</span></span>

    <span data-ttu-id="47d6a-137">此目錄包含三個使用 i/o 完成埠的範例程式。</span><span class="sxs-lookup"><span data-stu-id="47d6a-137">This directory contains three sample programs that use I/O completion ports.</span></span> <span data-ttu-id="47d6a-138">這些套裝程式括使用 [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) 函數的 winsock 伺服器 (iocpserver) 、使用 [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) 函式的 winsock 伺服器 (iocpserverex) ，以及用來測試其中一種伺服器的簡單多執行緒 Winsock 用戶端 (iocpclient) 。</span><span class="sxs-lookup"><span data-stu-id="47d6a-138">The programs include a Winsock server (iocpserver) that uses the [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) function, a Winsock server (iocpserverex) that uses the [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) function, and a simple multithreaded Winsock client (iocpclient) used to test either of these servers.</span></span> <span data-ttu-id="47d6a-139">伺服器程式支援透過 TCP/IP 連接的多個用戶端，並傳送伺服器接著回顯至用戶端的任意大小資料緩衝區。</span><span class="sxs-lookup"><span data-stu-id="47d6a-139">The server programs support multiple clients connecting via TCP/IP and sending arbitrary sized data buffers which the server then echoes back to the client.</span></span> <span data-ttu-id="47d6a-140">為了方便起見，我們開發了簡單的用戶端程式 iocpclient，並持續將資料傳送到伺服器，以使用多個執行緒來壓力。</span><span class="sxs-lookup"><span data-stu-id="47d6a-140">For convenience, a simple client program, iocpclient, was developed to connect and continually send data to the server to stress it using multiple threads.</span></span> <span data-ttu-id="47d6a-141">使用 i/o 完成埠的 Winsock 伺服器可提供最大的效能功能。</span><span class="sxs-lookup"><span data-stu-id="47d6a-141">Winsock servers that use I/O completion ports provide the most performance capability.</span></span>

-   <span data-ttu-id="47d6a-142">重疊</span><span class="sxs-lookup"><span data-stu-id="47d6a-142">overlap</span></span>

    <span data-ttu-id="47d6a-143">此目錄包含使用重迭 i/o 的範例伺服器程式。</span><span class="sxs-lookup"><span data-stu-id="47d6a-143">This directory contains a sample server program that uses overlapped I/O.</span></span> <span data-ttu-id="47d6a-144">範例程式會使用 [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) 函式和重迭 i/o 來有效處理來自用戶端的多個非同步連接要求。</span><span class="sxs-lookup"><span data-stu-id="47d6a-144">The sample program uses the [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) function and overlapped I/O to handle multiple asynchronous connection requests from clients effectively.</span></span> <span data-ttu-id="47d6a-145">伺服器使用 **AcceptEx** 函式，在單一執行緒 Win32 應用程式中多工不同的用戶端連接。</span><span class="sxs-lookup"><span data-stu-id="47d6a-145">The server uses the **AcceptEx** function to multiplex different client connections in a single-threaded Win32 application.</span></span> <span data-ttu-id="47d6a-146">使用重迭的 i/o 可提供更大的擴充性。</span><span class="sxs-lookup"><span data-stu-id="47d6a-146">Using overlapped I/O allows for greater scalability.</span></span>

-   <span data-ttu-id="47d6a-147">WSAPoll</span><span class="sxs-lookup"><span data-stu-id="47d6a-147">WSAPoll</span></span>

    <span data-ttu-id="47d6a-148">此目錄包含基本的範例程式，示範如何使用 [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) 函數。</span><span class="sxs-lookup"><span data-stu-id="47d6a-148">This directory contains a basic sample program that demonstrates the use of the [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) function.</span></span> <span data-ttu-id="47d6a-149">結合的用戶端和伺服器程式為非封鎖，並且使用 **WSAPoll** 函式來判斷何時可能傳送或接收，而不會封鎖。</span><span class="sxs-lookup"><span data-stu-id="47d6a-149">The combined client and server program are non-blocking and use the **WSAPoll** function to determine when it is possible to send or receive without blocking.</span></span> <span data-ttu-id="47d6a-150">此範例較適用于說明，而不是高效能伺服器。</span><span class="sxs-lookup"><span data-stu-id="47d6a-150">This sample is more for illustration and is not a high-performance server.</span></span>

-   <span data-ttu-id="47d6a-151">simple</span><span class="sxs-lookup"><span data-stu-id="47d6a-151">simple</span></span>

    <span data-ttu-id="47d6a-152">此目錄包含三個基本的範例程式，示範伺服器如何使用多個執行緒。</span><span class="sxs-lookup"><span data-stu-id="47d6a-152">This directory contains three basic sample programs that demonstrate the use of multiple threads by a server.</span></span> <span data-ttu-id="47d6a-153">這些套裝程式括簡單的 TCP/UDP 伺服器 (simples) ，這是一種僅限 TCP 的伺服器 (simples \_ ioctl) ，它會使用 Win32 主控台應用程式中的 [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) 函式來支援多個用戶端要求，而用戶端 TCP/udp 程式 (simplec) 用於測試伺服器。</span><span class="sxs-lookup"><span data-stu-id="47d6a-153">The programs include a simple TCP/UDP server (simples), a TCP-only server (simples\_ioctl) that uses the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) function in a Win32 console application to support multiple client requests, and a client TCP/UDP program (simplec) for testing the servers.</span></span> <span data-ttu-id="47d6a-154">伺服器示範如何使用多個執行緒來處理多個用戶端要求。</span><span class="sxs-lookup"><span data-stu-id="47d6a-154">The servers demonstrates the use of multiple threads to handle multiple client requests.</span></span> <span data-ttu-id="47d6a-155">因為為每個用戶端要求建立個別的執行緒，所以這個方法有擴充性問題。</span><span class="sxs-lookup"><span data-stu-id="47d6a-155">This method has scalability issues since a separate thread is created for each client request.</span></span>

-   <span data-ttu-id="47d6a-156">accept</span><span class="sxs-lookup"><span data-stu-id="47d6a-156">accept</span></span>

    <span data-ttu-id="47d6a-157">此目錄包含基本的範例伺服器和用戶端程式。</span><span class="sxs-lookup"><span data-stu-id="47d6a-157">This directory contains a basic sample server and client program.</span></span> <span data-ttu-id="47d6a-158">伺服器示範如何使用 [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) 函式或使用 [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) 函式的非同步接受，來使用非封鎖接受。</span><span class="sxs-lookup"><span data-stu-id="47d6a-158">The server demonstrates the use of either non-blocking accept using the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) function or asynchronous accept using the [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) function.</span></span> <span data-ttu-id="47d6a-159">此範例較適用于說明，而不是高效能伺服器。</span><span class="sxs-lookup"><span data-stu-id="47d6a-159">This sample is more for illustration and is not a high-performance server.</span></span>

 

 
