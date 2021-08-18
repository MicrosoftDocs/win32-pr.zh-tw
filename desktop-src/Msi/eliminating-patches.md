---
description: 不應再使用的修補程式可以從修補順序中排除。
ms.assetid: b1d499d9-4fd3-4996-84a1-c32acefbb98f
title: 消除修補程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f025c6487293d07df7963514b79f551045398f8d86f51dd7ab98b589a605e762
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913518"
---
# <a name="eliminating-patches"></a>消除修補程式

不應再使用的修補程式可以從修補順序中排除。 這可防止在修補目標應用程式時套用修補程式。 這與移除已套用至應用程式的修補程式不同。 如需移除已套用修補程式的相關資訊，請參閱 [移除修補程式](removing-patches.md)。

* * Windows Installer 3.0 和更新版本： * *

具有 [MsiPatchSequence](msipatchsequence-table.md) 資料表的修補程式可使用此資料表來消除修補順序的修補程式。 修補程式可以消除修補順序中之前的修補程式，並將這些修補程式的資訊取代為其本身的資訊。 這兩個修補程式會指定要排除的修補程式，以及要排除的修補程式，都必須有包含資訊的 MsiPatchSequence 資料表。

如果消除修補程式和取代修補程式沒有 [MsiPatchSequence](msipatchsequence-table.md) 資料表，修補程式套件可以在 [ [**修訂編號摘要**](revision-number-summary.md) ] 屬性中指定要從修補順序中排除的修補程式清單。 Windows如果已刪除或取代的修補程式具有 MsiPatchSequence 資料表，則安裝程式3.0 會忽略此清單。

當修補套件包含[MsiPatchSequence](msipatchsequence-table.md)資料表中具有順序資訊的修補程式，以及未使用這項資訊的一些修補程式時，Windows 安裝程式3.0 會依下一節中所述的順序來排列修補程式：[排序修補程式](sequencing-patches.md)。

例如，Patch1、Patch2 和 Patch3 可以是三個沒有 [MsiPatchSequence](msipatchsequence-table.md) 資料表的修補程式。 Patch2 可以是只適用于 Patch1 已套用至應用程式的修補程式。 Patch3 可以是較新的修補程式，其中包含 Patch1 中的所有資訊，也可從修補順序中排除 Patch1。 這表示當套用 Patch3 時，Patch 2 也會變成不適用，因為它需要 Patch1。 Patch2 中的任何資訊都不會傳遞至應用程式。

**Windows Installer 2.0：** 不支援。 唯一可用的方法是指定要從 [ [**修訂編號摘要**](revision-number-summary.md) ] 屬性中的修補順序中刪除的修補程式清單。

> [!Note]  
> Patch 作者應使用 [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) 和 [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) 函式來判斷實際套用至產品的修補程式順序，因為排除某些修補程式可能會轉譯其他修補程式不適用。

 

 

 



