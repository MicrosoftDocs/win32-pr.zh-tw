---
title: 卸載資料傳輸
description: 卸載資料傳輸
ms.assetid: 91EBE6D6-2DA7-48DA-AEB7-3FAFCA8341F5
keywords:
- odx
- 複製卸載
- 卸載
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1057ed27347fefc7ebc6a171eb7273da4341b024
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "106991300"
---
# <a name="offloaded-data-transfers"></a><span data-ttu-id="73c8f-106">卸載資料傳輸</span><span class="sxs-lookup"><span data-stu-id="73c8f-106">Offloaded data transfers</span></span>

## <a name="platforms"></a><span data-ttu-id="73c8f-107">平台</span><span class="sxs-lookup"><span data-stu-id="73c8f-107">Platforms</span></span>

<span data-ttu-id="73c8f-108">**用戶端** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="73c8f-108">**Clients** – Windows 8</span></span>  
<span data-ttu-id="73c8f-109">**伺服器** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="73c8f-109">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="73c8f-110">Description</span><span class="sxs-lookup"><span data-stu-id="73c8f-110">Description</span></span>

<span data-ttu-id="73c8f-111">為了推進儲存體資料的移動，Microsoft 開發了一項新的資料傳輸技術– (ODX) 卸載資料傳輸。</span><span class="sxs-lookup"><span data-stu-id="73c8f-111">To advance the storage data movement, Microsoft has developed a new data transfer technology – offloaded data transfer (ODX).</span></span> <span data-ttu-id="73c8f-112">Windows ODX 不會使用緩衝的讀取和緩衝寫入作業，而是會啟動複製作業，並讀取並取出代表儲存體裝置資料的權杖，然後使用具有權杖的卸載寫入命令來要求從源磁片到目的地磁片的資料移動。</span><span class="sxs-lookup"><span data-stu-id="73c8f-112">Instead of using buffered read and buffered write operations, Windows ODX starts the copy operation with an offload read and retrieves a token representing the data from the storage device, then uses an offload write command with the token to request data movement from the source disk to the destination disk.</span></span> <span data-ttu-id="73c8f-113">儲存體裝置的複製管理員會根據權杖來執行資料移動。</span><span class="sxs-lookup"><span data-stu-id="73c8f-113">The copy manager of the storage devices performs the data movement according to the token.</span></span> <span data-ttu-id="73c8f-114">在 Windows 8 中，IT 管理員和存放裝置系統管理員可以使用 Windows ODX 功能與存放裝置互動，以透過高速儲存網路移動大型檔案或資料。</span><span class="sxs-lookup"><span data-stu-id="73c8f-114">In the Windows 8, the IT manager and storage administrator are able to use the Windows ODX feature to interact with the storage device to move large files or data through the high-speed storage network.</span></span> <span data-ttu-id="73c8f-115">Windows ODX 會大幅減少大量資料傳輸期間的用戶端伺服器網路流量和 CPU 時間使用量，因為所有資料移動都是在後端儲存體網路上。</span><span class="sxs-lookup"><span data-stu-id="73c8f-115">Windows ODX will significantly reduce client-server network traffic and CPU time usage during large data transfers because all the data movement is at the backend storage network.</span></span> <span data-ttu-id="73c8f-116">ODX 可用於虛擬機器部署、大規模資料移轉和階層式存放裝置的支援，並可透過 ODX 和精簡布建儲存體功能，降低實體硬體部署的成本。</span><span class="sxs-lookup"><span data-stu-id="73c8f-116">ODX can be used in virtual machine deployment, massive data migration, and tiered storage device support, and can lower the cost of physical hardware deployment through the ODX and thin provisioning storage features.</span></span>

> [!Note]  
> <span data-ttu-id="73c8f-117">這項功能只適用于具有 SPC4 和 SBC3 規格執行的儲存裝置。</span><span class="sxs-lookup"><span data-stu-id="73c8f-117">This feature will only work on storage devices with SPC4 and SBC3 specification implementation.</span></span>

 

## <a name="functional-details"></a><span data-ttu-id="73c8f-118">功能詳細資料</span><span class="sxs-lookup"><span data-stu-id="73c8f-118">Functional details</span></span>

-   <span data-ttu-id="73c8f-119">Windows ODX 功能內嵌于 Windows 作業系統的複製引擎;在儲存體列舉期間，Windows 會查詢儲存體裝置的 ODX 功能</span><span class="sxs-lookup"><span data-stu-id="73c8f-119">The Windows ODX feature is embedded in the copy engine of the Windows operating system; during storage enumeration, Windows will query the ODX capability of the storage device</span></span>
-   <span data-ttu-id="73c8f-120">複製來源儲存體裝置和複製目的地儲存體裝置應在相同的複本管理員下管理，以提供複製卸載支援</span><span class="sxs-lookup"><span data-stu-id="73c8f-120">Copy source storage device and copy destination storage device should be managed under the same copy manager for copy offload support</span></span>
-   <span data-ttu-id="73c8f-121">如果複製卸載作業失敗，儲存裝置的複製管理員必須針對應用程式的錯誤處理傳回適當的額外意義資料</span><span class="sxs-lookup"><span data-stu-id="73c8f-121">If a copy offload operation fails, the storage device’s copy manager must return the proper additional sense data for the apps’ error handling</span></span>
-   <span data-ttu-id="73c8f-122">如果複製卸載作業失敗，則 Windows 複製引擎會切換回傳統的複製操作</span><span class="sxs-lookup"><span data-stu-id="73c8f-122">The Windows copy engine will fall back to the traditional copy operation if the copy offload operation fails</span></span>

