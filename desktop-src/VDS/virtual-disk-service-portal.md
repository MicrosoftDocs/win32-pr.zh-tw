---
description: 虛擬磁碟服務 (VDS) 管理各種不同的存放裝置設定，從單一磁片桌面到外部存放裝置陣列。 此服務會公開應用程式設計介面， (API) 。
ms.assetid: 536aafd2-cc04-48cc-8ee7-920efbba2a5f
title: 虛擬磁碟服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcfef0c5a73fcb2e6911395c829380c4bdfe56ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971819"
---
# <a name="virtual-disk-service"></a><span data-ttu-id="19e9f-104">虛擬磁碟服務</span><span class="sxs-lookup"><span data-stu-id="19e9f-104">Virtual Disk Service</span></span>

<span data-ttu-id="19e9f-105">\[從 Windows 8 和 Windows Server 2012 開始，虛擬磁碟服務 COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]</span><span class="sxs-lookup"><span data-stu-id="19e9f-105">\[Beginning with Windows 8 and Windows Server 2012, the Virtual Disk Service COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

## <a name="purpose"></a><span data-ttu-id="19e9f-106">目的</span><span class="sxs-lookup"><span data-stu-id="19e9f-106">Purpose</span></span>

<span data-ttu-id="19e9f-107">虛擬磁碟服務 (VDS) 管理各種不同的存放裝置設定，從單一磁片桌面到外部存放裝置陣列。</span><span class="sxs-lookup"><span data-stu-id="19e9f-107">The Virtual Disk Service (VDS) manages a wide range of storage configurations, from single-disk desktops to external storage arrays.</span></span> <span data-ttu-id="19e9f-108">此服務會公開應用程式設計介面， (API) 。</span><span class="sxs-lookup"><span data-stu-id="19e9f-108">The service exposes an application programming interface (API).</span></span>

## <a name="where-applicable"></a><span data-ttu-id="19e9f-109">適用時</span><span class="sxs-lookup"><span data-stu-id="19e9f-109">Where applicable</span></span>

<span data-ttu-id="19e9f-110">從 Windows 8 和 Windows Server 8 開始，虛擬磁碟服務 COM 介面會由儲存體管理 API （以 WMI 為基礎的程式設計介面）取代。</span><span class="sxs-lookup"><span data-stu-id="19e9f-110">Beginning with Windows 8 and Windows Server 8, the Virtual Disk Service COM interface is superseded by the Storage Management API, a WMI-based programming interface.</span></span> <span data-ttu-id="19e9f-111">若要管理儲存子系統、 (Windows) 磁片、磁碟分割和磁片區，強烈建議使用存放裝置管理 API。</span><span class="sxs-lookup"><span data-stu-id="19e9f-111">For managing storage subsystems, (Windows) disks, partitions, and volumes, we strongly recommend using the Storage Management API.</span></span> <span data-ttu-id="19e9f-112">如需詳細資訊，請參閱 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)。</span><span class="sxs-lookup"><span data-stu-id="19e9f-112">For more information, see the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).</span></span>

<span data-ttu-id="19e9f-113">針對鏡像開機磁碟區以外的所有使用方式 (使用鏡像磁片區來裝載作業系統 ) ，動態磁碟已淘汰。</span><span class="sxs-lookup"><span data-stu-id="19e9f-113">For all usages except mirror boot volumes (using a mirror volume to host the operating system ), dynamic disks are deprecated.</span></span> <span data-ttu-id="19e9f-114">對於需要針對磁片磁碟機失敗進行復原的資料，請使用儲存空間，這是一個彈性的儲存體虛擬化解決方案。</span><span class="sxs-lookup"><span data-stu-id="19e9f-114">For data that requires resiliency against drive failure, use Storage Spaces, a resilient storage virtualization solution.</span></span> <span data-ttu-id="19e9f-115">如需詳細資訊，請參閱 [儲存空間技術預覽](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831739(v=ws.11))。</span><span class="sxs-lookup"><span data-stu-id="19e9f-115">For more information, see [Storage Spaces Technical Preview](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831739(v=ws.11)).</span></span>

<span data-ttu-id="19e9f-116">使用本指南中所述介面的應用程式開發人員可以查詢及設定一組異類廠商提供和內部受控儲存體。</span><span class="sxs-lookup"><span data-stu-id="19e9f-116">Application developers who use the interfaces described in this guide can query and configure a heterogeneous set of vendor-supplied and internally managed storage.</span></span> <span data-ttu-id="19e9f-117">VDS 會從應用程式中隱藏與儲存體相關的複雜性，讓服務與廠商和技術中立。</span><span class="sxs-lookup"><span data-stu-id="19e9f-117">VDS hides from applications the complexities associated with storage, making the service both vendor and technology neutral.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="19e9f-118">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="19e9f-118">Developer audience</span></span>

