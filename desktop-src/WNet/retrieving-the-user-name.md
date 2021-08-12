---
title: 正在抓取使用者名稱
description: 若要使用連線到網路資源的本機裝置或網路的名稱來抓取相關聯的使用者名稱，應用程式可以呼叫 WNetGetUser 函數。
ms.assetid: aed410af-d5f0-4389-882b-5b4338b5f900
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98aeafc849e1a66b373fcb81af46ec47b49644c4b9c753fad480876180a5592a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118566476"
---
# <a name="retrieving-the-user-name"></a>正在抓取使用者名稱

若要使用連線到網路資源的本機裝置或網路的名稱來抓取相關聯的使用者名稱，應用程式可以呼叫 [**WNetGetUser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera) 函數。

下列範例會使用裝置名稱來取得使用者的名稱。 此範例會呼叫應用程式定義的錯誤處理常式來處理錯誤，以及使用 [**TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) 函式來進行列印。


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



如需使用應用程式定義錯誤處理常式的詳細資訊，請參閱抓取 [網路錯誤](retrieving-network-errors.md)。

 

 