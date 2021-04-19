---
description: LUN Plex 物件
ms.assetid: db6eabaa-1b84-4613-ab2a-8d5904305e08
title: LUN Plex 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f1b51657ccbfc0f1bd3d73e54128cac3f0b507c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975935"
---
# <a name="lun-plex-object"></a><span data-ttu-id="cb7ef-103">LUN Plex 物件</span><span class="sxs-lookup"><span data-stu-id="cb7ef-103">LUN Plex Object</span></span>

<span data-ttu-id="cb7ef-104">\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]</span><span class="sxs-lookup"><span data-stu-id="cb7ef-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="cb7ef-105">LUN plex 物件會為 lun 所包含的 LUN plex 建立模型。</span><span class="sxs-lookup"><span data-stu-id="cb7ef-105">A LUN plex object models a LUN plex that is contained by a LUN.</span></span> <span data-ttu-id="cb7ef-106">只有鏡像的 LUN 可以有多個 plex;所有其他 LUN 類型都有一個 plex。</span><span class="sxs-lookup"><span data-stu-id="cb7ef-106">Only a mirrored LUN can have multiple plexes; all other LUN types have one plex.</span></span> <span data-ttu-id="cb7ef-107">每個 plex 都包含 LUN 上的資料複本。</span><span class="sxs-lookup"><span data-stu-id="cb7ef-107">Each plex contains a copy of the data on the LUN.</span></span> <span data-ttu-id="cb7ef-108">新的 plex 可以新增至 LUN，而且除了原始的 plex 之外，現有的 plex 也可以移除。</span><span class="sxs-lookup"><span data-stu-id="cb7ef-108">New plexes can be added to a LUN, and, with the exception of the original plex, existing plexes can be removed.</span></span> <span data-ttu-id="cb7ef-109">VDS 支援四個 LUN 的 plex 類型：簡單、跨距、等量和同位檢查。</span><span class="sxs-lookup"><span data-stu-id="cb7ef-109">VDS supports four LUN plex types: simple, spanned, striped, and striped with parity.</span></span> <span data-ttu-id="cb7ef-110">如需這些 LUN 類型的說明，請參閱 [Lun 物件](lun-object.md)。</span><span class="sxs-lookup"><span data-stu-id="cb7ef-110">For a description of each of these LUN types, see the [LUN Object](lun-object.md).</span></span>

<span data-ttu-id="cb7ef-111">使用 [**IVdsLun：： AddPlex**](/windows/desktop/api/Vds/nf-vds-ivdslun-addplex) 方法將 plex 新增至 LUN，並使用 [**IVdsLun：： RemovePlex**](/windows/desktop/api/Vds/nf-vds-ivdslun-removeplex) 方法來刪除該 plex。</span><span class="sxs-lookup"><span data-stu-id="cb7ef-111">Use the [**IVdsLun::AddPlex**](/windows/desktop/api/Vds/nf-vds-ivdslun-addplex) method to add a plex to a LUN and the [**IVdsLun::RemovePlex**](/windows/desktop/api/Vds/nf-vds-ivdslun-removeplex) method to delete the plex.</span></span> <span data-ttu-id="cb7ef-112">您可以藉由叫用 [**IVdsLun：： QueryPlexes**](/windows/desktop/api/Vds/nf-vds-ivdslun-queryplexes) 方法來查詢 LUN 的 plex。</span><span class="sxs-lookup"><span data-stu-id="cb7ef-112">You can query for LUN plexes by invoking the [**IVdsLun::QueryPlexes**](/windows/desktop/api/Vds/nf-vds-ivdslun-queryplexes) method.</span></span> <span data-ttu-id="cb7ef-113">您可以從 **QueryPlexes** 方法所傳回的列舉中選取所需的 plex 物件，以取得特定 LUN plex 的指標。</span><span class="sxs-lookup"><span data-stu-id="cb7ef-113">You can get a pointer to a specific LUN plex by selecting the desired plex object from the enumeration that is returned by the **QueryPlexes** method.</span></span> <span data-ttu-id="cb7ef-114">您可以使用 plex 物件來查詢磁片區範圍和 automagic 提示，並套用新的提示。</span><span class="sxs-lookup"><span data-stu-id="cb7ef-114">With a plex object, you can query for the drive extents and automagic hints, and apply new hints.</span></span>

<span data-ttu-id="cb7ef-115">除了物件識別碼、名稱和序號之外，LUN plex 物件屬性還包括 plex 類型、大小、狀態、健康情況、轉換狀態和旗標;取消遮罩清單和 stripe 大小;以及重建優先權設定。</span><span class="sxs-lookup"><span data-stu-id="cb7ef-115">In addition to an object identifier, a name, and a serial number, LUN plex object properties include the plex type, size, status, health, transition state, and flags; an unmasking list and stripe size; and a rebuild priority setting.</span></span>

<span data-ttu-id="cb7ef-116">下表列出相關的介面、列舉和結構。</span><span class="sxs-lookup"><span data-stu-id="cb7ef-116">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="cb7ef-117">類型</span><span class="sxs-lookup"><span data-stu-id="cb7ef-117">Type</span></span>                                              | <span data-ttu-id="cb7ef-118">元素</span><span class="sxs-lookup"><span data-stu-id="cb7ef-118">Element</span></span>                                                                                                                                                          |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb7ef-119">一律由這個物件公開的介面</span><span class="sxs-lookup"><span data-stu-id="cb7ef-119">Interfaces that are always exposed by this object</span></span> | <span data-ttu-id="cb7ef-120">[**IVdsLunPlex**](/windows/desktop/api/Vds/nn-vds-ivdslunplex)。</span><span class="sxs-lookup"><span data-stu-id="cb7ef-120">[**IVdsLunPlex**](/windows/desktop/api/Vds/nn-vds-ivdslunplex).</span></span>                                                                                                                              |
| <span data-ttu-id="cb7ef-121">相關聯的列舉</span><span class="sxs-lookup"><span data-stu-id="cb7ef-121">Associated enumerations</span></span>                           | <span data-ttu-id="cb7ef-122">[**VDS \_LUN \_ plex \_ 旗**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_flag)標、 [**vds \_ Lun \_ plex \_ 狀態**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_status)，以及 [**vds \_ lun \_ plex \_ 類型**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_type)。</span><span class="sxs-lookup"><span data-stu-id="cb7ef-122">[**VDS\_LUN\_PLEX\_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_flag), [**VDS\_LUN\_PLEX\_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_status), and [**VDS\_LUN\_PLEX\_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_type).</span></span> |
| <span data-ttu-id="cb7ef-123">相關聯的結構</span><span class="sxs-lookup"><span data-stu-id="cb7ef-123">Associated structures</span></span>                             | <span data-ttu-id="cb7ef-124">[**VDS \_LUN \_ PLEX \_**](/windows/desktop/api/Vds/ns-vds-vds_lun_plex_prop)的一種。</span><span class="sxs-lookup"><span data-stu-id="cb7ef-124">[**VDS\_LUN\_PLEX\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_lun_plex_prop).</span></span>                                                                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="cb7ef-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="cb7ef-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb7ef-126">硬體提供者物件</span><span class="sxs-lookup"><span data-stu-id="cb7ef-126">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="cb7ef-127">LUN 物件</span><span class="sxs-lookup"><span data-stu-id="cb7ef-127">LUN Object</span></span>](lun-object.md)
</dt> </dl>

 

 
