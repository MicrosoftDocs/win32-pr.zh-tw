---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: daa383ba-994e-4986-9979-119576cecd1c
title: 'W (磁碟區陰影複製服務) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9295be608f81d82104c1d55f3656d1a24243a87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511505"
---
# <a name="w-volume-shadow-copy-service"></a>W (磁碟區陰影複製服務) 

[](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) W X [](vssgloss-v.md) Y Z

<dl> <dt>

<span id="base.vssgloss_windows_file_protection"></span><span id="BASE.VSSGLOSS_WINDOWS_FILE_PROTECTION"></span>**Windows 檔案保護**
</dt> <dd>

保護特殊作業系統檔案的系統服務。 如果刪除或覆寫這些檔案的其中一個，Windows 檔案保護會以原始檔取代其快取中的檔案。

</dd> <dt>

<span id="base.vssgloss_writer"></span><span id="BASE.VSSGLOSS_WRITER"></span>**作家**
</dt> <dd>

此應用程式會使用與 VSS 陰影複製和陰影複製相關的作業（例如備份和還原）來協調其 i/o 作業 (例如備份和還原) ，如此一來，陰影複製的磁片區上所含的資料就會處於一致的狀態。

為了支援此協調，寫入器必須執行衍生自抽象基類 **CVssWriter** 的類別實例，以與 VSS 基礎結構進行通訊。 另請參閱 [*陰影複製*](vssgloss-s.md)。

</dd> <dt>

<span id="base.vssgloss_writer_class"></span><span id="BASE.VSSGLOSS_WRITER_CLASS"></span>**寫入器類別**
</dt> <dd>

全域唯一識別碼 (GUID) 在初始化期間由寫入器提供，表示它屬於指定的寫入器類型。 例如，多個寫入器的執行可以共用相同的寫入器類別識別碼。

相同類別的寫入器可能會由其寫入器實例來區分。 應用程式開發人員可以指定寫入器類別。 另請參閱 *寫入器實例*。

</dd> <dt>

<span id="base.vssgloss_writer_instance"></span><span id="BASE.VSSGLOSS_WRITER_INSTANCE"></span>**寫入器實例**
</dt> <dd>

全域唯一識別碼 (GUID) 為系統上執行的每個寫入器處理常式提供。 每次寫入器啟動時，就會產生寫入器實例的唯一值。

</dd> <dt>

<span id="base.vssgloss_writer_metadata_document"></span><span id="BASE.VSSGLOSS_WRITER_METADATA_DOCUMENT"></span>**寫入器元資料檔案**
</dt> <dd>

寫入器所建立的 XML 檔 (使用 **IVssCreateWriterMetadata** 介面) 包含寫入器的狀態和元件的相關資訊。 要求者可以在執行還原或備份作業時，使用 **IVssExamineWriterMetadata** 介面) 來查詢寫入器元資料檔案 (。

寫入器元資料檔案包含所有寫入器元件的清單，其中任何一項都可能參與備份。 這與要求者的備份元件檔不同，其中只包含針對備份或還原作業明確包含的元件。

一旦建立之後，就應該將寫入器元資料檔案視為唯讀物件。 您可以將它儲存到磁片。 另請參閱 [*備份元件檔*](vssgloss-b.md)、 [*明確元件包含*](vssgloss-e.md)、 [*隱含元件包含*](vssgloss-i.md)。

</dd> </dl>

 

 



