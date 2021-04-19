---
description: 檔案管理的相關資訊。
ms.assetid: cf4e69b9-86dd-43a4-9011-6209fc65f550
title: 關於檔案管理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fe8e5f53a0021d4a6fba90a31698d05971e7bea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106967141"
---
# <a name="about-file-management"></a>關於檔案管理

下列主題包含有關檔案管理的詳細資訊。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                 | 描述                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [檔案系統功能比較](filesystem-functionality-comparison.md)<br/>            | 列出四個主要 Windows 檔案系統、NTFS、exFAT、UDF 和 FAT32 之功能和功能支援比較的表格。<br/>                                                                           |
| [檔案和叢集](files-and-clusters.md)<br/>                                               | 檔案 *是檔* 系統中，使用者可以存取和管理的資料單位。<br/>                                                                                                                              |
| [建立、刪除和維護檔案](creating--deleting--and-maintaining-files.md)<br/> | 用來建立、刪除和維護檔案的函數。<br/>                                                                                                                                                       |
| [取得和設定檔案資訊](obtaining-and-setting-file-information.md)<br/>       | 用來取得和設定檔案資訊的函式。<br/>                                                                                                                                                             |
| [讀取和寫入檔案](reading-from-and-writing-to-files.md)<br/>                 | 應用程式會使用 [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile)、 [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex)、 [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)和 [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) 函式來讀取和寫入檔案。<br/> |
| [檔案和目錄連結](file-and-directory-linking.md)<br/>                               | NTFS 檔案系統支援兩種類型的連結：永久 [連結和](hard-links-and-junctions.md)連接。<br/>                                                                                     |
| [封鎖複製](block-cloning.md)<br/>                                                         | *區塊複製* 作業會指示檔案系統代表應用程式複製某範圍的檔案位元組。<br/>                                                                                                |
| [檔案壓縮和解壓縮](file-compression-and-decompression.md)<br/>               | NTFS 檔案系統使用 Lempel-Ziv 壓縮，也就是不失真的壓縮演算法。<br/>                                                                                                                  |
| [檔案加密](file-encryption.md)<br/>                                                     | 加密檔案系統 (EFS) 使用公開金鑰系統，在 NTFS 檔案系統磁片區上提供個別檔案的密碼編譯保護。<br/>                                                               |
| [檔案安全性與存取權限](file-security-and-access-rights.md)<br/>                     | 由於檔案是 [安全的物件](/windows/desktop/SecAuthZ/securable-objects)，因此對它們的存取會受到控制 Windows 中所有其他安全物件存取權的存取控制模型所管制。<br/>                     |
| [輸入和輸出 (i/o) ](input-and-output--i-o-.md)<br/>                                       | Windows 提供在本機和遠端電腦上的存放裝置元件上執行輸入和輸出 (i/o) 作業的能力。<br/>                                                                        |
| [疏鬆檔案](sparse-files.md)<br/>                                                           | 檔案壓縮大部分的檔案，可有效率地使用磁碟空間。<br/>                                                                                                                        |
| [符號連結](symbolic-links.md)<br/>                                                       | 符號連結是指向另一個檔案系統物件的檔案系統物件。 所指向的物件稱為「目標」。<br/>                                                                          |



 

 

