---
description: 下列範例顯示如何使用 Windows Installer 3.0 和更新版本，以撰寫修補程式的順序來套用修補程式。
ms.assetid: 98771652-cec2-4371-8132-a741cf8431fb
title: 多個修補範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2d10274531ac4906ef61a49caee9ccbcde98bbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983575"
---
# <a name="multiple-patching-example"></a><span data-ttu-id="c547a-103">多個修補範例</span><span class="sxs-lookup"><span data-stu-id="c547a-103">Multiple Patching Example</span></span>

<span data-ttu-id="c547a-104">下列範例顯示如何使用 Windows Installer 3.0 和更新版本，以撰寫修補程式的順序來套用修補程式。</span><span class="sxs-lookup"><span data-stu-id="c547a-104">The following example shows how Windows Installer 3.0 and later can be used to apply patches in the order in which they are authored.</span></span>

## <a name="example"></a><span data-ttu-id="c547a-105">範例</span><span class="sxs-lookup"><span data-stu-id="c547a-105">Example</span></span>

<span data-ttu-id="c547a-106">在此範例中，有三個修補程式： QFE1、QFE2 和 ServicePack1，而且每個都有 [MsiPatchSequence](msipatchsequence-table.md) 資料表。</span><span class="sxs-lookup"><span data-stu-id="c547a-106">In this example there are three patches, QFE1, QFE2, and ServicePack1, and they each have a [MsiPatchSequence](msipatchsequence-table.md) table.</span></span> <span data-ttu-id="c547a-107">這些修補程式已撰寫成要套用至1.0 版的應用程式。</span><span class="sxs-lookup"><span data-stu-id="c547a-107">These patches have been authored to be applied to version 1.0 of the application.</span></span>



| <span data-ttu-id="c547a-108">修補程式名稱</span><span class="sxs-lookup"><span data-stu-id="c547a-108">Patch Name</span></span>   | <span data-ttu-id="c547a-109">修補類型</span><span class="sxs-lookup"><span data-stu-id="c547a-109">Patch Type</span></span>    | <span data-ttu-id="c547a-110">序號</span><span class="sxs-lookup"><span data-stu-id="c547a-110">Sequence Number</span></span> |
|--------------|---------------|-----------------|
| <span data-ttu-id="c547a-111">QFE1</span><span class="sxs-lookup"><span data-stu-id="c547a-111">QFE1</span></span>         | <span data-ttu-id="c547a-112">Small Update</span><span class="sxs-lookup"><span data-stu-id="c547a-112">Small Update</span></span>  | <span data-ttu-id="c547a-113">1.1.0</span><span class="sxs-lookup"><span data-stu-id="c547a-113">1.1.0</span></span>           |
| <span data-ttu-id="c547a-114">QFE2</span><span class="sxs-lookup"><span data-stu-id="c547a-114">QFE2</span></span>         | <span data-ttu-id="c547a-115">Small Update</span><span class="sxs-lookup"><span data-stu-id="c547a-115">Small Update</span></span>  | <span data-ttu-id="c547a-116">1.2.0</span><span class="sxs-lookup"><span data-stu-id="c547a-116">1.2.0</span></span>           |
| <span data-ttu-id="c547a-117">ServicePack1</span><span class="sxs-lookup"><span data-stu-id="c547a-117">ServicePack1</span></span> | <span data-ttu-id="c547a-118">次要升級</span><span class="sxs-lookup"><span data-stu-id="c547a-118">Minor Upgrade</span></span> | <span data-ttu-id="c547a-119">1.3.0</span><span class="sxs-lookup"><span data-stu-id="c547a-119">1.3.0</span></span>           |



 

<span data-ttu-id="c547a-120">每個修補程式的 [MsiPatchSequence](msipatchsequence-table.md) 資料表只有一筆記錄，其中包含 patch 系列、產品代碼和序號。</span><span class="sxs-lookup"><span data-stu-id="c547a-120">The [MsiPatchSequence](msipatchsequence-table.md) table of each patch has only one record that contains the patch family, product code, and sequence number.</span></span> <span data-ttu-id="c547a-121">這三個修補程式全都套用至相同的產品，而且屬於相同的 patch 系列（名為 AppPatch）。</span><span class="sxs-lookup"><span data-stu-id="c547a-121">The three patches are all applied to the same product and belong to the same patch family, named AppPatch.</span></span> <span data-ttu-id="c547a-122">沒有任何修補程式具有 **msidbPatchSequenceSupersedeEarlier** 屬性。</span><span class="sxs-lookup"><span data-stu-id="c547a-122">None of the patches have the **msidbPatchSequenceSupersedeEarlier** attribute.</span></span>

