---
description: 硬體提供者物件
ms.assetid: d1724219-1487-485b-9c52-5003069fe9e2
title: 硬體提供者物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1aaebf61e97487b48a6b8bf0dbd91cc6aa3e0bd
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2021
ms.locfileid: "106982786"
---
# <a name="hardware-provider-objects"></a><span data-ttu-id="28250-103">硬體提供者物件</span><span class="sxs-lookup"><span data-stu-id="28250-103">Hardware Provider Objects</span></span>

<span data-ttu-id="28250-104">\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]</span><span class="sxs-lookup"><span data-stu-id="28250-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="28250-105">VDS 物件模型包含一組用來查詢和設定硬體提供者實體的物件。</span><span class="sxs-lookup"><span data-stu-id="28250-105">The VDS object model includes a set of objects to query and configure hardware provider entities.</span></span> <span data-ttu-id="28250-106"> (請注意，雖然 VDS 包含軟體提供者，但您必須個別購買硬體提供者和相關聯的硬體，才能利用硬體提供者物件。 ) 這些硬體提供者物件代表實體裝置 (例如子系統、磁片磁碟機和控制器) 以及虛擬裝置 (例如 Lun 和 LUN plex) 。</span><span class="sxs-lookup"><span data-stu-id="28250-106">(Note that while VDS includes a software provider, you must purchase a hardware provider and the associated hardware separately to take advantage of the hardware provider objects.) These hardware provider objects represent physical devices (such as subsystems, drives, and controllers) and virtual devices (such as LUNs and LUN plexes).</span></span>

<span data-ttu-id="28250-107">硬體提供者應該針對每個實體或虛擬裝置建立一個 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="28250-107">A hardware provider should create one COM object for each physical or virtual device.</span></span>

<span data-ttu-id="28250-108">下圖顯示提供者物件與一組硬體提供者物件之間的關聯性，以及各種硬體提供者物件本身之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="28250-108">The illustration that follows shows the relationship between the provider object and the set of hardware provider objects, as well as the relationship between the various hardware provider objects themselves.</span></span>

![<span data-ttu-id="28250-109">顯示「提供者」和「子系統」、「控制器」、「LUN」、「LUN plex」、「磁片磁碟機」和「主軸」之間關聯性的圖表。</span><span class="sxs-lookup"><span data-stu-id="28250-109">Diagram that shows the relationship between the 'Provider' and 'Subsystem', 'Controller', 'LUN', 'LUN plex', 'Drive', and 'Spindle'.</span></span> ](images/vdshwobjects.png)

<span data-ttu-id="28250-110">提供者物件可以包含任何數目的子系統。</span><span class="sxs-lookup"><span data-stu-id="28250-110">A provider object can contain any number of subsystems.</span></span> <span data-ttu-id="28250-111">所有硬體提供者都能夠管理相同子系統模型的多個實例。</span><span class="sxs-lookup"><span data-stu-id="28250-111">All hardware providers are capable of managing multiple instances of the same subsystem model.</span></span> <span data-ttu-id="28250-112">許多硬體提供者也可以管理不同子系統模型的多個實例。</span><span class="sxs-lookup"><span data-stu-id="28250-112">Many hardware providers are also capable of managing multiple instances of different subsystem models.</span></span> <span data-ttu-id="28250-113">單一電腦可以裝載任意數量的硬體提供者。</span><span class="sxs-lookup"><span data-stu-id="28250-113">A single computer can host any number of hardware providers.</span></span>

<span data-ttu-id="28250-114">子系統物件可以包含任意數目的控制器和磁片磁碟機，而且可以呈現任何數目的 Lun。</span><span class="sxs-lookup"><span data-stu-id="28250-114">A subsystem object can contain any number of controllers and drives, and can surface any number of LUNs.</span></span> <span data-ttu-id="28250-115">LUN 物件是由至少一個 LUN plex 組成，而且每個 LUN plex 都對應至一或多個磁片磁碟機（視 plex 類型而定）。</span><span class="sxs-lookup"><span data-stu-id="28250-115">A LUN object comprises of at least one LUN plex, and each LUN plex maps to one or more drives, depending on the plex type.</span></span> <span data-ttu-id="28250-116">控制器物件可以管理任何數目之 LUN 物件的資料輸入/輸出。</span><span class="sxs-lookup"><span data-stu-id="28250-116">Controller objects can manage data input/output for any number of LUN objects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="28250-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="28250-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28250-118">VDS 物件模型</span><span class="sxs-lookup"><span data-stu-id="28250-118">VDS Object Model</span></span>](vds-object-model.md)
</dt> </dl>

 

 