<span data-ttu-id="19e9f-119">本檔適用于熟悉 Microsoft Windows 平臺的儲存功能，以及瞭解 COM 開發的應用程式開發人員。</span><span class="sxs-lookup"><span data-stu-id="19e9f-119">This documentation is intended for application developers who are familiar with the storage capabilities of Microsoft Windows platforms and who are knowledgeable about COM development.</span></span>

<span data-ttu-id="19e9f-120">本指南也適用于開發和支援 VDS 硬體提供者計畫的硬體子系統製造商。</span><span class="sxs-lookup"><span data-stu-id="19e9f-120">The guide is also intended for hardware subsystem manufacturers who develop and support VDS hardware provider programs.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="19e9f-121">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="19e9f-121">Run-time requirements</span></span>

<span data-ttu-id="19e9f-122">Windows Server 2003、Windows Vista 及更新版本都支援 VDS。</span><span class="sxs-lookup"><span data-stu-id="19e9f-122">VDS is supported on Windows Server 2003, Windows Vista, and later.</span></span> <span data-ttu-id="19e9f-123">如需特定程式設計專案之執行時間需求的詳細資訊，請參閱該元素檔集的需求一節。</span><span class="sxs-lookup"><span data-stu-id="19e9f-123">For information about run-time requirements for a particular programming element, see the Requirements section of the documentation for that element.</span></span>

<span data-ttu-id="19e9f-124">支援在 WOW64 下執行32位 VDS 應用程式，但64位 VDS 提供者必須在64位 Windows 版本上以原生應用程式的形式執行。</span><span class="sxs-lookup"><span data-stu-id="19e9f-124">Running 32-bit VDS applications under WOW64 is supported, but 64-bit VDS providers must run as native applications on 64-bit Windows versions.</span></span>

<span data-ttu-id="19e9f-125">Microsoft Windows 軟體開發套件 (SDK) 提供 VDS。</span><span class="sxs-lookup"><span data-stu-id="19e9f-125">VDS is available in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="19e9f-126">您可以從 [Windows 下載中心](https://www.microsoft.com/download/details.aspx?id=8279)安裝適用于 windows 7 和 windows Server 2008 R2 的 SDK。</span><span class="sxs-lookup"><span data-stu-id="19e9f-126">You can install the SDK for Windows 7 and Windows Server 2008 R2 from the [Windows Download Center](https://www.microsoft.com/download/details.aspx?id=8279).</span></span> <span data-ttu-id="19e9f-127">這一版的 Windows SDK 可以用來開發 Windows Server 2003、Windows Vista 和更新版本的 VDS 應用程式。</span><span class="sxs-lookup"><span data-stu-id="19e9f-127">This version of the Windows SDK can be used to develop VDS applications for Windows Server 2003, Windows Vista, and later.</span></span> <span data-ttu-id="19e9f-128">您也可以從 Windows 下載中心下載 [ISO 版本](https://www.microsoft.com/download/details.aspx?id=8442) 的 SDK。</span><span class="sxs-lookup"><span data-stu-id="19e9f-128">You can also download the [ISO version](https://www.microsoft.com/download/details.aspx?id=8442) of the SDK from the Windows Download Center.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="19e9f-129">本節內容</span><span class="sxs-lookup"><span data-stu-id="19e9f-129">In this section</span></span>



| <span data-ttu-id="19e9f-130">主題</span><span class="sxs-lookup"><span data-stu-id="19e9f-130">Topic</span></span>                                         | <span data-ttu-id="19e9f-131">描述</span><span class="sxs-lookup"><span data-stu-id="19e9f-131">Description</span></span>                                                                                            |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="19e9f-132">關於 VDS</span><span class="sxs-lookup"><span data-stu-id="19e9f-132">About VDS</span></span>](about-vds.md)<br/>         | <span data-ttu-id="19e9f-133">描述 VDS 物件模型、存放裝置設定策略和 VDS 通知。</span><span class="sxs-lookup"><span data-stu-id="19e9f-133">Describes the VDS object model, storage-configuration strategies, and VDS notifications.</span></span><br/>    |
| [<span data-ttu-id="19e9f-134">使用 VDS</span><span class="sxs-lookup"><span data-stu-id="19e9f-134">Using VDS</span></span>](using-vds.md)<br/>         | <span data-ttu-id="19e9f-135">說明如何使用 VDS 來查詢和設定存放裝置。</span><span class="sxs-lookup"><span data-stu-id="19e9f-135">Describes how to use VDS to query and configure storage devices.</span></span><br/>                            |
| [<span data-ttu-id="19e9f-136">VDS 參考</span><span class="sxs-lookup"><span data-stu-id="19e9f-136">VDS Reference</span></span>](vds-reference.md)<br/> | <span data-ttu-id="19e9f-137">描述 VDS 常數、資料類型、列舉、介面、結構和錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="19e9f-137">Describes VDS constants, data types, enumerations, interfaces, structures, and error codes.</span></span><br/> |



 

 

