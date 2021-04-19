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
# <a name="adding-a-network-connection"></a>新增網路連接

若要建立 [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) 結構所描述之網路資源的連線，應用程式可以呼叫 [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a)、 [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)或 [**WNetUseConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetuseconnectiona) 函式。 下列範例示範如何使用 **WNetAddConnection2** 函數。

此程式碼範例會呼叫 **WNetAddConnection2** 函式，指定系統應該使用資訊來更新使用者的設定檔，以建立「已記住」或持續性連接。 此範例會呼叫應用程式定義的錯誤處理常式來處理錯誤，以及使用 [**TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) 函式來進行列印。


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



[**WNetAddConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnectiona)函式支援與舊版 Windows 的工作組相容。 新的應用程式應該呼叫 [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) 函數或 [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a) 函數。

如需使用應用程式定義錯誤處理常式的詳細資訊，請參閱抓取 [網路錯誤](retrieving-network-errors.md)。

 

 