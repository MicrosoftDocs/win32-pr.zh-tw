---
description: 用來取得和設定檔案資訊的函式。
ms.assetid: 3b5fb709-c699-4651-8072-97210c8cf763
title: 取得和設定檔案資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c6eb6abf2554e1945e0782c667245ea0eaa99be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852796"
---
# <a name="obtaining-and-setting-file-information"></a>取得和設定檔案資訊

下列主題描述如何取得和設定檔案資訊。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                             | 描述                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [正在取出檔案類型資訊](retrieving-file-type-information.md)<br/>                               | [**GetFileType**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletype)函式會抓取檔案的類型：磁片、字元 (例如主控台) 、管道或不明。<br/>                                                                                                                                               |
| [判斷檔案的大小](determining-the-size-of-a-file.md)<br/>                                   | [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize)函式會捕獲檔案的大小。<br/>                                                                                                                                                                                                      |
| [搜尋一個或多個檔案](searching-for-one-or-more-files.md)<br/>                                 | 應用程式可以使用 [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea)、 [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa)、 [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)和 [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) 函數，在目前的目錄中搜尋符合指定模式的所有檔案名。<br/> |
| [設定和取得檔案的時間戳記](setting-and-getting-the-timestamp-of-a-file.md)<br/>         | 應用程式可以使用 [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) 和 [**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime) 函式來取得和設定檔案的建立日期和時間、上次修改時間或上次存取的時間。<br/>                                                                         |
| [判斷目前的字元集字碼頁](determining-the-current-character-set-code-page.md)<br/> | [**AreFileApisANSI**](/windows/desktop/api/fileapi/nf-fileapi-arefileapisansi)函式會判斷檔案 i/o 函數是否使用 ANSI 或 OEM 字元集字碼頁。<br/>                                                                                                                               |



 

 

