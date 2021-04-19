---
description: 控制器埠物件
ms.assetid: 5f94bcdc-93ab-4522-88bd-009a049b5dc9
title: 控制器埠物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7547581358bd79212b1093384ce1589e331f6ee0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974023"
---
# <a name="controller-port-object"></a><span data-ttu-id="93fc2-103">控制器埠物件</span><span class="sxs-lookup"><span data-stu-id="93fc2-103">Controller Port Object</span></span>

<span data-ttu-id="93fc2-104">\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]</span><span class="sxs-lookup"><span data-stu-id="93fc2-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="93fc2-105">控制器埠物件會建立子系統中控制器埠的模型。</span><span class="sxs-lookup"><span data-stu-id="93fc2-105">A controller port object models a controller port in a subsystem.</span></span> <span data-ttu-id="93fc2-106">主機電腦可以透過控制器埠寫入和讀取 Lun。</span><span class="sxs-lookup"><span data-stu-id="93fc2-106">Host computers can write to and read from LUNs through controller ports.</span></span> <span data-ttu-id="93fc2-107">控制器埠是由子系統中的控制器所包含。</span><span class="sxs-lookup"><span data-stu-id="93fc2-107">Controller ports are contained by controllers in a subsystem.</span></span> <span data-ttu-id="93fc2-108">在 VDS 1.1 和 VDS 2.0 中，每個子系統的控制器埠都會設定為 [作用中] 或 [非使用中] （相對於子系統所呈現的每個 Lun）。</span><span class="sxs-lookup"><span data-stu-id="93fc2-108">In VDS 1.1 and VDS2.0, each of a subsystem's controller ports is set to either active or inactive in relation to each of the LUNs the subsystem surfaces.</span></span> <span data-ttu-id="93fc2-109">然後，單一控制器埠可以同時設定為 [作用中]，讓某個 LUN 與其他 LUN 保持為作用中狀態。</span><span class="sxs-lookup"><span data-stu-id="93fc2-109">A single controller port, then, can be simultaneously set to active for one LUN and inactive for others.</span></span> <span data-ttu-id="93fc2-110">針對指定 LUN 使用的控制器埠，負責處理 LUN 的輸入和輸出。</span><span class="sxs-lookup"><span data-stu-id="93fc2-110">A controller port that is active for a given LUN carries responsibility for handling input to and output from the LUN.</span></span>

<span data-ttu-id="93fc2-111">作用中控制器埠可作為光纖通道硬體提供者中 MPIO 路徑的其中一個端點，可在此設定負載平衡原則。</span><span class="sxs-lookup"><span data-stu-id="93fc2-111">Active controller ports serve as one of the endpoints of MPIO paths in Fibre Channel hardware providers, upon which load balancing policies can be imposed.</span></span>

<span data-ttu-id="93fc2-112">使用 [**IVdsControllerControllerPort：： QueryControllerPorts**](/windows/desktop/api/Vds/nf-vds-ivdscontrollercontrollerport-querycontrollerports) 方法來判斷特定控制器所包含的控制器埠。</span><span class="sxs-lookup"><span data-stu-id="93fc2-112">Use the [**IVdsControllerControllerPort::QueryControllerPorts**](/windows/desktop/api/Vds/nf-vds-ivdscontrollercontrollerport-querycontrollerports) method to determine the controller ports that are contained by a specific controller.</span></span> <span data-ttu-id="93fc2-113">呼叫端可以從 **QueryControllerPorts** 方法所傳回的列舉中選取所需的控制器埠物件，以取得特定控制器埠的指標。</span><span class="sxs-lookup"><span data-stu-id="93fc2-113">Callers can get a pointer to a specific controller port by selecting the desired controller port object from the enumeration that is returned by the **QueryControllerPorts** method.</span></span> <span data-ttu-id="93fc2-114">使用控制器物件，呼叫端可以設定控制器埠狀態，並查詢其相關聯的 Lun。</span><span class="sxs-lookup"><span data-stu-id="93fc2-114">With a controller object, a caller can set the controller port status and query for its associated LUNs.</span></span>

<span data-ttu-id="93fc2-115">控制器物件屬性包括物件識別碼、名稱、序號和控制器埠狀態。</span><span class="sxs-lookup"><span data-stu-id="93fc2-115">Controller object properties include an object identifier, a name, a serial number, and the controller port status.</span></span>

<span data-ttu-id="93fc2-116">下表列出相關的介面、列舉和結構。</span><span class="sxs-lookup"><span data-stu-id="93fc2-116">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="93fc2-117">類型</span><span class="sxs-lookup"><span data-stu-id="93fc2-117">Type</span></span>                                                                                              | <span data-ttu-id="93fc2-118">元素</span><span class="sxs-lookup"><span data-stu-id="93fc2-118">Element</span></span>                                                                                               |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93fc2-119">只有在 VDS 1.1 和2.0 光纖通道提供者中，此物件一律公開的介面</span><span class="sxs-lookup"><span data-stu-id="93fc2-119">Interfaces that are always exposed by this object in VDS 1.1 and 2.0 Fibre Channel providers only</span></span> | [<span data-ttu-id="93fc2-120">**IVdsControllerPort**</span><span class="sxs-lookup"><span data-stu-id="93fc2-120">**IVdsControllerPort**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdscontrollerport)                                                      |
| <span data-ttu-id="93fc2-121">相關聯的列舉</span><span class="sxs-lookup"><span data-stu-id="93fc2-121">Associated enumerations</span></span>                                                                           | [<span data-ttu-id="93fc2-122">**VDS \_ 埠 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="93fc2-122">**VDS\_PORT\_STATUS**</span></span>](/windows/desktop/api/Vds/ne-vds-vds_port_status)                                                          |
| <span data-ttu-id="93fc2-123">相關聯的結構</span><span class="sxs-lookup"><span data-stu-id="93fc2-123">Associated structures</span></span>                                                                             | <span data-ttu-id="93fc2-124">[**VDS \_埠 \_**](/windows/desktop/api/Vds/ns-vds-vds_port_prop)和 [ **VDS \_ 埠 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_port_notification)</span><span class="sxs-lookup"><span data-stu-id="93fc2-124">[**VDS\_PORT\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_port_prop) and [**VDS\_PORT\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_port_notification)</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="93fc2-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="93fc2-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93fc2-126">硬體提供者物件</span><span class="sxs-lookup"><span data-stu-id="93fc2-126">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="93fc2-127">**IVdsControllerControllerPort::QueryControllerPorts**</span><span class="sxs-lookup"><span data-stu-id="93fc2-127">**IVdsControllerControllerPort::QueryControllerPorts**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdscontrollercontrollerport-querycontrollerports)
</dt> </dl>

 

 
