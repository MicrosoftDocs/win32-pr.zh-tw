---
title: 回應 WM_GETOBJECT 訊息的時機
description: 如果應用程式支援 UI 元素的 Microsoft Active Accessibility 或消費者介面自動化，則應用程式必須在 \_ 代表 ui 專案的物件完全初始化或應用程式開始關閉之後，才能回應 WM GETOBJECT 訊息。
ms.assetid: cc99f7ef-1eb6-40c4-9ec0-8fb18cb4a3e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18cfa8d6604a13e84ffa89bf1fcf93d5d13e66e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463561"
---
# <a name="when-to-respond-to-the-wm_getobject-message"></a><span data-ttu-id="57599-103">何時回應 WM \_ GETOBJECT 訊息</span><span class="sxs-lookup"><span data-stu-id="57599-103">When to Respond to the WM\_GETOBJECT Message</span></span>

<span data-ttu-id="57599-104">如果應用程式支援 UI 元素的 Microsoft Active Accessibility 或消費者介面自動化，則應用程式必須在代表 UI 專案的物件完全初始化或應用程式開始關閉之後，才能回應 [**WM \_ GETOBJECT**](wm-getobject.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="57599-104">If an application supports Microsoft Active Accessibility or UI Automation for a UI element, the application must not respond to the [**WM\_GETOBJECT**](wm-getobject.md) message before the object that represents the UI element is fully initialized, or after the application has begun to close.</span></span> <span data-ttu-id="57599-105">當應用程式建立新的視窗時，系統會引發 [**事件 \_ 物件 \_ create**](event-constants.md) new-winevent 來通知用戶端，然後再將 [**WM \_ 建立**](/windows/desktop/winmsg/wm-create) 訊息傳送至應用程式的視窗程式。</span><span class="sxs-lookup"><span data-stu-id="57599-105">When an application creates a new window, the system raises the [**EVENT\_OBJECT\_CREATE**](event-constants.md) WinEvent to notify clients before sending the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message to the application's window procedure.</span></span> <span data-ttu-id="57599-106">因為許多應用程式都使用 **WM \_ create** 來啟動初始化程式，所以在應用程式完成處理 **wm \_ 建立** 訊息之前，UI 元素的任何協助工具執行都不會回應 [**wm \_ GETOBJECT**](wm-getobject.md)訊息。</span><span class="sxs-lookup"><span data-stu-id="57599-106">Because many applications use **WM\_CREATE** to start the initialization process, any accessibility implementation of a UI element does not respond to the [**WM\_GETOBJECT**](wm-getobject.md) message until after the application has finished processing the **WM\_CREATE** message.</span></span>

 

 