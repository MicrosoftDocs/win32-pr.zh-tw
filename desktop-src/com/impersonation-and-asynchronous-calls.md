---
title: 模擬和非同步呼叫
description: 模擬和非同步呼叫
ms.assetid: 7eaa0a66-7a80-4831-b0b6-b8eff4abd036
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0854946b619f7580173ffcbc97c9af3f2540361b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683202"
---
# <a name="impersonation-and-asynchronous-calls"></a><span data-ttu-id="87132-103">模擬和非同步呼叫</span><span class="sxs-lookup"><span data-stu-id="87132-103">Impersonation and Asynchronous Calls</span></span>

<span data-ttu-id="87132-104">伺服器呼叫 [**ISynchronize：：信號**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal) 完成之後，伺服器無法模擬用戶端，即使 Begin \_ 方法尚未完成。</span><span class="sxs-lookup"><span data-stu-id="87132-104">The server cannot impersonate the client after the server's call to [**ISynchronize::Signal**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal) completes, even if the Begin\_ method has not yet completed.</span></span> <span data-ttu-id="87132-105">例如，假設用戶端呼叫 Begin \_ 方法，伺服器會立即處理呼叫，而伺服器會呼叫 **信號** 以表示它已完成處理。</span><span class="sxs-lookup"><span data-stu-id="87132-105">For example, suppose a client calls the Begin\_ method, the server processes the call immediately, and the server calls **Signal** to indicate it is finished processing.</span></span> <span data-ttu-id="87132-106">即使工作仍在 Begin 方法中完成 \_ ，伺服器仍無法在呼叫 **信號** 完成之後模擬用戶端。</span><span class="sxs-lookup"><span data-stu-id="87132-106">Even if work remains to be done in the Begin\_ method, the server cannot impersonate the client after the call to **Signal** completes.</span></span>

<span data-ttu-id="87132-107">如果伺服器在呼叫 [**信號**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal)之前模擬用戶端，將不會從執行緒移除模擬權杖，直到伺服器呼叫 [**IServerSecurity：： RevertToSelf**](/windows/win32/api/objidlbase/nf-objidlbase-iserversecurity-reverttoself) 為止，或直到伺服器的呼叫開始傳回（以先達到者為 \_ 准）。</span><span class="sxs-lookup"><span data-stu-id="87132-107">If the server impersonates the client before it calls [**Signal**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal), the impersonation token will not be removed from the thread until the server calls [**IServerSecurity::RevertToSelf**](/windows/win32/api/objidlbase/nf-objidlbase-iserversecurity-reverttoself) or until the server's call to Begin\_ returns, whichever comes first.</span></span>

## <a name="related-topics"></a><span data-ttu-id="87132-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="87132-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87132-109">委派和模擬</span><span class="sxs-lookup"><span data-stu-id="87132-109">Delegation and Impersonation</span></span>](delegation-and-impersonation.md)
</dt> <dt>

[<span data-ttu-id="87132-110">進行非同步呼叫</span><span class="sxs-lookup"><span data-stu-id="87132-110">Making an Asynchronous Call</span></span>](making-an-asynchronous-call.md)
</dt> </dl>

 

 