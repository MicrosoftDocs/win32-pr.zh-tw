---
description: 如何建立基本的 Windows 通訊端 (Winsock) 應用程式。
ms.assetid: 56af2e95-ea82-49e4-b335-86dcf4c38780
title: 建立基本 Winsock 應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0d5b5695ddb3b329bb4f81da6149fcf740a4240
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113092"
---
# <a name="creating-a-basic-winsock-application"></a><span data-ttu-id="35505-103">建立基本 Winsock 應用程式</span><span class="sxs-lookup"><span data-stu-id="35505-103">Creating a Basic Winsock Application</span></span>

<span data-ttu-id="35505-104">**若要建立基本 Winsock 應用程式**</span><span class="sxs-lookup"><span data-stu-id="35505-104">**To create a basic Winsock application**</span></span>

1.  <span data-ttu-id="35505-105">建立新的空白專案。</span><span class="sxs-lookup"><span data-stu-id="35505-105">Create a new empty project.</span></span>
2.  <span data-ttu-id="35505-106">將空的 c + + 原始程式檔加入至專案。</span><span class="sxs-lookup"><span data-stu-id="35505-106">Add an empty C++ source file to the project.</span></span>
3.  <span data-ttu-id="35505-107">確定組建環境是指 Microsoft Windows 軟體開發套件 (SDK) 或舊版平臺軟體發展工具組 (SDK) 的包含、Lib 和 Src 目錄。</span><span class="sxs-lookup"><span data-stu-id="35505-107">Ensure that the build environment refers to the Include, Lib, and Src directories of the Microsoft Windows Software Development Kit (SDK) or the earlier Platform Software Development Kit (SDK).</span></span>
4.  <span data-ttu-id="35505-108">確定組建環境會連結到 Winsock 程式庫檔案 Ws2 \_ 32..。</span><span class="sxs-lookup"><span data-stu-id="35505-108">Ensure that the build environment links to the Winsock Library file Ws2\_32.lib.</span></span> <span data-ttu-id="35505-109">使用 Winsock 的應用程式必須與 Ws2 \_ 32 .lib 程式庫檔案連結。</span><span class="sxs-lookup"><span data-stu-id="35505-109">Applications that use Winsock must be linked with the Ws2\_32.lib library file.</span></span> <span data-ttu-id="35505-110">\#Pragma 批註指出需要 *Ws2 \_ 32 .lib* 檔案的連結器。</span><span class="sxs-lookup"><span data-stu-id="35505-110">The \#pragma comment indicates to the linker that the *Ws2\_32.lib* file is needed.</span></span>
5.  <span data-ttu-id="35505-111">開始程式設計 Winsock 應用程式。</span><span class="sxs-lookup"><span data-stu-id="35505-111">Begin programming the Winsock application.</span></span> <span data-ttu-id="35505-112">包含 Winsock 2 標頭檔，以使用 Winsock API。</span><span class="sxs-lookup"><span data-stu-id="35505-112">Use the Winsock API by including the Winsock 2 header files.</span></span> <span data-ttu-id="35505-113">*Winsock2* 標頭檔包含大部分的 Winsock 函數、結構和定義。</span><span class="sxs-lookup"><span data-stu-id="35505-113">The *Winsock2.h* header file contains most of the Winsock functions, structures, and definitions.</span></span> <span data-ttu-id="35505-114">*Ws2tcpip .h* 標頭檔包含 WinSock 2 Protocol-Specific 附錄檔中針對 tcp/ip 所引進的定義，其中包含用來抓取 IP 位址的較新函數和結構。</span><span class="sxs-lookup"><span data-stu-id="35505-114">The *Ws2tcpip.h* header file contains definitions introduced in the WinSock 2 Protocol-Specific Annex document for TCP/IP that includes newer functions and structures used to retrieve IP addresses.</span></span>
    > [!Note]  
    > <span data-ttu-id="35505-115">Stdio.h 會用於標準輸入和輸出，特別是 **printf ()** 函式。</span><span class="sxs-lookup"><span data-stu-id="35505-115">Stdio.h is used for standard input and output, specifically the **printf()** function.</span></span>

     


