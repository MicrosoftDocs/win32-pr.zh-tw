---
description: 在 NTFS 檔案系統中，資料流程包含寫入檔案的資料，並提供比屬性和屬性更多的檔案相關資訊。
ms.assetid: 41dda6f1-a6d1-4e76-94f3-a72f9e491bee
title: '檔案串流 (本機檔案系統) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a934a51225a886e3d5a7de4d9e1e91900fab460
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692259"
---
# <a name="file-streams-local-file-systems"></a>檔案串流 (本機檔案系統) 

資料流程是一連串的位元組。 在 NTFS 檔案系統中，資料流程包含寫入檔案的資料，並提供比屬性和屬性更多的檔案相關資訊。 例如，您可以建立包含搜尋關鍵字的資料流程，或是建立檔案之使用者帳戶的身分識別。

與檔案相關聯的每個資料流程都有自己的配置大小、實際大小和有效的資料長度：

-   配置大小是為數據流保留的磁碟空間量。
-   實際大小是呼叫者正在使用的位元組數目。
-   有效的資料長度 (VDL) 是從資料流程的配置大小初始化的位元組數目。

每個串流也會針對壓縮、加密和疏鬆度維護其本身的狀態。 如果任何資料流程曾經是稀疏的，則會在從 [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea)、 [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa)和 [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)函式傳回的 [**WIN32 \_ 尋找 \_ 資料**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa)結構的 **dwFileAttributes** 成員中設定檔案的 **檔 \_ 屬性 \_ 稀疏 \_ 檔** 屬性。 如果未指定任何資料流程， [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa)、 [**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa)、 [**GetFileAttributesTransacted**](/windows/desktop/api/WinBase/nf-winbase-getfileattributestransacteda)、 [**GetFileInformationByHandle**](/windows/desktop/api/FileAPI/nf-fileapi-getfileinformationbyhandle)和 [**GetFileInformationByHandleEx**](/windows/desktop/api/WinBase/nf-winbase-getfileinformationbyhandleex)會傳回預設資料流程的稀疏狀態。

沒有與資料流程相關聯的檔案時間。 當檔案中的任何資料流程更新時，檔案的檔案時間就會更新。

每個資料流程會維護隨機鎖定。 每個串流也會維護共用模式。 當對檔案要求刪除存取時，作業系統會檢查檔案中所有開啟的資料流程是否有刪除存取權。 如果另一個進程已在沒有檔案 **\_ 共用 \_ 刪除** 許可權的情況下開啟資料流程，您就無法開啟檔案以供刪除存取。

如果要複製的檔案具有資料流程，而使用網路重新導向程式，則只有在用戶端同時具有 [讀取] 許可權和 [讀取屬性] 許可權時，才能複製該檔案。

## <a name="naming-conventions-for-streams"></a>資料流程的命名慣例

從 Windows shell 命令列指定時，資料流程的完整名稱為 "*filename*：*stream name*：*stream type*"，如下列範例所示： "myfile.txt .dat： stream1： $DATA"。

針對檔案名合法的任何字元也都是資料流程名稱的合法字元，包括空格。 如需詳細資訊，請參閱 [命名](naming-a-file.md)檔案。 資料流程類型 (也稱為屬性類型代碼) 是 NTFS 檔案系統的內部。 因此，使用者無法建立新的資料流程類型，但可以開啟現有的 NTFS 檔案系統類型。 資料流程類型規範值一律以貨幣符號 ($) 符號開頭。 請參閱下面的資料流程類型清單。

預設的資料流程預設為未命名。 若要完整指定預設資料流程，請使用 "*filename*：： $DATA"，其中 $DATA 是資料流程類型。 這相當於「*filename*」。 您可以使用檔案 [命名慣例](naming-a-file.md)，在檔案中建立命名的資料流程。 請注意，"$DATA" 是合法的資料流程名稱。 例如，名為 "*sample*" 的檔案上名為 "$DATA" 的資料流程完整名稱會是 "*sample*： $DATA： $DATA"。 如果您在相同的檔案中建立名為 "bar" 的資料流程，其完整名稱將會是 "*sample*： bar： $DATA"。

