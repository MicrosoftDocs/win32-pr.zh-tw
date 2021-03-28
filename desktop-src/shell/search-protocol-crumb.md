---
description: 連結引數支援完整的 Advanced Query 語法 (AQS) 語句，特別適用于控制搜尋範圍的方法。
title: " (Windows Shell 的連結引數) "
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 8f87a2b7-7f5a-4629-b881-44bf418b2df0
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 7d38fff38c14a6b537bde068b92e19cedf53d5d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973472"
---
# <a name="crumb-argument-the-windows-shell"></a> (Windows Shell 的連結引數) 

`crumb`引數支援 (AQS) 語句的完整先進查詢語法，特別適用于控制搜尋範圍的方法。 除了 AQS 語句之外， `crumb` 引數也可以 `location` 在 windows Vista 上採用特殊參數，以及在 `kind` windows XP 上採用 `store` 參數，如本主題稍後所述。

本主題包含下列幾節：

-   [連結語法](#crumb-syntax)
    -   [一般範例](#general-examples)
-   [使用連結搭配 Vista (位置) ](#using-crumb-with-vista-location)
    -   [Vista 範例](#vista-examples)
    -   [一般資料夾的常數](#constants-for-common-folders)
    -   [引數資訊](#argument-information)

## <a name="crumb-syntax"></a>連結語法

連結語法如下所示：


```
crumb=<column>:<value>[,<label>][,<column>:<value>[,<label>]]& 
```



<column>部分是屬性系統中的任何屬性，而 <value> 部分是該屬性的有效值。 <label>部分是顯示為使用者介面提示之屬性的選擇性別名。

### <a name="general-examples"></a>一般範例


```
crumb=System.Author:paolo&
crumb=store:mapi&
crumb=location:c%3a%5cMyVacationPix,Vacation&
```



## <a name="using-crumb-with-vista-location"></a>使用連結搭配 Vista (位置) 

在連結參數中，Windows Vista 支援完整 AQS 和 `location` 屬性，只有在 Windows vista 上才有提供特殊的執行功能。 您可以在 `location` 單一連結參數中使用 AQS 字串或屬性，但不能同時使用兩者。 如果連結參數包含 AQS，則會忽略該連結參數中的其他專案。

`location`屬性可讓您指定要搜尋的路徑。 如果位置是在索引子的編目範圍之外，Windows Vista 可以略過索引子並直接進行目錄。 因此，這些搜尋可能會比使用索引子的搜尋更慢。

當您指定 `location` 屬性時，支援兩個額外的參數和選擇性參數：



| 參數 | 值                  | 描述                                                                                                                                                                       |
|-----------|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 包含 | 包含、排除        | 指定查詢是否應包含或排除該路徑的專案。 "Include" 是預設值。 Windows Vista 不支援排除專案，不含任何專案。  (請參閱範例)  |
| 遞迴 | 遞迴、非遞迴 | 指定搜尋是否應從位置中定義的值開始遞迴所有子資料夾：<value>. 「遞迴」是預設值。                             |



 

若要使用 **search：** protocol 設定搜尋範圍，您有不同的選項，視範圍的目標而定。

本機電腦上的資料夾：

-   使用 AQS (連結 = folder： <URL 編碼路徑>) 
-   使用位置引數 (連結 = location： <URL 編碼路徑>) 

遠端電腦/網路上的資料夾：

-   使用位置引數 (連結 = location： <URL 編碼路徑>) 

透過已知通用命名慣例存取的資料夾 (UNC) 通訊協定處理常式：

-   使用 AQS (連結 = store： <UNC protocol handler name>) 
-   使用位置引數 (連結 = location： <URL 編碼路徑>) 

### <a name="vista-examples"></a>Vista 範例


```
search:query=vacation&crumb=location:shell%3aPersonal,include,recursive&
    
search:crumb=location:c%3a%5cPictures&crumb=location:c%3a%5cPictures%5cDuplicates,,exclude& 
    
search:crumb=location:c%3a%5cDocuments&crumb=kind:pics&
```



第一個範例會從位置開始搜尋「休假」 `shell://Personal` ， (使用者的 **我的檔** 資料夾) 的特殊快捷方式，包括該資料夾和所有子資料夾。 請參閱下表。

第二個範例會在 C： pictures 內執行搜尋 \\ ，但無法在 c： \\ pictures \\ 重複。

第三個範例會在 C：檔內執行搜尋 \\ ，限制為 `kind` 屬性設定為 [圖片] 的檔案。

### <a name="constants-for-common-folders"></a>一般資料夾的常數

Windows Vista 可讓您使用 CSIDL 值，以提供獨特的系統獨立方式來識別應用程式經常使用的特殊資料夾，但在任何指定的系統上可能不會有相同的名稱或位置。 例如，系統資料夾在一個系統上可能是 "C： \\ Windows"，另一個則為 "c： \\ Winnt"。

使用下列語法來使用這些位置：


```
crumb=location:shell%3a<LocationName>&
```



下表列出 CSIDL 值。 如需詳細資訊，請參閱 [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) 。



| Name                        | 搜尋字串                   | Description                                                                                                                                                                            |
|-----------------------------|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 系統管理工具        | 系統管理% 20TOOLS          | 檔案系統目錄，作為系統管理工具的儲存機制。                                                                                                            |
| APPDATA                     | APPDATA                         | 檔案系統目錄，做為應用程式特定資料的通用存放庫。 典型的路徑是 C： \\ 檔和設定使用者 \\ 名稱的 \\ 應用程式資料。                      |
| CACHE                       | CACHE                           | 檔案系統目錄，做為暫時性網際網路檔案的通用存放庫。 典型的路徑是 C： \\ 檔和設定使用者 \\ 名稱的 \\ 臨時網際網路檔案。               |
| CD 燒錄                  | CD% 20BURNING                    | 資料夾，其中包含要燒錄到 CD 的資料。                                                                                                                                             |
| 一般系統管理工具 | 常見的% 20ADMINISTRATIVE% 20TOOLS | 適用于所有使用者的系統管理工具。                                                                                                                                                    |
| 一般 APPDATA              | 常見的% 20APPDATA                | 所有使用者的應用程式資料。 典型的路徑是 C： [ \\ 檔] 和 [設定 \\ 所有使用者的 \\ 應用程式資料]。                                                                             |
| 一般桌面              | 一般桌面                  | 適用于所有使用者的 Microsoft Windows 桌面資料。 虛擬資料夾，也就是命名空間的根目錄。                                                                                        |
| 一般檔            | 常見的% 20DOCUMENTS              | 適用于所有使用者的檔。 一般路徑為 C： [ \\ 檔] 和 [設定 \\ 所有使用者 \\ 我的檔。                                                                                        |
| 一般程式             | 常見的% 20PROGRAMS               | 所有使用者通用的程式群組。 典型的路徑是 C： [ \\ 檔] 和 [設定 \\ 所有使用者] \\ 開始功能表 \\ 程式。                                                                     |
| 一般開始功能表           | 常見的% 20START% 20MENU           | [開始] 功能表所有使用者通用的專案。 典型的路徑是 C： [ \\ 檔和設定 \\ 所有使用者 \\ 開始] 功能表。                                                                             |
| 一般啟動              | 常見的% 20STARTUP                | 所有使用者通用的啟始方案群組。                                                                                                                                             |
| 一般範本            | 常見的% 20TEMPLATES              | 所有使用者通用的檔範本。                                                                                                                                                |
| COMMONMUSIC                 | 我的% 20MUSIC                      | 所有使用者通用的 [我的音樂] 資料夾範本。                                                                                                                                         |
| COMMONPICTURES              | 我的% 20PICTURES                   | [我的圖片] 資料夾範本通用於所有使用者。                                                                                                                                      |
| COMMONVIDEO                 | 我的% 20VIDEO                      | 所有使用者通用的我的影片資料夾範本。                                                                                                                                         |
| CONNECTIONSFOLDER           | CONNECTIONSFOLDER               | 包含連接資料的資料夾。                                                                                                                                                     |
| 控制台資料夾        | CONTROLPANELFOLDER              | 包含主控台應用程式圖示的虛擬資料夾。                                                                                                                    |
| 餅乾                     | 餅乾                         | 作為網際網路 cookie 一般儲存機制的檔案系統目錄。 典型的路徑是 C： \\ Documents 和 Settings \\ username \\ cookie。                                        |
| DESKTOP                     | DESKTOP                         | Microsoft Windows Desktop。 虛擬資料夾，也就是命名空間的根目錄。                                                                                                           |
| 我的最愛                   | 我的最愛                       | 檔案系統目錄，做為使用者的我的最愛專案的通用存放庫。 典型的路徑是 C： Documents 和 Settings username 的 [我的最愛 \\ \\ \\ ]。                             |
| 字體                       | 字體                           | 包含已安裝字型的虛擬資料夾。 典型的路徑是 C： \\ WINDOWS 字型 \\ 。                                                                                                       |
| 歷程記錄                     | 歷程記錄                         | 檔案系統目錄，做為網際網路歷程記錄專案的通用存放庫。                                                                                                   |
| INTERNETFOLDER              | INTERNETFOLDER                  | 包含網際網路資料的資料夾。                                                                                                                                                    |
| 本機 APPDATA               | 本機% 20APPDATA                 | 作為本機 (非漫遊) 應用程式之資料存放庫的檔案系統目錄。 典型的路徑是 C： [ \\ 檔] 和 [設定使用者名稱] \\ \\ 本機設定 \\ 應用程式資料。 |
| LOCALIZEDRESOURCEDIR        | LOCALIZEDRESOURCEDIR            | 當地語系化的資原始目錄。                                                                                                                                                          |
| MYCOMPUTERFOLDER            | MYCOMPUTERFOLDER                | 我的電腦： 虛擬資料夾，其中包含本機電腦上的所有內容：儲存裝置、印表機及主控台。 此資料夾也可能包含對應的網路磁碟機機。             |
| 我的音樂                    | 我的% 20MUSIC                      | [我的音樂] 資料夾。 典型的路徑是 C： [ \\ 檔] 和 [設定 \\ 使用者名稱] \\ 我的檔我的 \\ 音樂。                                                                                       |
| 我的圖片                 | 我的% 20PICTURES                   | [我的圖片] 資料夾。 一般路徑為 C： [ \\ 檔] 和 [設定 \\ 使用者名稱]， \\ 我的檔 \\ 我的圖片。                                                                                 |
| 我的影片                    | 我的% 20VIDEO                      | [我的影片] 資料夾。 典型的路徑是 C： \\ Documents 和 Settings \\ username \\ 我的檔 \\ 我的影片。                                                                                       |
| NETHOOD                     | NETHOOD                         | 代表網路命名空間階層根目錄的虛擬資料夾。                                                                                                               |
| 網路位置資料夾       | NETWORKDPLACESFOLDER            | 檔系統資料夾，其中包含 [我的網路] 中可能存在的連結化物件的虛擬資料夾。 它與代表網路命名空間根目錄的 NETHOOD 不同。   |
| OEM 連結                   | OEM% 20LINKS                     | 包含 OEM 網站連結的資料夾。                                                                                                                                                  |
| 個人                    | 個人                        | 檔案系統目錄，做為使用者檔的通用存放庫。 典型的路徑是 C： [ \\ 檔] 和 [設定使用者名稱] \\ \\ 我的檔。                                 |
| 印表機資料夾             | 印表機資料夾                 | 包含已安裝印表機的虛擬資料夾。                                                                                                                                          |
| PRINTHOOD                   | PRINTHOOD                       | 檔案系統目錄，包含印表機虛擬資料夾中可能存在的連結化物件。 典型的路徑是 C： \\ Documents 和 Settings \\ username \\ PrintHood。                 |
| 計劃                    | 計劃                        | 檔案系統目錄，其中包含使用者的程式群組 (也是) 的檔案系統目錄。 典型的路徑是 C： [檔] 和 [設定] 使用者 \\ 名稱 [開始] \\ \\ 功能表 \\ 程式。  |
| 設定檔                     | 設定檔                         | 使用者的設定檔資料夾。                                                                                                                                                                 |
| PROGRAM FILES               | 程式% 20FILES                 | Program Files 資料夾。 典型的路徑是 C： \\ Program Files。                                                                                                                             |
| 一般程式檔        | PROGRAMFILESCOMMON              | 所有使用者通用的 Program Files 資料夾。                                                                                                                                              |
| COMMON x86 程式檔    | PROGRAMFILESCOMMONX86           | X86 電腦上所有使用者通用的 Program Files 資料夾。                                                                                                                              |
| 程式 FILESx86            | PROGRAMFILESx86                 | X86 電腦上的 Program Files 資料夾。                                                                                                                                                  |
| 最近                      | 最近                          | 包含使用者最近使用之檔的檔案系統目錄。 一般路徑為 C： [ \\ 檔] 和 [設定使用者 \\ 名稱 \\ 最新]。                                           |
| 回收站資料夾          | RECYCLEBINFOLDER                | 虛擬資料夾，其中包含使用者資源回收筒中的物件。                                                                                                                       |
| RESOURCEDIR                 | RESOURCEDIR                     | 資原始目錄。                                                                                                                                                                |
| SENDTO                      | SENDTO                          | 包含 [傳送至] 功能表項目的檔案系統目錄。 典型的路徑是 C： \\ Documents 和 Settings 使用者 \\ 名稱 \\ SendTo。                                                                |
| 開始功能表                  | 開始% 20MENU                    | 包含 [開始] 功能表專案的檔案系統目錄。 典型的路徑是 C： [檔] 和 [設定使用者名稱] 的 [ \\ \\ 開始] \\ 功能表。                                                                 |
| 啟動                     | 啟動                         | 對應至使用者之啟動程式群組的檔案系統目錄。                                                                                                            |
| SYSTEMx86                   | SYSTEMx86                       | X86 電腦上的系統資料夾。                                                                                                                                                         |
| 範本                   | 範本                       | 檔案系統目錄，做為檔範本的通用存放庫。                                                                                                       |
| 系統                      | 系統                          | 系統資料夾。 典型的路徑是 C： \\ Windows \\ 系統。                                                                                                                                  |
| WINDOWS                     | WINDOWS                         | Windows 目錄或 SYSROOT。                                                                                                                                                          |



 

### <a name="argument-information"></a>引數資訊



|                          |                                         |
|--------------------------|-----------------------------------------|
| 最低作業系統 | Windows Vista 包含 Service Pack 1 (SP1) |



 

 

 



