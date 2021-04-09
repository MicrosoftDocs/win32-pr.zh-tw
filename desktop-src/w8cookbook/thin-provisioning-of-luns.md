---
title: 精簡布建邏輯單元
description: 精簡布建邏輯單元
ms.assetid: D64ECA7B-62AC-4C14-BE4B-84DA2E20C16B
keywords:
- LUN
- LBA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4abb6fa3cec112737b23e3cd658a48984cb0fcd1
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "104024231"
---
# <a name="thin-provisioning-of-logical-units"></a><span data-ttu-id="957c6-105">精簡布建邏輯單元</span><span class="sxs-lookup"><span data-stu-id="957c6-105">Thin provisioning of logical units</span></span>

## <a name="platforms"></a><span data-ttu-id="957c6-106">平台</span><span class="sxs-lookup"><span data-stu-id="957c6-106">Platforms</span></span>

<span data-ttu-id="957c6-107">**用戶端** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="957c6-107">**Clients** – Windows 8</span></span>  
<span data-ttu-id="957c6-108">**伺服器** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="957c6-108">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="957c6-109">Description</span><span class="sxs-lookup"><span data-stu-id="957c6-109">Description</span></span>

<span data-ttu-id="957c6-110">Windows 精簡布建是端對端儲存體布建解決方案的介面。</span><span class="sxs-lookup"><span data-stu-id="957c6-110">Windows Thin Provisioning is an interface to the end-to-end storage provisioning solution.</span></span> <span data-ttu-id="957c6-111">若要提供高可用性、可擴充且方便使用的儲存體布建服務，您需要從伺服器主機到儲存體目標裝置的健全實行。</span><span class="sxs-lookup"><span data-stu-id="957c6-111">To deliver a highly available, scalable and user-friendly storage provisioning service requires robust implementations from the server host to the storage target device.</span></span> <span data-ttu-id="957c6-112">Windows 精簡布建功能可透過精簡布建邏輯單元的 (LUN 的) 識別、閾值通知、資源耗盡處理、空間回收，以及邏輯區塊定址 (LBA) 狀態抓取，來為系統管理員、IT 管理員和存放裝置系統管理員提供精簡布建存放裝置的同步觀點。</span><span class="sxs-lookup"><span data-stu-id="957c6-112">The Windows thin provisioning feature provides a synchronous view of the thin provisioning storage devices to the system administrator, IT manager, and storage administrator through the thinly provisioned logical unit’s (LUN’s) identification, threshold notification, resource exhaustion handling, space reclamation, and logical block addressing (LBA) state retrieval.</span></span> <span data-ttu-id="957c6-113">Windows 精簡布建功能提供穩固的儲存體布建服務模型，可套用至用戶端伺服器儲存體系統、虛擬化儲存體和雲端儲存體服務。</span><span class="sxs-lookup"><span data-stu-id="957c6-113">The Windows thin provisioning feature presents a robust storage provisioning service model that can be applied to client-server storage systems, virtualization storage, and cloud storage services.</span></span> <span data-ttu-id="957c6-114">Microsoft 會強制執行存放裝置陣列產品的 Windows 精簡布建硬體認證套件需求，以確保高品質的精簡布建功能。</span><span class="sxs-lookup"><span data-stu-id="957c6-114">Microsoft will ensure the high quality of the thin provisioning feature by enforcing the Windows Thin Provisioning Hardware Certification Kit requirements for storage array products.</span></span>

<span data-ttu-id="957c6-115">Windows 精簡布建儲存體解決方案：</span><span class="sxs-lookup"><span data-stu-id="957c6-115">The Windows Thin Provisioning storage solution:</span></span>

-   <span data-ttu-id="957c6-116">允許存放裝置系統管理員以較少的實體磁片資源建立較大的 LUN</span><span class="sxs-lookup"><span data-stu-id="957c6-116">Allows storage administrators to create a larger LUN with fewer physical disk resources</span></span>
-   <span data-ttu-id="957c6-117">在不中斷儲存體布建服務的情況下新增或移除實體磁片資源</span><span class="sxs-lookup"><span data-stu-id="957c6-117">Adds or removes physical disk resource without interrupting the storage provisioning service</span></span>
-   <span data-ttu-id="957c6-118">透過閾值設定將使用者的儲存體磁片區使用量警示</span><span class="sxs-lookup"><span data-stu-id="957c6-118">Alerts users to the storage volume usage through the threshold setting</span></span>
-   <span data-ttu-id="957c6-119">透過共用存放集區設定支援存放裝置布建</span><span class="sxs-lookup"><span data-stu-id="957c6-119">Supports storage provisioning through the shared storage pool configuration</span></span>
-   <span data-ttu-id="957c6-120">根據儲存空間的需求和使用量，增加或減少儲存集區的大小</span><span class="sxs-lookup"><span data-stu-id="957c6-120">Increases or decreases the size of the storage pool according to the demand and usage of storage space</span></span>

<span data-ttu-id="957c6-121">Windows 精簡布建功能的摘要：</span><span class="sxs-lookup"><span data-stu-id="957c6-121">Summary of the Windows Thin Provisioning features:</span></span>

