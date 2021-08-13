---
title: 註冊攔截函式
description: 用戶端應用程式會在 WinEventProc 回呼函數中接收 WinEvents。 回呼函式所執行的動作是由應用程式定義，但語法必須如原型中所指定。
ms.assetid: 7e999335-6a41-4d22-82ef-1a8dd6cb656e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c444d2ee291cb07386e775a649ba0c3d42486c45b70e4d3f4629b9b67274f89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118564648"
---
# <a name="registering-a-hook-function"></a>註冊攔截函式

用戶端應用程式會在 [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) 回呼函數中接收 WinEvents。 回呼函式所執行的動作是由應用程式定義，但語法必須如原型中所指定。

函式必須先透過呼叫 [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook)來註冊，才能接收事件。 用戶端可以多次呼叫 **SetWinEventHook** 來註冊不同的攔截函式，或為先前註冊的攔截函式設定其他事件。

呼叫 [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) 時，用戶端會指定要接收的事件以及接收它們的方式。 用戶端可以選擇：

-   接收所有事件或一組特定的事件。
-   從所有線程或從特定執行緒接收事件。
-   從所有進程或特定進程接收事件。
-   處理進程中或進程外的事件。

當產生的事件符合指定的準則時，系統會呼叫用戶端的 [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) 回呼函數 (或「攔截程式」 ) 。 攔截函式接收的參數會告訴用戶端有關視窗、物件，以及產生事件的可能子項目。 用戶端會在物件抓取呼叫中使用這些參數，例如 [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)。

 

 




