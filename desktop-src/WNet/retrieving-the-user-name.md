---
title: 正在抓取使用者名稱
description: 若要使用連線到網路資源的本機裝置或網路的名稱來抓取相關聯的使用者名稱，應用程式可以呼叫 WNetGetUser 函數。
ms.assetid: aed410af-d5f0-4389-882b-5b4338b5f900
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d0aeb8df11187828be0865d6b73e08325f2e0e7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104186044"
---
# <a name="retrieving-the-user-name"></a><span data-ttu-id="09a9e-103">正在抓取使用者名稱</span><span class="sxs-lookup"><span data-stu-id="09a9e-103">Retrieving the User Name</span></span>

<span data-ttu-id="09a9e-104">若要使用連線到網路資源的本機裝置或網路的名稱來抓取相關聯的使用者名稱，應用程式可以呼叫 [**WNetGetUser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera) 函數。</span><span class="sxs-lookup"><span data-stu-id="09a9e-104">To retrieve the name of the user associated either with a local device connected to a network resource or with the name of a network, an application can call the [**WNetGetUser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera) function.</span></span>

<span data-ttu-id="09a9e-105">下列範例會使用裝置名稱來取得使用者的名稱。</span><span class="sxs-lookup"><span data-stu-id="09a9e-105">The following example uses the device name to retrieve the name of the user.</span></span> <span data-ttu-id="09a9e-106">此範例會呼叫應用程式定義的錯誤處理常式來處理錯誤，以及使用 [**TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) 函式來進行列印。</span><span class="sxs-lookup"><span data-stu-id="09a9e-106">The sample calls an application-defined error handler to process errors, and the [**TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) function for printing.</span></span>


```C++
CHAR szUserName[80]; 
DWORD dwResult, cchBuff = 80; 
 
// Call the WNetGetUser function.
//
dwResult = WNetGetUser("z:", 
    (LPSTR) szUserName, 
    &cchBuff); 
 
// If the call succeeds, print the user name.
//
if(dwResult == NO_ERROR) 
    printf("User name: %s\n", szUserName); 
 
// Handle the error.
//
else 
{ 
    printf("WNetGetUser failed.\n"); 
}
```



<span data-ttu-id="09a9e-107">如需使用應用程式定義錯誤處理常式的詳細資訊，請參閱抓取 [網路錯誤](retrieving-network-errors.md)。</span><span class="sxs-lookup"><span data-stu-id="09a9e-107">For more information about using an application-defined error handler, see [Retrieving Network Errors](retrieving-network-errors.md).</span></span>

 

 