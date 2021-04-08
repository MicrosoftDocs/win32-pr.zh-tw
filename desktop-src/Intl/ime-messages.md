---
description: 作業系統會在特定事件發生時會影響 IME 視窗時，將輸入法視窗訊息傳送至應用程式的視窗程式。
ms.assetid: 7eac1ab7-d04b-4e1b-9e2c-fa9a778756cd
title: 輸入法訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0f30baa01081e0aca1423f3384926938e6fdc07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026290"
---
# <a name="ime-messages"></a><span data-ttu-id="87808-103">輸入法訊息</span><span class="sxs-lookup"><span data-stu-id="87808-103">IME Messages</span></span>

<span data-ttu-id="87808-104">作業系統會在特定事件發生時會影響 IME 視窗時，將輸入法視窗訊息傳送至應用程式的視窗程式。</span><span class="sxs-lookup"><span data-stu-id="87808-104">The operating system sends IME window messages to the window procedure of an application when certain events occur that affect the IME windows.</span></span> <span data-ttu-id="87808-105">例如，當視窗啟用時，作業系統會將 [**WM \_ IME \_ SETCONTEXT**](wm-ime-setcontext.md) 訊息傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="87808-105">For example, the operating system sends the [**WM\_IME\_SETCONTEXT**](wm-ime-setcontext.md) message to the application when a window is activated.</span></span> <span data-ttu-id="87808-106">未感知的應用程式會將這些訊息傳遞至 [DefWindowProc](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式，以將它們傳送至對應的預設 IME 視窗。</span><span class="sxs-lookup"><span data-stu-id="87808-106">IME-unaware applications pass these messages to the [DefWindowProc](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function, which sends them to the corresponding default IME window.</span></span> <span data-ttu-id="87808-107">IME 感知的應用程式可以處理這些訊息，或將它們轉寄給自己的 IME 視窗。</span><span class="sxs-lookup"><span data-stu-id="87808-107">IME-aware applications either process these messages or forward them to their own IME windows.</span></span>

<span data-ttu-id="87808-108">您的應用程式可以指示 IME 視窗執行命令，例如，使用 [ [**WM \_ IME] \_ 控制項**](wm-ime-control.md) 訊息來變更組合視窗的位置。</span><span class="sxs-lookup"><span data-stu-id="87808-108">Your application can direct an IME window to carry out a command, for example, change the position of a composition window, by using the [**WM\_IME\_CONTROL**](wm-ime-control.md) message.</span></span> <span data-ttu-id="87808-109">IME 會透過傳送 [**wm \_ 輸入法 \_ 通知**](wm-ime-notify.md)訊息，通知應用程式有關組合字元串的變更，方法是使用 [**wm \_ IME \_ 撰寫**](wm-ime-composition.md)訊息，以及關於 IME 視窗狀態的一般變更。</span><span class="sxs-lookup"><span data-stu-id="87808-109">The IME notifies the application about changes to the composition string by using the [**WM\_IME\_COMPOSITION**](wm-ime-composition.md) message, and about general changes to the status of the IME windows by sending the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="87808-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="87808-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87808-111">關於輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="87808-111">About Input Method Manager</span></span>](about-input-method-manager.md)
</dt> </dl>

 

 
