---
description: 如何建立基本 IP 協助程式應用程式。
ms.assetid: b53f1cf5-3659-407e-8279-5c94333f3017
title: 建立基本 IP 協助程式應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baae961f8ffb6aa899e96fd05f0cb9f0c41469ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321083"
---
# <a name="creating-a-basic-ip-helper-application"></a><span data-ttu-id="b050d-103">建立基本 IP 協助程式應用程式</span><span class="sxs-lookup"><span data-stu-id="b050d-103">Creating a Basic IP Helper Application</span></span>

<span data-ttu-id="b050d-104">**建立基本 IP 協助程式應用程式**</span><span class="sxs-lookup"><span data-stu-id="b050d-104">**To create a basic IP Helper application**</span></span>

1.  <span data-ttu-id="b050d-105">建立新的空白專案。</span><span class="sxs-lookup"><span data-stu-id="b050d-105">Create a new empty project.</span></span>
2.  <span data-ttu-id="b050d-106">將空的 c + + 原始程式檔加入至專案。</span><span class="sxs-lookup"><span data-stu-id="b050d-106">Add an empty C++ source file to the project.</span></span>
3.  <span data-ttu-id="b050d-107">請確定組建環境參考平臺軟體發展工具組 (SDK) 的 Include、Lib 和 Src 目錄。</span><span class="sxs-lookup"><span data-stu-id="b050d-107">Ensure that the build environment refers to the Include, Lib, and Src directories of the Platform Software Development Kit (SDK).</span></span>
4.  <span data-ttu-id="b050d-108">確定組建環境會連結至 IP 協助程式程式庫檔案 Iphlpapi .lib 和 Winsock 程式庫檔案 WS2 \_ 32..。</span><span class="sxs-lookup"><span data-stu-id="b050d-108">Ensure that the build environment links to the IP Helper Library file Iphlpapi.lib and the Winsock Library file WS2\_32.lib.</span></span>
    > [!Note]  
    > <span data-ttu-id="b050d-109">某些基本的 Winsock 函數是用來傳回 IP 位址值和其他資訊。</span><span class="sxs-lookup"><span data-stu-id="b050d-109">Some basic Winsock functions are used to return IP address values and other information.</span></span>

     

