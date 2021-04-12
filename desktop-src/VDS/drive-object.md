---
description: 磁片磁碟機物件
ms.assetid: c1c17a97-cf4b-45b7-bc32-4bad94c3ddb2
title: 磁片磁碟機物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7df8501c79f9381dba80a1fe0276014dccdf7a34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104192921"
---
# <a name="drive-object"></a><span data-ttu-id="5df6d-103">磁片磁碟機物件</span><span class="sxs-lookup"><span data-stu-id="5df6d-103">Drive Object</span></span>

<span data-ttu-id="5df6d-104">\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]</span><span class="sxs-lookup"><span data-stu-id="5df6d-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="5df6d-105">磁片磁碟機物件會建立包含在子系統內的實體磁片磁碟機模型。</span><span class="sxs-lookup"><span data-stu-id="5df6d-105">A drive object models a physical disk drive that is contained within a subsystem.</span></span> <span data-ttu-id="5df6d-106">每個磁片磁碟機會連線至匯流排、佔用插槽，並包含一組磁片磁碟機範圍。</span><span class="sxs-lookup"><span data-stu-id="5df6d-106">Each drive connects to a bus, occupies a slot, and contains a set of drive extents.</span></span> <span data-ttu-id="5df6d-107">每個磁片磁碟機都可將範圍貢獻至任意數目的 Lun。</span><span class="sxs-lookup"><span data-stu-id="5df6d-107">Each drive can contribute extents to any number of LUNs.</span></span> <span data-ttu-id="5df6d-108">磁片磁碟機也可以指定為熱備用。</span><span class="sxs-lookup"><span data-stu-id="5df6d-108">A drive can also be designated as a hot spare.</span></span>

<span data-ttu-id="5df6d-109">使用 [**IVdsSubSystem：： QueryDrives**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querydrives) 方法來判斷特定子系統所包含的磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="5df6d-109">Use the [**IVdsSubSystem::QueryDrives**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querydrives) method to determine the drives that are contained by a specific subsystem.</span></span> <span data-ttu-id="5df6d-110">呼叫端可以取得特定磁片磁碟機的指標，方法是從 **QueryDrives** 方法所傳回的列舉中選取所需的磁片磁碟機物件，或是叫用 [**IVdsSubSystem：： GetDrive**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-getdrive) 方法，並傳入所需的匯流排和插槽號碼。</span><span class="sxs-lookup"><span data-stu-id="5df6d-110">Callers can get a pointer to a specific drive by selecting the desired drive object from the enumeration that is returned by the **QueryDrives** method, or by invoking the [**IVdsSubSystem::GetDrive**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-getdrive) method and passing in the desired bus and slot number.</span></span> <span data-ttu-id="5df6d-111">您可以使用磁片磁碟機物件，設定磁片磁碟機的狀態和查詢磁片磁碟機內容、相關聯的磁片區，以及包含該磁片磁碟機的子系統。</span><span class="sxs-lookup"><span data-stu-id="5df6d-111">With a drive object, you can set the drive status and query for drive properties, associated drive extents, and the subsystem containing the drive.</span></span>

<span data-ttu-id="5df6d-112">除了物件識別碼、名稱和序號之外，磁片磁碟機物件屬性還包括磁片磁碟機狀態、健康情況和旗標;以位元組為單位的大小;以及匯流排和插槽號碼。</span><span class="sxs-lookup"><span data-stu-id="5df6d-112">In addition to an object identifier, a name, and a serial number, drive object properties include the drive status, health, and flags; the size in bytes; and a bus and slot number.</span></span>

<span data-ttu-id="5df6d-113">下表列出相關的介面、列舉和結構。</span><span class="sxs-lookup"><span data-stu-id="5df6d-113">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="5df6d-114">類型</span><span class="sxs-lookup"><span data-stu-id="5df6d-114">Type</span></span>                                              | <span data-ttu-id="5df6d-115">元素</span><span class="sxs-lookup"><span data-stu-id="5df6d-115">Element</span></span>                                                                                                                                         |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5df6d-116">一律由這個物件公開的介面</span><span class="sxs-lookup"><span data-stu-id="5df6d-116">Interfaces that are always exposed by this object</span></span> | [<span data-ttu-id="5df6d-117">**IVdsDrive**</span><span class="sxs-lookup"><span data-stu-id="5df6d-117">**IVdsDrive**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsdrive)                                                                                                                  |
| <span data-ttu-id="5df6d-118">此物件可能公開的介面</span><span class="sxs-lookup"><span data-stu-id="5df6d-118">Interfaces that may be exposed by this object</span></span>     | [<span data-ttu-id="5df6d-119">**IVdsMaintenance**</span><span class="sxs-lookup"><span data-stu-id="5df6d-119">**IVdsMaintenance**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance)                                                                                                      |
| <span data-ttu-id="5df6d-120">相關聯的列舉</span><span class="sxs-lookup"><span data-stu-id="5df6d-120">Associated enumerations</span></span>                           | <span data-ttu-id="5df6d-121">[**VDS \_磁片磁碟機 \_ 旗**](/windows/desktop/api/Vds/ne-vds-vds_drive_flag)標、 [**vds \_ 磁片磁碟機 \_ 狀態**](/windows/desktop/api/Vds/ne-vds-vds_drive_status)，以及 [**vds \_ 磁片區的 \_ 範圍**](/windows/desktop/api/Vds/ns-vds-vds_drive_extent)。</span><span class="sxs-lookup"><span data-stu-id="5df6d-121">[**VDS\_DRIVE\_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_drive_flag), [**VDS\_DRIVE\_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_drive_status), and [**VDS\_DRIVE\_EXTENT**](/windows/desktop/api/Vds/ns-vds-vds_drive_extent).</span></span> |
| <span data-ttu-id="5df6d-122">相關聯的結構</span><span class="sxs-lookup"><span data-stu-id="5df6d-122">Associated structures</span></span>                             | <span data-ttu-id="5df6d-123">[**VDS \_磁片 \_ 磁碟機**](/windows/desktop/api/Vds/ns-vds-vds_drive_prop) 和 [**VDS \_ 磁片磁碟機 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification)。</span><span class="sxs-lookup"><span data-stu-id="5df6d-123">[**VDS\_DRIVE\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_drive_prop) and [**VDS\_DRIVE\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification).</span></span>                                      |



 

## <a name="related-topics"></a><span data-ttu-id="5df6d-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="5df6d-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5df6d-125">硬體提供者物件</span><span class="sxs-lookup"><span data-stu-id="5df6d-125">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="5df6d-126">**IVdsSubSystem::QueryDrives**</span><span class="sxs-lookup"><span data-stu-id="5df6d-126">**IVdsSubSystem::QueryDrives**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querydrives)
</dt> <dt>

[<span data-ttu-id="5df6d-127">**IVdsSubSystem::GetDrive**</span><span class="sxs-lookup"><span data-stu-id="5df6d-127">**IVdsSubSystem::GetDrive**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-getdrive)
</dt> </dl>

 

 
