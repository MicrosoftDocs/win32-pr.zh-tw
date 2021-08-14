---
title: SendMessage、PostMessage 和相關函數
description: 本節說明使用 SendMessage、PostMessage 和相關函式搭配觸控訊息來轉送訊息的考慮。
ms.assetid: 9fba2013-17a3-499c-80dc-627e89c0edaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1274327b53630058779bc3913ce4466394c4c4fa37ba78528d122b8d68e376e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118435296"
---
# <a name="sendmessage-postmessage-and-related-functions"></a>SendMessage、PostMessage 和相關函數

本節說明使用 [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage)、 [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea)和相關函式搭配觸控訊息來轉送訊息的考慮。

如果使用 [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage)、 [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea)或某些其他相關函式來轉送觸控訊息，則會關閉觸控輸入控點。 如果您已透過呼叫 [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo)來抓取觸控輸入控制碼所參考的資訊，則在您釋出記憶體之前，該資料會保持有效。

接收透過上述其中一種機制轉送之觸控訊息的應用程式，會擁有它在訊息 *LPARAM* 中收到的觸控輸入控點，並負責將其關閉。 如果您未在呼叫 [**CloseTouchInputHandle**](/windows/desktop/api/winuser/nf-winuser-closetouchinputhandle)的情況下關閉控制碼，請將訊息傳遞至 [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca)，或使用 [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage)、 [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea)或某些相關函數轉寄訊息，您將會發生記憶體流失。

> [!Note]  
> 觸控訊息受限於一般消費者介面許可權隔離 (在轉送時 UIPI) 規則。

 

## <a name="functions-related-to-sendmessage-and-postmessage"></a>與 SendMessage 和 PostMessage 相關的函數

下列函式可能會影響觸控輸入控點的狀態。

-   [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage)
-   [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea)
-   SendNotifyMessage
-   SendMessageCallback
-   SendMessageTimeout
-   PostThreadMessage

## <a name="related-topics"></a>相關主題

<dl> <dt>

[函數](mtfunctions.md)
</dt> <dt>

[DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca)
</dt> </dl>

 

 