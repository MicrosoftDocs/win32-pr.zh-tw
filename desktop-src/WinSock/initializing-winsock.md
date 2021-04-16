---
description: 呼叫 Winsock 函式 (應用程式或 Dll) 的所有進程都必須先初始化 Windows 通訊端 DLL 的使用，再進行其他 Winsock 函式呼叫。 這也可確保系統支援 Winsock。
ms.assetid: 300858d8-bed3-4a3c-abb5-2cecd100e5d7
title: 初始化 Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d3d02805c684c677c4358cf79c421d6a577f64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511433"
---
# <a name="initializing-winsock"></a><span data-ttu-id="82aaa-104">初始化 Winsock</span><span class="sxs-lookup"><span data-stu-id="82aaa-104">Initializing Winsock</span></span>

<span data-ttu-id="82aaa-105">呼叫 Winsock 函式 (應用程式或 Dll) 的所有進程都必須先初始化 Windows 通訊端 DLL 的使用，再進行其他 Winsock 函式呼叫。</span><span class="sxs-lookup"><span data-stu-id="82aaa-105">All processes (applications or DLLs) that call Winsock functions must initialize the use of the Windows Sockets DLL before making other Winsock functions calls.</span></span> <span data-ttu-id="82aaa-106">這也可確保系統支援 Winsock。</span><span class="sxs-lookup"><span data-stu-id="82aaa-106">This also makes certain that Winsock is supported on the system.</span></span>

<span data-ttu-id="82aaa-107">**初始化 Winsock**</span><span class="sxs-lookup"><span data-stu-id="82aaa-107">**To initialize Winsock**</span></span>

1.  <span data-ttu-id="82aaa-108">建立名為 wsaData 的 [**WSADATA**](/windows/desktop/api/winsock/ns-winsock-wsadata) 物件。</span><span class="sxs-lookup"><span data-stu-id="82aaa-108">Create a [**WSADATA**](/windows/desktop/api/winsock/ns-winsock-wsadata) object called wsaData.</span></span>
    ```C++
    WSADATA wsaData;
    ```

    

2.  <span data-ttu-id="82aaa-109">呼叫 [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) 並以整數形式傳回其值，並檢查是否有錯誤。</span><span class="sxs-lookup"><span data-stu-id="82aaa-109">Call [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) and return its value as an integer and check for errors.</span></span>
    ```C++
    int iResult;

    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2,2), &wsaData);
    if (iResult != 0) {
        printf("WSAStartup failed: %d\n", iResult);
        return 1;
    }
    ```

    

<span data-ttu-id="82aaa-110">呼叫 [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) 函數，以起始使用 WS2 \_32.dll。</span><span class="sxs-lookup"><span data-stu-id="82aaa-110">The [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) function is called to initiate use of WS2\_32.dll.</span></span>

<span data-ttu-id="82aaa-111">[**WSADATA**](/windows/desktop/api/winsock/ns-winsock-wsadata)結構包含 Windows 通訊端執行的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="82aaa-111">The [**WSADATA**](/windows/desktop/api/winsock/ns-winsock-wsadata) structure contains information about the Windows Sockets implementation.</span></span> <span data-ttu-id="82aaa-112">[**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup)的 MAKEWORD (2，2) 參數會在系統上提出2.2 版 Winsock 的要求，並將傳遞的版本設定為呼叫端可以使用的最高 Windows 通訊端支援版本。</span><span class="sxs-lookup"><span data-stu-id="82aaa-112">The MAKEWORD(2,2) parameter of [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) makes a request for version 2.2 of Winsock on the system, and sets the passed version as the highest version of Windows Sockets support that the caller can use.</span></span>

<span data-ttu-id="82aaa-113">用戶端的下一個步驟：為 [用戶端建立通訊端](creating-a-socket-for-the-client.md)</span><span class="sxs-lookup"><span data-stu-id="82aaa-113">Next Step for a Client: [Creating a Socket for the Client](creating-a-socket-for-the-client.md)</span></span>

<span data-ttu-id="82aaa-114">伺服器的下一個步驟： [建立伺服器的通訊端](creating-a-socket-for-the-server.md)</span><span class="sxs-lookup"><span data-stu-id="82aaa-114">Next Step for a Server: [Creating a Socket for the Server](creating-a-socket-for-the-server.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="82aaa-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="82aaa-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82aaa-116">使用 Winsock 開始使用</span><span class="sxs-lookup"><span data-stu-id="82aaa-116">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="82aaa-117">建立基本 Winsock 應用程式</span><span class="sxs-lookup"><span data-stu-id="82aaa-117">Creating a Basic Winsock Application</span></span>](creating-a-basic-winsock-application.md)
</dt> </dl>

 

 



