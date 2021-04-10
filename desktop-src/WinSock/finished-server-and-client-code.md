---
description: 執行完整的 TCP/IP 用戶端和伺服器應用程式範例程式碼。
ms.assetid: 617dfdf6-f7a7-4e72-8c77-8cfa3ab232e7
title: 執行 Winsock 用戶端和伺服器程式碼範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9b3588af6bac668f0b7c785bafe2f69de4ef2b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943425"
---
# <a name="running-the-winsock-client-and-server-code-sample"></a><span data-ttu-id="21eed-103">執行 Winsock 用戶端和伺服器程式碼範例</span><span class="sxs-lookup"><span data-stu-id="21eed-103">Running the Winsock Client and Server Code Sample</span></span>

<span data-ttu-id="21eed-104">本節包含 TCP/IP 用戶端和伺服器應用程式的完整原始碼：</span><span class="sxs-lookup"><span data-stu-id="21eed-104">This section contains the complete source code for the TCP/IP Client and Server applications:</span></span>

-   [<span data-ttu-id="21eed-105">完成 Winsock 用戶端程式代碼</span><span class="sxs-lookup"><span data-stu-id="21eed-105">Complete Winsock Client Code</span></span>](complete-client-code.md)
-   [<span data-ttu-id="21eed-106">完整的 Winsock 伺服器程式碼</span><span class="sxs-lookup"><span data-stu-id="21eed-106">Complete Winsock Server Code</span></span>](complete-server-code.md)

<span data-ttu-id="21eed-107">在啟動用戶端應用程式之前，應該先啟動伺服器應用程式。</span><span class="sxs-lookup"><span data-stu-id="21eed-107">The server application should be started before the client application is started.</span></span>

<span data-ttu-id="21eed-108">若要執行伺服器，請編譯完整的伺服器原始程式碼，然後執行可執行檔。</span><span class="sxs-lookup"><span data-stu-id="21eed-108">To execute the server, compile the complete server source code and run the executable file.</span></span> <span data-ttu-id="21eed-109">伺服器應用程式會接聽 TCP 通訊埠27015，讓用戶端連接。</span><span class="sxs-lookup"><span data-stu-id="21eed-109">The server application listens on TCP port 27015 for a client to connect.</span></span> <span data-ttu-id="21eed-110">一旦用戶端連線之後，伺服器會從用戶端接收資料，並 (傳送) 傳回給用戶端的資料。</span><span class="sxs-lookup"><span data-stu-id="21eed-110">Once a client connects, the server receives data from the client and echoes (sends) the data received back to the client.</span></span> <span data-ttu-id="21eed-111">當用戶端關閉連線時，伺服器會關閉用戶端通訊端、關閉通訊端並結束。</span><span class="sxs-lookup"><span data-stu-id="21eed-111">When the client shuts down the connection, the server shuts down the client socket, closes the socket, and exits.</span></span>

<span data-ttu-id="21eed-112">若要執行用戶端，請編譯完整的用戶端原始程式碼，然後執行可執行檔。</span><span class="sxs-lookup"><span data-stu-id="21eed-112">To execute the client, compile the complete client source code and run the executable file.</span></span> <span data-ttu-id="21eed-113">用戶端應用程式需要執行伺服器應用程式之電腦的電腦名稱稱或 IP 位址，在執行用戶端時，會以命令列參數的形式傳遞。</span><span class="sxs-lookup"><span data-stu-id="21eed-113">The client application requires that name of the computer or IP address of the computer where the server application is running is passed as a command-line parameter when the client is executed.</span></span> <span data-ttu-id="21eed-114">如果在範例電腦上執行用戶端和伺服器，用戶端就可以依照下列方式啟動：</span><span class="sxs-lookup"><span data-stu-id="21eed-114">If the client and server are executed on the sample computer, the client can be started as follows:</span></span>

<span data-ttu-id="21eed-115">**用戶端 localhost**</span><span class="sxs-lookup"><span data-stu-id="21eed-115">**client localhost**</span></span>

<span data-ttu-id="21eed-116">用戶端嘗試連接到 TCP 埠27015上的伺服器。</span><span class="sxs-lookup"><span data-stu-id="21eed-116">The client tries to connect to the server on TCP port 27015.</span></span> <span data-ttu-id="21eed-117">用戶端連接之後，用戶端會將資料傳送到伺服器，並接收從伺服器傳回的任何資料。</span><span class="sxs-lookup"><span data-stu-id="21eed-117">Once the client connects, the client sends data to the server and receives any data send back from the server.</span></span> <span data-ttu-id="21eed-118">用戶端接著會關閉通訊端並結束。</span><span class="sxs-lookup"><span data-stu-id="21eed-118">The client then closes the socket and exits.</span></span>

## <a name="related-topics"></a><span data-ttu-id="21eed-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="21eed-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21eed-120">使用 Winsock 開始使用</span><span class="sxs-lookup"><span data-stu-id="21eed-120">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> </dl>

 

 



