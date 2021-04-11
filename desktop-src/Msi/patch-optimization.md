---
description: Windows Installer 可以優化修補程式，以減少將修補程式套用至已安裝應用程式所需的時間。
ms.assetid: 2bb1c94a-55b6-4aee-b86d-ee9e1f8ed290
title: 修補程式優化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86215855bb02314d7eb54c774541b0a2086c7c99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848771"
---
# <a name="patch-optimization"></a><span data-ttu-id="b2a1f-103">修補程式優化</span><span class="sxs-lookup"><span data-stu-id="b2a1f-103">Patch Optimization</span></span>

<span data-ttu-id="b2a1f-104">Windows Installer 可以優化修補程式，以減少將修補程式套用至已安裝應用程式所需的時間。</span><span class="sxs-lookup"><span data-stu-id="b2a1f-104">Windows Installer can optimize patching to reduce the time that is required to apply patches to installed applications.</span></span>

<span data-ttu-id="b2a1f-105">**Windows Installer 2.0：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="b2a1f-105">**Windows Installer 2.0:** Not supported.</span></span> <span data-ttu-id="b2a1f-106">針對 Windows Installer 3.0 之前發行的 Windows Installer 版本，修補會執行應用程式的完整修複安裝，這可能需要花費更多時間。</span><span class="sxs-lookup"><span data-stu-id="b2a1f-106">For versions of Windows Installer released before Windows Installer 3.0, patching runs a complete repair installation of the application, which can take significantly more time.</span></span>

<span data-ttu-id="b2a1f-107">**Windows Installer 3.0 和更新版本：** 修補程式只會變更修補程式修改過的應用程式部分。</span><span class="sxs-lookup"><span data-stu-id="b2a1f-107">**Windows Installer 3.0 and later:** The patching process only changes the parts of an application that are modified by a patch.</span></span>

<span data-ttu-id="b2a1f-108">**Windows Installer 3.1 和更新版本：** 從 Windows Installer 3.1 開始，修補程式優化要求交易中的所有修補程式都會將 OptimizedInstallMode 屬性設定為1， ([MsiPatchMetadata 資料表](msipatchmetadata-table.md)中的一個) 。</span><span class="sxs-lookup"><span data-stu-id="b2a1f-108">**Windows Installer 3.1 and later:** Beginning with Windows Installer 3.1, patch optimization requires that all patches in the transaction have the OptimizedInstallMode property set to 1 (one) in the [MsiPatchMetadata Table](msipatchmetadata-table.md).</span></span>

<span data-ttu-id="b2a1f-109">如果 patch 只修改了下表，則 Windows Installer 3.0 或更新版本會略過與其他所有資料表相關聯的動作，即使這些動作列在原始應用程式安裝套件的順序資料表中， ( .msi 檔案) 。</span><span class="sxs-lookup"><span data-stu-id="b2a1f-109">If a patch only modifies the following tables, Windows Installer 3.0 or later skips the actions that are associated with all the other tables, even if those actions are listed in the sequence tables of the original application installation package (.msi file).</span></span>