```C++
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>

#pragma comment(lib, "Ws2_32.lib")

int main() {
  return 0;
}

```



> [!Note]
>
> <span data-ttu-id="35505-116">如果應用程式使用 IP 協助程式 Api，則需要 *Iphlpapi .h* 標頭檔。</span><span class="sxs-lookup"><span data-stu-id="35505-116">The *Iphlpapi.h* header file is required if an application is using the IP Helper APIs.</span></span> <span data-ttu-id="35505-117">需要 *Iphlpapi .h* 標頭檔時，必須在 \#  \# *Iphlpapi .h* 標頭檔的包含行之前放置 Winsock2 標頭檔的 include 行。</span><span class="sxs-lookup"><span data-stu-id="35505-117">When the *Iphlpapi.h* header file is required, the \#include line for the *Winsock2.h* header file should be placed before the \#include line for the *Iphlpapi.h* header file.</span></span>
>
> <span data-ttu-id="35505-118">*Winsock2. h* 標頭檔內部包含來自 *Windows .h* 標頭檔的核心元素，因此 \# Winsock 應用程式中的 *Windows .h* 標頭檔通常不會有包含行。</span><span class="sxs-lookup"><span data-stu-id="35505-118">The *Winsock2.h* header file internally includes core elements from the *Windows.h* header file, so there is not usually an \#include line for the *Windows.h* header file in Winsock applications.</span></span> <span data-ttu-id="35505-119">如果 \# *Windows .h* 標頭檔需要包含行，則前面應該有 \# 定義 WIN32 的「精簡」和「MEAN」 \_ \_ \_ 宏。</span><span class="sxs-lookup"><span data-stu-id="35505-119">If an \#include line is needed for the *Windows.h* header file, this should be preceded with the \#define WIN32\_LEAN\_AND\_MEAN macro.</span></span> <span data-ttu-id="35505-120">基於歷史原因， *windows .h* 標頭預設為包含 Windows 通訊端1.1 的 *Winsock* 標頭檔。</span><span class="sxs-lookup"><span data-stu-id="35505-120">For historical reasons, the *Windows.h* header defaults to including the *Winsock.h* header file for Windows Sockets 1.1.</span></span> <span data-ttu-id="35505-121">*Winsock* 標頭檔中的宣告會與 Windows 通訊端2.0 所需的 *Winsock2* 標頭檔中的宣告相衝突。</span><span class="sxs-lookup"><span data-stu-id="35505-121">The declarations in the *Winsock.h* header file will conflict with the declarations in the *Winsock2.h* header file required by Windows Sockets 2.0.</span></span> <span data-ttu-id="35505-122">WIN32 的「 \_ 精簡」和「MEAN」 \_ \_ 宏可防止在 *Windows .h* 標頭中包含 *Winsock. h。*</span><span class="sxs-lookup"><span data-stu-id="35505-122">The WIN32\_LEAN\_AND\_MEAN macro prevents the *Winsock.h* from being included by the *Windows.h* header.</span></span> <span data-ttu-id="35505-123">以下顯示說明這種情況的範例。</span><span class="sxs-lookup"><span data-stu-id="35505-123">An example illustrating this is shown below.</span></span>

 


```C++
#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include <windows.h>
#include <winsock2.h>
#include <ws2tcpip.h>
#include <iphlpapi.h>
#include <stdio.h>

#pragma comment(lib, "Ws2_32.lib")

int main() {
  return 0;
}

```



<span data-ttu-id="35505-124">下一步： [初始化 Winsock](initializing-winsock.md)</span><span class="sxs-lookup"><span data-stu-id="35505-124">Next Step: [Initializing Winsock](initializing-winsock.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="35505-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="35505-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35505-126">使用 Winsock 開始使用</span><span class="sxs-lookup"><span data-stu-id="35505-126">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="35505-127">關於伺服器和用戶端</span><span class="sxs-lookup"><span data-stu-id="35505-127">About Servers and Clients</span></span>](about-clients-and-servers.md)
</dt> </dl>

 

 



