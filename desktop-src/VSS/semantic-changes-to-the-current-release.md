---
description: 使用 IVssCreateWriterMetadata：： AddFilesToFileGroup、IVssCreateWriterMetadata：： AddDatabaseFiles 或 IVssCreateWriterMetadata：： AddDatabaseLogFiles 時) ，路徑、檔案規格和遞迴旗標 (wszPath、wszFileSpec 和 bRecursive 的組合，必須符合其中一個使用：：、：：或：：新增至寫入器元件的其中一個檔案集合：
ms.assetid: debf181a-1579-46f2-86ef-a1d2a850e99e
title: Windows Server 2003 的語義變更
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8319259dc27c981822bb242d20243264ca9025d959693aafcb3836976fd7754d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866258"
---
# <a name="semantic-changes-to-windows-server-2003"></a>Windows Server 2003 的語義變更

使用 IVssCreateWriterMetadata：： AddFilesToFileGroup、IVssCreateWriterMetadata：： AddDatabaseFiles 或 IVssCreateWriterMetadata：： AddDatabaseLogFiles 時) ，路徑、檔案規格和遞迴旗標 (*wszPath*、 *wszFileSpec* 和 *bRecursive* 的組合，必須符合其中一個使用 [**：：**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)、 [**：：**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)或 [**：：**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) 新增至寫入器元件的其中一個檔案集合：

-   要求者會使用 [**>ivssbackupcomponents：： AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)來加入新的目標。
-   寫入器會使用 [**IVssCreateWriterMetadata：： AddAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addalternatelocationmapping)新增替代位置對應。
-   現有的檔案會使用 [**>ivsscomponent：： AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime)新增為差異檔案。
-   要求者表示使用替代位置對應來還原使用 [**>ivssbackupcomponents：： AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping)的檔案集。

 

 



