---
title: 使用連接對話方塊
description: WNetConnectionDialog 函式會建立一個對話方塊，讓使用者能夠流覽並聯機到網路資源。
ms.assetid: ef375004-e426-4dee-b318-b470721116fa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f69d0f32772e614d60598853af620ae3c6452f5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315682"
---
# <a name="using-the-connections-dialog-box"></a>使用連接對話方塊

[**WNetConnectionDialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog)函式會建立一個對話方塊，讓使用者能夠流覽並聯機到網路資源。 您也可以呼叫 [**WNetConnectionDialog1**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog1a) 函數來建立連接對話方塊。 **WNetConnectionDialog1** 需要 [**CONNECTDLGSTRUCT**](/windows/win32/api/winnetwk/ns-winnetwk-connectdlgstructa) 結構。

[**WNetDisconnectDialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetdisconnectdialog)函式會建立一個對話方塊，讓使用者可以與網路資源中斷連線。

下列程式碼範例示範如何呼叫 **WNetConnectionDialog** 函式，以建立會顯示磁片資源的對話方塊。 如果呼叫失敗，範例會呼叫應用程式定義的錯誤處理常式。


```C++
DWORD dwResult; 
//
// Call the WNetConnectionDialog function.
//
dwResult = WNetConnectionDialog(hwnd, RESOURCETYPE_DISK);
//
// Call an application-defined error handler 
//  to process errors.
//
if(dwResult != NO_ERROR) 
{
    NetErrorHandler(hwnd, dwResult, (LPSTR)"WNetConnectionDialog"); 
    return FALSE; 
}
```



如需使用應用程式定義錯誤處理常式的詳細資訊，請參閱抓取 [網路錯誤](retrieving-network-errors.md)。

 

 