---
title: 正在抓取網路資源的相關資訊
description: 若要識別擁有資源的網路提供者，應用程式可以呼叫 WNetGetResourceInformation 函式，如下列程式碼範例所示。
ms.assetid: 4bddb55c-181d-4c6f-bd92-9c27d6b894bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf21e48be540f5307fc1ebd2359aea7ff03cbe0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092927"
---
# <a name="retrieving-information-about-a-network-resource"></a><span data-ttu-id="cda3b-103">正在抓取網路資源的相關資訊</span><span class="sxs-lookup"><span data-stu-id="cda3b-103">Retrieving Information About a Network Resource</span></span>

<span data-ttu-id="cda3b-104">若要識別擁有資源的網路提供者，應用程式可以呼叫 [**WNetGetResourceInformation**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetresourceinformationa) 函式，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="cda3b-104">To identify the network provider that owns a resource, an application can call the [**WNetGetResourceInformation**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetresourceinformationa) function, as illustrated in the following code sample.</span></span>

<span data-ttu-id="cda3b-105">下列範例是 (CheckServer) 的函式，它會使用伺服器名稱做為參數，並傳回該伺服器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cda3b-105">The following sample is a function (CheckServer) that takes a server name as a parameter and returns information about that server.</span></span> <span data-ttu-id="cda3b-106">首先，函式會呼叫 [**ZeroMemory**](/previous-versions/windows/desktop/legacy/aa366920(v=vs.85)) 函數，將記憶體區塊的內容初始化為零。</span><span class="sxs-lookup"><span data-stu-id="cda3b-106">First the function calls the [**ZeroMemory**](/previous-versions/windows/desktop/legacy/aa366920(v=vs.85)) function to initialize the contents of a block of memory to zero.</span></span> <span data-ttu-id="cda3b-107">然後，此範例會呼叫 [**WNetGetResourceInformation**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetresourceinformationa) 函式，並指定夠大的緩衝區以容納 [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) 結構。</span><span class="sxs-lookup"><span data-stu-id="cda3b-107">Then the sample calls the [**WNetGetResourceInformation**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetresourceinformationa) function, specifying a buffer large enough to hold only a [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) structure.</span></span> <span data-ttu-id="cda3b-108">當這個大小的緩衝區不足以容納 **NETRESOURCE** 結構點成員的可變長度字串時，此常式會包含處理案例的錯誤處理。</span><span class="sxs-lookup"><span data-stu-id="cda3b-108">The routine includes error processing to handle the case when a buffer of this size is insufficient to hold the variable-length strings to which members of the **NETRESOURCE** structure point.</span></span> <span data-ttu-id="cda3b-109">如果發生這個錯誤，範例會配置足夠的記憶體，然後再次呼叫 **WNetGetResourceInformation** 。</span><span class="sxs-lookup"><span data-stu-id="cda3b-109">If this error occurs, the sample allocates sufficient memory and calls **WNetGetResourceInformation** again.</span></span> <span data-ttu-id="cda3b-110">最後，此範例會釋出配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="cda3b-110">Finally, the sample frees the allocated memory.</span></span>

<span data-ttu-id="cda3b-111">請注意，此範例假設 *pszServer* 參數指向本機電腦上的其中一個網路提供者可辨識的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="cda3b-111">Note that the sample assumes that the *pszServer* parameter points to a server name that one of the network providers on the local computer recognizes.</span></span>


```C++
#include <Windows.h>
#include <Winnetwk.h >

// Need to link with Mpr.lib
#pragma comment(lib, "Mpr.lib")
//
// Verify a server on the network. 
//
DWORD
CheckServer( LPTSTR pszServer )
{  
    DWORD dwBufferSize = sizeof(NETRESOURCE);
    LPBYTE lpBuffer;                  // buffer
    NETRESOURCE nr;
    LPTSTR pszSystem = NULL;          // variable-length strings

    //
    // Set the block of memory to zero; then initialize
    // the NETRESOURCE structure. 
    //
    ZeroMemory(&nr, sizeof(nr));

    nr.dwScope       = RESOURCE_GLOBALNET;
    nr.dwType        = RESOURCETYPE_ANY;
    nr.lpRemoteName  = pszServer;

    //
    // First call the WNetGetResourceInformation function with 
    // memory allocated to hold only a NETRESOURCE structure. This 
    // method can succeed if all the NETRESOURCE pointers are NULL.
    // If the call fails because the buffer is too small, allocate
    // a larger buffer.
    //
    lpBuffer = (LPBYTE) malloc( dwBufferSize );
    if (lpBuffer == NULL) 
        return FALSE;

    while ( WNetGetResourceInformation(&nr, lpBuffer, &dwBufferSize, 
                &pszSystem) == ERROR_MORE_DATA)
    {
        lpBuffer = (LPBYTE) realloc(lpBuffer, dwBufferSize);
    }

    // Process the contents of the NETRESOURCE structure and the
    // variable-length strings in lpBuffer and set dwValue. When
    // finished, free the memory.

    free(lpBuffer);

    return TRUE;
}
```



 

 