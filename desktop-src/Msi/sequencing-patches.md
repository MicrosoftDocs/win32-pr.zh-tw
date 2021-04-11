---
description: 從 Windows Installer 3.0 開始，作者可以將修補程式排序資訊新增至 MsiPatchSequence 資料表中的 patch 封裝資料庫。
ms.assetid: 9cdcb25f-2c3d-411e-9aae-bdd52df38a97
title: 排序修補程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa9cbd9aead596abfaeb50d972915bf4d618440d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195420"
---
# <a name="sequencing-patches"></a>排序修補程式

從 Windows Installer 3.0 開始，作者可以將修補程式排序資訊新增至 [MsiPatchSequence](msipatchsequence-table.md) 資料表中的 patch 封裝資料庫。 安裝程式可以使用這項資訊來判斷哪些修補程式適用于安裝套件、判斷最佳修補順序，以及以固定順序安裝修補程式，而不受系統提供的順序影響。

**Windows Installer 2.0：** 不支援。 Windows Installer Windows Installer 3.0 之前的版本會依照提供給系統的順序來安裝修補程式，而不論它們是否包含 [MsiPatchSequence](msipatchsequence-table.md) 資料表。

以下是使用修補程式排序功能的必要條件。

-    ( .msp 檔) [修補套件](patch-packages.md)必須有一個包含順序資訊的[MsiPatchSequence](msipatchsequence-table.md)資料表。 安裝程式會以提供給系統的順序來安裝沒有 MsiPatchSequence 資料表的修補程式。
-   使用 Windows Installer 3.0 或更新版本安裝修補程式。

Windows Installer 3.0 版具有下列功能，可讓應用程式用來判斷最佳的修補順序。

-   [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea)函式會取得修補程式的清單，並決定可將它們套用至已安裝產品的順序。 此函式會針對已安裝在系統上的任何修補程式或產品進行帳戶。
-   [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa)函式會取得修補程式的清單，並決定可將它們套用至已安裝產品的順序。 此函式不會考慮已安裝在系統上的任何修補程式或產品。

Windows Installer 版本3.0 可在單一修補安裝中，將多個修補程式套用至產品。 修補程式的群組可以包含修補程式，其中包括修補順序資訊 ([MsiPatchSequence](msipatchsequence-table.md) 資料表) 和不包含的修補程式。 Windows Installer 會以提供給系統的順序，安裝沒有此資料表的修補套件。 安裝程式會將缺少 MsiPatchSequence 資料表的修補程式帳戶，但在下一節中所述的方法標示為已淘汰或取代的修補程式。

當 Windows Installer 3.0 版安裝多個修補程式時，會遵循下列步驟來判斷將個別修補程式套用至產品的順序：

1.  安裝的修補程式如果沒有 [MsiPatchSequence](msipatchsequence-table.md) 資料表，則會依照套用至產品的順序放入順序中。 第一個套用的修補程式會先放置於序列中。
2.  在序列中會放入沒有 [MsiPatchSequence 資料表](msipatchsequence-table.md) 的新修補程式。 目前的修補安裝正在套用這些修補程式。 它們會依照提供給系統的順序放置，並放在步驟1中的所有修補程式之後。
3.  已淘汰的修補程式會從修補程式順序中去除。
    > [!Note]  
    > Patch 封裝可在 [ [**修訂編號摘要**](revision-number-summary.md) ] 屬性中指定修補程式要移除之過時修補程式的明確清單。 這份清單適用于3.0 版之前的 Windows Installer 版本。 Windows Installer 版本3.0 會從序列中移除標示為過時的修補程式（只有在修補程式沒有 [MsiPatchSequence 資料表](msipatchsequence-table.md)時）。

     

4.  安裝程式會逐步解說修補順序，並判斷哪些修補程式適用于指定的順序。 當有多個修補程式套用至產品時，序列中的每個修補程式也會將產品的安裝資料庫轉換 ( .msi 檔案) 。 只有當修補程式的資料庫轉換能夠採用將所有先前 [修補封裝](patch-packages.md)的轉換套用至 product 資料庫所產生的 [產品代碼](product-codes.md)、[**版本**](productversion.md)、[**語言**](productlanguage.md)和 [**upgradecode**](upgradecode.md)時，才適用于特定的順序。 安裝程式會從序列中排除任何不適用修補程式。
5.  安裝程式會開始將具有排序資訊的修補程式放在其 [MsiPatchSequence](msipatchsequence-table.md) 資料表中。 具有 MsiPatchSequence 資料表的[次要升級](minor-upgrades.md)修補程式會放在先前步驟中已排序的修補程式之後，以及升級後的最低到最高產品版本順序。 Windows Installer 接著會排除在此順序中不適用的任何次要升級修補程式。
6.  以具有[MsiPatchSequence](msipatchsequence-table.md)資料表的[次要](minor-upgrades.md)升級為目標的[小型更新](small-updates.md)修補程式，會指派給順序中最高版本的次要升級修補程式。
7.  在先前步驟之後維持未指派，且具有[MsiPatchSequence](msipatchsequence-table.md)資料表的所有[小型更新](small-updates.md)修補程式，都會放在具有 MsiPatchSequence 資料表的第一個[次要升級](minor-upgrades.md)之前，以及在 .msi 安裝資料庫和沒有 MsiPatchSequence 資料表的任何修補程式之後。 Windows Installer 接著會排除在此順序中不適用的任何小型更新修補程式。
8.  Windows Installer 版本3.0 會從序列中排除已取代的修補程式。 當修補程式取代稍早在修補程式順序中所發生的修補程式時，修補程式會包含先前修補程式中的所有修正程式。 不再需要較舊的修補程式。 Windows Installer 需要 [MsiPatchSequence](msipatchsequence-table.md) 資料表中的資訊，以排除取代的修補程式。
    > [!Note]  
    > 必須撰寫修補程式以取代舊版修補程式的修補程式，以取代所有修補程式系列中的較早修補程式。 [小型更新](small-updates.md) 修補程式只能取代小更新。 [次要升級](minor-upgrades.md) 可以取代小型更新和其他次要升級。

     

9.  包含[MsiPatchSequence](msipatchsequence-table.md)資料表的[小型更新](small-updates.md)修補程式，會根據其 MsiPatchSequence 資料表中的排序資訊，在產品版本中進行排序。 這會決定最終的修補順序。

不應再使用的修補程式可以從修補順序中排除。 如需如何從修補順序中消除修補程式的詳細資訊，請參閱 [消除修補程式](eliminating-patches.md)。

如需如何使用 [MsiPatchSequence](msipatchsequence-table.md) 資料表來依照撰寫的順序套用修補程式的範例，請參閱 [多個修補範例](multiple-patching-example.md)。

 

 



