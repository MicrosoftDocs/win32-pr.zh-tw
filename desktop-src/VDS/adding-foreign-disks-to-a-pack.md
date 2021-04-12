---
description: 將外部磁片新增至套件
ms.assetid: 4018c742-1d23-47b9-a787-69bf8847b54a
title: 將外部磁片新增至套件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fbfa2ff3d00857fd4e1b92e78f1760c25ce516b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320688"
---
# <a name="adding-foreign-disks-to-a-pack"></a><span data-ttu-id="ed274-103">將外部磁片新增至套件</span><span class="sxs-lookup"><span data-stu-id="ed274-103">Adding Foreign Disks to a Pack</span></span>

<span data-ttu-id="ed274-104">\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]</span><span class="sxs-lookup"><span data-stu-id="ed274-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="ed274-105">最常見的情況是，外部磁片是配置在一部電腦上，並實際移至另一部電腦上的動態磁碟。</span><span class="sxs-lookup"><span data-stu-id="ed274-105">Most commonly, a foreign disk is a dynamic disk that is allocated on one computer and physically moved to another computer.</span></span> <span data-ttu-id="ed274-106">不過，屬於線上套件以外套件的任何磁片都會被視為屬於外部磁片套件的外部磁片。</span><span class="sxs-lookup"><span data-stu-id="ed274-106">However, any disk that belongs to a pack other than the online pack is considered to be a foreign disk that belongs to a foreign disk pack.</span></span>

<span data-ttu-id="ed274-107">在 [**vds \_ pack \_**](/windows/desktop/api/Vds/ns-vds-vds_pack_prop)架構結構的 **ulFlags** 成員中，有一個外建的 **\_ PKF \_ 外** 旗標已設定的外部套件。</span><span class="sxs-lookup"><span data-stu-id="ed274-107">A foreign pack has the **VDS\_PKF\_FOREIGN** flag set in the **ulFlags** member of the [**VDS\_PACK\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_pack_prop) structure.</span></span> <span data-ttu-id="ed274-108">外部套件永遠都是離線的。</span><span class="sxs-lookup"><span data-stu-id="ed274-108">Foreign packs are always offline.</span></span>

<span data-ttu-id="ed274-109">下列程式說明如何匯入一或多個外部磁片。</span><span class="sxs-lookup"><span data-stu-id="ed274-109">The following procedure describes how to import one or more foreign disks.</span></span>

<span data-ttu-id="ed274-110">**匯入一或多個外部磁片**</span><span class="sxs-lookup"><span data-stu-id="ed274-110">**To import one or more foreign disks**</span></span>

1.  <span data-ttu-id="ed274-111">將磁片移至新電腦。</span><span class="sxs-lookup"><span data-stu-id="ed274-111">Move disks to the new computer.</span></span>
2.  <span data-ttu-id="ed274-112">在新電腦上，使用 [**IVdsService：： Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) 方法來安裝外部磁片。</span><span class="sxs-lookup"><span data-stu-id="ed274-112">On the new computer, use the [**IVdsService::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) method to install the foreign disks.</span></span>
3.  <span data-ttu-id="ed274-113">選取要作為接收外部磁片之目標套件的線上套件。</span><span class="sxs-lookup"><span data-stu-id="ed274-113">Select the online pack to be the target pack that receives the foreign disks.</span></span> <span data-ttu-id="ed274-114">如果沒有任何線上元件存在，請使用 [**IVdsSwProvider：： CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) 方法來建立新的空白套件。</span><span class="sxs-lookup"><span data-stu-id="ed274-114">If no online pack exists, use the [**IVdsSwProvider::CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) method to create a new empty pack.</span></span>
4.  <span data-ttu-id="ed274-115">使用 [**IVdsPack：： MigrateDisks**](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks) 方法將磁片匯入至新的動態套件。</span><span class="sxs-lookup"><span data-stu-id="ed274-115">Use the [**IVdsPack::MigrateDisks**](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks) method to import the disks to the new dynamic pack.</span></span>
5.  <span data-ttu-id="ed274-116">使用 [**IVdsSwProvider：： QueryPacks**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-querypacks) 方法來列舉套件，並使用 [**IVdsPack：： GetProperties**](/windows/desktop/api/Vds/nf-vds-ivdspack-getproperties) 來判斷哪個套件現在是線上套件。</span><span class="sxs-lookup"><span data-stu-id="ed274-116">Use the [**IVdsSwProvider::QueryPacks**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-querypacks) method to enumerate the packs and [**IVdsPack::GetProperties**](/windows/desktop/api/Vds/nf-vds-ivdspack-getproperties) to determine which pack is now the online pack.</span></span>

<span data-ttu-id="ed274-117">如果您建立新的空目標套件，則不會實際將外部磁片遷移至該套件。</span><span class="sxs-lookup"><span data-stu-id="ed274-117">If you create a new empty target pack, the foreign disks are not actually migrated to that pack.</span></span> <span data-ttu-id="ed274-118">相反地，外部套件會標示為 [線上]， (套件的 [ **VDS] \_ PKF \_ 外** 旗標，使套件不再是外部) ，而且會捨棄您所建立的目標套件。</span><span class="sxs-lookup"><span data-stu-id="ed274-118">Instead, the foreign pack is marked online, the **VDS\_PKF\_FOREIGN** flag for the pack is cleared (so the pack is no longer foreign), and the target pack that you created is discarded.</span></span>

> [!Note]  
> <span data-ttu-id="ed274-119">使用 [**IVdsPack：： AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) 方法，將未配置的磁片（提供者所宣告的磁片）新增至套件。</span><span class="sxs-lookup"><span data-stu-id="ed274-119">Use the [**IVdsPack::AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) method to add unallocated disks—disks not claimed by a provider—to a pack.</span></span> <span data-ttu-id="ed274-120">未配置的磁片不得為外部。</span><span class="sxs-lookup"><span data-stu-id="ed274-120">An unallocated disk cannot be foreign.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ed274-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="ed274-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed274-122">使用 VDS</span><span class="sxs-lookup"><span data-stu-id="ed274-122">Using VDS</span></span>](using-vds.md)
</dt> <dt>

[<span data-ttu-id="ed274-123">**IVdsService::Reenumerate**</span><span class="sxs-lookup"><span data-stu-id="ed274-123">**IVdsService::Reenumerate**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate)
</dt> <dt>

[<span data-ttu-id="ed274-124">**IVdsSwProvider::CreatePack**</span><span class="sxs-lookup"><span data-stu-id="ed274-124">**IVdsSwProvider::CreatePack**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack)
</dt> <dt>

[<span data-ttu-id="ed274-125">**IVdsPack::MigrateDisks**</span><span class="sxs-lookup"><span data-stu-id="ed274-125">**IVdsPack::MigrateDisks**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks)
</dt> <dt>

[<span data-ttu-id="ed274-126">**IVdsPack::AddDisk**</span><span class="sxs-lookup"><span data-stu-id="ed274-126">**IVdsPack::AddDisk**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk)
</dt> </dl>

 

 
