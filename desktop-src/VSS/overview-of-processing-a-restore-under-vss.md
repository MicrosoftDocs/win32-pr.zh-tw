---
description: 在 VSS 下處理備份時，要求者和寫入器會一起運作，以產生穩定的系統映射來備份資料，而這需要協調和建立目前系統的陰影複製。
ms.assetid: 1cefb6ac-f2bb-464b-a62f-05be91ae56f7
title: 在 VSS 下處理還原的總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b01094a02b823f372271f14c04801820407573b9351bfe7e2fc2ad9dc74077
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117937956"
---
# <a name="overview-of-processing-a-restore-under-vss"></a>在 VSS 下處理還原的總覽

在 VSS 下處理備份時，要求者和寫入器會一起運作，以產生穩定的系統映射來備份資料，而這需要協調和建立目前系統的陰影複製。

相較于 VSS 備份，要求者和寫入器的目的是要產生穩定的系統映射，以從中複製資料，以 VSS 為基礎的還原目標是將檔案以最實用的方式傳回磁片，以對目前在系統上執行的應用程式)  (的寫入器。 這不需要穩定的系統映射，因此不需要陰影複製。

相反地，注意的重點是要避免寫入器活動中斷、防止在磁片上建立不一致的資料集，並允許寫入器在必要時評估及合併資料所需的範圍。

如同備份作業，VSS 還原需要存取備份元件檔和寫入元資料檔案。 這些檔通常不會藉由查詢執行中的應用程式取得，而是從備份媒體上儲存為 XML 檔的版本中取出。

就像備份作業期間一樣，寫入器元資料檔案仍會保留唯讀物件，且 (取出之後) 備份元件檔仍可進行修改。 修改備份元件檔可讓寫入器和要求者進行下列動作：

-   使用 [*還原目標*](vssgloss-r.md)覆寫 [*restore 方法*](vssgloss-r.md)
-   使用 [*替代位置* 對應](vssgloss-a.md)
-   將檔案還原至磁片上的新位置
-   在備份期間使用不同的選取規則

為了更充分了解執行還原所牽涉到的基本工作，將此概觀細分成下列主題會很有用：

-   [還原初始化的總覽](overview-of-restore-initialization.md)
-   [準備還原的總覽](overview-of-preparing-for-restore.md)
-   [實際檔案還原的總覽](overview-of-actual-file-restoration.md)
-   [還原清除和終止的總覽](overview-of-restore-clean-up-and-termination.md)

 

 



