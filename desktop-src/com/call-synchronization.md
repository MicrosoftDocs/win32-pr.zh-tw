---
title: 呼叫同步處理
description: 呼叫同步處理
ms.assetid: e74407ef-f500-4d13-aef4-ca6bb37d5858
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9969c968294a3dfdbfbc4cb78d40e64ad65c17392bf3b9fd09fc7a5f99b9049b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048736"
---
# <a name="call-synchronization"></a>呼叫同步處理

COM 應用程式在處理來自 COM 或作業系統的一或多個呼叫時，必須能夠正確地處理使用者輸入。 COM 僅提供單一執行緒單元的呼叫同步處理。 多執行緒單元 (包含無限制執行緒的執行緒) 不會在) 的相同執行緒上進行 (呼叫時接收呼叫。 多執行緒單元無法進行輸入同步處理呼叫。 非同步呼叫會轉換成多執行緒單元中的同步呼叫。 不會針對多執行緒單元中的任何執行緒呼叫訊息篩選器。 如需執行緒問題的詳細資訊，請參閱 [進程、執行緒和單元](processes--threads--and-apartments.md)。

進程之間的 COM 呼叫分為三個類別，如下所示：

<dl> <dt>

<span id="Synchronous_calls"></span><span id="synchronous_calls"></span><span id="SYNCHRONOUS_CALLS"></span>*同步呼叫*
</dt> <dd>

大部分在 COM 中發生的通訊都是同步的。 進行同步呼叫時，呼叫端會先等候回復，再繼續進行，並可在等候時接收傳入訊息。 COM 進入強制回應迴圈，以控制的方式來等候回復、接收和分派其他訊息。

</dd> <dt>

<span id="Asynchronous_notifications"></span><span id="asynchronous_notifications"></span><span id="ASYNCHRONOUS_NOTIFICATIONS"></span>*非同步通知*
</dt> <dd>

傳送非同步通知時，呼叫端不會等候回復。 COM 會使用 [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) 或高階事件來傳送非同步通知（視平臺而定）。 COM 定義五個 [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink)的非同步方法：

-   [**OnDataChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-ondatachange)
-   [**OnViewChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onviewchange)
-   [**OnRename**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onrename)
-   [**OnSave**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onsave)
-   [**OnClose**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onclose)

> [!Note]  
> 當 COM 正在處理非同步呼叫時，無法進行同步呼叫。 例如，容器應用程式的 [**OnDataChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-ondatachange) 執行不能包含 [**IPersistStorage：： Save**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststorage-save)的呼叫。 這些呼叫是 COM 唯一支援的非同步呼叫。 目前沒有任何方法可建立非同步自訂介面。

 

</dd> <dt>

<span id="Input-synchronized_calls"></span><span id="input-synchronized_calls"></span><span id="INPUT-SYNCHRONIZED_CALLS"></span>*輸入同步呼叫*
</dt> <dd>

進行輸入同步處理呼叫時，呼叫的物件必須先完成呼叫，才能產生控制權。 這有助於確保焦點管理能正常運作，而且會適當地處理使用者輸入的資料。 這些呼叫是由 COM 透過 [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) 函式來進行，而不需要進入強制回應迴圈。 處理輸入同步處理的呼叫時，呼叫的物件不能呼叫任何函數或方法 (包括可能會產生控制權) 的同步方法。 下列是輸入同步處理的方法

-   [**IOleWindow：： GetWindow**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-getwindow)
-   [**IOleInPlaceActiveObject：： OnFrameWindowActivate**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceactiveobject-onframewindowactivate)
-   [**IOleInPlaceActiveObject：： OnDocWindowActivate**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceactiveobject-ondocwindowactivate)
-   [**IOleInPlaceActiveObject：： ResizeBorder**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceactiveobject-resizeborder)
-   [**IOleInPlaceUIWindow::GetBorder**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-getborder)
-   [**IOleInPlaceUIWindow::RequestBorderSpace**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-requestborderspace)
-   [**IOleInPlaceUIWindow::SetBorderSpace**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-setborderspace)
-   [**IOleInPlaceFrame：： SetMenu**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setmenu)
-   [**IOleInPlaceFrame：： SetStatusText**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setstatustext)
-   [**IOleInPlaceObject::SetObjectRects**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceobject-setobjectrects)

</dd> </dl>

為了將非同步訊息處理可能產生的問題降至最低，大部分的 COM 方法呼叫都是同步的。 透過同步通訊，不需要特殊的程式碼來分派和處理傳入的訊息。 當應用程式進行同步方法呼叫時，COM 會進入強制回應的等候迴圈，以處理所需的回復，並將傳入訊息分派到能夠處理這些訊息的應用程式。

COM 會藉由指派稱為 *邏輯執行緒* 識別碼的識別碼來管理方法呼叫。 當使用者選取功能表命令或應用程式起始新的 COM 作業時，就會指派新的。 後續與初始 COM 呼叫相關的呼叫會被指派與初始呼叫相同的邏輯執行緒識別碼。

 

 