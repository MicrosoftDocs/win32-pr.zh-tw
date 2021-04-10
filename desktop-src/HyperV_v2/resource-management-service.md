---
description: 資源虛擬化設定檔提供了一種方法，讓用戶端可以探索虛擬化系統所支援的虛擬資源。
ms.assetid: CEF58153-F634-4E32-9C1D-385F1C740314
title: 資源管理服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c405cac60df719195466da6ea0c7aadb7bf0d765
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027365"
---
# <a name="resource-management-service"></a><span data-ttu-id="10888-103">資源管理服務</span><span class="sxs-lookup"><span data-stu-id="10888-103">Resource management service</span></span>

<span data-ttu-id="10888-104">資源虛擬化設定檔提供了一種方法，讓用戶端可以探索虛擬化系統所支援的虛擬資源。</span><span class="sxs-lookup"><span data-stu-id="10888-104">The Resource Virtualization Profile provides the means by which a client can discover the virtual resources supported by the virtualization system.</span></span> <span data-ttu-id="10888-105">它也會描述每種虛擬資源類型支援的容量（或配置數量）。</span><span class="sxs-lookup"><span data-stu-id="10888-105">It also describes the capacity—or number of allocations—that is supported for each type of virtual resource.</span></span> <span data-ttu-id="10888-106">下圖顯示資源虛擬化設定檔。</span><span class="sxs-lookup"><span data-stu-id="10888-106">The following illustration shows the Resource Virtualization Profile.</span></span>

![資源虛擬化設定檔](images/resourcemanagement.png)

<span data-ttu-id="10888-108">資源虛擬化設定檔會定義兩個不同類別的虛擬資源：</span><span class="sxs-lookup"><span data-stu-id="10888-108">Two different classes of virtual resources are defined by the Resource Virtualization Profile:</span></span>

-   <span data-ttu-id="10888-109">共用資源：代表主機的資源，也就是能夠在多部虛擬機器之間共用的資源。</span><span class="sxs-lookup"><span data-stu-id="10888-109">Shared Resource: Represents the resources of the host that are, or are capable of being shared among multiple virtual machines.</span></span> <span data-ttu-id="10888-110">[**Msvm \_處理器**](msvm-processor.md) 是共用資源的範例。</span><span class="sxs-lookup"><span data-stu-id="10888-110">[**Msvm\_Processor**](msvm-processor.md) is an example of a shared resource.</span></span>
-   <span data-ttu-id="10888-111">綜合資源：代表沒有對應主機資源的虛擬資源。</span><span class="sxs-lookup"><span data-stu-id="10888-111">Synthetic Resource: Represents the virtual resources that have no corresponding host resource.</span></span> <span data-ttu-id="10888-112">[**Msvm \_EmulatedEthernetPort**](msvm-emulatedethernetport.md) 是綜合資源的範例。</span><span class="sxs-lookup"><span data-stu-id="10888-112">[**Msvm\_EmulatedEthernetPort**](msvm-emulatedethernetport.md) is an example of a synthetic resource.</span></span>

<span data-ttu-id="10888-113">資源集區可用來收集主機資源的類別，以便在中央位置描述其功能和設定時可以輕鬆地找到。</span><span class="sxs-lookup"><span data-stu-id="10888-113">The resource pool is used to collect a class of host resources so that it can be easily discovered while its capabilities and settings can be described in a central location.</span></span> <span data-ttu-id="10888-114">「基本」或「高階」的實作為所收集資源的執行方式沒有任何限制。</span><span class="sxs-lookup"><span data-stu-id="10888-114">There is no limit to how basic or advanced an implementation of the collected resource can be.</span></span>

<span data-ttu-id="10888-115">從資源集區中，用戶端可以存取 (AC) 的相關聯配置功能。</span><span class="sxs-lookup"><span data-stu-id="10888-115">From the resource pool, the client may access the associated Allocation Capabilities (AC).</span></span> <span data-ttu-id="10888-116">此類別說明此資源集區所描述之資源的功能。</span><span class="sxs-lookup"><span data-stu-id="10888-116">This class describes the capabilities of the resource described by this resource pool.</span></span> <span data-ttu-id="10888-117">例如，它可能會指出此資源集區所代表的 [**Msvm \_ EmulatedEthernetPort**](msvm-emulatedethernetport.md) 是否支援 (vlan) 或篩選器的虛擬 lan。</span><span class="sxs-lookup"><span data-stu-id="10888-117">For instance, it may indicate whether the [**Msvm\_EmulatedEthernetPort**](msvm-emulatedethernetport.md) represented by this resource pool supports virtual LANs (VLANs) or filters.</span></span>

<span data-ttu-id="10888-118">AC 設定檔會定義用戶端可以探索指定虛擬資源之有效範圍和預設設定的方式。</span><span class="sxs-lookup"><span data-stu-id="10888-118">The AC Profile defines the means by which a client can discover the valid range of and default settings for a given virtual resource.</span></span> <span data-ttu-id="10888-119">AC 物件與每個資源集區相關聯。</span><span class="sxs-lookup"><span data-stu-id="10888-119">An AC object is associated with each resource pool.</span></span> <span data-ttu-id="10888-120">四個資源配置設定資料 (RASD) 物件與 AC 物件相關聯，以描述所指定資源配置的最小值、最大值、預設值和增量值。</span><span class="sxs-lookup"><span data-stu-id="10888-120">Four Resource Allocation Setting Data (RASD) objects are associated with the AC object to describe the minimum, maximum, default and incremental values for the given resource's allocation.</span></span> <span data-ttu-id="10888-121">這些類別一起描述支援功能的整體範圍。</span><span class="sxs-lookup"><span data-stu-id="10888-121">Together, these classes describe the overall range of supported capabilities.</span></span> <span data-ttu-id="10888-122">[**Msvm \_ AllocationCapabilities**](msvm-allocationcapabilities.md)實例提供一組 [**Msvm \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md)實例的錨點，這些實例會指定虛擬資源的預設和有效的設定範圍。</span><span class="sxs-lookup"><span data-stu-id="10888-122">The [**Msvm\_AllocationCapabilities**](msvm-allocationcapabilities.md) instance provides an anchor point for the set of [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) instances that specify the default and valid range of settings for a virtual resource.</span></span> <span data-ttu-id="10888-123">[**Msvm \_ SettingsDefineCapabilities**](msvm-settingsdefinecapabilities.md) association 類別提供了虛擬化平臺所支援之資源的 AC 實例與最小值、最大值、增量和預設設定之間的連結。</span><span class="sxs-lookup"><span data-stu-id="10888-123">The [**Msvm\_SettingsDefineCapabilities**](msvm-settingsdefinecapabilities.md) association class provides the link between the AC instance and the minimum, maximum, incremental and default settings for a resource supported by the virtualization platform.</span></span>

 

 



