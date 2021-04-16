---
title: 關於 DDEML
description: 本主題討論動態資料交換。
ms.assetid: 155b4cb0-dfbb-42f5-9fa3-8129349a0754
keywords:
- 'Windows 消費者介面，動態資料交換 (DDE) '
- 動態資料交換 (的 DDE) ，關於
- DDE (動態資料交換) ，關於
- '資料交換、動態資料交換 (DDE) '
- 'Windows 消費者介面、動態資料交換管理程式庫 (DDEML) '
- 動態資料交換管理程式庫 (DDEML) ，關於
- DDEML (動態資料交換管理程式庫) ，關於
- '資料交換、動態資料交換管理程式庫 (DDEML) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84ed77565c8b4e20841ad2ef80ae84c1f5c39724
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507448"
---
# <a name="about-the-ddeml"></a><span data-ttu-id="eaa5c-111">關於 DDEML</span><span class="sxs-lookup"><span data-stu-id="eaa5c-111">About the DDEML</span></span>

<span data-ttu-id="eaa5c-112">動態資料交換 (的 DDE) 與剪貼簿資料傳輸機制不同。</span><span class="sxs-lookup"><span data-stu-id="eaa5c-112">Dynamic Data Exchange (DDE) differs from the clipboard data-transfer mechanism.</span></span> <span data-ttu-id="eaa5c-113">其中一個差異是剪貼簿幾乎一律會用來做為使用者特定動作的一次性回應，例如按一下功能表上的 [ **貼** 上]。</span><span class="sxs-lookup"><span data-stu-id="eaa5c-113">One difference is that the clipboard is almost always used as a one-time response to a specific action by the user — such as clicking **Paste** from a menu.</span></span> <span data-ttu-id="eaa5c-114">雖然 DDE 也可以由使用者起始，但它通常會在沒有使用者進一步介入的情況下繼續進行。</span><span class="sxs-lookup"><span data-stu-id="eaa5c-114">Although DDE can also be initiated by a user, it typically continues without the user's further involvement.</span></span>

<span data-ttu-id="eaa5c-115">動態資料交換 Management Library (DDEML) 提供可簡化將 DDE 功能新增至應用程式之工作的介面。</span><span class="sxs-lookup"><span data-stu-id="eaa5c-115">The Dynamic Data Exchange Management Library (DDEML) provides an interface that simplifies the task of adding DDE capability to an application.</span></span> <span data-ttu-id="eaa5c-116">應用程式會使用 DDEML 所提供的函式來管理 DDE 交談，而不是直接傳送、張貼和處理 DDE 訊息。</span><span class="sxs-lookup"><span data-stu-id="eaa5c-116">Instead of sending, posting, and processing DDE messages directly, an application uses the functions provided by the DDEML to manage DDE conversations.</span></span> <span data-ttu-id="eaa5c-117">DDE 交談是用戶端與伺服器應用程式之間的互動。</span><span class="sxs-lookup"><span data-stu-id="eaa5c-117">A DDE conversation is the interaction between client and server applications.</span></span> <span data-ttu-id="eaa5c-118">DDEML 也提供一種方法來管理在 DDE 應用程式之間共用的字串和資料。</span><span class="sxs-lookup"><span data-stu-id="eaa5c-118">The DDEML also provides a means for managing the strings and data shared among DDE applications.</span></span> <span data-ttu-id="eaa5c-119">DDE 應用程式不會使用原子和指向共用記憶體物件的指標，而是會建立和交換字串控制碼，以識別用來識別 DDE 物件的字串和資料控制碼。</span><span class="sxs-lookup"><span data-stu-id="eaa5c-119">Instead of using atoms and pointers to shared memory objects, DDE applications create and exchange string handles, which identify strings, and data handles, which identify DDE objects.</span></span> <span data-ttu-id="eaa5c-120">DDEML 提供的函式 ([**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)) ，可讓伺服器應用程式註冊它所支援的服務名稱。</span><span class="sxs-lookup"><span data-stu-id="eaa5c-120">The DDEML provides a function ([**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)) that enables a server application to register the service names it supports.</span></span> <span data-ttu-id="eaa5c-121">接著，服務名稱會廣播到系統中的其他應用程式，而該應用程式會使用名稱連接到伺服器。</span><span class="sxs-lookup"><span data-stu-id="eaa5c-121">The service names are then broadcast to other applications in the system, which use the names to connect to the server.</span></span> <span data-ttu-id="eaa5c-122">DDEML 也可確保 DDE 應用程式之間的相容性，方法是要求這些應用程式以一致的方式執行 DDE 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="eaa5c-122">The DDEML also ensures compatibility among DDE applications by requiring them to implement the DDE protocol in a consistent manner.</span></span>

<span data-ttu-id="eaa5c-123">使用以訊息為基礎之 DDE 通訊協定的現有應用程式與使用 DDEML 的應用程式完全相容;也就是說，使用訊息型 DDE 的應用程式可以使用 DDEML 來建立交談，以及與應用程式執行交易。</span><span class="sxs-lookup"><span data-stu-id="eaa5c-123">Existing applications using the message-based DDE protocol are fully compatible with those that use the DDEML; that is, an application using message-based DDE can establish conversations and perform transactions with applications using the DDEML.</span></span> <span data-ttu-id="eaa5c-124">除了在新的應用程式中使用 DDE 訊息，您還可利用 DDEML 以及它所提供的許多增強功能。</span><span class="sxs-lookup"><span data-stu-id="eaa5c-124">Instead of using DDE messages in your new application, take advantage of the DDEML and the many improvements it offers.</span></span>

<span data-ttu-id="eaa5c-125">若要使用 DDEML，您必須包含 DDEML。H 標頭檔的原始程式檔中，與 USER32 連結。LIB 檔案，並確定 DDEML.DLL 檔案位於系統的路徑中。</span><span class="sxs-lookup"><span data-stu-id="eaa5c-125">To use the DDEML, you must include the DDEML.H header file in your source files, link with the USER32.LIB file, and ensure that the DDEML.DLL file resides in the system's path.</span></span>

<span data-ttu-id="eaa5c-126">每當 DDEML 函式失敗時，應用程式就可以呼叫 [**DdeGetLastError**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetlasterror) 函數來判斷失敗的原因。</span><span class="sxs-lookup"><span data-stu-id="eaa5c-126">Whenever a DDEML function fails, an application can call the [**DdeGetLastError**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetlasterror) function to determine the cause of the failure.</span></span> <span data-ttu-id="eaa5c-127">**DdeGetLastError** 會傳回錯誤值，以指定最新錯誤的原因。</span><span class="sxs-lookup"><span data-stu-id="eaa5c-127">**DdeGetLastError** returns an error value that specifies the cause of the most recent error.</span></span>

 

 




