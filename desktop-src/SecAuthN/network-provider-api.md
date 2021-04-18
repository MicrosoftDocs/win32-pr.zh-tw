---
description: 網路提供者是一種 DLL，可讓 Windows 作業系統與其他種類的網路（例如 Novell）進行互動。 它是 Windows WNet 驅動程式的用戶端。
ms.assetid: d316f159-4fe3-4b78-9efc-177906875918
title: 網路提供者 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc68184f60639a603614cbaf71631a2521012cf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978074"
---
# <a name="network-provider-api"></a><span data-ttu-id="d3f44-104">網路提供者 API</span><span class="sxs-lookup"><span data-stu-id="d3f44-104">Network Provider API</span></span>

<span data-ttu-id="d3f44-105">網路提供者是一種 DLL，可讓 Windows 作業系統與其他種類的網路（例如 Novell）進行互動。</span><span class="sxs-lookup"><span data-stu-id="d3f44-105">A network provider is a DLL that enables the Windows operating system to interact with other kinds of networks, such as Novell.</span></span> <span data-ttu-id="d3f44-106">它是 Windows WNet 驅動程式的用戶端。</span><span class="sxs-lookup"><span data-stu-id="d3f44-106">It is a client of the Windows WNet driver.</span></span> <span data-ttu-id="d3f44-107">網路提供者會執行網路特定的動作，例如建立連線，並公開 Windows 的通用介面。</span><span class="sxs-lookup"><span data-stu-id="d3f44-107">A network provider implements network-specific actions, such as making a connection, and exposes a common interface to Windows.</span></span> <span data-ttu-id="d3f44-108">此介面稱為網路提供者 API，並由網路提供者所執行的函式所組成。</span><span class="sxs-lookup"><span data-stu-id="d3f44-108">This interface is called the Network Provider API and consists of functions implemented by the network provider.</span></span> <span data-ttu-id="d3f44-109">您可以建立網路提供者 DLL 來支援新的網路通訊協定。</span><span class="sxs-lookup"><span data-stu-id="d3f44-109">You can create a network provider DLL to support new network protocols.</span></span>

<span data-ttu-id="d3f44-110">由於每個網路都會透過其提供者公開通用介面，因此 Windows 可以與數種網路類型互動，而不需要知道其網路特定的執行詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d3f44-110">Because each network exposes a common interface through its provider, Windows can interact with several types of networks without knowing their network-specific implementation details.</span></span>

<span data-ttu-id="d3f44-111">[*多個提供者路由器*](../secgloss/m-gly.md) (MPR) 處理與系統上所有不同網路提供者的通訊，並向使用者呈現整合的網路。</span><span class="sxs-lookup"><span data-stu-id="d3f44-111">The [*Multiple Provider Router*](../secgloss/m-gly.md) (MPR) handles communication with all of the various network providers on the system and presents an integrated network to the user.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3f44-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="d3f44-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3f44-113">網路提供者</span><span class="sxs-lookup"><span data-stu-id="d3f44-113">Network Providers</span></span>](network-providers.md)
</dt> <dt>

[<span data-ttu-id="d3f44-114">認證管理員</span><span class="sxs-lookup"><span data-stu-id="d3f44-114">Credential Manager</span></span>](credential-manager.md)
</dt> <dt>

[<span data-ttu-id="d3f44-115">多個提供者路由器</span><span class="sxs-lookup"><span data-stu-id="d3f44-115">Multiple Provider Router</span></span>](multiple-provider-router.md)
</dt> <dt>

[<span data-ttu-id="d3f44-116">網路提供者所執行的函式</span><span class="sxs-lookup"><span data-stu-id="d3f44-116">Functions Implemented by Network Providers</span></span>](functions-implemented-by-network-providers.md)
</dt> <dt>

[<span data-ttu-id="d3f44-117">認證管理 API</span><span class="sxs-lookup"><span data-stu-id="d3f44-117">Credential Management API</span></span>](credential-management-api.md)
</dt> <dt>

[<span data-ttu-id="d3f44-118">連接通知 API</span><span class="sxs-lookup"><span data-stu-id="d3f44-118">Connection Notification API</span></span>](connection-notification-api.md)
</dt> </dl>

 

 
