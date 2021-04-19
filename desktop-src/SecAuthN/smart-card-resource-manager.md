---
description: 智慧卡 Resource Manager
ms.assetid: 96434996-88fa-47d3-bb44-3ebb23610b27
title: 智慧卡 Resource Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c3ee8e0bf311539863502d3e789544717e6dff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987718"
---
# <a name="smart-card-resource-manager"></a><span data-ttu-id="7f5f5-103">智慧卡 Resource Manager</span><span class="sxs-lookup"><span data-stu-id="7f5f5-103">Smart Card Resource Manager</span></span>

<span data-ttu-id="7f5f5-104">[*智慧卡*](../secgloss/s-gly.md)[*資源管理員*](../secgloss/r-gly.md)管理對 [*讀者*](../secgloss/r-gly.md)和 *智慧卡* 的存取。</span><span class="sxs-lookup"><span data-stu-id="7f5f5-104">The [*smart card*](../secgloss/s-gly.md) [*resource manager*](../secgloss/r-gly.md) manages access to [*readers*](../secgloss/r-gly.md) and to *smart cards*.</span></span> <span data-ttu-id="7f5f5-105">為了管理這些資源，它會執行下列功能。</span><span class="sxs-lookup"><span data-stu-id="7f5f5-105">To manage these resources, it performs the following functions.</span></span>

-   <span data-ttu-id="7f5f5-106">識別和追蹤資源。</span><span class="sxs-lookup"><span data-stu-id="7f5f5-106">Identifies and tracks resources.</span></span>
-   <span data-ttu-id="7f5f5-107">跨多個應用程式分配讀取器和資源。</span><span class="sxs-lookup"><span data-stu-id="7f5f5-107">Allocates readers and resources across multiple applications.</span></span>
-   <span data-ttu-id="7f5f5-108">支援存取指定卡片上可用之服務的 [*交易*](../secgloss/t-gly.md) 基本專案。</span><span class="sxs-lookup"><span data-stu-id="7f5f5-108">Supports [*transaction*](../secgloss/t-gly.md) primitives for accessing services available on a given card.</span></span>
    > [!Note]  
    > <span data-ttu-id="7f5f5-109">這是很重要的一點，因為目前的卡片是單一執行緒裝置，通常需要執行多個命令才能完成單一函式。</span><span class="sxs-lookup"><span data-stu-id="7f5f5-109">This is an important point because current cards are single-threaded devices that often require the execution of multiple commands to complete a single function.</span></span> <span data-ttu-id="7f5f5-110">[*交易*](../secgloss/t-gly.md) 可讓您在不中斷的情況下執行多個命令，以確保中繼 [*狀態*](../secgloss/s-gly.md) 資訊未損毀。</span><span class="sxs-lookup"><span data-stu-id="7f5f5-110">[*Transactions*](../secgloss/t-gly.md) allow multiple commands to be executed without interruption, ensuring that intermediate [*state*](../secgloss/s-gly.md) information is not corrupted.</span></span>

     

<span data-ttu-id="7f5f5-111">您可以透過 resource manager API 直接存取資源管理員，或透過任何智慧卡 [*服務提供者*](../secgloss/s-gly.md)間接存取資源管理員。</span><span class="sxs-lookup"><span data-stu-id="7f5f5-111">The resource manager can be accessed directly by way of the resource manager API or indirectly through any smart card [*service provider*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="7f5f5-112">資源管理員 API 是一組 Windows 功能，可直接存取 resource manager 的服務。</span><span class="sxs-lookup"><span data-stu-id="7f5f5-112">The resource manager API is a set of Windows functions that provide direct access to the resource manager's services.</span></span> <span data-ttu-id="7f5f5-113">如需 API 所提供的 Windows 函式總覽，請參閱 [智慧卡 RESOURCE MANAGER api](smart-card-resource-manager-api.md)。</span><span class="sxs-lookup"><span data-stu-id="7f5f5-113">For an overview of the Windows functions provided by the API, see [Smart Card Resource Manager API](smart-card-resource-manager-api.md).</span></span> <span data-ttu-id="7f5f5-114">相較之下，智慧卡服務提供者會使用 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="7f5f5-114">In comparison, smart card service providers use COM interfaces.</span></span>

<span data-ttu-id="7f5f5-115">資源管理員 API 中的許多 Windows 函式在智慧卡服務提供者的 COM 介面的屬性和方法中都有對等專案。</span><span class="sxs-lookup"><span data-stu-id="7f5f5-115">Many of the Windows functions in the resource manager API have equivalents in the properties and methods of the smart card service providers' COM interfaces.</span></span> <span data-ttu-id="7f5f5-116">雖然大部分的應用程式開發人員會發現 COM 更容易使用，但有些應用程式仍然需要使用 Windows 功能來執行某些工作。</span><span class="sxs-lookup"><span data-stu-id="7f5f5-116">And although most application developers will find COM easier to work with, some applications will still need to use the Windows functions to perform certain tasks.</span></span> <span data-ttu-id="7f5f5-117">例如，需要操作 [*智慧卡資料庫*](../secgloss/s-gly.md)中讀取器或讀者群組清單的應用程式，以及需要直接控制讀取器的應用程式，都必須使用 RESOURCE manager API。</span><span class="sxs-lookup"><span data-stu-id="7f5f5-117">For example, applications that need to manipulate the list of readers or reader groups in the [*smart card database*](../secgloss/s-gly.md), and those that need direct control of a reader, must use the resource manager API.</span></span> <span data-ttu-id="7f5f5-118">提供這些功能的服務僅適用于 Windows 函式，而不是在服務提供者提供的 COM 中。</span><span class="sxs-lookup"><span data-stu-id="7f5f5-118">The services that provide these capabilities are available only in the Windows functions, not in the COM provided by the service providers.</span></span>

<span data-ttu-id="7f5f5-119">如需有關如何在 Windows 中執行 [*資源管理員*](../secgloss/r-gly.md) 的詳細資訊，請參閱 [Resource Manager 執行](resource-manager-implementation.md)。</span><span class="sxs-lookup"><span data-stu-id="7f5f5-119">For information about how the [*resource manager*](../secgloss/r-gly.md) is implemented in Windows, see [Resource Manager Implementation](resource-manager-implementation.md).</span></span>

 

 