當您建立和使用具有單一字元名稱的檔案時，請在檔案名前面加上句號，再加上反斜線 (。 \) 或使用完整路徑名稱。 這樣做的原因是 Windows 會將一個字元的檔案名視為磁碟機號。 使用相對路徑指定磁碟機號時，冒號會分隔磁碟機號與路徑。 如果有一個字元名稱是磁碟機號或檔案名時，Windows 會假設它是一個磁碟機號，如果冒號後面的字串是有效的路徑，即使磁碟機號無效也是一樣。

## <a name="stream-types"></a>資料流程類型

以下是 NTFS 串流類型的清單，也稱為屬性類型代碼。 部分資料流程類型是 NTFS 內部的，且其格式未記載。



| 資料流程類型                | Description                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ：： $ATTRIBUTE \_ 清單         | 包含組成檔案的所有屬性清單，並識別每個屬性所在的位置。                                                                                                                                                                                                                                                                                                                                          |
| ：： $BITMAP                  | 索引用來管理目錄之 b 型樹狀目錄可用空間的點陣圖。 B 型樹狀目錄是以 4 KB 區塊來管理 (無論叢集大小為何) ，這是用來管理這些區塊的配置。 此資料流程類型存在於每個目錄中。                                                                                                                                                                                           |
| ：： $DATA                    | 資料流程。 預設資料流程沒有名稱。 您可以使用 [**FindFirstStreamW**](/windows/desktop/api/fileapi/nf-fileapi-findfirststreamw) 和 [**FindNextStreamW**](/windows/desktop/api/fileapi/nf-fileapi-findnextstreamw) 函數來列舉資料流程。                                                                                                                                                                                                                                                |
| ：： $EA                      | 包含擴充的屬性資料。|
| ：： $EA \_ 資訊         | 包含擴充屬性的支援資訊。                                                                                                                                                                                                                                                                                                                                                                                      |
| ：： $FILE \_ 名稱              | 檔案名（以 Unicode 字元為單位）。 這包括檔案的簡短名稱，以及任何的永久連結。                                                                                                                                                                                                                                                                                                                                 |
| ：： $INDEX \_ 配置       | 目錄的資料流程類型。 用來執行大型目錄的檔案名配置。 此資料流程代表目錄本身，並包含目錄的所有資料。 此類型的資料流程變更會記錄到 NTFS 變更日誌中。 $INDEX 配置資料流程類型的預設資料流程名稱 \_ 是 $I 30，因此 "*DirName*"、"*DirName*：： $INDEX \_ 配置" 和 "*DirName*： $I 30： $INDEX \_ 配置" 都是相等的。 |
| ：： $INDEX \_ 根             | 此資料流程代表索引 b 型樹狀結構的根。 此資料流程類型存在於每個目錄中。                                                                                                                                                                                                                                                                                                                                           |
| ：： $LOGGED \_ 公用程式 \_ 資料流程 | 類似于：： $DATA 但作業會記錄到 NTFS 變更日誌中。 由 EFS 和 [交易式 NTFS (TxF) ](transactional-ntfs-portal.md)使用。 適用于 EFS 的 "：*StreamName*： $*StreamType*" 組是 "： $EFS： $LOGGED \_ 公用程式 \_ 串流」，而 TxF 的"： $TXF \_ DATA： $LOGGED \_ utility \_ stream "。                                                                                                                                                    |
| ：： $OBJECT \_ 識別碼              | 16位元組的識別碼，用來識別連結追蹤服務的檔案。                                                                                                                                                                                                                                                                                                                                                                           |
| ：： $REPARSE \_ 點          | 重新 [分析點](reparse-points.md) 資料。|



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用資料流程](using-streams.md)
</dt> </dl>

 

 



