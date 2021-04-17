---
description: 入口網站群組物件
ms.assetid: e5892e96-b6ad-447a-9627-b44fc6f1b27a
title: 入口網站群組物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c915e76debac959a1dc7684d87c9770033b4aa34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514096"
---
# <a name="portal-group-object"></a><span data-ttu-id="e6822-103">入口網站群組物件</span><span class="sxs-lookup"><span data-stu-id="e6822-103">Portal Group Object</span></span>

<span data-ttu-id="e6822-104">\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]</span><span class="sxs-lookup"><span data-stu-id="e6822-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="e6822-105">入口網站群組物件會建立 iscsi 目標中所含 iSCSI 入口網站群組的模型。</span><span class="sxs-lookup"><span data-stu-id="e6822-105">A portal group object models an iSCSI portal group that is contained within an iSCSI target.</span></span>

<span data-ttu-id="e6822-106">使用 [**IVdsIscsiTarget：： QueryPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsitarget-queryportalgroups) 方法來判斷特定目標所包含的入口網站群組。</span><span class="sxs-lookup"><span data-stu-id="e6822-106">Use the [**IVdsIscsiTarget::QueryPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsitarget-queryportalgroups) method to determine the portal groups that are contained by a specific target.</span></span> <span data-ttu-id="e6822-107">使用 [**IVdsIscsiPortal：： QueryAssociatedPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsiportal-queryassociatedportalgroups) 方法來判斷與指定的入口網站相關聯的入口網站群組。</span><span class="sxs-lookup"><span data-stu-id="e6822-107">Use the [**IVdsIscsiPortal::QueryAssociatedPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsiportal-queryassociatedportalgroups) method to determine the portal groups that are associated with a specified portal.</span></span> <span data-ttu-id="e6822-108">呼叫端可以從 **QueryPortalGroups** 方法或 **QueryAssociatedPortalGroups** 方法所傳回的列舉中選取所需的入口網站群組物件，以取得特定入口網站群組的指標。</span><span class="sxs-lookup"><span data-stu-id="e6822-108">Callers can get a pointer to a specific portal group by selecting the desired portal group object from the enumeration that is returned by the **QueryPortalGroups** method or the **QueryAssociatedPortalGroups** method.</span></span> <span data-ttu-id="e6822-109">使用入口網站群組物件時，您可以新增或移除入口網站群組屬性、相關聯的入口網站，以及包含入口網站群組的目標的入口網站和查詢。</span><span class="sxs-lookup"><span data-stu-id="e6822-109">With a portal group object, you can add or remove portals and query for portal group properties, associated portals, and the target that contains the portal group.</span></span>

<span data-ttu-id="e6822-110">入口網站群組物件屬性包括 [物件識別碼](vds-data-types.md) 和入口網站群組標記。</span><span class="sxs-lookup"><span data-stu-id="e6822-110">Portal group object properties include an [object identifier](vds-data-types.md) and the portal group tag.</span></span> <span data-ttu-id="e6822-111">如需入口網站群組標記的詳細資訊，請參閱中的 iSCSI 規格 <https://go.microsoft.com/fwlink/p/?linkid=158752> 。</span><span class="sxs-lookup"><span data-stu-id="e6822-111">For more information about portal group tags, see the iSCSI specification at <https://go.microsoft.com/fwlink/p/?linkid=158752>.</span></span>

<span data-ttu-id="e6822-112">下表列出相關的介面、列舉和結構。</span><span class="sxs-lookup"><span data-stu-id="e6822-112">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="e6822-113">類型</span><span class="sxs-lookup"><span data-stu-id="e6822-113">Type</span></span>                                                                                      | <span data-ttu-id="e6822-114">元素</span><span class="sxs-lookup"><span data-stu-id="e6822-114">Element</span></span>                                                                                                                                            |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6822-115">只有在 VDS 1.1 和 2.0 iSCSI 提供者中，此物件一律公開的介面</span><span class="sxs-lookup"><span data-stu-id="e6822-115">Interfaces that are always exposed by this object in VDS 1.1 and 2.0 iSCSI providers only</span></span> | <span data-ttu-id="e6822-116">[**IVdsIscsiPortalGroup**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportalgroup)。</span><span class="sxs-lookup"><span data-stu-id="e6822-116">[**IVdsIscsiPortalGroup**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportalgroup).</span></span>                                                                                              |
| <span data-ttu-id="e6822-117">相關聯的列舉</span><span class="sxs-lookup"><span data-stu-id="e6822-117">Associated enumerations</span></span>                                                                   | <span data-ttu-id="e6822-118">無。</span><span class="sxs-lookup"><span data-stu-id="e6822-118">None.</span></span>                                                                                                                                              |
| <span data-ttu-id="e6822-119">相關聯的結構</span><span class="sxs-lookup"><span data-stu-id="e6822-119">Associated structures</span></span>                                                                     | <span data-ttu-id="e6822-120">[**VDS \_ISCSI \_ PORTALGROUP \_**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_portalgroup_prop) 和 [**VDS \_ 入口網站 \_ 群組 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_portal_group_notification)。</span><span class="sxs-lookup"><span data-stu-id="e6822-120">[**VDS\_ISCSI\_PORTALGROUP\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_portalgroup_prop) and [**VDS\_PORTAL\_GROUP\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_portal_group_notification).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e6822-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="e6822-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6822-122">硬體提供者物件</span><span class="sxs-lookup"><span data-stu-id="e6822-122">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="e6822-123">**IVdsIscsiPortal::QueryAssociatedPortalGroups**</span><span class="sxs-lookup"><span data-stu-id="e6822-123">**IVdsIscsiPortal::QueryAssociatedPortalGroups**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsiscsiportal-queryassociatedportalgroups)
</dt> <dt>

[<span data-ttu-id="e6822-124">**IVdsIscsiTarget::QueryPortalGroups**</span><span class="sxs-lookup"><span data-stu-id="e6822-124">**IVdsIscsiTarget::QueryPortalGroups**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsiscsitarget-queryportalgroups)
</dt> </dl>

 

 
