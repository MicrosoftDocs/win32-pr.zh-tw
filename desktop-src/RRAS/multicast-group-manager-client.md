---
title: 多播群組管理員用戶端
description: 用戶端是呼叫 MGM 函數的實體，例如路由通訊協定或系統管理應用程式。
ms.assetid: 98d13b48-9f1d-4649-a5a3-03926c7facee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4a5f2a8ba63903c084547e3d04ea04474171651
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675576"
---
# <a name="multicast-group-manager-client"></a><span data-ttu-id="80f4d-103">多播群組管理員用戶端</span><span class="sxs-lookup"><span data-stu-id="80f4d-103">Multicast Group Manager Client</span></span>

<span data-ttu-id="80f4d-104">用戶端是呼叫 MGM 函數的實體，例如路由通訊協定或系統管理應用程式。</span><span class="sxs-lookup"><span data-stu-id="80f4d-104">A client is an entity that calls an MGM function, such as a routing protocol or an administrative application.</span></span>

<span data-ttu-id="80f4d-105">MGM API 主要是由多播路由通訊協定使用。</span><span class="sxs-lookup"><span data-stu-id="80f4d-105">The MGM API is used primarily by multicast routing protocols.</span></span> <span data-ttu-id="80f4d-106">多播路由通訊協定的開發人員會使用 MGM API 來：</span><span class="sxs-lookup"><span data-stu-id="80f4d-106">Developers of multicast routing protocols use the MGM API to:</span></span>

-   <span data-ttu-id="80f4d-107">維護群組成員資格</span><span class="sxs-lookup"><span data-stu-id="80f4d-107">Maintain group membership</span></span>
-   <span data-ttu-id="80f4d-108">控制介面擁有權</span><span class="sxs-lookup"><span data-stu-id="80f4d-108">Control interface ownership</span></span>
-   <span data-ttu-id="80f4d-109">從多播群組管理員接收有關多播資料的其他多播路由通訊協定要求的通知</span><span class="sxs-lookup"><span data-stu-id="80f4d-109">Receive notifications from the multicast group manager regarding other multicast routing protocols' requests for multicast data</span></span>

<span data-ttu-id="80f4d-110">必須監視多播轉送專案的特定系統管理應用程式 (MFEs) 可以這麼做，而不需要新增或移除群組成員資格。</span><span class="sxs-lookup"><span data-stu-id="80f4d-110">Specific administrative applications that must monitor multicast forwarding entries (MFEs) can do so without adding or removing group membership.</span></span> <span data-ttu-id="80f4d-111">系統管理應用程式開發人員會使用特定的 MGM 函式來檢查 MFEs 中的資訊。</span><span class="sxs-lookup"><span data-stu-id="80f4d-111">Administrative application developers use specific MGM functions to review information in MFEs.</span></span>

> [!Note]  
> <span data-ttu-id="80f4d-112">多播路由通訊協定也會存取 MFEs。</span><span class="sxs-lookup"><span data-stu-id="80f4d-112">Multicast routing protocols also access MFEs.</span></span>

 

<span data-ttu-id="80f4d-113">MFE 是「多播群組管理員」依據群組成員資格建立的轉送資訊。</span><span class="sxs-lookup"><span data-stu-id="80f4d-113">An MFE is forwarding information that the multicast group manager creates based on group membership.</span></span> <span data-ttu-id="80f4d-114">從多播群組管理員中取出的 MFEs 可以提供統計資訊。</span><span class="sxs-lookup"><span data-stu-id="80f4d-114">The MFEs that are retrieved from the multicast group manager can provide statistical information.</span></span> <span data-ttu-id="80f4d-115">系統管理應用程式接著可以使用此資訊來判斷適當的動作。</span><span class="sxs-lookup"><span data-stu-id="80f4d-115">An administrative application can then use this information to determine the appropriate actions.</span></span> <span data-ttu-id="80f4d-116">例如，系統管理應用程式可以根據特定介面上的封包量來執行動作。</span><span class="sxs-lookup"><span data-stu-id="80f4d-116">For example, an administrative application could perform actions that are based on the volume of packets on a specific interface.</span></span>

 

 




