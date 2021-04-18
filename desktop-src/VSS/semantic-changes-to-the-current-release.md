---
description: 使用 IVssCreateWriterMetadata：： AddFilesToFileGroup、IVssCreateWriterMetadata：： AddDatabaseFiles 或 IVssCreateWriterMetadata：： AddDatabaseLogFiles 時) ，路徑、檔案規格和遞迴旗標 (wszPath、wszFileSpec 和 bRecursive 的組合，必須符合其中一個使用：：、：：或：：新增至寫入器元件的其中一個檔案集合：
ms.assetid: debf181a-1579-46f2-86ef-a1d2a850e99e
title: Windows Server 2003 的語義變更
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53b9d2edc56f215f554b497eebff9f76a1da53dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192286"
---
# <a name="semantic-changes-to-windows-server-2003"></a>Windows Server 2003 的語義變更

使用 IVssCreateWriterMetadata：： AddFilesToFileGroup、IVssCreateWriterMetadata：： AddDatabaseFiles 或 IVssCreateWriterMetadata：： AddDatabaseLogFiles 時) ，路徑、檔案規格和遞迴旗標 (*wszPath*、 *wszFileSpec* 和 *bRecursive* 的組合，必須符合其中一個使用 [**：：**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)、 [**：：**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)或 [**：：**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) 新增至寫入器元件的其中一個檔案集合：

-   要求者會使用 [**>ivssbackupcomponents：： AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)來加入新的目標。
-   寫入器會使用 [**IVssCreateWriterMetadata：： AddAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addalternatelocationmapping)新增替代位置對應。
-   現有的檔案會使用 [**>ivsscomponent：： AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime)新增為差異檔案。
-   要求者表示使用替代位置對應來還原使用 [**>ivssbackupcomponents：： AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping)的檔案集。

 

 



