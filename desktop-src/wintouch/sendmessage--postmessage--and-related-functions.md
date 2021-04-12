---
title: SendMessage、PostMessage 和相關函數
description: 本節說明使用 SendMessage、PostMessage 和相關函式搭配觸控訊息來轉送訊息的考慮。
ms.assetid: 9fba2013-17a3-499c-80dc-627e89c0edaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fc42e31f3c971c704d18f04a961fb6bd40eb91d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375957"
---
# <a name="sendmessage-postmessage-and-related-functions"></a><span data-ttu-id="d040c-103">SendMessage、PostMessage 和相關函數</span><span class="sxs-lookup"><span data-stu-id="d040c-103">SendMessage, PostMessage, and Related Functions</span></span>

<span data-ttu-id="d040c-104">本節說明使用 [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage)、 [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea)和相關函式搭配觸控訊息來轉送訊息的考慮。</span><span class="sxs-lookup"><span data-stu-id="d040c-104">This section describes considerations about forwarding messages using [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea), and related functions with touch messages.</span></span>

<span data-ttu-id="d040c-105">如果使用 [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage)、 [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea)或某些其他相關函式來轉送觸控訊息，則會關閉觸控輸入控點。</span><span class="sxs-lookup"><span data-stu-id="d040c-105">If a touch message is forwarded using [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea), or some other related function, the touch input handle is closed.</span></span> <span data-ttu-id="d040c-106">如果您已透過呼叫 [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo)來抓取觸控輸入控制碼所參考的資訊，則在您釋出記憶體之前，該資料會保持有效。</span><span class="sxs-lookup"><span data-stu-id="d040c-106">If you have retrieved the information contained referenced by a touch input handle through a call to [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo), that data will remain valid until you free the memory.</span></span>

<span data-ttu-id="d040c-107">接收透過上述其中一種機制轉送之觸控訊息的應用程式，會擁有它在訊息 *LPARAM* 中收到的觸控輸入控點，並負責將其關閉。</span><span class="sxs-lookup"><span data-stu-id="d040c-107">An application that receives touch messages forwarded through one of these mechanisms owns the touch input handle it receives in the message *LPARAM* and is responsible for closing it.</span></span> <span data-ttu-id="d040c-108">如果您未在呼叫 [**CloseTouchInputHandle**](/windows/desktop/api/winuser/nf-winuser-closetouchinputhandle)的情況下關閉控制碼，請將訊息傳遞至 [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca)，或使用 [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage)、 [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea)或某些相關函數轉寄訊息，您將會發生記憶體流失。</span><span class="sxs-lookup"><span data-stu-id="d040c-108">If you don't close the handle with a call to [**CloseTouchInputHandle**](/windows/desktop/api/winuser/nf-winuser-closetouchinputhandle), pass the message to [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca), or forward the message using [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea), or some related function, you will have a memory leak.</span></span>

> [!Note]  
> <span data-ttu-id="d040c-109">觸控訊息受限於一般消費者介面許可權隔離 (在轉送時 UIPI) 規則。</span><span class="sxs-lookup"><span data-stu-id="d040c-109">Touch messages are subject to normal User Interface Privilege Isolation (UIPI) rules when they are forwarded.</span></span>

 

## <a name="functions-related-to-sendmessage-and-postmessage"></a><span data-ttu-id="d040c-110">與 SendMessage 和 PostMessage 相關的函數</span><span class="sxs-lookup"><span data-stu-id="d040c-110">Functions related to SendMessage and PostMessage</span></span>

<span data-ttu-id="d040c-111">下列函式可能會影響觸控輸入控點的狀態。</span><span class="sxs-lookup"><span data-stu-id="d040c-111">The following functions that can affect the state of the touch input handle.</span></span>

-   [<span data-ttu-id="d040c-112">SendMessage</span><span class="sxs-lookup"><span data-stu-id="d040c-112">SendMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
-   [<span data-ttu-id="d040c-113">PostMessage</span><span class="sxs-lookup"><span data-stu-id="d040c-113">PostMessage</span></span>](/windows/win32/api/winuser/nf-winuser-postmessagea)
-   <span data-ttu-id="d040c-114">SendNotifyMessage</span><span class="sxs-lookup"><span data-stu-id="d040c-114">SendNotifyMessage</span></span>
-   <span data-ttu-id="d040c-115">SendMessageCallback</span><span class="sxs-lookup"><span data-stu-id="d040c-115">SendMessageCallback</span></span>
-   <span data-ttu-id="d040c-116">SendMessageTimeout</span><span class="sxs-lookup"><span data-stu-id="d040c-116">SendMessageTimeout</span></span>
-   <span data-ttu-id="d040c-117">PostThreadMessage</span><span class="sxs-lookup"><span data-stu-id="d040c-117">PostThreadMessage</span></span>

## <a name="related-topics"></a><span data-ttu-id="d040c-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="d040c-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d040c-119">函數</span><span class="sxs-lookup"><span data-stu-id="d040c-119">Functions</span></span>](mtfunctions.md)
</dt> <dt>

[<span data-ttu-id="d040c-120">DefWindowProc</span><span class="sxs-lookup"><span data-stu-id="d040c-120">DefWindowProc</span></span>](/windows/win32/api/winuser/nf-winuser-defwindowproca)
</dt> </dl>

 

 