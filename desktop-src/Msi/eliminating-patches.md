---
description: 不應再使用的修補程式可以從修補順序中排除。
ms.assetid: b1d499d9-4fd3-4996-84a1-c32acefbb98f
title: 消除修補程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a705ce5919ffd36e6fc860403e11db56c6df1592
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981155"
---
# <a name="eliminating-patches"></a><span data-ttu-id="db099-103">消除修補程式</span><span class="sxs-lookup"><span data-stu-id="db099-103">Eliminating Patches</span></span>

<span data-ttu-id="db099-104">不應再使用的修補程式可以從修補順序中排除。</span><span class="sxs-lookup"><span data-stu-id="db099-104">A patch that should no longer be used can be eliminated from the patching sequence.</span></span> <span data-ttu-id="db099-105">這可防止在修補目標應用程式時套用修補程式。</span><span class="sxs-lookup"><span data-stu-id="db099-105">This prevents the patch from being applied when the target application is patched.</span></span> <span data-ttu-id="db099-106">這與移除已套用至應用程式的修補程式不同。</span><span class="sxs-lookup"><span data-stu-id="db099-106">This is different than removing a patch that is already applied to an application.</span></span> <span data-ttu-id="db099-107">如需移除已套用修補程式的相關資訊，請參閱 [移除修補程式](removing-patches.md)。</span><span class="sxs-lookup"><span data-stu-id="db099-107">For information about removing applied patches, see [Removing Patches](removing-patches.md).</span></span>

<span data-ttu-id="db099-108">\* \* Windows Installer 3.0 和更新版本： \* \*</span><span class="sxs-lookup"><span data-stu-id="db099-108">\*\*Windows Installer 3.0 and later:  \*\*</span></span>

<span data-ttu-id="db099-109">具有 [MsiPatchSequence](msipatchsequence-table.md) 資料表的修補程式可使用此資料表來消除修補順序的修補程式。</span><span class="sxs-lookup"><span data-stu-id="db099-109">Patches that have the [MsiPatchSequence](msipatchsequence-table.md) table can use this table to eliminate patches from the patching sequence.</span></span> <span data-ttu-id="db099-110">修補程式可以消除修補順序中之前的修補程式，並將這些修補程式的資訊取代為其本身的資訊。</span><span class="sxs-lookup"><span data-stu-id="db099-110">A patch can eliminate patches that come before it in the patching sequence, and replace the information from those patches with its own information.</span></span> <span data-ttu-id="db099-111">這兩個修補程式會指定要排除的修補程式，以及要排除的修補程式，都必須有包含資訊的 MsiPatchSequence 資料表。</span><span class="sxs-lookup"><span data-stu-id="db099-111">Both the patch that specifies which patches to eliminate and the patches being eliminated must have a MsiPatchSequence table that contains information.</span></span>

<span data-ttu-id="db099-112">如果消除修補程式和取代修補程式沒有 [MsiPatchSequence](msipatchsequence-table.md) 資料表，修補程式套件可以在 [ [**修訂編號摘要**](revision-number-summary.md) ] 屬性中指定要從修補順序中排除的修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="db099-112">If the eliminated patches and replacement patch do not have [MsiPatchSequence](msipatchsequence-table.md) tables, the patch package can specify a list of patches to be eliminated from the patching sequence in its [**Revision Number Summary**](revision-number-summary.md) property.</span></span> <span data-ttu-id="db099-113">如果已刪除或取代的修補程式具有 MsiPatchSequence 資料表，則 Windows Installer 3.0 會忽略此清單。</span><span class="sxs-lookup"><span data-stu-id="db099-113">Windows Installer 3.0 ignores this list if either the eliminated or replacement patches have a MsiPatchSequence table.</span></span>

<span data-ttu-id="db099-114">當修補套件包含 [MsiPatchSequence](msipatchsequence-table.md) 資料表中具有順序資訊的修補程式，以及未使用這項資訊的一些修補程式時，Windows installer 3.0 會依下一節所述的順序來排序修補程式： [排序修補程式](sequencing-patches.md)。</span><span class="sxs-lookup"><span data-stu-id="db099-114">When the patch package contains patches with sequence information in the [MsiPatchSequence](msipatchsequence-table.md) table and some patches without this information, Windows installer 3.0 sequences the patches in the order described in the following section: [Sequencing Patches](sequencing-patches.md).</span></span>

<span data-ttu-id="db099-115">例如，Patch1、Patch2 和 Patch3 可以是三個沒有 [MsiPatchSequence](msipatchsequence-table.md) 資料表的修補程式。</span><span class="sxs-lookup"><span data-stu-id="db099-115">For example, Patch1, Patch2, and Patch3 can be three patches that do not have the [MsiPatchSequence](msipatchsequence-table.md) table.</span></span> <span data-ttu-id="db099-116">Patch2 可以是只適用于 Patch1 已套用至應用程式的修補程式。</span><span class="sxs-lookup"><span data-stu-id="db099-116">Patch2 can be a patch that is only applicable if Patch1 has already been applied to the application.</span></span> <span data-ttu-id="db099-117">Patch3 可以是較新的修補程式，其中包含 Patch1 中的所有資訊，也可從修補順序中排除 Patch1。</span><span class="sxs-lookup"><span data-stu-id="db099-117">Patch3 can be a later patch that has all the information in Patch1 and also eliminates Patch1 from the patching sequence.</span></span> <span data-ttu-id="db099-118">這表示當套用 Patch3 時，Patch 2 也會變成不適用，因為它需要 Patch1。</span><span class="sxs-lookup"><span data-stu-id="db099-118">This means that when Patch3 is applied, Patch 2 also becomes inapplicable, because it requires Patch1.</span></span> <span data-ttu-id="db099-119">Patch2 中的任何資訊都不會傳遞至應用程式。</span><span class="sxs-lookup"><span data-stu-id="db099-119">Any information in Patch2 alone does not get delivered to the application.</span></span>

<span data-ttu-id="db099-120">**Windows Installer 2.0：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="db099-120">**Windows Installer 2.0:** Not supported.</span></span> <span data-ttu-id="db099-121">唯一可用的方法是指定要從 [ [**修訂編號摘要**](revision-number-summary.md) ] 屬性中的修補順序中刪除的修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="db099-121">The only method available is to specify the list of patches to be eliminated from the patching sequence in the [**Revision Number Summary**](revision-number-summary.md) property.</span></span>

> [!Note]  
> <span data-ttu-id="db099-122">Patch 作者應使用 [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) 和 [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) 函式來判斷實際套用至產品的修補程式順序，因為排除某些修補程式可能會轉譯其他修補程式不適用。</span><span class="sxs-lookup"><span data-stu-id="db099-122">Patch authors should use the [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) and [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) functions to determine the sequence of patches that actually get applied to the product because the elimination of some patches can render other patches inapplicable.</span></span>

 

 

 