5.  <span data-ttu-id="b050d-110">開始程式設計 IP 協助程式應用程式。</span><span class="sxs-lookup"><span data-stu-id="b050d-110">Begin programming the IP Helper application.</span></span> <span data-ttu-id="b050d-111">藉由包含 IP Helper 標頭檔來使用 IP 協助程式 API。</span><span class="sxs-lookup"><span data-stu-id="b050d-111">Use the IP Helper API by including the IP Helper header file.</span></span>

    ```C++
    #include <winsock2.h>
    #include <iphlpapi.h>
    #include <stdio.h>

    int main() {
      return 0;
    }
    
    ```

    

    > [!Note]
    >
    > <span data-ttu-id="b050d-112">使用 IP Helper 函式的應用程式需要 *Iphlpapi .h* 標頭檔。</span><span class="sxs-lookup"><span data-stu-id="b050d-112">The *Iphlpapi.h* header file is required for applications that use the IP Helper functions.</span></span> <span data-ttu-id="b050d-113">*Iphlpapi .h* 標頭檔會自動包含其他標頭檔案，其中包含了 IP Helper 函式所使用的結構和列舉。</span><span class="sxs-lookup"><span data-stu-id="b050d-113">The *Iphlpapi.h* header file automatically includes other headers files with structures and enumerations used by the IP Helper functions.</span></span>
    >
    > <span data-ttu-id="b050d-114">在 Windows Vista 和更新版本中引進的新 IP 協助程式函式會定義在 *Netioapi .h* 標頭檔中，該檔案會自動包含在 *Iphlpapi .h* 標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="b050d-114">The new IP Helper functions introduced in Windows Vista and later are defined in the *Netioapi.h* header file which is automatically included by the *Iphlpapi.h* header file.</span></span> <span data-ttu-id="b050d-115">不應直接使用 *Netioapi* 標頭檔。</span><span class="sxs-lookup"><span data-stu-id="b050d-115">The *Netioapi.h* header file should never be used directly.</span></span>
    >
    > <span data-ttu-id="b050d-116">IP Helper 函式所使用的許多結構和列舉都定義于 *Iprtrmib .h*、 *Ipexport .h* 和 *Iptypes .h* 標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="b050d-116">Many of the structures and enumerations used by IP Helper functions are defined in the *Iprtrmib.h*, *Ipexport.h*, and *Iptypes.h* header files.</span></span> <span data-ttu-id="b050d-117">這些標頭檔會自動包含在 *Iphlpapi .h* 標頭檔中，而且永遠不會直接使用。</span><span class="sxs-lookup"><span data-stu-id="b050d-117">These header files are automatically included in the *Iphlpapi.h* header file and should never be used directly.</span></span>
    >
    > <span data-ttu-id="b050d-118">在 Windows Vista 和更新版本的 Microsoft Windows 軟體開發套件 (SDK) 上，標頭檔的組織已經變更。</span><span class="sxs-lookup"><span data-stu-id="b050d-118">On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed.</span></span> <span data-ttu-id="b050d-119">部分結構現在定義于 *Ipmib .h*、 *Tcpmib .h* 和 *Udpmib .h* 標頭檔中，而不是 *Iprtrmib .h* 標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="b050d-119">Some of the structures are now defined in the *Ipmib.h*, *Tcpmib.h*, and *Udpmib.h* header files, not in the *Iprtrmib.h* header file.</span></span> <span data-ttu-id="b050d-120">*Ipmib .h* 標頭檔會自動包含 *Ifmib .h* 標頭檔。</span><span class="sxs-lookup"><span data-stu-id="b050d-120">The *Ipmib.h* header file automatically includes the *Ifmib.h* header file.</span></span> <span data-ttu-id="b050d-121">請注意，這些標頭檔會自動包含在 *Iprtrmib* 中，這會自動包含在 *Iphlpapi .h* 標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="b050d-121">Note that these header files are automatically included in *Iprtrmib.h*, which is automatically included in the *Iphlpapi.h* header file.</span></span>
    >
    > <span data-ttu-id="b050d-122">大部分使用 IP 協助程式 Api 的應用程式都需要 Windows 通訊端2.0 的 *Winsock2* 標頭檔。</span><span class="sxs-lookup"><span data-stu-id="b050d-122">The *Winsock2.h* header file for Windows Sockets 2.0 is required by most applications using the IP Helper APIs.</span></span> <span data-ttu-id="b050d-123">需要 *Winsock2. h* 標頭檔案時，應在 \# \# *Iphlpapi .h* 標頭檔的包含行之前放置此檔案的包含行。</span><span class="sxs-lookup"><span data-stu-id="b050d-123">When the *Winsock2.h* header file is required, the \#include line for this file should be placed before the \#include line for the *Iphlpapi.h* header file.</span></span>
    >
    > <span data-ttu-id="b050d-124">*Winsock2. h* 標頭檔內部包含來自 *Windows .h* 標頭檔的核心元素，因此 \# IP 協助程式應用程式中的 *Windows .h* 標頭檔通常不會有內含行。</span><span class="sxs-lookup"><span data-stu-id="b050d-124">The *Winsock2.h* header file internally includes core elements from the *Windows.h* header file, so there is not usually an \#include line for *Windows.h* header file in IP Helper applications.</span></span> <span data-ttu-id="b050d-125">如果 \# *Windows .h* 標頭檔需要包含行，則前面應該有 \# 定義 WIN32 的「精簡」和「MEAN」 \_ \_ \_ 宏。</span><span class="sxs-lookup"><span data-stu-id="b050d-125">If an \#include line is needed for the *Windows.h* header file, this should be preceded with the \#define WIN32\_LEAN\_AND\_MEAN macro.</span></span> <span data-ttu-id="b050d-126">基於歷史原因， *windows .h* 標頭預設為包含 Windows 通訊端1.1 的 *Winsock* 標頭檔。</span><span class="sxs-lookup"><span data-stu-id="b050d-126">For historical reasons, the *Windows.h* header defaults to including the *Winsock.h* header file for Windows Sockets 1.1.</span></span> <span data-ttu-id="b050d-127">Windows 通訊端1.1 的 *Winsock* 標頭檔中的宣告會與 Windows 通訊端2.0 所需的 *Winsock2* 標頭檔中的宣告相衝突。</span><span class="sxs-lookup"><span data-stu-id="b050d-127">The declarations in the *Winsock.h* header file for Windows Sockets 1.1 will conflict with the declarations in the *Winsock2.h* header file required by Windows Sockets 2.0.</span></span> <span data-ttu-id="b050d-128">WIN32 的「 \_ 精簡」和「MEAN」 \_ \_ 宏可防止 *Windows .H* 標頭檔包含 *Winsock* 標頭檔。</span><span class="sxs-lookup"><span data-stu-id="b050d-128">The WIN32\_LEAN\_AND\_MEAN macro prevents the *Winsock.h* header file from being included by the *Windows.h* header file.</span></span> <span data-ttu-id="b050d-129">以下顯示說明這種情況的範例。</span><span class="sxs-lookup"><span data-stu-id="b050d-129">An example illustrating this is shown below.</span></span>

     

    ```C++
    #ifndef WIN32_LEAN_AND_MEAN
    #define WIN32_LEAN_AND_MEAN
    #endif

    #include <windows.h>

    #include <winsock2.h>
    #include <iphlpapi.h>
    #include <stdio.h>

    int main() {
      return 0;
    }
    
    ```

    

    > [!Note]
    >
    > <span data-ttu-id="b050d-130">這個基本 IP 協助程式應用程式只會使用一些 IP 位址資料結構和 IP 位址，從 Windows 通訊端2.0 進行字串轉換函式。</span><span class="sxs-lookup"><span data-stu-id="b050d-130">This basic IP Helper application only uses some IP address data structures and IP address to string conversion functions from Windows Sockets 2.0.</span></span> <span data-ttu-id="b050d-131">使用這些資源完成時，可以使用這些 Windows 通訊端函式，而不需要呼叫 [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) 來初始化 Windows 通訊端資源和 [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) 。</span><span class="sxs-lookup"><span data-stu-id="b050d-131">These Windows Sockets functions can be used without calling [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) to initialize Windows Sockets resources and [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) when done using these resources.</span></span>
    >
    > <span data-ttu-id="b050d-132">在使用非這些 IP 位址的其他 Winsock 函數到字串函式的 IP 協助程式中，必須先呼叫 [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) 函式來初始化 Windows 通訊端資源，然後再呼叫任何 Windows 通訊端函式，並在應用程式使用 Windows 通訊端資源完成時呼叫 [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) 。</span><span class="sxs-lookup"><span data-stu-id="b050d-132">In IP Helper applications that use other Winsock functions other than these IP address to string functions, the [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) function must be called to initialize Windows Sockets resources before calling any Windows Sockets functions and [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) should be called when the application is done using Windows Sockets resources.</span></span>

     

    > [!Note]
    >
    > <span data-ttu-id="b050d-133">在此基本 IP 協助程式應用程式中使用各種標準 C 函式時，需要 *stdio.h .h* 標頭檔。</span><span class="sxs-lookup"><span data-stu-id="b050d-133">The *Stdio.h* header file is required for the use of various standard C functions in this basic IP Helper application.</span></span>

     

    <span data-ttu-id="b050d-134">下一步： [使用 GetNetworkParams 來抓取資訊](retrieving-information-using-getnetworkparams.md)</span><span class="sxs-lookup"><span data-stu-id="b050d-134">Next Step: [Retrieving Information Using GetNetworkParams](retrieving-information-using-getnetworkparams.md)</span></span>

 

 
