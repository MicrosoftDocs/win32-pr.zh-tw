---
title: 處理 WM_GETOBJECT 訊息
description: Microsoft Active Accessibility 和 Microsoft 消費者介面自動化都會將 WM \_ GETOBJECT 訊息傳送至伺服器或提供者應用程式，以取得伺服器或提供者所支援之可存取物件的相關資訊。
ms.assetid: 4b8e551f-aba7-4a89-8874-ba690175f525
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 732ebd21cc6d198040e5502554ce2a8cf1abb718c055bc9af9f88e0c5d123b4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994188"
---
# <a name="handling-the-wm_getobject-message"></a>處理 WM \_ GETOBJECT 訊息

Microsoft Active Accessibility 和 Microsoft 消費者介面自動化都會將 [**WM \_ GETOBJECT**](wm-getobject.md) 訊息傳送至伺服器或提供者應用程式，以取得伺服器或提供者所支援之可存取物件的相關資訊。 用戶端永遠不會直接傳送 **WM \_ GETOBJECT** 。 相反地，Microsoft Active Accessibility 會在用戶端呼叫 [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)、 [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)和 [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) 函數時傳送此訊息。 當用戶端呼叫 [**IUIAutomation：： ElementFromHandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle)、 [**ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)和 [**system.windows.input.focusmanager.getfocusedelement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement)，以及處理用戶端已註冊的事件時，消費者介面自動化傳送 **WM \_ GETOBJECT** 。

Microsoft Active Accessibility 或消費者介面自動化指定所需資訊的物件類型，方法是傳遞稱為 *物件識別碼* 的值與 [**WM \_ GETOBJECT**](wm-getobject.md) 訊息。 當接收到訊息時，伺服器或提供者會檢查物件識別碼，以判斷如何回應訊息。 回應取決於接收應用程式是否要為指定的物件 (伺服器) 的 Microsoft Active Accessibility，消費者介面自動化 (提供者) ，或兩者皆非。

-   如果接收應用程式是 Microsoft Active Accessibility 的伺服器，而 [**WM \_ GETOBJECT**](wm-getobject.md) 訊息包含 [**OBJID \_ 用戶端**](object-identifiers.md)的物件識別碼，伺服器應該將物件的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面傳遞至 [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) 函式，以傳回所取得的值。
-   如果接收應用程式是 aUI Automation 提供者，而且物件識別碼是 **UiaRootObjectId**，則提供者應該傳回物件的 [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) 介面。 提供者會藉由呼叫 [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) 函數來取得介面。
-   如果接收應用程式未同時執行 Microsoft Active Accessibility 也不消費者介面自動化，則應該將 [**WM \_ GETOBJECT**](wm-getobject.md) Message 傳遞給 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函數。 傳遞訊息可讓協助工具架構判斷指定之物件的 proxy 是否可供使用。
-   如果物件識別碼不是 [**OBJID \_ 用戶端**](object-identifiers.md) 或 UiaRootObjectId，則接收應用程式應該將 [**WM \_ GETOBJECT**](wm-getobject.md) 訊息傳遞給 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式。 傳遞訊息可讓協助工具架構使用標準 UI 元素的預設提供者。

Microsoft Active Accessibility 和消費者介面自動化可以在 [**WM \_ GETOBJECT**](wm-getobject.md) 訊息中傳遞自訂物件識別碼，以從伺服器或提供者取出應用程式定義的值或物件。 [**OBJID \_ NATIVEOM**](object-identifiers.md)或 [**OBJID \_ QUERYCLASSNAMEIDX**](object-identifiers.md)物件識別碼可以用來取出原生物件模型介面，或要求 Oleacc.dll 所支援的特定 proxy 物件。

藉由同時處理 [**OBJID \_ 用戶端**](object-identifiers.md) 和 **UiaRootObjectId** 物件識別碼，Microsoft Active Accessibility 伺服器的執行可與消費者介面自動化提供者的執行並存。 因為大部分的標準 Windows 控制項和通用控制項程式庫所執行的通用控制項 (ComCtl32.dll) 不會執行 Microsoft Active Accessibility 或消費者介面自動化，所以這些控制項通常不會處理 [**WM \_ GETOBJECT**](wm-getobject.md)訊息。 相反地，Microsoft Active Accessibility 或消費者介面自動化架構會檢查 proxy 物件是否適用于特定的 UI 元素。 否則，它會提供主機視窗物件的預設 proxy 物件。

 

 