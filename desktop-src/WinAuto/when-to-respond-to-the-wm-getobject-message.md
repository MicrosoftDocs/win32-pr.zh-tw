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
# <a name="when-to-respond-to-the-wm_getobject-message"></a>何時回應 WM \_ GETOBJECT 訊息

如果應用程式支援 UI 元素的 Microsoft Active Accessibility 或消費者介面自動化，則應用程式必須在代表 UI 專案的物件完全初始化或應用程式開始關閉之後，才能回應 [**WM \_ GETOBJECT**](wm-getobject.md) 訊息。 當應用程式建立新的視窗時，系統會引發 [**事件 \_ 物件 \_ create**](event-constants.md) new-winevent 來通知用戶端，然後再將 [**WM \_ 建立**](/windows/desktop/winmsg/wm-create) 訊息傳送至應用程式的視窗程式。 因為許多應用程式都使用 **WM \_ create** 來啟動初始化程式，所以在應用程式完成處理 **wm \_ 建立** 訊息之前，UI 元素的任何協助工具執行都不會回應 [**wm \_ GETOBJECT**](wm-getobject.md)訊息。

 

 