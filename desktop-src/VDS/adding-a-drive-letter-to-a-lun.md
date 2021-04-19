---
description: 將磁碟機號新增至 LUN
ms.assetid: 3f350312-3f1f-4020-90d0-85521ea9c7c8
title: 將磁碟機號新增至 LUN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 426a4f3bf720b21a02462edde4a381012d2084d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997081"
---
# <a name="adding-a-drive-letter-to-a-lun"></a><span data-ttu-id="2afd5-103">將磁碟機號新增至 LUN</span><span class="sxs-lookup"><span data-stu-id="2afd5-103">Adding a Drive Letter to a LUN</span></span>

<span data-ttu-id="2afd5-104">\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]</span><span class="sxs-lookup"><span data-stu-id="2afd5-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="2afd5-105">您可以直接將磁碟機號指派給磁片區物件;但是，如果您的磁片是 LUN 物件，您會有幾個額外的步驟。</span><span class="sxs-lookup"><span data-stu-id="2afd5-105">You can assign drive letters to volume objects directly; however, if your disk is a LUN object, you have a few additional steps.</span></span>

<span data-ttu-id="2afd5-106">**指派磁碟機號給 LUN 物件**</span><span class="sxs-lookup"><span data-stu-id="2afd5-106">**To assign a drive letter to a LUN object**</span></span>

1.  <span data-ttu-id="2afd5-107">如有必要，請將 LUN 取消遮罩至本機主機。</span><span class="sxs-lookup"><span data-stu-id="2afd5-107">If necessary, unmask the LUN to the local host.</span></span>
    > [!Note]  
    > <span data-ttu-id="2afd5-108">您無法對目前 VDS 會話內的另一部電腦取消遮罩的 LUN 物件執行軟體系統管理作業。</span><span class="sxs-lookup"><span data-stu-id="2afd5-108">You cannot perform software administrative operations on a LUN object that is unmasked to another computer within the current VDS session.</span></span>

     