<span data-ttu-id="c547a-123">QFE1 [small update](small-updates.md)的[MsiPatchSequence 資料表](msipatchsequence-table.md)。</span><span class="sxs-lookup"><span data-stu-id="c547a-123">[MsiPatchSequence Table](msipatchsequence-table.md) for the QFE1 [small update](small-updates.md).</span></span> 

| <span data-ttu-id="c547a-124">PatchFamily</span><span class="sxs-lookup"><span data-stu-id="c547a-124">PatchFamily</span></span> | <span data-ttu-id="c547a-125">ProductCode</span><span class="sxs-lookup"><span data-stu-id="c547a-125">ProductCode</span></span>                            | <span data-ttu-id="c547a-126">順序</span><span class="sxs-lookup"><span data-stu-id="c547a-126">Sequence</span></span> | <span data-ttu-id="c547a-127">屬性</span><span class="sxs-lookup"><span data-stu-id="c547a-127">Attributes</span></span> |
|-------------|----------------------------------------|----------|------------|
| <span data-ttu-id="c547a-128">AppPatch</span><span class="sxs-lookup"><span data-stu-id="c547a-128">AppPatch</span></span>    | <span data-ttu-id="c547a-129">{18A9233C-0B34-4127-A966-C257386270BC}</span><span class="sxs-lookup"><span data-stu-id="c547a-129">{18A9233C-0B34-4127-A966-C257386270BC}</span></span> | <span data-ttu-id="c547a-130">1.1.0</span><span class="sxs-lookup"><span data-stu-id="c547a-130">1.1.0</span></span>    |            |



 

<span data-ttu-id="c547a-131">QFE2 [small update](small-updates.md)的[MsiPatchSequence 資料表](msipatchsequence-table.md)。</span><span class="sxs-lookup"><span data-stu-id="c547a-131">[MsiPatchSequence Table](msipatchsequence-table.md) for the QFE2 [small update](small-updates.md).</span></span> 

| <span data-ttu-id="c547a-132">PatchFamily</span><span class="sxs-lookup"><span data-stu-id="c547a-132">PatchFamily</span></span> | <span data-ttu-id="c547a-133">ProductCode</span><span class="sxs-lookup"><span data-stu-id="c547a-133">ProductCode</span></span>                            | <span data-ttu-id="c547a-134">順序</span><span class="sxs-lookup"><span data-stu-id="c547a-134">Sequence</span></span> | <span data-ttu-id="c547a-135">屬性</span><span class="sxs-lookup"><span data-stu-id="c547a-135">Attributes</span></span> |
|-------------|----------------------------------------|----------|------------|
| <span data-ttu-id="c547a-136">AppPatch</span><span class="sxs-lookup"><span data-stu-id="c547a-136">AppPatch</span></span>    | <span data-ttu-id="c547a-137">{18A9233C-0B34-4127-A966-C257386270BC}</span><span class="sxs-lookup"><span data-stu-id="c547a-137">{18A9233C-0B34-4127-A966-C257386270BC}</span></span> | <span data-ttu-id="c547a-138">1.2.0</span><span class="sxs-lookup"><span data-stu-id="c547a-138">1.2.0</span></span>    |            |



 

<span data-ttu-id="c547a-139">用於 ServicePack1[次要升級](minor-upgrades.md)的[MsiPatchSequence 資料表](msipatchsequence-table.md)。</span><span class="sxs-lookup"><span data-stu-id="c547a-139">[MsiPatchSequence Table](msipatchsequence-table.md) for ServicePack1 [minor upgrade](minor-upgrades.md).</span></span> 

