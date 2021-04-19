---
description: VDS 所支援的資料類型會定義函數傳回值、函數參數和結構成員。 資料類型會定義這些元素的大小和意義。
ms.assetid: f17e8c7e-e3cb-49ca-9060-2299dda55770
title: VDS 資料類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a868606110d9cf1c3cad5c3036789d041a5d86c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985355"
---
# <a name="vds-data-types"></a><span data-ttu-id="e80cc-104">VDS 資料類型</span><span class="sxs-lookup"><span data-stu-id="e80cc-104">VDS Data Types</span></span>

<span data-ttu-id="e80cc-105">\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]</span><span class="sxs-lookup"><span data-stu-id="e80cc-105">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="e80cc-106">VDS 所支援的資料類型會定義函數傳回值、函數參數和結構成員。</span><span class="sxs-lookup"><span data-stu-id="e80cc-106">The data types supported by VDS define function return values, function parameters, and structure members.</span></span> <span data-ttu-id="e80cc-107">資料類型會定義這些元素的大小和意義。</span><span class="sxs-lookup"><span data-stu-id="e80cc-107">Data types define the size and meaning of these elements.</span></span>



| <span data-ttu-id="e80cc-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="e80cc-108">Data type</span></span>                                                                                      | <span data-ttu-id="e80cc-109">描述</span><span class="sxs-lookup"><span data-stu-id="e80cc-109">Description</span></span>                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e80cc-110"><span id="VDS_OBJECT_ID"></span><span id="vds_object_id"></span>**VDS \_ 物件 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="e80cc-110"><span id="VDS_OBJECT_ID"></span><span id="vds_object_id"></span>**VDS\_OBJECT\_ID**</span></span><br/> | <span data-ttu-id="e80cc-111">VDS 物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="e80cc-111">VDS object ID.</span></span> <span data-ttu-id="e80cc-112">在重新開機時，這些值不保證是唯一的。</span><span class="sxs-lookup"><span data-stu-id="e80cc-112">These values are not guaranteed to be unique across reboots.</span></span> <br/> <span data-ttu-id="e80cc-113">這種類型是在 Vds. h (VdsHwPrv，) 硬體提供者的 GUID。</span><span class="sxs-lookup"><span data-stu-id="e80cc-113">This type is declared in Vds.h (VdsHwPrv.h for hardware providers) as a GUID.</span></span> <br/> |
| <span data-ttu-id="e80cc-114"><span id="VDS_PATH_ID"></span><span id="vds_path_id"></span>**VDS \_ 路徑 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="e80cc-114"><span id="VDS_PATH_ID"></span><span id="vds_path_id"></span>**VDS\_PATH\_ID**</span></span><br/>       | <span data-ttu-id="e80cc-115">多重路徑 i/o (MPIO) 的 VDS 路徑識別碼。</span><span class="sxs-lookup"><span data-stu-id="e80cc-115">VDS path ID for multipath I/O (MPIO).</span></span> <br/> <span data-ttu-id="e80cc-116">這種類型是在 Vds. h (VdsHwPrv，) 作為 UINT64 的硬體提供者。</span><span class="sxs-lookup"><span data-stu-id="e80cc-116">This type is declared in Vds.h (VdsHwPrv.h for hardware providers) as a UINT64.</span></span><br/>                                      |



 

 