2.  <span data-ttu-id="2afd5-109">在正在執行硬體提供者的電腦上叫用 [**IVdsService：： Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) 方法。</span><span class="sxs-lookup"><span data-stu-id="2afd5-109">Invoke the [**IVdsService::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) method on the computer that is running the hardware provider.</span></span>
3.  <span data-ttu-id="2afd5-110">將 LUN 初始化為基本磁碟，如下所示：</span><span class="sxs-lookup"><span data-stu-id="2afd5-110">Initialize the LUN as a basic disk as follows:</span></span>
    1.  <span data-ttu-id="2afd5-111">在 LUN 物件上叫用 [**IUnknown：： QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 方法，以查詢 [**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk) 介面。</span><span class="sxs-lookup"><span data-stu-id="2afd5-111">Invoke the [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method on the LUN object to query for the [**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk) interface.</span></span>
    2.  <span data-ttu-id="2afd5-112">叫用 [**IVdsSwProvider：： CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) 方法，以建立基本套件。</span><span class="sxs-lookup"><span data-stu-id="2afd5-112">Invoke the [**IVdsSwProvider::CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) method to create a basic pack.</span></span>
    3.  <span data-ttu-id="2afd5-113">叫用 [**IVdsPack：： AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) 方法，將磁片新增至新的套件。</span><span class="sxs-lookup"><span data-stu-id="2afd5-113">Invoke the [**IVdsPack::AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) method to add the disk to the new pack.</span></span>
4.  <span data-ttu-id="2afd5-114">在磁片上建立磁碟分割，並取得磁片區物件，如下所示：</span><span class="sxs-lookup"><span data-stu-id="2afd5-114">Create a partition on the disk and obtain the volume object as follows:</span></span>
    1.  <span data-ttu-id="2afd5-115">叫用 [**IVdsCreatePartitionEx：： CreatePartitionEx**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex) 方法來建立資料分割。</span><span class="sxs-lookup"><span data-stu-id="2afd5-115">Invoke the [**IVdsCreatePartitionEx::CreatePartitionEx**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex) method to create a partition.</span></span>
    2.  <span data-ttu-id="2afd5-116">在 [**CreatePartitionEx**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex)所傳回的非同步物件上叫用 [**IVdsAsync：： Wait**](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait)方法，以從 [**VDS \_ 非同步 \_ 輸出**](/windows/desktop/api/Vds/ns-vds-vds_async_output)結構取得磁片區識別碼。</span><span class="sxs-lookup"><span data-stu-id="2afd5-116">Invoke the [**IVdsAsync::Wait**](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait) method on the async object that is returned by [**CreatePartitionEx**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex) to get the volume identifier from the [**VDS\_ASYNC\_OUTPUT**](/windows/desktop/api/Vds/ns-vds-vds_async_output) structure.</span></span>
    3.  <span data-ttu-id="2afd5-117">將磁片區識別碼作為參數傳遞給 [**IVdsService：： GetObject**](/windows/desktop/api/Vds/nf-vds-ivdsservice-getobject) 方法，以取得磁片區物件指標。</span><span class="sxs-lookup"><span data-stu-id="2afd5-117">Pass the volume identifier as a parameter to the [**IVdsService::GetObject**](/windows/desktop/api/Vds/nf-vds-ivdsservice-getobject) method to get a volume object pointer.</span></span>
5.  <span data-ttu-id="2afd5-118">叫用 [**IVdsVolumeMF：： AddAccessPath**](/windows/desktop/api/Vds/nf-vds-ivdsvolumemf-addaccesspath) 方法以指派磁碟機號。</span><span class="sxs-lookup"><span data-stu-id="2afd5-118">Invoke the [**IVdsVolumeMF::AddAccessPath**](/windows/desktop/api/Vds/nf-vds-ivdsvolumemf-addaccesspath) method to assign the drive letter.</span></span>

> [!Note]  
> <span data-ttu-id="2afd5-119">[**IVdsAdvancedDisk：： AssignDriveLetter**](/windows/desktop/api/Vds/nf-vds-ivdsadvanceddisk-assigndriveletter)方法會將磁碟機號指派給沒有相關聯磁片區的磁碟分割，例如 OEM 或 ESP 磁碟分割。</span><span class="sxs-lookup"><span data-stu-id="2afd5-119">The [**IVdsAdvancedDisk::AssignDriveLetter**](/windows/desktop/api/Vds/nf-vds-ivdsadvanceddisk-assigndriveletter) method assigns drive letters to partitions without associated volumes, such as OEM or ESP partitions.</span></span> <span data-ttu-id="2afd5-120">您無法使用它來指派磁碟機號給 LUN 物件。</span><span class="sxs-lookup"><span data-stu-id="2afd5-120">You cannot use it to assign a drive letter to a LUN object.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="2afd5-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="2afd5-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2afd5-122">使用 VDS</span><span class="sxs-lookup"><span data-stu-id="2afd5-122">Using VDS</span></span>](using-vds.md)
</dt> <dt>

[<span data-ttu-id="2afd5-123">**IVdsService::Reenumerate**</span><span class="sxs-lookup"><span data-stu-id="2afd5-123">**IVdsService::Reenumerate**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate)
</dt> <dt>

[<span data-ttu-id="2afd5-124">**IVdsDisk**</span><span class="sxs-lookup"><span data-stu-id="2afd5-124">**IVdsDisk**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsdisk)
</dt> <dt>

[<span data-ttu-id="2afd5-125">**IVdsSwProvider::CreatePack**</span><span class="sxs-lookup"><span data-stu-id="2afd5-125">**IVdsSwProvider::CreatePack**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack)
</dt> <dt>

[<span data-ttu-id="2afd5-126">**IVdsPack::AddDisk**</span><span class="sxs-lookup"><span data-stu-id="2afd5-126">**IVdsPack::AddDisk**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk)
</dt> <dt>

[<span data-ttu-id="2afd5-127">**IVdsCreatePartitionEx::CreatePartitionEx**</span><span class="sxs-lookup"><span data-stu-id="2afd5-127">**IVdsCreatePartitionEx::CreatePartitionEx**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex)
</dt> <dt>

[<span data-ttu-id="2afd5-128">**IVdsAsync：： Wait**</span><span class="sxs-lookup"><span data-stu-id="2afd5-128">**IVdsAsync::Wait**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait)
</dt> <dt>

[<span data-ttu-id="2afd5-129">**VDS \_ 非同步 \_ 輸出**</span><span class="sxs-lookup"><span data-stu-id="2afd5-129">**VDS\_ASYNC\_OUTPUT**</span></span>](/windows/desktop/api/Vds/ns-vds-vds_async_output)
</dt> <dt>

[<span data-ttu-id="2afd5-130">**IVdsVolumeMF::AddAccessPath**</span><span class="sxs-lookup"><span data-stu-id="2afd5-130">**IVdsVolumeMF::AddAccessPath**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsvolumemf-addaccesspath)
</dt> <dt>

[<span data-ttu-id="2afd5-131">**IVdsAdvancedDisk::AssignDriveLetter**</span><span class="sxs-lookup"><span data-stu-id="2afd5-131">**IVdsAdvancedDisk::AssignDriveLetter**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsadvanceddisk-assigndriveletter)
</dt> </dl>

 

 
