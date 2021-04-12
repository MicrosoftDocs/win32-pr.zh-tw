---
description: 要求者是使用 VSS API 的任何應用程式 (特別是 >ivssbackupcomponents 介面) 要求磁碟區陰影複製服務的服務，以建立和管理一或多個磁片區的陰影複製和陰影複製集。
ms.assetid: e49920d0-5b66-4aa1-b3ca-641629df5f8a
title: 要求者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b676b8cd287365b257e3b6ee85a7e47a70f88ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192288"
---
# <a name="requesters"></a>要求者

要求 [*者是使用*](vssgloss-r.md) VSS API 的任何應用程式 (特別是 [**>ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) 介面) 要求磁碟區陰影複製服務的服務，以建立和管理一或多個磁片區的陰影複製和陰影複製集。

要求者 (的最常見範例和本檔中所述的唯一) 是 VSS 感知的備份/還原應用程式，它會使用陰影複製的資料做為其備份作業的穩定來源。

除了初始陰影複製之外，備份/復原要求者應用程式還會與資料產生者 (寫入器通訊) 收集系統資訊，以及指示寫入器準備資料進行備份。

## <a name="requester-state"></a>要求者狀態

要求者會將其狀態資訊保留在名為「備份元件」檔的 XML 中繼資料物件中。 要求者中繼資料是必要的，但不足以允許要求者進行備份，然後還原檔案系統。 原因如下：

-   在備份作業期間，只會在備份中包含的所有元件的子集：[*其*](vssgloss-s.md) 備份元件，而不是可針對備份的備份元件進行選取，並且可針對已在備份中 [*明確包含*](vssgloss-e.md) 的備份元件進行選擇，也就是將其資訊新增至要求者的備份元件檔。
-   即使是新增至備份元件檔的元件，也不完整的資訊，也不會包含檔案和路徑規格。
-   在還原作業期間，可 [*針對還原選取*](vssgloss-s.md)[*隱含包含*](vssgloss-i.md)在備份中的元件，因此可以明確地包含在還原中。 這將需要更新要求者的備份元件檔，並提供來自寫入器寫入器元資料檔案之預存複本的資訊。

若要允許完整的備份或還原作業規格，VSS API 可讓要求者在備份期間查詢執行中的寫入器中繼資料 () 或在還原) 期間檢查儲存的寫入器中繼資料 (。 此外，寫入器可以在備份或還原作業期間，修改備份元件檔中的元件資訊。

使用已針對備份和還原選取哪些元件的相關資訊，以及有關元件選取的規則 (如需詳細資訊，請參閱 [設定元件組織](definition-of-components-by-writers.md) 和 [使用 Selectability 和邏輯路徑](working-with-selectability-and-logical-paths.md)) ，要求者可以判斷需要備份或還原的寫入器檔案，以及可在何處找到這些檔案。

在備份過程中，要求者和寫入器中繼資料必須儲存，才能用於還原。 相反地，還原作業需要抓取舊的備份元件和寫入器元資料檔案，以取得還原檔案的完整指示。

## <a name="requester-interprocess-communication"></a>要求者處理序間通訊

要求者會藉由在要求者 API 中透過各種呼叫產生 COM 事件，來維持對 VSS 備份和還原作業的控制權。 這些呼叫可以執行下列作業：

-   要求提供者（例如， [**>ivssbackupcomponents：:D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) ）會讓提供者建立所選磁片區的陰影複製。
-   觸發寫入器以傳回信息，例如， [**>ivssbackupcomponents：： GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) 可讓要求者取得每個寫入器的寫入器元資料檔案。
-   需要寫入器來準備或處理陰影複製和備份作業的各個階段，例如， [**>ivssbackupcomponents：:P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) 會發出 i/o 凍結的寫入器。

要求者會透過即時或儲存的寫入器元資料檔案，以及透過使用 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 介面（可供寫入器進行更新），從寫入器接收資訊。

## <a name="life-cycle-of-a-requester-during-backup"></a>備份期間要求者的生命週期

以下是備份的要求者生命週期摘要：

1.  具現化並初始化 VSS API 介面。
2.  聯絡寫入器並取得其資訊。
3.  選擇要備份的資料。
4.  要求提供者的陰影複製。
5.  備份資料。
6.  釋放介面和陰影複製。

## <a name="life-cycle-of-a-requester-during-restore"></a>在還原期間要求者的生命週期

還原生命週期不需要陰影複製，但仍需要寫入合作：

1.  具現化 VSS API 介面。
2.  藉由載入儲存的備份元件檔，初始化還原作業的要求者。
3.  取出儲存的寫入器中繼資料和備份元件檔。
4.  請聯絡寫入器以初始化合作。
5.  檢查備份元件檔的寫入器更新。
6.  還原資料。

 

 



