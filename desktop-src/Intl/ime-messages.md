---
description: 作業系統會在特定事件發生時會影響 IME 視窗時，將輸入法視窗訊息傳送至應用程式的視窗程式。
ms.assetid: 7eac1ab7-d04b-4e1b-9e2c-fa9a778756cd
title: 輸入法訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aa34228f695a18187654707668067ac34562098b48aae185a8d66d777b6f507
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118949259"
---
# <a name="ime-messages"></a>輸入法訊息

作業系統會在特定事件發生時會影響 IME 視窗時，將輸入法視窗訊息傳送至應用程式的視窗程式。 例如，當視窗啟用時，作業系統會將 [**WM \_ IME \_ SETCONTEXT**](wm-ime-setcontext.md) 訊息傳送至應用程式。 未感知的應用程式會將這些訊息傳遞至 [DefWindowProc](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式，以將它們傳送至對應的預設 IME 視窗。 IME 感知的應用程式可以處理這些訊息，或將它們轉寄給自己的 IME 視窗。

您的應用程式可以指示 IME 視窗執行命令，例如，使用 [ [**WM \_ IME] \_ 控制項**](wm-ime-control.md) 訊息來變更組合視窗的位置。 IME 會透過傳送 [**wm \_ 輸入法 \_ 通知**](wm-ime-notify.md)訊息，通知應用程式有關組合字元串的變更，方法是使用 [**wm \_ IME \_ 撰寫**](wm-ime-composition.md)訊息，以及關於 IME 視窗狀態的一般變更。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於輸入方法管理員](about-input-method-manager.md)
</dt> </dl>

 

 