-   [<span data-ttu-id="b2a1f-110">AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="b2a1f-110">AdminExecuteSequence</span></span>](adminexecutesequence-table.md)
-   [<span data-ttu-id="b2a1f-111">AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="b2a1f-111">AdminUISequence</span></span>](adminuisequence-table.md)
-   [<span data-ttu-id="b2a1f-112">Condition</span><span class="sxs-lookup"><span data-stu-id="b2a1f-112">Condition</span></span>](condition-table.md)
-   [<span data-ttu-id="b2a1f-113">CustomAction</span><span class="sxs-lookup"><span data-stu-id="b2a1f-113">CustomAction</span></span>](customaction-table.md)
-   [<span data-ttu-id="b2a1f-114">檔案</span><span class="sxs-lookup"><span data-stu-id="b2a1f-114">File</span></span>](file-table.md)
-   [<span data-ttu-id="b2a1f-115">FileSFPCatalog</span><span class="sxs-lookup"><span data-stu-id="b2a1f-115">FileSFPCatalog</span></span>](filesfpcatalog-table.md)
-   [<span data-ttu-id="b2a1f-116">InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="b2a1f-116">InstallExecuteSequence</span></span>](installexecutesequence-table.md)
-   [<span data-ttu-id="b2a1f-117">InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="b2a1f-117">InstallUISequence</span></span>](installuisequence-table.md)
-   [<span data-ttu-id="b2a1f-118">媒體</span><span class="sxs-lookup"><span data-stu-id="b2a1f-118">Media</span></span>](media-table.md)
-   [<span data-ttu-id="b2a1f-119">MoveFile</span><span class="sxs-lookup"><span data-stu-id="b2a1f-119">MoveFile</span></span>](movefile-table.md)
-   [<span data-ttu-id="b2a1f-120">MsiAssembly</span><span class="sxs-lookup"><span data-stu-id="b2a1f-120">MsiAssembly</span></span>](msiassembly-table.md)
-   [<span data-ttu-id="b2a1f-121">MsiDigitalCertificate</span><span class="sxs-lookup"><span data-stu-id="b2a1f-121">MsiDigitalCertificate</span></span>](msidigitalcertificate-table.md)
-   [<span data-ttu-id="b2a1f-122">MsiDigitalSignature</span><span class="sxs-lookup"><span data-stu-id="b2a1f-122">MsiDigitalSignature</span></span>](msidigitalsignature-table.md)
-   [<span data-ttu-id="b2a1f-123">MsiFileHash</span><span class="sxs-lookup"><span data-stu-id="b2a1f-123">MsiFileHash</span></span>](msifilehash-table.md)
-   [<span data-ttu-id="b2a1f-124">MsiPatchHeaders</span><span class="sxs-lookup"><span data-stu-id="b2a1f-124">MsiPatchHeaders</span></span>](msipatchheaders-table.md)
-   [<span data-ttu-id="b2a1f-125">修補</span><span class="sxs-lookup"><span data-stu-id="b2a1f-125">Patch</span></span>](patch-table.md)
-   [<span data-ttu-id="b2a1f-126">PatchPackage</span><span class="sxs-lookup"><span data-stu-id="b2a1f-126">PatchPackage</span></span>](patchpackage-table.md)
-   [<span data-ttu-id="b2a1f-127">屬性</span><span class="sxs-lookup"><span data-stu-id="b2a1f-127">Property</span></span>](property-table.md)
-   [<span data-ttu-id="b2a1f-128">登錄</span><span class="sxs-lookup"><span data-stu-id="b2a1f-128">Registry</span></span>](registry-table.md)
-   [<span data-ttu-id="b2a1f-129">SFPCatalog</span><span class="sxs-lookup"><span data-stu-id="b2a1f-129">SFPCatalog</span></span>](sfpcatalog-table.md)
-   [<span data-ttu-id="b2a1f-130">類型</span><span class="sxs-lookup"><span data-stu-id="b2a1f-130">TypeLib</span></span>](typelib-table.md)
-   [<span data-ttu-id="b2a1f-131">\_資料行</span><span class="sxs-lookup"><span data-stu-id="b2a1f-131">\_Columns</span></span>](-columns-table.md)
-   [<span data-ttu-id="b2a1f-132">\_存儲</span><span class="sxs-lookup"><span data-stu-id="b2a1f-132">\_Storages</span></span>](-storages-table.md)
-   [<span data-ttu-id="b2a1f-133">\_串流</span><span class="sxs-lookup"><span data-stu-id="b2a1f-133">\_Streams</span></span>](-streams-table.md)
-   [<span data-ttu-id="b2a1f-134">\_Tables</span><span class="sxs-lookup"><span data-stu-id="b2a1f-134">\_Tables</span></span>](-tables-table.md)
-   [<span data-ttu-id="b2a1f-135">\_TransformView 資料表</span><span class="sxs-lookup"><span data-stu-id="b2a1f-135">\_TransformView Table</span></span>](-transformview-table.md)
-   [<span data-ttu-id="b2a1f-136">\_驗證</span><span class="sxs-lookup"><span data-stu-id="b2a1f-136">\_Validation</span></span>](-validation-table.md)

<span data-ttu-id="b2a1f-137">若要關閉修補程式優化選項，請使用 [DisableFlyWeightPatching](disableflyweightpatching.md) 原則。</span><span class="sxs-lookup"><span data-stu-id="b2a1f-137">To turn off the patch optimization option, use the [DisableFlyWeightPatching](disableflyweightpatching.md) policy.</span></span>

 

 



