---
description: 儲存集區物件會在儲存子系統中建立存放集區的模型。
ms.assetid: a6104742-3ef9-4570-9728-3e6580953117
title: 存放集區物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c44719b825193faa75546ba1a0f7b42155a3e49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997972"
---
# <a name="storage-pool-object"></a><span data-ttu-id="0b040-103">存放集區物件</span><span class="sxs-lookup"><span data-stu-id="0b040-103">Storage Pool Object</span></span>

<span data-ttu-id="0b040-104">\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]</span><span class="sxs-lookup"><span data-stu-id="0b040-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="0b040-105">儲存集區物件會在儲存子系統中建立存放集區的模型。</span><span class="sxs-lookup"><span data-stu-id="0b040-105">A storage pool object models a storage pool in a storage subsystem.</span></span>

<span data-ttu-id="0b040-106">存放集區包含一或多個由相同硬體提供者所管理之磁片磁碟機的磁片區。</span><span class="sxs-lookup"><span data-stu-id="0b040-106">A storage pool contains drive extents from one or more drives that are managed by the same hardware provider.</span></span>

<span data-ttu-id="0b040-107">下表列出相關的介面、列舉和結構。</span><span class="sxs-lookup"><span data-stu-id="0b040-107">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="0b040-108">類型</span><span class="sxs-lookup"><span data-stu-id="0b040-108">Type</span></span>                                              | <span data-ttu-id="0b040-109">元素</span><span class="sxs-lookup"><span data-stu-id="0b040-109">Element</span></span>                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b040-110">一律由這個物件公開的介面</span><span class="sxs-lookup"><span data-stu-id="0b040-110">Interfaces that are always exposed by this object</span></span> | [<span data-ttu-id="0b040-111">**IVdsStoragePool**</span><span class="sxs-lookup"><span data-stu-id="0b040-111">**IVdsStoragePool**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsstoragepool)                                                                                                                                                                                                                                                               |
| <span data-ttu-id="0b040-112">相關聯的列舉</span><span class="sxs-lookup"><span data-stu-id="0b040-112">Associated enumerations</span></span>                           | <span data-ttu-id="0b040-113">[**VDS \_RAID \_ 類型**](/windows/desktop/api/Vds/ne-vds-vds_raid_type)、 [**vds \_ 存放 \_ 集區 \_ 狀態**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_status)，以及 [**vds \_ 儲存 \_ 集區 \_ 類型**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_type)。</span><span class="sxs-lookup"><span data-stu-id="0b040-113">[**VDS\_RAID\_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_raid_type), [**VDS\_STORAGE\_POOL\_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_status), and [**VDS\_STORAGE\_POOL\_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_type).</span></span>                                                                                                                                  |
| <span data-ttu-id="0b040-114">相關聯的結構</span><span class="sxs-lookup"><span data-stu-id="0b040-114">Associated structures</span></span>                             | <span data-ttu-id="0b040-115">[**VDS \_HINTS2**](/windows/desktop/api/Vds/ns-vds-vds_hints2)、 [**vds \_ 集區 \_ 屬性**](/windows/desktop/api/Vds/ns-vds-vds_pool_attributes)、 [**vds 集區 \_ \_ 自訂 \_ 屬性**](/windows/desktop/api/Vds/ns-vds-vds_pool_custom_attributes)、 [**vds \_ 儲存 \_ 集 \_ \_ 區磁片區**](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_drive_extent)，以及 [**vds \_ 存放 \_ 集 \_**](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_prop)區的屬性。</span><span class="sxs-lookup"><span data-stu-id="0b040-115">[**VDS\_HINTS2**](/windows/desktop/api/Vds/ns-vds-vds_hints2), [**VDS\_POOL\_ATTRIBUTES**](/windows/desktop/api/Vds/ns-vds-vds_pool_attributes), [**VDS\_POOL\_CUSTOM\_ATTRIBUTES**](/windows/desktop/api/Vds/ns-vds-vds_pool_custom_attributes), [**VDS\_STORAGE\_POOL\_DRIVE\_EXTENT**](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_drive_extent), and [**VDS\_STORAGE\_POOL\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_prop).</span></span> |



 

 

 
