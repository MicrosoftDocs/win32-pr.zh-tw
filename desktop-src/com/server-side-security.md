---
title: Server-Side 安全性
description: Server-Side 安全性
ms.assetid: 6c1d210e-daf0-490a-a6b9-65d99b9e1d7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77501c395c3ae1f14c8451d4691e7e776545e756
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103933649"
---
# <a name="server-side-security"></a><span data-ttu-id="7f26b-103">Server-Side 安全性</span><span class="sxs-lookup"><span data-stu-id="7f26b-103">Server-Side Security</span></span>

<span data-ttu-id="7f26b-104">伺服器可以使用 [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity)的方法來取得呼叫端的安全性資訊，或模擬呼叫者。</span><span class="sxs-lookup"><span data-stu-id="7f26b-104">The server can retrieve security information about a caller or impersonate the caller by using the methods of [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity).</span></span> <span data-ttu-id="7f26b-105">使用標準封送處理時，在目前呼叫的內容物件上，COM 會提供 **IServerSecurity** 的實作為。</span><span class="sxs-lookup"><span data-stu-id="7f26b-105">An implementation of **IServerSecurity** is supplied by COM on the context object for the current call when standard marshaling is used.</span></span> <span data-ttu-id="7f26b-106">不過，某些自訂封送處理介面可能沒有這個介面。</span><span class="sxs-lookup"><span data-stu-id="7f26b-106">However, this interface may be absent for some custom-marshaled interfaces.</span></span>

<span data-ttu-id="7f26b-107">當呼叫抵達伺服器時，伺服器可以呼叫 [**CoGetCallCoNtext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) 來取得 [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="7f26b-107">When a call arrives at the server, the server can call [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) to obtain a pointer to the [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) interface.</span></span> <span data-ttu-id="7f26b-108">使用這個指標時，伺服器可以呼叫 **IServerSecurity** 方法，找出用戶端的驗證設定，以及模擬用戶端（如有需要）。</span><span class="sxs-lookup"><span data-stu-id="7f26b-108">With this pointer, **IServerSecurity** methods can be called by the server to find out what the client's authentication settings are and to impersonate the client, if needed.</span></span> <span data-ttu-id="7f26b-109">**IServerSecurity** 物件在所有的執行緒中都是有效的，直到 **IServerSecurity** 所表示的呼叫完成為止。</span><span class="sxs-lookup"><span data-stu-id="7f26b-109">The **IServerSecurity** object is valid on any thread in the apartment until the call represented by **IServerSecurity** completes.</span></span> <span data-ttu-id="7f26b-110">如需模擬的詳細資訊， [請參閱模擬](impersonation.md) 和 [掩蓋](cloaking.md)。</span><span class="sxs-lookup"><span data-stu-id="7f26b-110">For more information about impersonation, see [Impersonation](impersonation.md) and [Cloaking](cloaking.md).</span></span>

<span data-ttu-id="7f26b-111">您也可以使用依賴呼叫內容物件之 [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) 介面實作為的下列 helper 函數：</span><span class="sxs-lookup"><span data-stu-id="7f26b-111">The following helper functions that rely on the call context object's [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) interface implementation are also available:</span></span>

-   [<span data-ttu-id="7f26b-112">**CoQueryClientBlanket**</span><span class="sxs-lookup"><span data-stu-id="7f26b-112">**CoQueryClientBlanket**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket)
-   [<span data-ttu-id="7f26b-113">**CoImpersonateClient**</span><span class="sxs-lookup"><span data-stu-id="7f26b-113">**CoImpersonateClient**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient)
-   [<span data-ttu-id="7f26b-114">**CoRevertToSelf**</span><span class="sxs-lookup"><span data-stu-id="7f26b-114">**CoRevertToSelf**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself)

## <a name="related-topics"></a><span data-ttu-id="7f26b-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="7f26b-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f26b-116">COM 中的安全性</span><span class="sxs-lookup"><span data-stu-id="7f26b-116">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 