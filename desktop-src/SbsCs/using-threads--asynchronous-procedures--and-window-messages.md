---
description: 整個過程中都會顯示啟用內容。
ms.assetid: 6eda00d5-9dac-4267-bf61-b481814201f8
title: 執行緒、非同步程式和視窗訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e615eb9795ba32bcf4bd227a4933e890e9b89055
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847896"
---
# <a name="using-threads-asynchronous-procedures-and-window-messages"></a><span data-ttu-id="715ce-103">使用執行緒、非同步程式和視窗訊息</span><span class="sxs-lookup"><span data-stu-id="715ce-103">Using Threads, Asynchronous Procedures, and Window Messages</span></span>

<span data-ttu-id="715ce-104">整個過程中都會顯示啟用內容。</span><span class="sxs-lookup"><span data-stu-id="715ce-104">Activation contexts are visible throughout the entire process.</span></span> <span data-ttu-id="715ce-105">不過，啟用內容堆疊是針對每個執行緒，而且相同進程中的兩個執行緒可以有不同的啟用堆疊。</span><span class="sxs-lookup"><span data-stu-id="715ce-105">The activation context stacks are however per-thread, and two threads in the same process can have different activation stacks.</span></span> <span data-ttu-id="715ce-106">[**CreateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread) 會自動將目前的啟用內容放在新執行緒的啟用堆疊的頂端。</span><span class="sxs-lookup"><span data-stu-id="715ce-106">[**CreateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread) automatically puts the current activation context at the top of the new thread's activation stack.</span></span> <span data-ttu-id="715ce-107">這有助於升級現有的程式碼以使用並存元件，因為新執行緒可以立即在目前的啟用內容中執行。</span><span class="sxs-lookup"><span data-stu-id="715ce-107">This can facilitate upgrading existing code to use side-by-side components because the new thread can run immediately in the current activation context.</span></span>

<span data-ttu-id="715ce-108">非同步程序呼叫、完成埠回呼，以及其他執行緒上的任何其他回呼都會自動取得來源的啟用內容。</span><span class="sxs-lookup"><span data-stu-id="715ce-108">Asynchronous procedure calls, completion port callbacks, and any other callbacks on other threads automatically get the activation context of the source.</span></span> <span data-ttu-id="715ce-109">呼叫回呼時，會清除啟用堆疊。</span><span class="sxs-lookup"><span data-stu-id="715ce-109">When the callback is called, the activation stack is cleaned up.</span></span> <span data-ttu-id="715ce-110">這表示您的應用程式可以使用非同步程序呼叫和回呼，而不需要明確地啟用任何內容，因為內容管理將會由基礎並存基礎結構來完成。</span><span class="sxs-lookup"><span data-stu-id="715ce-110">This means that your application can use asynchronous procedure calls and callbacks without explicitly activating any contexts because context management will be done by the underlying side-by-side infrastructure.</span></span> <span data-ttu-id="715ce-111">若要讓其他內容在回呼或新執行緒期間變成作用中，您的應用程式可以執行自己的內容管理。</span><span class="sxs-lookup"><span data-stu-id="715ce-111">To make other contexts active during a callback or new thread, your application can do its own context management.</span></span> <span data-ttu-id="715ce-112">在此情況下，您的程式必須使用正確的啟用內容啟用函式順序和停用功能。</span><span class="sxs-lookup"><span data-stu-id="715ce-112">In this case your program must use the proper sequence of activation context activate functions and deactivate functions.</span></span>

<span data-ttu-id="715ce-113">啟用內容是執行緒中立的。</span><span class="sxs-lookup"><span data-stu-id="715ce-113">Activation contexts are thread-neutral.</span></span> <span data-ttu-id="715ce-114">啟用內容只會變更目前線程的堆疊，而您無法線上程之間啟用內容。</span><span class="sxs-lookup"><span data-stu-id="715ce-114">Activating a context only changes the current thread's stack, and you cannot activate a context across threads.</span></span> <span data-ttu-id="715ce-115">執行緒 A 無法強制內容進入執行緒 B。啟用內容 API 的功能也可感知執行緒。</span><span class="sxs-lookup"><span data-stu-id="715ce-115">Thread A cannot force a context onto thread B. The functions of the activation context API are also threading-aware.</span></span>

<span data-ttu-id="715ce-116">當您使用 [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) 或 [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) 將視窗訊息傳送至進程中的另一個視窗程式時，目前的啟用內容會先啟動，然後再將訊息傳遞至目的程式。</span><span class="sxs-lookup"><span data-stu-id="715ce-116">When you use [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) or [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) to send a window message to another window procedure in your process, the current activation context is activated before the message is passed on to the target procedure.</span></span> <span data-ttu-id="715ce-117">目前的啟用內容與訊息一起進行。</span><span class="sxs-lookup"><span data-stu-id="715ce-117">The current activation context goes along with the message.</span></span> <span data-ttu-id="715ce-118">這可確保參考 COM 物件、DLL 名稱或其他並存資源的訊息會保留其正確的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="715ce-118">This ensures that messages that refer to COM objects, DLL names, or other side-by-side resources retain their correct context information.</span></span>

 

 
