---
title: 取消網路連接
description: 若要取消與網路資源的連接，應用程式可以呼叫 WNetCancelConnection2 函式，如下列範例所示。
ms.assetid: a1c80222-4986-4c51-86a5-a1caacb4b2fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22cc5fb9536a5d073a6c99d8b49a00e3c2771546
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842579"
---
# <a name="canceling-a-network-connection"></a><span data-ttu-id="25717-103">取消網路連接</span><span class="sxs-lookup"><span data-stu-id="25717-103">Canceling a Network Connection</span></span>

<span data-ttu-id="25717-104">若要取消與網路資源的連接，應用程式可以呼叫 [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a) 函式，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="25717-104">To cancel a connection to a network resource, an application can call the [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a) function, as shown in the following example.</span></span>

<span data-ttu-id="25717-105">對 **WNetCancelConnection2** 的呼叫指定網路連接應該不再是持續性。</span><span class="sxs-lookup"><span data-stu-id="25717-105">The call to **WNetCancelConnection2** specifies that a network connection should no longer be persistent.</span></span> <span data-ttu-id="25717-106">此範例會呼叫應用程式定義的錯誤處理常式來處理錯誤，以及使用 [**TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) 函式來進行列印。</span><span class="sxs-lookup"><span data-stu-id="25717-106">The sample calls an application-defined error handler to process errors, and the [**TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) function for printing.</span></span>


```C++
DWORD dwResult; 
 
// Call the WNetCancelConnection2 function, specifying
//  that the connection should no longer be a persistent one.
//
dwResult = WNetCancelConnection2("z:", 
    CONNECT_UPDATE_PROFILE, // remove connection from profile 
    FALSE);                 // fail if open files or jobs 
 
// Process errors.
//  The device is not a local redirected device.
//
if (dwResult == ERROR_NOT_CONNECTED) 
{ 
    printf("Drive z: not connected.\n"); 
    return dwResult; 
} 
 
// Call an application-defined error handler.
//
else if(dwResult != NO_ERROR) 
{ 
    printf("WNetCancelConnection2 failed.\n"); 
    return dwResult; 
}
//
// Otherwise, report canceling the connection.
//
printf("Connection closed for z: drive.\n"); 
```



<span data-ttu-id="25717-107">[**WNetCancelConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnectiona)函式支援與舊版 Windows 的工作組相容。</span><span class="sxs-lookup"><span data-stu-id="25717-107">The [**WNetCancelConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) function is supported for compatibility with earlier versions of Windows for Workgroups.</span></span> <span data-ttu-id="25717-108">若為新的應用程式，請使用 [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a)。</span><span class="sxs-lookup"><span data-stu-id="25717-108">For new applications, use [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a).</span></span>

<span data-ttu-id="25717-109">如需使用應用程式定義錯誤處理常式的詳細資訊，請參閱抓取 [網路錯誤](retrieving-network-errors.md)。</span><span class="sxs-lookup"><span data-stu-id="25717-109">For more information about using an application-defined error handler, see [Retrieving Network Errors](retrieving-network-errors.md).</span></span>

 

 