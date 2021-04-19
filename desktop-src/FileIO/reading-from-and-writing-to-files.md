---
description: 應用程式會使用 ReadFile、ReadFileEx、WriteFile 和 WriteFileEx 函式來讀取和寫入檔案。
ms.assetid: 14ecb06c-3f80-47b8-9964-6a2c3b572300
title: 讀取和寫入檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffd0e6518ce2430e18bbb11033023ee6dc274573
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979289"
---
# <a name="reading-from-and-writing-to-files"></a>讀取和寫入檔案

應用程式會使用 [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile)、 [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex)、 [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)和 [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) 函式來讀取和寫入檔案。 這些函式需要開啟檔案的控制碼，才能分別供讀取和寫入。 它們會在檔案指標所指示的位置讀取和寫入指定的位元組數目。 資料的讀取和寫入與指定的完全相同;這些函數不會格式化資料。

當檔案指標到達檔案結尾，而應用程式嘗試從檔案讀取時，不會發生任何錯誤，但不會讀取任何位元組。 因此，讀取零位元組而不發生錯誤，表示應用程式已到達檔案結尾。 寫入零位元組不會執行任何動作。

如需詳細資訊，請參閱下列主題。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                                                           | 描述                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [放置檔案指標](positioning-a-file-pointer.md)<br/>                                                                         | Windows 使用檔案指標來追蹤讀取或寫入的位元組。<br/>                                                       |
| [使用 Scatter-Gather 配置讀取或寫入檔案](reading-from-or-writing-to-files-using-a-scatter-gather-scheme.md)<br/> | 描述在一項作業中用來讀取或寫入非連續資料區塊的散佈集合配置。<br/>                   |
| [將 System-Buffered i/o 資料排清到磁片](flushing-system-buffered-i-o-data-to-disk.md)<br/>                                           | Windows 會將資料儲存在系統維護的資料緩衝區中的檔案讀取和寫入作業，以將磁片效能優化。<br/> |
| [截斷或擴充檔案](truncating-or-extending-files.md)<br/>                                                                   | 應用程式可以藉由呼叫 [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile)來截斷或擴充檔案。<br/>                             |



 

 

 