| <span data-ttu-id="c547a-140">PatchFamily</span><span class="sxs-lookup"><span data-stu-id="c547a-140">PatchFamily</span></span> | <span data-ttu-id="c547a-141">ProductCode</span><span class="sxs-lookup"><span data-stu-id="c547a-141">ProductCode</span></span>                            | <span data-ttu-id="c547a-142">順序</span><span class="sxs-lookup"><span data-stu-id="c547a-142">Sequence</span></span> | <span data-ttu-id="c547a-143">屬性</span><span class="sxs-lookup"><span data-stu-id="c547a-143">Attributes</span></span> |
|-------------|----------------------------------------|----------|------------|
| <span data-ttu-id="c547a-144">AppPatch</span><span class="sxs-lookup"><span data-stu-id="c547a-144">AppPatch</span></span>    | <span data-ttu-id="c547a-145">{18A9233C-0B34-4127-A966-C257386270BC}</span><span class="sxs-lookup"><span data-stu-id="c547a-145">{18A9233C-0B34-4127-A966-C257386270BC}</span></span> | <span data-ttu-id="c547a-146">1.3.0</span><span class="sxs-lookup"><span data-stu-id="c547a-146">1.3.0</span></span>    |            |



 

<span data-ttu-id="c547a-147">如果使用者安裝1.0 版的產品，然後再套用 QFE2，然後在稍後決定要套用 QFE1，Windows Installer 可確保在 QFE2 上 QFE1 套用修補應用程式的有效順序。</span><span class="sxs-lookup"><span data-stu-id="c547a-147">If a user installs version 1.0 of the product, and then applies QFE2, and then at a later date decides to apply QFE1, Windows Installer ensures that the effective sequence of patch application to the product is QFE1 applied ahead of QFE2.</span></span> <span data-ttu-id="c547a-148">如果使用者套用 ServicePack1，然後在日後套用 QFE2 和 QFE1，Windows Installer 可確保修補應用程式在產品上的有效順序 QFE1 在 QFE2 之前，以及在 ServicePack1 之前。</span><span class="sxs-lookup"><span data-stu-id="c547a-148">If the user applies ServicePack1, then applies QFE2 and QFE1 together at a later date, Windows Installer ensures that the effective sequence of patch application to the product is QFE1 ahead of QFE2 and ahead of ServicePack1.</span></span>

<span data-ttu-id="c547a-149">如果 ServicePack1 在其 [MsiPatchSequence](msipatchsequence-table.md)資料表的 Attributes 資料行中設定 **msidbPatchSequenceSupersedeEarlier** ，這表示 service PACK 包含 QFE1 和 QFE2 中的所有變更。</span><span class="sxs-lookup"><span data-stu-id="c547a-149">If ServicePack1 has **msidbPatchSequenceSupersedeEarlier** set in the Attributes column of its [MsiPatchSequence](msipatchsequence-table.md) table, this means that the service pack contains all the changes in QFE1 and QFE2.</span></span> <span data-ttu-id="c547a-150">在此情況下，套用 ServicePack1 時，不會套用 QFE1 和 QFE2。</span><span class="sxs-lookup"><span data-stu-id="c547a-150">In this case, QFE1 and QFE2 are not applied when ServicePack1 is applied.</span></span>

<span data-ttu-id="c547a-151">**Windows Installer 2.0：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="c547a-151">**Windows Installer 2.0:** Not supported.</span></span> <span data-ttu-id="c547a-152">早于 Windows Installer 3.0 的版本，每個交易只可安裝一個修補程式，而修補程式會依照提供的順序套用。</span><span class="sxs-lookup"><span data-stu-id="c547a-152">Versions earlier than Windows Installer 3.0 can install only one patch per transaction and patches are applied in the sequence that they are provided.</span></span> <span data-ttu-id="c547a-153">在上述範例中，如果先套用 QFE2，然後套用 QFE1，則這是兩筆交易，而修補程式會套用至順序 QFE2 中的應用程式1.0 版，後面接著 QFE1。</span><span class="sxs-lookup"><span data-stu-id="c547a-153">For the preceding example, if QFE2 is applied first and then QFE1 is applied, that is two transactions and the patches are applied to version 1.0 of the application in the sequence QFE2 followed by QFE1.</span></span> <span data-ttu-id="c547a-154">如果先套用 ServicePack1，則 QFE1 或 QFE2 無法套用於稍後的交易，因為 ServicePack1 是變更應用程式版本的次要升級。</span><span class="sxs-lookup"><span data-stu-id="c547a-154">If ServicePack1 is applied first, then QFE1 or QFE2 cannot be applied in a later transaction because ServicePack1 is a minor upgrade that changes the application version.</span></span> <span data-ttu-id="c547a-155">QFE1 和 QFE2 只能套用至應用程式的1.0 版。</span><span class="sxs-lookup"><span data-stu-id="c547a-155">QFE1 and QFE2 can only be applied to version 1.0 of the application.</span></span>

 

 



