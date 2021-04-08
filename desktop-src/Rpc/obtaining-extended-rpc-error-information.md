---
title: 取得延伸的 RPC 錯誤資訊
description: RPC 提供取得延伸錯誤資訊的功能。 本節說明如何取得這類錯誤資訊，以及提供如何使用資訊的建議。
ms.assetid: 7a386def-c640-42f4-9869-b6a1c522984a
keywords:
- 遠端程序呼叫 RPC、最佳作法、延伸錯誤資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7856dd76a86763fc3f537577f9c547508fbf34ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673144"
---
# <a name="obtaining-extended-rpc-error-information"></a><span data-ttu-id="63809-105">取得延伸的 RPC 錯誤資訊</span><span class="sxs-lookup"><span data-stu-id="63809-105">Obtaining Extended RPC Error Information</span></span>

<span data-ttu-id="63809-106">RPC 提供取得延伸錯誤資訊的功能。</span><span class="sxs-lookup"><span data-stu-id="63809-106">RPC provides the capability to obtain extended error information.</span></span> <span data-ttu-id="63809-107">本節說明如何取得這類錯誤資訊，以及提供如何使用資訊的建議。</span><span class="sxs-lookup"><span data-stu-id="63809-107">This section describes how such error information can be obtained, and offers recommendations on how to use the information.</span></span>

<span data-ttu-id="63809-108">本節分為下列主題：</span><span class="sxs-lookup"><span data-stu-id="63809-108">This section is broken into the following topics:</span></span>

-   [<span data-ttu-id="63809-109">擴充錯誤資訊的需求</span><span class="sxs-lookup"><span data-stu-id="63809-109">The Need For Extended Error Information</span></span>](the-need-for-extended-error-information.md)
-   [<span data-ttu-id="63809-110">安全性和延伸錯誤資訊</span><span class="sxs-lookup"><span data-stu-id="63809-110">Security and Extended Error Information</span></span>](security-and-extended-error-information.md)
-   [<span data-ttu-id="63809-111">啟用延伸的錯誤資訊</span><span class="sxs-lookup"><span data-stu-id="63809-111">Enabling Extended Error Information</span></span>](enabling-extended-error-information.md)
-   [<span data-ttu-id="63809-112">瞭解延伸的錯誤資訊</span><span class="sxs-lookup"><span data-stu-id="63809-112">Understanding Extended Error Information</span></span>](understanding-extended-error-information.md)
-   [<span data-ttu-id="63809-113">擴充錯誤資訊的可靠性</span><span class="sxs-lookup"><span data-stu-id="63809-113">Reliability of Extended Error Information</span></span>](reliability-of-extended-error-information.md)
-   [<span data-ttu-id="63809-114">與其他元件的獨立性</span><span class="sxs-lookup"><span data-stu-id="63809-114">Independence From Other Components</span></span>](independence-from-other-components.md)
-   [<span data-ttu-id="63809-115">使用者的延伸錯誤資訊</span><span class="sxs-lookup"><span data-stu-id="63809-115">Extended Error Information for the User</span></span>](extended-error-information-for-the-user.md)
-   [<span data-ttu-id="63809-116">伺服器或應用程式的延伸錯誤資訊</span><span class="sxs-lookup"><span data-stu-id="63809-116">Extended Error Information for the Server or Application</span></span>](extended-error-information-for-the-server-or-application.md)
-   [<span data-ttu-id="63809-117">擴充錯誤資訊偵測位置</span><span class="sxs-lookup"><span data-stu-id="63809-117">Extended Error Information Detection Locations</span></span>](extended-error-information-detection-locations.md)

<span data-ttu-id="63809-118">本節與 RPC 應用程式的偵錯工具密切相關。</span><span class="sxs-lookup"><span data-stu-id="63809-118">This section is closely tied with RPC application debugging.</span></span> <span data-ttu-id="63809-119">如需 RPC 偵錯工具的詳細資訊，請參閱 \[ 偵錯工具封裝 \] 。</span><span class="sxs-lookup"><span data-stu-id="63809-119">For additional information about RPC debugging, see \[debugger package\].</span></span>

 

 




