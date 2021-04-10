---
title: RPC 和 COM 的版本控制理論
description: 遠端程序呼叫的版本設定理論 (RPC) 和 COM。
ms.assetid: c4df0a7b-e1be-481d-9149-317ffc9179b9
keywords:
- 遠端程序呼叫 RPC、最佳作法、版本控制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e03b23c91bf69fbc3c4f72366b80812fd54330d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093076"
---
# <a name="the-versioning-theory-for-rpc-and-com"></a><span data-ttu-id="53909-104">RPC 和 COM 的版本控制理論</span><span class="sxs-lookup"><span data-stu-id="53909-104">The Versioning Theory for RPC and COM</span></span>

<span data-ttu-id="53909-105">只有兩個完全萬無一失的方法支援新功能，而不會有網路相容性問題的風險：</span><span class="sxs-lookup"><span data-stu-id="53909-105">Only two completely foolproof methods support new functionality without risk of wire compatibility problems:</span></span>

-   <span data-ttu-id="53909-106">根據規則變更介面版本;這可防止新的用戶端與舊的伺服器通訊，而且可能會防止舊的用戶端與新的伺服器通訊。</span><span class="sxs-lookup"><span data-stu-id="53909-106">Change the interface version according to the rules; this prevents new clients from communicating with an old server, and may or may not prevent an old client from communicating with the new server.</span></span> <span data-ttu-id="53909-107">本節稍後會說明這一點。</span><span class="sxs-lookup"><span data-stu-id="53909-107">This is clarified later in this section.</span></span>
-   <span data-ttu-id="53909-108">引進處理新功能的不同介面。</span><span class="sxs-lookup"><span data-stu-id="53909-108">Introduce a different interface dealing with the new functionality.</span></span>

<span data-ttu-id="53909-109">標準 RPC 介面可透過 GUID 和版本號碼組合來識別;COM 介面是由其 GUID 識別。</span><span class="sxs-lookup"><span data-stu-id="53909-109">A standard RPC interface is identified by a GUID and version number combination; a COM interface is identified by its GUID.</span></span> <span data-ttu-id="53909-110">版本包含主要和次要部分。</span><span class="sxs-lookup"><span data-stu-id="53909-110">The version consists of major and minor parts.</span></span> <span data-ttu-id="53909-111">如果是具有相同 GUID 和不同版本號碼的標準介面，則只有在主要版本相同，而且用戶端不是高於伺服器的次要版本時，才有可能連接。</span><span class="sxs-lookup"><span data-stu-id="53909-111">For standard interfaces with the same GUID and different version numbers, a connection is possible only when the major version is the same, and the client is not higher than the minor version of the server.</span></span>

<span data-ttu-id="53909-112">結果是變更 RPC 介面的 GUID 中斷連線相容性，而變更介面名稱則否。</span><span class="sxs-lookup"><span data-stu-id="53909-112">A consequence is that changing the RPC interface GUID breaks wire compatibility, while changing the interface name does not.</span></span>

<span data-ttu-id="53909-113">在標準 RPC 中，已妥善定義升級和延伸模組的路徑，而且基本上需要在介面結尾新增新的方法，而新的類型只能在新的方法中使用。</span><span class="sxs-lookup"><span data-stu-id="53909-113">In standard RPC, a path for upgrades and extensions is well defined, and basically requires that new methods only be added at the end of the interface, and new types be used only in the new methods.</span></span> <span data-ttu-id="53909-114">如果需要這類新增專案，則必須增加次要版本。</span><span class="sxs-lookup"><span data-stu-id="53909-114">If such additions are needed, the minor version must be increased.</span></span> <span data-ttu-id="53909-115">任何其他變更都需要主要版本的變更，因為用戶端和伺服器軟體在網路上會不相容。</span><span class="sxs-lookup"><span data-stu-id="53909-115">Any other change requires a change in the major version, because the client and server software would be incompatible on the wire.</span></span> <span data-ttu-id="53909-116">遵循這些規則可確保新用戶端與舊伺服器之間有連接，反之亦然，雙方都完全相容。</span><span class="sxs-lookup"><span data-stu-id="53909-116">Adhering to these rules assures whenever there is a connection between a new client and old server, or vice-versa, both sides are fully compatible.</span></span>

<span data-ttu-id="53909-117">如果是 COM 介面，則無法使用 version 屬性。</span><span class="sxs-lookup"><span data-stu-id="53909-117">For a COM interface, the version attribute cannot be used.</span></span> <span data-ttu-id="53909-118">建立新的介面並繼承自舊介面，相當於在 RPC 中操作版本。</span><span class="sxs-lookup"><span data-stu-id="53909-118">Creating new interfaces and inheriting from the old interfaces is an equivalent of manipulating the version in RPC.</span></span> <span data-ttu-id="53909-119">一般而言，COM 的最佳方法是為擴充的功能建立新的介面。</span><span class="sxs-lookup"><span data-stu-id="53909-119">Typically, the best approach in COM is to create a new interface for the expanded functionality.</span></span> <span data-ttu-id="53909-120">次要版本相當於繼承自舊版本的新介面。</span><span class="sxs-lookup"><span data-stu-id="53909-120">An equivalent of the minor version is the new interface inheriting from the old one.</span></span> <span data-ttu-id="53909-121">變更舊的方法或舊的資料類型需要全新的 COM 介面，此介面不會繼承自舊的介面。</span><span class="sxs-lookup"><span data-stu-id="53909-121">Changing old methods or old data types requires an entirely new COM interface—an interface that does not inherit from the old one.</span></span>

<span data-ttu-id="53909-122">針對 COM， [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 函式是一種已建立的方法，可檢查伺服器是否支援介面;因此，可以輕鬆地解析用戶端可以與舊版本或新版介面互動的情況。</span><span class="sxs-lookup"><span data-stu-id="53909-122">For COM, the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) function is an established method of checking whether a server supports an interface; hence, the situations where a client can talk to an old or a new version of an interface can be easily resolved.</span></span>

 

 