---
title: COM 伺服器責任
description: COM 伺服器責任
ms.assetid: 9853bbf5-b989-45b7-8fa8-8cd2f0d48d3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86b9d3104af80a7b2dca49dbbd5b55e66a613ee7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382958"
---
# <a name="com-server-responsibilities"></a><span data-ttu-id="dc752-103">COM 伺服器責任</span><span class="sxs-lookup"><span data-stu-id="dc752-103">COM Server Responsibilities</span></span>

<span data-ttu-id="dc752-104">用戶端若要取得物件指標，最重要的方法之一就是讓用戶端要求啟動伺服器，並建立和啟動伺服器所提供的物件實例。</span><span class="sxs-lookup"><span data-stu-id="dc752-104">One of the most important ways for a client to get a pointer to an object is for the client to ask that a server be launched and that an instance of the object provided by the server be created and activated.</span></span> <span data-ttu-id="dc752-105">這是伺服器的責任，可確保正常運作。</span><span class="sxs-lookup"><span data-stu-id="dc752-105">It is the responsibility of the server to ensure that this happens properly.</span></span> <span data-ttu-id="dc752-106">這有幾個重要的部分。</span><span class="sxs-lookup"><span data-stu-id="dc752-106">There are several important parts to this.</span></span>

<span data-ttu-id="dc752-107">伺服器必須透過 [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) 或 [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) 介面的實執行類別物件的程式碼。</span><span class="sxs-lookup"><span data-stu-id="dc752-107">The server must implement code for a class object through an implementation of either the [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) or [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) interface.</span></span>

<span data-ttu-id="dc752-108">伺服器必須在其所在電腦上的系統登錄中登錄其 CLSID，並且可選擇將其電腦位置發佈到網路上的其他系統，以允許用戶端呼叫它，而不需要用戶端知道伺服器的位置。</span><span class="sxs-lookup"><span data-stu-id="dc752-108">The server must register its CLSID in the system registry on the machine on which it resides and further, has the option of publishing its machine location to other systems on a network to allow clients to call it without requiring the client to know the server's location.</span></span>

<span data-ttu-id="dc752-109">伺服器主要負責安全性;亦即，在大部分的情況下，伺服器會決定是否要將其一個物件的指標提供給用戶端。</span><span class="sxs-lookup"><span data-stu-id="dc752-109">The server is primarily responsible for security; that is, for the most part, the server determines whether it will provide a pointer to one of its objects to a client.</span></span>

<span data-ttu-id="dc752-110">同進程伺服器應該會執行並匯出某些函數，讓用戶端進程具現化它們。</span><span class="sxs-lookup"><span data-stu-id="dc752-110">In-process servers should implement and export certain functions that allow the client process to instantiate them.</span></span>

<span data-ttu-id="dc752-111">下列主題將詳細說明 COM 伺服器的職責：</span><span class="sxs-lookup"><span data-stu-id="dc752-111">The following topics detail the responsibilities of the COM server:</span></span>

-   [<span data-ttu-id="dc752-112">執行 IClassFactory</span><span class="sxs-lookup"><span data-stu-id="dc752-112">Implementing IClassFactory</span></span>](implementing-iclassfactory.md)
-   [<span data-ttu-id="dc752-113">授權和 IClassFactory2</span><span class="sxs-lookup"><span data-stu-id="dc752-113">Licensing and IClassFactory2</span></span>](licensing-and-iclassfactory2.md)
-   [<span data-ttu-id="dc752-114">註冊 COM 伺服器</span><span class="sxs-lookup"><span data-stu-id="dc752-114">Registering COM Servers</span></span>](registering-com-servers.md)
-   [<span data-ttu-id="dc752-115">跨進程伺服器執行協助程式</span><span class="sxs-lookup"><span data-stu-id="dc752-115">Out-of-Process Server Implementation Helpers</span></span>](out-of-process-server-implementation-helpers.md)
-   [<span data-ttu-id="dc752-116">建立和優化 GUID</span><span class="sxs-lookup"><span data-stu-id="dc752-116">GUID Creation and Optimizations</span></span>](guid-creation-and-optimizations.md)

## <a name="related-topics"></a><span data-ttu-id="dc752-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="dc752-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc752-118">COM 用戶端和伺服器</span><span class="sxs-lookup"><span data-stu-id="dc752-118">COM Clients and Servers</span></span>](com-clients-and-servers.md)
</dt> </dl>

 

 