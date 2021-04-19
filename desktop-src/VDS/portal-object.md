---
description: 入口網站物件
ms.assetid: 6655bbae-07d3-416b-9e45-ddcbe3433f40
title: 入口網站物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01328d8dccfe7a29c0686cde9b531df63d56e63e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990457"
---
# <a name="portal-object"></a><span data-ttu-id="e6c0b-103">入口網站物件</span><span class="sxs-lookup"><span data-stu-id="e6c0b-103">Portal Object</span></span>

<span data-ttu-id="e6c0b-104">\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]</span><span class="sxs-lookup"><span data-stu-id="e6c0b-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="e6c0b-105">入口網站物件會建立包含在 iSCSI 子系統內的 iSCSI 入口網站模型。</span><span class="sxs-lookup"><span data-stu-id="e6c0b-105">A portal object models an iSCSI portal that is contained within an iSCSI subsystem.</span></span>

<span data-ttu-id="e6c0b-106">使用 [**IVdsSubSystemIscsi：： QueryPortals**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-queryportals) 方法來判斷子系統的 iSCSI 入口網站。</span><span class="sxs-lookup"><span data-stu-id="e6c0b-106">Use the [**IVdsSubSystemIscsi::QueryPortals**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-queryportals) method to determine the iSCSI portals of the subsystem.</span></span> <span data-ttu-id="e6c0b-107">呼叫端可以從 **QueryPortals** 方法所傳回的列舉中選取所需的入口網站物件，以取得特定入口網站的指標。</span><span class="sxs-lookup"><span data-stu-id="e6c0b-107">Callers can get a pointer to a specific portal by selecting the desired portal object from the enumeration that is returned by the **QueryPortals** method.</span></span> <span data-ttu-id="e6c0b-108">您可以使用入口網站物件，設定入口網站屬性、相關聯的入口網站群組和包含入口網站的子系統的入口網站狀態和查詢。</span><span class="sxs-lookup"><span data-stu-id="e6c0b-108">With a portal object, you can set the portal status and query for portal properties, associated portal groups, and the subsystem that contains the portal.</span></span>

<span data-ttu-id="e6c0b-109">入口網站物件最多隻能與指定目標的一個入口網站群組相關聯。</span><span class="sxs-lookup"><span data-stu-id="e6c0b-109">A portal object can only be associated with at most one portal group of a specified target.</span></span>

<span data-ttu-id="e6c0b-110">入口網站可作為 iSCSI 硬體提供者中 MPIO 路徑的其中一個端點，可在此設定負載平衡原則。</span><span class="sxs-lookup"><span data-stu-id="e6c0b-110">Portals serve as one of the endpoints of MPIO paths in iSCSI hardware providers, upon which load balancing policies can be imposed.</span></span>

<span data-ttu-id="e6c0b-111">入口網站物件屬性包括物件識別碼、IP 位址和埠，以及入口網站的狀態。</span><span class="sxs-lookup"><span data-stu-id="e6c0b-111">Portal object properties include an object identifier, an IP address and port, and the portal status.</span></span>

<span data-ttu-id="e6c0b-112">下表列出相關的介面、列舉和結構。</span><span class="sxs-lookup"><span data-stu-id="e6c0b-112">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="e6c0b-113">類型</span><span class="sxs-lookup"><span data-stu-id="e6c0b-113">Type</span></span>                                                                                      | <span data-ttu-id="e6c0b-114">元素</span><span class="sxs-lookup"><span data-stu-id="e6c0b-114">Element</span></span>                                                                                                                 |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6c0b-115">只有在 VDS 1.1 和 2.0 iSCSI 提供者中，此物件一律公開的介面</span><span class="sxs-lookup"><span data-stu-id="e6c0b-115">Interfaces that are always exposed by this object in VDS 1.1 and 2.0 iSCSI providers only</span></span> | <span data-ttu-id="e6c0b-116">[**IVdsIscsiPortal**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportal)。</span><span class="sxs-lookup"><span data-stu-id="e6c0b-116">[**IVdsIscsiPortal**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportal).</span></span>                                                                             |
| <span data-ttu-id="e6c0b-117">相關聯的列舉</span><span class="sxs-lookup"><span data-stu-id="e6c0b-117">Associated enumerations</span></span>                                                                   | <span data-ttu-id="e6c0b-118">[**VDS \_ISCSI \_ 入口網站的 \_ 狀態**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_portal_status)。</span><span class="sxs-lookup"><span data-stu-id="e6c0b-118">[**VDS\_ISCSI\_PORTAL\_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_portal_status).</span></span>                                                          |
| <span data-ttu-id="e6c0b-119">相關聯的結構</span><span class="sxs-lookup"><span data-stu-id="e6c0b-119">Associated structures</span></span>                                                                     | <span data-ttu-id="e6c0b-120">[**VDS \_ISCSI \_ 入口 \_ 網站**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_portal_prop) 和 [**VDS \_ 埠 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_port_notification)。</span><span class="sxs-lookup"><span data-stu-id="e6c0b-120">[**VDS\_ISCSI\_PORTAL\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_portal_prop) and [**VDS\_PORT\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_port_notification).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e6c0b-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="e6c0b-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6c0b-122">硬體提供者物件</span><span class="sxs-lookup"><span data-stu-id="e6c0b-122">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="e6c0b-123">**IVdsSubSystemIscsi::QueryPortals**</span><span class="sxs-lookup"><span data-stu-id="e6c0b-123">**IVdsSubSystemIscsi::QueryPortals**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-queryportals)
</dt> </dl>

 

 
