---
description: 在處理備份時，「要求者」和「寫入器」會協調以提供穩定的系統映射， (陰影複製的磁片區) 來備份資料、將檔案群組在一起，以及將資訊儲存在儲存的資料上。
ms.assetid: d7acb2a2-bb58-47e3-a950-d32f663ae36d
title: 在 VSS 下處理備份的總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a11aeab87b503241acefdd15a153c9e417e537
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318984"
---
# <a name="overview-of-processing-a-backup-under-vss"></a>在 VSS 下處理備份的總覽

在處理備份時，「要求者」和「寫入器」會協調以提供穩定的系統映射， (陰影複製的磁片區) 來備份資料、將檔案群組在一起，以及將資訊儲存在儲存的資料上。 這必須在只為寫入器的一般工作流程產生最少量的中斷時完成。

要求者會查詢其中繼資料的寫入器、處理此資料、在陰影複製和備份作業開始前通知寫入器，然後在陰影複製和備份作業結束之後再次通知寫入器。

為了回應這些通知，寫入器會提供要備份之檔案的相關資訊，包括指定要協調 ([*元件*](vssgloss-c.md) 的檔案群組) -在陰影複製之前，在其 i/o 作業中暫停，然後在陰影複製完成或備份結束後回到正常操作。

在處理備份的過程中，寫入器會透過其唯讀中繼資料來指定其負責的檔案（寫入器元資料檔案 (參閱 [VSS 中繼資料：使用寫入器元資料檔案](working-with-the-writer-metadata-document.md)) 。 然後，要求者會解讀此中繼資料、選擇要備份的內容，並將這些決策儲存在自己的中繼資料物件中、備份元件檔 (參閱 [VSS 中繼資料：使用備份元件檔](working-with-the-backup-components-document.md)) 。 這份備份元件檔適用于備份和還原作業期間的寫入器檢查和修改。

下圖顯示要求者、VSS 服務、VSS 核心支援、相關的任何 VSS 寫入器，以及任何 VSS 硬體提供者之間的互動。

![要求者、備份元件、寫入器與提供者之間的互動](images/vssimpl.png)

若要更充分瞭解執行備份所牽涉到的基本工作，將此總覽細分為下列主題會很有用：

-   [備份初始化的總覽](overview-of-backup-initialization.md)
-   [備份探索階段總覽](overview-of-the-backup-discovery-phase.md)
-   [備份前工作總覽](overview-of-pre-backup-tasks.md)
-   [檔的實際備份總覽](overview-of-actual-backup-of-files.md)
-   [備份終止的總覽](overview-of-backup-termination.md)

 

 



