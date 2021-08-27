---
description: 為了回應識別事件，系統中出現的每個寫入器都會使用 IVssCreateWriterMetadata 來建立自己的寫入器元資料檔案。 識別事件通常是由呼叫 >ivssbackupcomponents：： GatherWriterMetadata 的要求者所產生。
ms.assetid: bae9bbe7-ca55-47cb-b253-8092007cb181
title: 寫入器元資料檔案生命週期
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2796d1a7b995f13829ac81485f74fa342bebe5e0e312b7b014d761a9962aa74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118121570"
---
# <a name="writer-metadata-document-life-cycle"></a>寫入器元資料檔案生命週期

為了回應 [*識別事件*](vssgloss-i.md)，系統中出現的每個寫入器都會使用 [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata)來建立自己的寫入器元資料檔案。 *識別事件* 通常是由呼叫 [**>ivssbackupcomponents：： GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)的要求者所產生。

建立寫入器元資料檔案時，可以透過 [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) 介面或透過寫入器初始化 ([**CVssWriter：： Initialize**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-initialize)) ，寫入器必須明確指定下列各項：

-   [*Restore 方法*](vssgloss-r.md)
-   寫入器名稱
-   [*寫入器類別識別碼*](vssgloss-w.md)
-   數據使用量 (請參閱 [**VSS \_ 使用 \_ 類型**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type)) 
-   日期來源類型 (請參閱 [**VSS \_ 來源 \_ 類型**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type)) 

此外，也可以指定下列各項：

-   元件 (不一定會包含檔案集) 
-   新增替代對應
-   排除檔案清單

在 [備份初始化期間的寫入器動作](overview-of-backup-initialization.md)中，可找到寫入器元資料檔案建立的總覽。

要求者通常會使用兩種方法之一來取得寫入器中繼資料的存取權：

-   在大部分的備份作業期間，要求者會使用 [**>ivssbackupcomponents：： GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) 來取得 [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) 介面的實例，以允許存取目前執行之寫入器的中繼資料。
-   針對還原作業或使用匯入陰影複製的備份 (如需匯入陰影複製的詳細資訊，請參閱匯入可 [傳送的陰影複製磁片](importing-transportable-shadow-copied-volumes.md) 區) ，要求者會抓取包含中繼資料的 XML 檔，並使用 [**CreateVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssexaminewritermetadata) 取得 [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) 介面，以用來讀取還原中繼資料。

寫入器元資料檔案可讓要求者執行備份，以瞭解目前在備份的探索階段期間執行的寫入器。

針對選擇要參與備份的寫入器，要求者會在備份的探索階段期間，將寫入器元資料檔案中的大部分資訊（但不是全部）匯入自己的備份元件檔中。

不過，只有寫入器元資料檔案，而不是備份元件檔包含檔案和路徑規格。

如需有關如何執行備份作業之探索階段的詳細資訊，請參閱 [備份探索階段的總覽](overview-of-the-backup-discovery-phase.md)。

此外，只有 [*明確包含*](vssgloss-e.md) 的元件會在備份作業期間，將其資訊儲存在備份元件檔中。 在備份作業期間，不會在備份元件檔中包含 [*隱含包含*](vssgloss-i.md) 元件的相關資訊，而且必須使用明確包含的元件和可用的寫入器元資料檔案的相關資訊來插入。

隱含包含的元件可能仍可 [*供還原*](vssgloss-s.md) ，而且可能需要在還原時明確包含在備份元件檔中。 在這種情況下，如同在備份作業期間新增元件所需的 writer's 寫入器元資料檔案的存取權， (接著從寫入器中取出) ，要求者需要存取該寫入器的寫入器元資料檔案（在備份時儲存）的複本。

因此，若要取得有關備份或還原之所有檔案和元件的所有資訊，唯一的方法就是將參與備份的每個寫入器的每個寫入器元資料檔案，與備份元件檔一起儲存。  (需詳細資訊，請參閱 [實際檔案還原的總覽](overview-of-actual-file-restoration.md)。 ) 

 

 



