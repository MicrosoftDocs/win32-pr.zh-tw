---
title: 'Windows 映像檔案開機 (的 WimBoot) '
description: 'Windows 映像檔案開機 (的 WimBoot) '
ms.assetid: 1C4EFC42-6698-4981-8C55-D1DFC6309F31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9f14ea506226e2c16d771ecec52fa31a8c871b4
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/10/2020
ms.locfileid: "103684193"
---
# <a name="windows-image-file-boot-wimboot"></a><span data-ttu-id="4dea9-103">Windows 映像檔案開機 (的 WimBoot) </span><span class="sxs-lookup"><span data-stu-id="4dea9-103">Windows Image File Boot (WimBoot)</span></span>

## <a name="platform"></a><span data-ttu-id="4dea9-104">平台</span><span class="sxs-lookup"><span data-stu-id="4dea9-104">Platform</span></span>

<span data-ttu-id="4dea9-105">**用戶端：** Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="4dea9-105">**Clients:** Windows 8.1</span></span>  

## <a name="description"></a><span data-ttu-id="4dea9-106">Description</span><span class="sxs-lookup"><span data-stu-id="4dea9-106">Description</span></span>

<span data-ttu-id="4dea9-107">WimBoot 是 Oem 部署 Windows 的另一種方式。</span><span class="sxs-lookup"><span data-stu-id="4dea9-107">WimBoot is an alternative way for OEMs to deploy Windows.</span></span> <span data-ttu-id="4dea9-108">WimBoot 部署會從壓縮的 Windows 映像檔案中，直接啟動並執行 Windows (WIM) 。</span><span class="sxs-lookup"><span data-stu-id="4dea9-108">A WimBoot deployment boots and runs Windows directly out of a compressed Windows Image File (WIM).</span></span> <span data-ttu-id="4dea9-109">此 WIM 檔案是不可變的，且其存取權是由新的檔案系統篩選器驅動程式 (WoF.sys) 所管理。</span><span class="sxs-lookup"><span data-stu-id="4dea9-109">This WIM file is immutable, and access to it is managed by a new file system filter driver (WoF.sys).</span></span>

<span data-ttu-id="4dea9-110">結果是安裝 Windows 所需的磁碟空間大幅減少。</span><span class="sxs-lookup"><span data-stu-id="4dea9-110">The result is a significant reduction in the disk space required to install Windows.</span></span>

## <a name="manifestations"></a><span data-ttu-id="4dea9-111">表現</span><span class="sxs-lookup"><span data-stu-id="4dea9-111">Manifestations</span></span>

<span data-ttu-id="4dea9-112">大部分的應用程式應該完全不會受到 WimBoot 的影響。</span><span class="sxs-lookup"><span data-stu-id="4dea9-112">Most applications should be completely unaffected by WimBoot.</span></span> <span data-ttu-id="4dea9-113">只有存取和解除鎖定系統檔案或預先載入之檔案的應用程式可能會受到影響。</span><span class="sxs-lookup"><span data-stu-id="4dea9-113">Only applications that access and unlock system files or pre-loaded files for write access may be affected.</span></span> <span data-ttu-id="4dea9-114">由於 WIM 是不可變的，因此 (也就是系統或預先載入的檔案) 的更新，只會儲存在 C： \\ 磁碟分割上。</span><span class="sxs-lookup"><span data-stu-id="4dea9-114">Since the WIM is immutable, updates to it (that is, system or pre-loaded files) are simply stored on the C:\\ partition.</span></span>

<span data-ttu-id="4dea9-115">如果應用程式解除鎖定所有 WIM 型系統和預先載入之檔案的寫入存取權，則 WimBoot 提供的節省將會完全遺失，因為這些檔案都將解壓縮並放在 C：磁片區上 \\ 。</span><span class="sxs-lookup"><span data-stu-id="4dea9-115">If an application unlocked write access for all WIM-backed system and pre-loaded files, the savings that WimBoot delivers would be completely lost, as all of these files would be decompressed and placed on the C:\\ volume.</span></span>

<span data-ttu-id="4dea9-116">此外，備份與還原應用程式必須留意到 WimBoot 部署，因為 WIM 存在於不同的磁碟分割;也就是說，在備份時， \\ 必須儲存 C：和 WIM 磁碟分割，而且兩者都必須一起還原。</span><span class="sxs-lookup"><span data-stu-id="4dea9-116">Furthermore, back-up and restore applications need to be aware of WimBoot deployments, as the WIM is present in a separate partition; that is, on back-up, both the C:\\ and WIM partitions must be saved and both must be restored together.</span></span>

## <a name="solution"></a><span data-ttu-id="4dea9-117">解決方法</span><span class="sxs-lookup"><span data-stu-id="4dea9-117">Solution</span></span>

<span data-ttu-id="4dea9-118">引進新的 Api，可讓應用程式直接查詢指定的磁片區或檔案是否受 WIM 支援。</span><span class="sxs-lookup"><span data-stu-id="4dea9-118">New APIs were introduced that allow applications to directly query if a given volume or file is backed by a WIM.</span></span> <span data-ttu-id="4dea9-119">這項資訊可讓應用程式做出適當的決策，例如僅針對讀取權限開啟這些檔案，或識別必須一起備份和還原的磁片區/磁碟分割。</span><span class="sxs-lookup"><span data-stu-id="4dea9-119">This information allows applications to make appropriate decisions, such as opening these files only for read access or to identify volumes/partitions that have to be backed up and restored together.</span></span>

## <a name="compatibility-performance-reliability-or-usability-tests"></a><span data-ttu-id="4dea9-120">相容性、效能、可靠性或可用性測試</span><span class="sxs-lookup"><span data-stu-id="4dea9-120">Compatibility, performance, reliability, or usability tests</span></span>

<span data-ttu-id="4dea9-121">應用程式開發人員應該在 WimBoot 系統上測試其軟體及其對應的案例，特別是當這些應用程式存取系統或預先載入的檔案時。</span><span class="sxs-lookup"><span data-stu-id="4dea9-121">Application developers should test their software and its corresponding scenarios on a WimBoot system, especially if these applications access system or pre-loaded files.</span></span> <span data-ttu-id="4dea9-122">在完成案例後，請特別注意，以大幅減少可用磁碟空間。</span><span class="sxs-lookup"><span data-stu-id="4dea9-122">Special attention should be paid to a significant reduction in available disk space after a scenario has been completed.</span></span>

 

 




