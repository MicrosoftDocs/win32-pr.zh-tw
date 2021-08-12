---
title: 取消網路連接
description: 若要取消與網路資源的連接，應用程式可以呼叫 WNetCancelConnection2 函式，如下列範例所示。
ms.assetid: a1c80222-4986-4c51-86a5-a1caacb4b2fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbb5c74faa1e1f8b75d0e3b604d89615c6ad1481384a661253ee204dd3ee6081
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118566918"
---
# <a name="canceling-a-network-connection"></a>取消網路連接

若要取消與網路資源的連接，應用程式可以呼叫 [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a) 函式，如下列範例所示。

對 **WNetCancelConnection2** 的呼叫指定網路連接應該不再是持續性。 此範例會呼叫應用程式定義的錯誤處理常式來處理錯誤，以及使用 [**TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) 函式來進行列印。


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



[**WNetCancelConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnectiona)函式支援與工作組的舊版 Windows 相容性。 若為新的應用程式，請使用 [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a)。

如需使用應用程式定義錯誤處理常式的詳細資訊，請參閱抓取 [網路錯誤](retrieving-network-errors.md)。

 

 