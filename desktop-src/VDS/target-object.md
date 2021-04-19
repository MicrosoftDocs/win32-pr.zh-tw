---
description: 目標物件
ms.assetid: e88d65ad-9b56-4620-a0f5-573c5e245b3e
title: 目標物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e1e81ea94a2f608378eba069defc83a721e0fb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987373"
---
# <a name="target-object"></a><span data-ttu-id="3189d-103">目標物件</span><span class="sxs-lookup"><span data-stu-id="3189d-103">Target Object</span></span>

<span data-ttu-id="3189d-104">\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]</span><span class="sxs-lookup"><span data-stu-id="3189d-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="3189d-105">目標物件會建立包含在 iSCSI 子系統內的 iSCSI 目標模型。</span><span class="sxs-lookup"><span data-stu-id="3189d-105">A target object models an iSCSI target that is contained within an iSCSI subsystem.</span></span>

<span data-ttu-id="3189d-106">使用 [**IVdsSubSystemIscsi：： QueryTargets**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-querytargets) 方法來判斷子系統的 iSCSI 目標。</span><span class="sxs-lookup"><span data-stu-id="3189d-106">Use the [**IVdsSubSystemIscsi::QueryTargets**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-querytargets) method to determine the iSCSI targets of the subsystem.</span></span> <span data-ttu-id="3189d-107">呼叫端可以從 **QueryTargets** 方法所傳回的列舉中選取所需的目標物件，以取得特定目標的指標。</span><span class="sxs-lookup"><span data-stu-id="3189d-107">Callers can get a pointer to a specific target by selecting the desired target object from the enumeration that is returned by the **QueryTargets** method.</span></span> <span data-ttu-id="3189d-108">使用目標物件時，您可以設定目標內容的易記名稱和查詢、相關聯的 Lun，以及包含目標的子系統。</span><span class="sxs-lookup"><span data-stu-id="3189d-108">With a target object, you can set the target's friendly name and query for target properties, associated LUNs, and the subsystem that contains the target.</span></span>

<span data-ttu-id="3189d-109">主機電腦必須登入目標，才能存取其相關聯的 Lun。</span><span class="sxs-lookup"><span data-stu-id="3189d-109">Host computers must log on to targets to access their associated LUNs.</span></span> <span data-ttu-id="3189d-110">若要對目標執行登入，目標在其中一個入口網站群組中至少必須有一個相關聯的入口網站。</span><span class="sxs-lookup"><span data-stu-id="3189d-110">To perform a logon to a target, the target must have at least one associated portal in one of its portal groups.</span></span> <span data-ttu-id="3189d-111">相關聯 Lun 的輸入和輸出會透過此登入會話進行處理。</span><span class="sxs-lookup"><span data-stu-id="3189d-111">Input to and output from associated LUNs is handled through this logon session.</span></span>

<span data-ttu-id="3189d-112">目標物件屬性包括物件識別碼、iSCSI 名稱、易記名稱，以及啟用 CHAP 的旗標。</span><span class="sxs-lookup"><span data-stu-id="3189d-112">Target object properties include an object identifier, an iSCSI name, a friendly name, and a CHAP-enabled flag.</span></span>

<span data-ttu-id="3189d-113">下表列出相關的介面、列舉和結構。</span><span class="sxs-lookup"><span data-stu-id="3189d-113">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="3189d-114">類型</span><span class="sxs-lookup"><span data-stu-id="3189d-114">Type</span></span>                                                                                      | <span data-ttu-id="3189d-115">元素</span><span class="sxs-lookup"><span data-stu-id="3189d-115">Element</span></span>                                                                                                                     |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3189d-116">只有在 VDS 1.1 和 2.0 iSCSI 提供者中，此物件一律公開的介面</span><span class="sxs-lookup"><span data-stu-id="3189d-116">Interfaces that are always exposed by this object in VDS 1.1 and 2.0 iSCSI providers only</span></span> | <span data-ttu-id="3189d-117">[**IVdsIscsiTarget**](/windows/desktop/api/Vds/nn-vds-ivdsiscsitarget)。</span><span class="sxs-lookup"><span data-stu-id="3189d-117">[**IVdsIscsiTarget**](/windows/desktop/api/Vds/nn-vds-ivdsiscsitarget).</span></span>                                                                                 |
| <span data-ttu-id="3189d-118">相關聯的列舉</span><span class="sxs-lookup"><span data-stu-id="3189d-118">Associated enumerations</span></span>                                                                   | <span data-ttu-id="3189d-119">無。</span><span class="sxs-lookup"><span data-stu-id="3189d-119">None.</span></span>                                                                                                                       |
| <span data-ttu-id="3189d-120">相關聯的結構</span><span class="sxs-lookup"><span data-stu-id="3189d-120">Associated structures</span></span>                                                                     | <span data-ttu-id="3189d-121">[**VDS \_ISCSI \_ 目標的 \_ 主張**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_target_prop) 和 [**VDS \_ 目標 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_target_notification)。</span><span class="sxs-lookup"><span data-stu-id="3189d-121">[**VDS\_ISCSI\_TARGET\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_target_prop) and [**VDS\_TARGET\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_target_notification).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="3189d-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="3189d-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3189d-123">硬體提供者物件</span><span class="sxs-lookup"><span data-stu-id="3189d-123">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="3189d-124">**IVdsSubSystemIscsi::QueryTargets**</span><span class="sxs-lookup"><span data-stu-id="3189d-124">**IVdsSubSystemIscsi::QueryTargets**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-querytargets)
</dt> </dl>

 

 
