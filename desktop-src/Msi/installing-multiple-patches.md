---
description: 從 Windows Installer 3.0 開始，可以將多個修補程式依固定順序套用至產品，而不考慮將修補程式提供給系統的順序。
ms.assetid: 10af1857-d59f-490d-9b50-49619b1e892c
title: 安裝多個修補程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65dc6b65997bd6bcb2b9f4c8da5022adda9a38b0b93401dc507397421799d260
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893848"
---
# <a name="installing-multiple-patches"></a>安裝多個修補程式

從 Windows Installer 3.0 開始，可以將多個修補程式依固定順序套用至產品，而不考慮將修補程式提供給系統的順序。

**Windows Installer 2.0：** 不支援。 Windows版本3.0 之前的安裝程式版本一律會依照提供給系統的順序來安裝修補程式。

**Windows Installer 3.0 和更新版本：** 安裝程式可以使用 [MsiPatchSequence](msipatchsequence-table.md)資料表中提供的資訊，判斷哪些修補程式適用于 Windows Installer 封裝，以及應套用修補程式的順序。 應用程式可以使用 [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) 和 [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) 函數。

[**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa)函式會決定要將哪些修補程式套用至 Windows Installer 套件，以及在何種順序中。 此函數可以考慮已取代或已淘汰的修補程式。 此函式不會將安裝在未指定之系統上的產品或修補程式考慮。

[**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) Sequence 函數可以針對指定之已安裝產品的修補程式，判斷其最適合的應用程式順序。 此函式會針對已套用至產品的修補程式，以及已淘汰和取代的修補程式帳戶。

當 patch 封裝沒有 [MsiPatchSequence](msipatchsequence-table.md) 資料表時，安裝程式一律會依照提供給系統的順序套用修補程式。

當修補套件包含[MsiPatchSequence](msipatchsequence-table.md)資料表中具有順序資訊的修補程式混合，以及未使用這項資訊的一些修補程式時，Windows 安裝程式3.0 版會依照下一節所述的順序來排序修補程式：[排序修補程式](sequencing-patches.md)。

安裝或更新應用程式時，Windows Installer 套件可以安裝127以上的修補程式。 當需要許多更新時，應該將它們合併，而舊的過時修補程式應從修補順序中去除。

您可以從修補順序中排除不應使用的修補程式。 這可防止在修補目標應用程式時套用修補程式。 這與移除已套用至應用程式的修補程式不同。 如需有關從修補順序中刪除修補程式的詳細資訊，請參閱 [消除修補程式](eliminating-patches.md)。 如需移除已套用修補程式的相關資訊，請參閱 [移除修補程式](removing-patches.md)。

如需 Windows Installer 如何在全部都有[MsiPatchSequence](msipatchsequence-table.md)資料表時套用多個修補程式的範例，請參閱[多個修補範例](multiple-patching-example.md)。

 

 