-   <span data-ttu-id="957c6-122">精簡布建 LUN 識別</span><span class="sxs-lookup"><span data-stu-id="957c6-122">Thin Provisioning LUN identification</span></span>
-   <span data-ttu-id="957c6-123">閾值通知、暫存資源耗盡和永久資源耗盡的控制碼</span><span class="sxs-lookup"><span data-stu-id="957c6-123">Handles for threshold notification, temporary resource exhaustion, and permanent resource exhaustion</span></span>
-   <span data-ttu-id="957c6-124">儲存空間回收</span><span class="sxs-lookup"><span data-stu-id="957c6-124">Storage space reclamation</span></span>
-   <span data-ttu-id="957c6-125">邏輯區塊的對應狀態查詢</span><span class="sxs-lookup"><span data-stu-id="957c6-125">Mapping state queries of logical blocks</span></span>

## <a name="manifestation"></a><span data-ttu-id="957c6-126">表現</span><span class="sxs-lookup"><span data-stu-id="957c6-126">Manifestation</span></span>

<span data-ttu-id="957c6-127">如果沒有適當瞭解精簡布建 LUN 的 Windows 控制碼，應用程式可能會因為未預期的行為或不明的原因而失敗。</span><span class="sxs-lookup"><span data-stu-id="957c6-127">Without the proper understanding of the Windows handles for thin provisioning LUN, the app could fail with unexpected behavior or for an unknown cause.</span></span>

## <a name="using-thin-provisioning-luns"></a><span data-ttu-id="957c6-128">使用精簡布建 Lun</span><span class="sxs-lookup"><span data-stu-id="957c6-128">Using thin provisioning LUNs</span></span>

<span data-ttu-id="957c6-129">若要在 Windows 8 或 Windows Server 2012 中使用精簡布建的 Lun，系統和存放裝置系統管理員應留意這些重要事項：</span><span class="sxs-lookup"><span data-stu-id="957c6-129">To use thinly provisioned LUNs in Windows 8 or Windows Server 2012, system and storage administrators should be aware of these matters:</span></span>

-   <span data-ttu-id="957c6-130">精簡布建 LUN 識別;系統管理員或終端使用者可以使用重組和儲存優化器公用程式來識別存放裝置的媒體類型</span><span class="sxs-lookup"><span data-stu-id="957c6-130">Thin provisioning LUN identification; system administrators or end users can use Defrag and the Storage Optimizer utility to identify the media type of the storage device</span></span>
-   <span data-ttu-id="957c6-131">當達到閾值或永久資源耗盡事件時，Windows 會記錄系統事件以警示系統管理員</span><span class="sxs-lookup"><span data-stu-id="957c6-131">When a threshold or a permanent resource exhaustion event is hit, Windows will log a system event to alert the system administrator</span></span>
-   <span data-ttu-id="957c6-132">儲存體空間回收可透過檔案刪除通知或存放裝置優化器的排程器來手動或自動執行</span><span class="sxs-lookup"><span data-stu-id="957c6-132">Storage space reclamation can be performed manually or automatically by file delete notification or the scheduler of the storage optimizer</span></span>
-   <span data-ttu-id="957c6-133">存放裝置系統管理員應執行閾值通知，以警示系統管理員或使用者，並避免任何未預期的儲存體服務中斷</span><span class="sxs-lookup"><span data-stu-id="957c6-133">Storage administrator should implement the threshold notification to alert system administrator or end user and avoid any unexpected storage service interruption</span></span>

## <a name="tests"></a><span data-ttu-id="957c6-134">測試</span><span class="sxs-lookup"><span data-stu-id="957c6-134">Tests</span></span>

-   <span data-ttu-id="957c6-135">存放裝置陣列必須接收 Windows 8 精簡布建憑證，才能支援 Windows 精簡布建功能</span><span class="sxs-lookup"><span data-stu-id="957c6-135">Storage array must receive Windows 8 Thin Provisioning certificate to support Windows Thin Provisioning features</span></span>
-   <span data-ttu-id="957c6-136">適用于存放裝置陣列的 Windows 精簡布建硬體認證套件將是一個有用的測試控管，可確認存放裝置陣列的 Windows 精簡布建功能支援的功能</span><span class="sxs-lookup"><span data-stu-id="957c6-136">Windows Thin Provisioning Hardware Certification Kit for storage array will be a useful test tool to verify storage array’s capability for Windows Thin Provisioning feature support</span></span>
-   <span data-ttu-id="957c6-137">Windows 預期精簡布建 LUN 和完整布建 LUN 可在相同的系統中運作，而不會發生任何問題</span><span class="sxs-lookup"><span data-stu-id="957c6-137">Windows expects the Thin Provisioning LUN and Full Provisioning LUN to work in the same system without any issue</span></span>

## <a name="resources"></a><span data-ttu-id="957c6-138">資源</span><span class="sxs-lookup"><span data-stu-id="957c6-138">Resources</span></span>

-   [<span data-ttu-id="957c6-139">T10 SCSI Block 命令規格 (SBC3r27) </span><span class="sxs-lookup"><span data-stu-id="957c6-139">T10 SCSI Block Command Spec (SBC3r27)</span></span>](https://www.t10.org/cgi-bin/ac.pl?t=f&f=sbc3r27.pdf)
-   [<span data-ttu-id="957c6-140">硬體儀表板服務</span><span class="sxs-lookup"><span data-stu-id="957c6-140">Hardware Dashboard Services</span></span>](/windows-hardware/drivers/dashboard/)

 

 