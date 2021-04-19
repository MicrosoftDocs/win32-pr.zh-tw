---
title: 新增網路連接
description: 若要建立 NETRESOURCE 結構所描述之網路資源的連線，應用程式可以呼叫 WNetAddConnection2、WNetAddConnection3 或 WNetUseConnection 函式。
ms.assetid: 0dab9eed-9019-4075-833b-324e5caee257
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 476e03193b919f17a2060e415db5e7ea60c8364e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106966261"
---
# <a name="adding-a-network-connection"></a><span data-ttu-id="59a05-103">新增網路連接</span><span class="sxs-lookup"><span data-stu-id="59a05-103">Adding a Network Connection</span></span>

<span data-ttu-id="59a05-104">若要建立 [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) 結構所描述之網路資源的連線，應用程式可以呼叫 [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a)、 [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)或 [**WNetUseConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetuseconnectiona) 函式。</span><span class="sxs-lookup"><span data-stu-id="59a05-104">To make a connection to a network resource described by a [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) structure, an application can call the [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a), the [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a), or the [**WNetUseConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetuseconnectiona) function.</span></span> <span data-ttu-id="59a05-105">下列範例示範如何使用 **WNetAddConnection2** 函數。</span><span class="sxs-lookup"><span data-stu-id="59a05-105">The following example demonstrates use of the **WNetAddConnection2** function.</span></span>

<span data-ttu-id="59a05-106">此程式碼範例會呼叫 **WNetAddConnection2** 函式，指定系統應該使用資訊來更新使用者的設定檔，以建立「已記住」或持續性連接。</span><span class="sxs-lookup"><span data-stu-id="59a05-106">The code sample calls the **WNetAddConnection2** function, specifying that the system should update the user's profile with the information, creating a "remembered" or persistent connection.</span></span> <span data-ttu-id="59a05-107">此範例會呼叫應用程式定義的錯誤處理常式來處理錯誤，以及使用 [**TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) 函式來進行列印。</span><span class="sxs-lookup"><span data-stu-id="59a05-107">The sample calls an application-defined error handler to process errors, and the [**TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) function for printing.</span></span>


```C++
DWORD dwResult; 
NETRESOURCE nr; 
//
// Call the WNetAddConnection2 function to make the connection,
//   specifying a persistent connection.
//
dwResult = WNetAddConnection2(&nr, // NETRESOURCE from enumeration 
    (LPSTR) NULL,                  // no password 
    (LPSTR) NULL,                  // logged-in user 
    CONNECT_UPDATE_PROFILE);       // update profile with connect information 
 
// Process errors.
//  The local device is already connected to a network resource.
//
if (dwResult == ERROR_ALREADY_ASSIGNED) 
{ 
    printf("Already connected to specified resource.\n"); 
    return dwResult; 
} 
 
//  An entry for the local device already exists in the user profile.
//
else if (dwResult == ERROR_DEVICE_ALREADY_REMEMBERED) 
{ 
    printf("Attempted reassignment of remembered device.\n"); 
    return dwResult; 
} 
else if(dwResult != NO_ERROR) 
{ 
    //
    // Call an application-defined error handler.
    //
    printf("WNetAddConnection2 failed.\n"); 
    return dwResult; 
} 
 
//
// Otherwise, report a successful connection.
//
printf("Connected to the specified resource.\n"); 
```



<span data-ttu-id="59a05-108">[**WNetAddConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnectiona)函式支援與舊版 Windows 的工作組相容。</span><span class="sxs-lookup"><span data-stu-id="59a05-108">The [**WNetAddConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnectiona) function is supported for compatibility with earlier versions of Windows for Workgroups.</span></span> <span data-ttu-id="59a05-109">新的應用程式應該呼叫 [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) 函數或 [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a) 函數。</span><span class="sxs-lookup"><span data-stu-id="59a05-109">New applications should call the [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) function or the [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a) function.</span></span>

<span data-ttu-id="59a05-110">如需使用應用程式定義錯誤處理常式的詳細資訊，請參閱抓取 [網路錯誤](retrieving-network-errors.md)。</span><span class="sxs-lookup"><span data-stu-id="59a05-110">For more information about using an application-defined error handler, see [Retrieving Network Errors](retrieving-network-errors.md).</span></span>

 

 