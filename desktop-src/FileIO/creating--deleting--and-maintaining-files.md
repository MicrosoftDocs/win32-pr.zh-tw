---
description: 用來建立、刪除和維護檔案的函數。
ms.assetid: b9cf0ddf-efda-4997-bcc3-3056026c1264
title: 建立、刪除和維護檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff20362e2ff5f1d8b01b515c7cbbb9fae250d930b2610c49c5e8aaeeabe7b401
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982118"
---
# <a name="creating-deleting-and-maintaining-files"></a>建立、刪除和維護檔案

下列主題描述如何建立、刪除和維護檔案。

## <a name="in-this-section"></a>本節內容



| 主題                                                                   | 描述                                                                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [命名檔案、路徑和命名空間](naming-a-file.md)<br/>     | 檔案和目錄名稱的規則、慣例和限制，包括命名慣例、簡短檔案名與完整檔案名、完整路徑與相對路徑、最大路徑長度限制、8.3 檔案名和命名空間。<br/>            |
| [建立和開啟檔案](creating-and-opening-files.md)<br/> | 使用 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 函數建立或開啟檔案的考慮。<br/>                                                                                                                                                            |
| [移動和取代檔案](moving-and-replacing-files.md)<br/> | 使用 CopyFileEx、CreateFile、Replacefile 和 MoveFileEx 函數移動和取代檔案的考慮。<br/>                                                                                                                                        |
| [關閉和刪除檔案](closing-and-deleting-files.md)<br/> | 若要有效率地使用作業系統資源，應用程式應該在不再需要使用 [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) 函式時關閉檔案。 如果在應用程式終止時開啟檔案，系統會自動將它關閉。<br/> |
| [磁碟重組檔案](defragmenting-files.md)<br/>               | *磁碟重組* 是指將檔案的部分移到磁片上以重組檔案的程式，也就是在磁片上移動檔案叢集以使其成為連續的進程。<br/>                                                                               |



 

 

