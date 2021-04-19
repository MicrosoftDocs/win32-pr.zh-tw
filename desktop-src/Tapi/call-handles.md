---
description: 如同會話識別碼總覽中所述，呼叫控制碼是 TAPI 2.2 應用程式用來識別特定通訊會話的方法。
ms.assetid: 5f6a7adf-c074-4bf6-9828-76604eb7609c
title: 呼叫控制碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aacad5b73d9d22caa006b734acaf8b992203d7d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974942"
---
# <a name="call-handles"></a><span data-ttu-id="b3027-103">呼叫控制碼</span><span class="sxs-lookup"><span data-stu-id="b3027-103">Call Handles</span></span>

<span data-ttu-id="b3027-104">如同 [會話識別碼](./session-identifier-ovr.md) 總覽中所述，呼叫控制碼是 TAPI 2.2 應用程式用來識別特定通訊會話的方法。</span><span class="sxs-lookup"><span data-stu-id="b3027-104">As is mentioned in the [Session Identifier](./session-identifier-ovr.md) overview, a call handle is the means by which a TAPI 2.2 application identifies a particular communications session.</span></span> <span data-ttu-id="b3027-105">當應用程式啟動會話時，TAPI 會傳回呼叫控制碼，以便在進一步的作業或查詢中使用。</span><span class="sxs-lookup"><span data-stu-id="b3027-105">When an application initiates a session, TAPI returns a call handle for use in further operations or queries.</span></span> <span data-ttu-id="b3027-106">當應用程式收到傳入會話的通知時，TAPI 也會在呼叫控制碼中傳遞。</span><span class="sxs-lookup"><span data-stu-id="b3027-106">When an application is notified of an incoming session, TAPI also passes in a call handle.</span></span>

<span data-ttu-id="b3027-107">當會話結束且會話狀態為閒置時，呼叫控制碼會維持有效，直到應用程式解除配置控制碼或關閉該行為止。</span><span class="sxs-lookup"><span data-stu-id="b3027-107">After a session has ended and the session state is idle, the call handle remains valid until the application deallocates the handle or the line is closed.</span></span> <span data-ttu-id="b3027-108">應用程式可能會關閉該行，或可能會收到 [**行 \_ 關閉**](line-close.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="b3027-108">The line might be closed by the application, or it may receive a [**LINE\_CLOSE**](line-close.md) message.</span></span> <span data-ttu-id="b3027-109">如果行已關閉，則行呼叫的所有呼叫控制碼都會立即變成無效。</span><span class="sxs-lookup"><span data-stu-id="b3027-109">If a line is closed, all call handles to calls on the line instantly become invalid.</span></span>

<span data-ttu-id="b3027-110">在呼叫還原為 *閒置* 狀態之後，仍允許應用程式讀取呼叫的資訊結構和狀態。</span><span class="sxs-lookup"><span data-stu-id="b3027-110">After a call reverts to the *idle* state, the application is still allowed to read the call's information structure and status.</span></span> <span data-ttu-id="b3027-111">這可讓應用程式使用像是 [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) 的作業來取得記錄用途的呼叫資訊。</span><span class="sxs-lookup"><span data-stu-id="b3027-111">This enables applications to use operations such as [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) to retrieve call information for logging purposes.</span></span>

<span data-ttu-id="b3027-112">當應用程式不再針對閒置呼叫的控制碼使用時，它必須呼叫 [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) 來釋放與呼叫相關的系統組態記憶體。</span><span class="sxs-lookup"><span data-stu-id="b3027-112">When the application has no further use for the handle of an idle call, it must call [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) to free system-allocated memory related to the call.</span></span> <span data-ttu-id="b3027-113">TAPI 會為每個具有呼叫控制碼的應用程式佈建記憶體。</span><span class="sxs-lookup"><span data-stu-id="b3027-113">TAPI allocates memory for each call for each application that has a handle to the call.</span></span> <span data-ttu-id="b3027-114">服務提供者可能會配置記憶體來保存呼叫資訊。</span><span class="sxs-lookup"><span data-stu-id="b3027-114">It is likely that service providers will allocate memory to hold call information as well.</span></span> <span data-ttu-id="b3027-115">解除配置應用程式的呼叫控制碼，可讓程式庫和服務提供者回收這些記憶體資源。</span><span class="sxs-lookup"><span data-stu-id="b3027-115">Deallocation of an application's call handle allows the library and the service provider to reclaim these memory resources.</span></span> <span data-ttu-id="b3027-116">成功解除配置之後，應用程式在呼叫上的控制碼會變成 void。</span><span class="sxs-lookup"><span data-stu-id="b3027-116">An application's handle for a call becomes void after a successful deallocation.</span></span>

<span data-ttu-id="b3027-117">應用程式本身必須釋放與它針對其本身所配置之呼叫相關的記憶體。</span><span class="sxs-lookup"><span data-stu-id="b3027-117">The application must itself free memory related to the call that it allocated for its own purposes.</span></span>

 

 