## <a name="using-odx"></a><span data-ttu-id="73c8f-123">使用 ODX</span><span class="sxs-lookup"><span data-stu-id="73c8f-123">Using ODX</span></span>

-   <span data-ttu-id="73c8f-124">資料傳輸應用程式必須確保複製來源 LUN 和複製目的地 LUN 都能 ODX，然後再呼叫 ODX API 常式</span><span class="sxs-lookup"><span data-stu-id="73c8f-124">The data transfer app must ensure both copy source LUN and copy destination LUN are ODX capable before calling the ODX API routines</span></span>
-   <span data-ttu-id="73c8f-125">在 Windows explorer 中，使用者可以使用「拖曳」或「複製並貼上」來執行複製卸載</span><span class="sxs-lookup"><span data-stu-id="73c8f-125">In Windows explorer, users could use “drag” or “copy and paste” to perform copy offload</span></span>
-   <span data-ttu-id="73c8f-126">當來源 LUN 和目的地 LUN 掛接于檔案系統時，應用程式必須只呼叫 FSCTL 卸載 \_ \_ READ 和 FSCTL 卸載 \_ 寫入， \_ 才能執行從源 lun 到目的地 lun 的資料傳輸</span><span class="sxs-lookup"><span data-stu-id="73c8f-126">When the source LUN and destination LUN are mounted with the file system, the app must only call FSCTL\_Offload\_Read and FSCTL\_Offload\_Write to perform data transfer from the source LUN to the destination LUN</span></span>
-   <span data-ttu-id="73c8f-127">如果複製卸載作業失敗，儲存裝置的複製管理員必須針對應用程式的錯誤處理傳回適當的額外意義資料</span><span class="sxs-lookup"><span data-stu-id="73c8f-127">If a copy offload operation fails, the storage device’s copy manager must return the proper additional sense data for apps’ error handling</span></span>
-   <span data-ttu-id="73c8f-128">當來源 LUN 或目的地 LUN 未與檔案系統一起裝載且已鎖定時，應用程式必須呼叫 IOCTL \_ 儲存體，並 \_ \_ \_ \_ 使用 DeviceDsmAction \_ OffloadRead 或 DeviceDsmAction OffloadWrite 動作來管理資料集屬性， \_ 以執行複製卸載</span><span class="sxs-lookup"><span data-stu-id="73c8f-128">When the source LUN or destination LUN is not mounted with the file system and locked, the app must call IOCTL\_STORAGE\_MANAGE\_DATA\_SET\_ATTRIBUTES with DeviceDsmAction\_OffloadRead or DeviceDsmAction\_OffloadWrite action to perform copy offload</span></span>
-   <span data-ttu-id="73c8f-129">\_ \_ 當來源和目的地 lun 都未與任何檔案系統一起掛接且鎖定時，存放裝置管理應用程式可能會使用 SCSI 通過 API 來執行卸載資料傳輸</span><span class="sxs-lookup"><span data-stu-id="73c8f-129">Storage management apps may use SCSI\_PASS\_THROUGH API to perform offloaded data transfers when both source and destination LUNs are not mounted with any file system and locked</span></span>

## <a name="tests"></a><span data-ttu-id="73c8f-130">測試</span><span class="sxs-lookup"><span data-stu-id="73c8f-130">Tests</span></span>

-   <span data-ttu-id="73c8f-131">為確保健全的使用者體驗，請確認存放裝置陣列的 Windows ODX 認證</span><span class="sxs-lookup"><span data-stu-id="73c8f-131">To ensure a robust user experience, verify the Windows ODX certification of the storage array</span></span>
-   <span data-ttu-id="73c8f-132">存放裝置必須符合 Windows 卸載資料傳輸認證 (用於支援 ODX 功能的標誌) 需求</span><span class="sxs-lookup"><span data-stu-id="73c8f-132">The storage device must comply with Windows Offloaded Data Transfers certification (used to be Logo) requirements to support ODX feature</span></span>
-   <span data-ttu-id="73c8f-133">使用 Windows 卸載資料傳輸硬體認證套件來確認存放裝置的 ODX 功能支援</span><span class="sxs-lookup"><span data-stu-id="73c8f-133">Use the Windows Offloaded Data Transfers Hardware Certification Kit to verify the ODX feature support of the storage devices</span></span>

## <a name="resources"></a><span data-ttu-id="73c8f-134">資源</span><span class="sxs-lookup"><span data-stu-id="73c8f-134">Resources</span></span>

-   <span data-ttu-id="73c8f-135">T10 XCOPY Lite 規格 (11-059r8) </span><span class="sxs-lookup"><span data-stu-id="73c8f-135">T10 XCOPY Lite Spec (11-059r8)</span></span>
    -   [https://www.t10.org/cgi-bin/ac.pl?t=f&f=spc4r35b.pdf](https://www.t10.org/cgi-bin/ac.pl?t=f&f=spc4r35b.pdf)
    -   [https://www.t10.org/cgi-bin/ac.pl?t=f&f=sbc3r30.pdf](https://www.t10.org/cgi-bin/ac.pl?t=f&f=sbc3r30.pdf)
-   [<span data-ttu-id="73c8f-136">硬體儀表板服務</span><span class="sxs-lookup"><span data-stu-id="73c8f-136">Hardware Dashboard Services</span></span>](/windows-hardware/drivers/dashboard/)
-   [<span data-ttu-id="73c8f-137">SCSI \_ \_ 通過結構</span><span class="sxs-lookup"><span data-stu-id="73c8f-137">SCSI\_PASS\_THROUGH Structure</span></span>](/windows-hardware/drivers/ddi/ntddscsi/ns-ntddscsi-_scsi_pass_through)

 

 