---
title: 錯誤訊息和通知
description: 錯誤訊息和通知
ms.assetid: 7f804364-d8be-4e52-ab0e-fba05bcf76ce
keywords:
- MCIWndGetError 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37e40e78c72dc378baa37b56dbb2d5718ae2d85b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023372"
---
# <a name="error-messages-and-notifications"></a><span data-ttu-id="a4585-104">錯誤訊息和通知</span><span class="sxs-lookup"><span data-stu-id="a4585-104">Error Messages and Notifications</span></span>

<span data-ttu-id="a4585-105">MCIWnd 使用 MCI 來控制播放和錄製多媒體資料的裝置。</span><span class="sxs-lookup"><span data-stu-id="a4585-105">MCIWnd uses MCI to control the devices that play and record multimedia data.</span></span> <span data-ttu-id="a4585-106">一般情況下，MCIWnd 會在 [錯誤] 對話方塊中顯示 MCI 錯誤。</span><span class="sxs-lookup"><span data-stu-id="a4585-106">In general, MCIWnd displays MCI errors in an error dialog box.</span></span> <span data-ttu-id="a4585-107">只要 MCI 命令失敗，就會產生 MCI 錯誤。</span><span class="sxs-lookup"><span data-stu-id="a4585-107">An MCI error is generated whenever an MCI command fails.</span></span> <span data-ttu-id="a4585-108">例如，如果您的應用程式嘗試使用 [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) 宏繼續暫停播放，而目前的裝置不支援 resume，則會向使用者回報錯誤。</span><span class="sxs-lookup"><span data-stu-id="a4585-108">For example, if your application tries to resume paused playback by using the [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) macro and the current device does not support resume, an error is reported to the user.</span></span>

<span data-ttu-id="a4585-109">MCIWnd 可讓您選擇兩種方式來處理錯誤訊息：</span><span class="sxs-lookup"><span data-stu-id="a4585-109">MCIWnd allows you two choices for handling error messages:</span></span>

-   <span data-ttu-id="a4585-110">您可以防止錯誤訊息抵達使用者。</span><span class="sxs-lookup"><span data-stu-id="a4585-110">You can prevent error messages from reaching the user.</span></span> <span data-ttu-id="a4585-111">若要防止顯示 MCI 錯誤訊息，請 \_ 在使用 [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) 或 [CreateWindowEx](/windows/win32/api/winuser/nf-winuser-createwindowexa) 函數建立 MCIWnd 視窗的實例時，指定 MCIWNDF NOERRORDLG 視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="a4585-111">To prevent the display of MCI error messages, specify the MCIWNDF\_NOERRORDLG window style when you create an instance of an MCIWnd window by using the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) or [CreateWindowEx](/windows/win32/api/winuser/nf-winuser-createwindowexa) function.</span></span>
-   <span data-ttu-id="a4585-112">您可以將它們重新導向至您的應用程式以供顯示。</span><span class="sxs-lookup"><span data-stu-id="a4585-112">You can redirect them to your application for display.</span></span> <span data-ttu-id="a4585-113">若要將 MCI 錯誤訊息重新導向至您的應用程式，請 \_ 在使用 **MCIWndCreate** 或 **CreateWindowEx** 建立 MCIWnd 視窗的實例時，指定 MCIWNDF NOTIFYERROR 視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="a4585-113">To redirect MCI error messages to your application, specify the MCIWNDF\_NOTIFYERROR window style when you create an instance of an MCIWnd window by using **MCIWndCreate** or **CreateWindowEx**.</span></span>

<span data-ttu-id="a4585-114">啟用錯誤通知時，MCIWnd 會將每個通知訊息 ([**MCIWNDM \_ NOTIFYERROR**](mciwndm-notifyerror.md)) 傳送至 MCIWnd 視窗父系的主要訊息處理常式。</span><span class="sxs-lookup"><span data-stu-id="a4585-114">When error notification is enabled, MCIWnd sends each notification message ([**MCIWNDM\_NOTIFYERROR**](mciwndm-notifyerror.md)) to the main message handler of the parent of the MCIWnd window.</span></span> <span data-ttu-id="a4585-115">您的應用程式必須具有訊息處理常式，才能處理它所收到的通知訊息。</span><span class="sxs-lookup"><span data-stu-id="a4585-115">Your application must have a message handler to process the notification messages it receives.</span></span>

<span data-ttu-id="a4585-116">您可以使用 [**MCIWndGetError**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror) 宏來取得最新的 MCI 錯誤訊息的文字描述。</span><span class="sxs-lookup"><span data-stu-id="a4585-116">You can obtain a textual description of the most recent MCI error message by using the [**MCIWndGetError**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror) macro.</span></span> <span data-ttu-id="a4585-117">此宏會傳回應用程式定義緩衝區中的文字。</span><span class="sxs-lookup"><span data-stu-id="a4585-117">This macro returns the text in an application-defined buffer.</span></span> <span data-ttu-id="a4585-118">如果錯誤字串的長度超過緩衝區，MCIWnd 會截斷字串。</span><span class="sxs-lookup"><span data-stu-id="a4585-118">If the error string is longer than the buffer, MCIWnd truncates the string.</span></span>

<span data-ttu-id="a4585-119">您可以使用 [**MCIWndSetOwner**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner) 宏將所有通知路由傳送到另一個視窗。</span><span class="sxs-lookup"><span data-stu-id="a4585-119">You can route all notifications to another window by using the [**MCIWndSetOwner**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner) macro.</span></span>

 

 