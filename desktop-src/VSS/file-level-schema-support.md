---
description: 寫入器可以藉由指定檔案規格備份類型（以位元遮罩表示），或使用 VSS \_ 檔 \_ 規格 \_ 備份 \_ 類型列舉的成員位或成員，來微調檔案集層級的各種備份效能。
ms.assetid: a3ac69b4-894a-4536-8fab-f45ad7e5118a
title: 檔案層級架構支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550885a540e62fc145541bae979fad34cb9488f62f9f26ea17e647068c1fad46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006367"
---
# <a name="file-level-schema-support"></a>檔案層級架構支援

寫入器可以藉由指定檔案規格備份類型（以位元遮罩表示），或使用 [**VSS \_ 檔 \_ 規格 \_ 備份 \_ 類型**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)列舉的成員位或成員，來微調檔案 [*集*](vssgloss-f.md)層級的各種備份效能。

針對指定的備份類型，寫入器會指出下列各項：

-   是否需要將磁片區陰影複製，以正確地備份檔案集。 比方說，如果檔案集中的檔案不是由寫入器獨佔開啟，而且可以確保它是穩定的，就不需要陰影複製。
-   無論要求者是否需要以這樣的方式來執行備份，不論上次修改時間或其他問題為何，都會還原備份的檔案集檔案的版本。 一般而言，這表示會在備份過程中複製檔案集。

表示陰影複製需求的 [**VSS \_ 檔 \_ 規格 \_ 備份 \_ 類型**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) 值為：

-   VSS \_ FSBT \_ 需要所有的 \_ 快照 \_ 集
-   VSS \_ FSBT \_ \_ 需要完整快照 \_ 集
-   \_需要 VSS FSBT \_ 差異 \_ 快照 \_ 集
-   \_需要 VSS FSBT \_ 增量 \_ 快照 \_ 集
-   \_需要 VSS FSBT \_ 記錄 \_ 快照 \_ 集

[**VSS \_ 檔 \_ 規格 \_ 備份 \_ 類型**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)的值，表示備份檔案的需求如下：

-   VSS \_ FSBT \_ \_ 需要所有備份 \_
-   VSS \_ FSBT \_ \_ 需要完整備份 \_
-   \_需要 VSS FSBT \_ 差異 \_ 備份 \_
-   \_需要 VSS FSBT \_ 增量 \_ 備份 \_
-   \_需要 VSS FSBT \_ 記錄 \_ 備份 \_

根據預設，檔案集會標記為 VSS \_ FSBT \_ 所有 \_ 需要備份的 \_ \| vss \_ FSBT \_ 所有 \_ 需要的快照集 \_ ，這表示在處理檔案集的檔案時一律需要陰影複製，而且應該將檔案複製到所有類型的備份中。

 

 



