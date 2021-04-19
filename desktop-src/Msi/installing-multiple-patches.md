---
description: 從 Windows Installer 3.0 開始，可以將多個修補程式依固定順序套用至產品，而不考慮將修補程式提供給系統的順序。
ms.assetid: 10af1857-d59f-490d-9b50-49619b1e892c
title: 安裝多個修補程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d4edb8d085ede6aee81690bf67bd9c5e19780ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977801"
---
# <a name="installing-multiple-patches"></a><span data-ttu-id="97302-103">安裝多個修補程式</span><span class="sxs-lookup"><span data-stu-id="97302-103">Installing Multiple Patches</span></span>

<span data-ttu-id="97302-104">從 Windows Installer 3.0 開始，可以將多個修補程式依固定順序套用至產品，而不考慮將修補程式提供給系統的順序。</span><span class="sxs-lookup"><span data-stu-id="97302-104">Beginning with Windows Installer 3.0, multiple patches can be applied to a product in a constant order, regardless of the order that the patches are provided to the system.</span></span>

<span data-ttu-id="97302-105">**Windows Installer 2.0：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="97302-105">**Windows Installer 2.0:** Not supported.</span></span> <span data-ttu-id="97302-106">版本3.0 之前的 Windows Installer 版本一律會依照提供給系統的順序來安裝修補程式。</span><span class="sxs-lookup"><span data-stu-id="97302-106">Windows Installer versions earlier than version 3.0 always install patches in the order that they are provided to the system.</span></span>

<span data-ttu-id="97302-107">**Windows Installer 3.0 和更新版本：** 安裝程式可以使用 [MsiPatchSequence](msipatchsequence-table.md) 資料表中提供的資訊，判斷哪些修補程式適用于 Windows Installer 封裝，以及應套用修補程式的順序。</span><span class="sxs-lookup"><span data-stu-id="97302-107">**Windows Installer 3.0 and later:** The installer can use the information provided in the [MsiPatchSequence](msipatchsequence-table.md) table to determine which patches are applicable to the Windows Installer package and in which order the patches should be applied.</span></span> <span data-ttu-id="97302-108">應用程式可以使用 [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) 和 [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) 函數。</span><span class="sxs-lookup"><span data-stu-id="97302-108">Applications can use the [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) and [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) functions.</span></span>

<span data-ttu-id="97302-109">[**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa)函式會決定要將哪些修補程式套用至 Windows Installer 套件，以及在何種順序中。</span><span class="sxs-lookup"><span data-stu-id="97302-109">The [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) function determines which patches apply to the Windows Installer package and in what sequence.</span></span> <span data-ttu-id="97302-110">此函數可以考慮已取代或已淘汰的修補程式。</span><span class="sxs-lookup"><span data-stu-id="97302-110">The function can account for superseded or obsolete patches.</span></span> <span data-ttu-id="97302-111">此函式不會將安裝在未指定之系統上的產品或修補程式考慮。</span><span class="sxs-lookup"><span data-stu-id="97302-111">This function does not account for products or patches that are installed on the system that are not specified in the set.</span></span>

<span data-ttu-id="97302-112">[**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) Sequence 函數可以針對指定之已安裝產品的修補程式，判斷其最適合的應用程式順序。</span><span class="sxs-lookup"><span data-stu-id="97302-112">The [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) Sequence function can determine the best sequence of application for the patches to a specified installed product.</span></span> <span data-ttu-id="97302-113">此函式會針對已套用至產品的修補程式，以及已淘汰和取代的修補程式帳戶。</span><span class="sxs-lookup"><span data-stu-id="97302-113">This function accounts for patches that have already been applied to the product, and accounts for obsolete and superseded patches.</span></span>

<span data-ttu-id="97302-114">當 patch 封裝沒有 [MsiPatchSequence](msipatchsequence-table.md) 資料表時，安裝程式一律會依照提供給系統的順序套用修補程式。</span><span class="sxs-lookup"><span data-stu-id="97302-114">When the patch package does not have a [MsiPatchSequence](msipatchsequence-table.md) table, the installer always applies the patches in the order that they are provide to the system.</span></span>

<span data-ttu-id="97302-115">當修補套件包含 [MsiPatchSequence](msipatchsequence-table.md) 資料表中具有順序資訊的修補程式混合，以及未使用此資訊的一些修補程式時，Windows installer 版本3.0 會依下一節中所述的順序，將修補程式順序 [排序：排序修補程式](sequencing-patches.md)。</span><span class="sxs-lookup"><span data-stu-id="97302-115">When the patch package contains a mixture of patches with sequence information in the [MsiPatchSequence](msipatchsequence-table.md) table and some patches without this information, Windows installer version 3.0 sequences the patches in the order described in the following section: [Sequencing Patches](sequencing-patches.md).</span></span>

<span data-ttu-id="97302-116">安裝或更新應用程式時，Windows Installer 套件可以安裝127以上的修補程式。</span><span class="sxs-lookup"><span data-stu-id="97302-116">A Windows Installer package can install no more than 127 patches when installing or updating an application.</span></span> <span data-ttu-id="97302-117">當需要許多更新時，應該將它們合併，而舊的過時修補程式應從修補順序中去除。</span><span class="sxs-lookup"><span data-stu-id="97302-117">When many updates are necessary, they should be combined and previous obsolete patches should be eliminated from the patching sequence.</span></span>

<span data-ttu-id="97302-118">您可以從修補順序中排除不應使用的修補程式。</span><span class="sxs-lookup"><span data-stu-id="97302-118">A patch that should not be used can be eliminated from the patching sequence.</span></span> <span data-ttu-id="97302-119">這可防止在修補目標應用程式時套用修補程式。</span><span class="sxs-lookup"><span data-stu-id="97302-119">This prevents the patch from being applied when the target application is patched.</span></span> <span data-ttu-id="97302-120">這與移除已套用至應用程式的修補程式不同。</span><span class="sxs-lookup"><span data-stu-id="97302-120">This is different than removing a patch that has already been applied to an application.</span></span> <span data-ttu-id="97302-121">如需有關從修補順序中刪除修補程式的詳細資訊，請參閱 [消除修補程式](eliminating-patches.md)。</span><span class="sxs-lookup"><span data-stu-id="97302-121">For more information about eliminating patches from the patching sequence, see [Eliminating Patches](eliminating-patches.md).</span></span> <span data-ttu-id="97302-122">如需移除已套用修補程式的相關資訊，請參閱 [移除修補程式](removing-patches.md)。</span><span class="sxs-lookup"><span data-stu-id="97302-122">For information about removing applied patches, see [Removing Patches](removing-patches.md).</span></span>

<span data-ttu-id="97302-123">如需 Windows Installer 如何在全部都有 [MsiPatchSequence](msipatchsequence-table.md) 資料表時套用多個修補程式的範例，請參閱 [多個修補範例](multiple-patching-example.md)。</span><span class="sxs-lookup"><span data-stu-id="97302-123">For an example of how Windows Installer applies multiple patches when all have [MsiPatchSequence](msipatchsequence-table.md) tables, see the [Multiple Patching Example](multiple-patching-example.md).</span></span>

 

 



