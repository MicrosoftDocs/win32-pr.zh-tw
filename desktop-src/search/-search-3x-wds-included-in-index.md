---
description: 本主題說明 Windows Search 索引的專案。
ms.assetid: vs|search|~\search\wds3x\overviews\misc_items_in_index.htm
title: 索引中包含的內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5560a14e3537c8e3ac8c7544aa7ffc9a0bc1bc64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966687"
---
# <a name="what-is-included-in-the-index"></a>索引中包含的內容

本主題說明 Windows Search 索引的專案。

本主題的組織方式如下：

-   [依預設編制索引](#indexed-by-default)
-   [支援的檔案格式](#file-formats-supported)
-   [檔案排除](#file-exclusions)
-   [資料夾排除專案](#folder-exclusions)
-   [磁片磁碟機排除](#drive-exclusions)
-   [相關主題](#related-topics)

 

## <a name="indexed-by-default"></a>依預設編制索引

通訊協定處理常式和篩選器會包含在 Windows Search 中，以針對下列種類的內容編制索引：

-   在 Windows Vista 和更新版本中，會在郵件應用程式執行時編制使用者的 Microsoft Outlook 和 Microsoft Outlook Express mail 專案的索引。
-    (CSC) 的用戶端快取中的離線檔案，會在本機 Windows Search 編制索引。
-   Windows Search 支援收集 NTFS 和 FAT32 磁片區上的檔案開始位址。 NTFS 支援以通知為基礎的索引，而 FAT32 可在啟動時支援累加式編目，然後回應通知。
-   Windows Vista 和更新版本會繼續公開每個資料夾/每個檔案的屬性，以啟用編制索引：在 [**屬性**] 對話方塊中，[**用於快速搜尋，讓索引服務可為此資料夾編制索引**] 選項。 設定 FANCI 位旗標可確保來自通訊協定的基本屬性（例如 URL、檔案名和大小）已編制索引，但不會執行篩選處理常式或屬性處理常式。
-   文字內容已編制索引，但不是標點符號。

## <a name="file-formats-supported"></a>支援的檔案格式

Windows Search 有通訊協定處理常式、屬性處理常式和篩選處理常式，可自動編制下列格式的索引：

-   媒體檔案：所有媒體檔案類型
-   **HTML** (nlhtml.dll) ： .ascx、.asp、.aspx、.css、（.）、.htm、.html、htt、. htw、htx、.odc、.stm
-   **MIME HTML** (mimefilt.dll) ： .mht、mhtml
-   **Office** (offfilt.dll) ： .doc、.dot、.pot、.pps、.ppt、xlb、. xlc、.xls、.xlt
-   **Text** (query.dll) ： .asm、。 asx、.bat、.c、.cmd、.cpp、. cxx、.def、. scripting.dic、.h、. .hpp、hxx、.idl、idq、.inf、.ini、. inx、.js、.log、......... x.. url、.vbs、. wtx
-   **Xml** (xmlfilt.dll) ： .xml、.xsl
-   **OneNote**：. one
-   **Tablet 日記本** (jntfiltr.dll) ：. .jnt

針對結構化儲存體以外的所有檔案，會編制屬性的索引。 在 Windows Vista 和更新版本中，會編制許多媒體檔案屬性的索引;但是，如果檔案受到數位版權管理 (DRM) 的保護，則不會建立內容的索引。

> [!Note]  
> HTML 篩選不會為 HTML 批註編制索引。

 

## <a name="file-exclusions"></a>檔案排除

當檔案類型沒有相關聯的篩選，或檔案沒有副檔名時，就會為該類型的檔案建立系統屬性的索引，但不會為檔案內容編制索引。

此外，Windows Search 不會為資訊版權管理 (IRM) 或數位版權管理 (DRM) 下的檔案內容編制索引。

在 Windows Vista (只) ，預設會將下列檔案從索引中排除：

-   標記為隱藏或系統的檔案。
-   具有下列副檔名的檔案：

    386、. ap、。AudioCD、bin、. bk1、. bk2、.bkf、.bsc、btr、.chk、ci、crwl、dbg、. dct、。DeskLink、dir、dl \_ 、.dll、. winspool.drv、dvd-rom、.evt、ex \_ 、.exe、exp、. eyb、fnd、. fnt、。Folder、. fon、. ghi、. gthr、hqx、icm、.idb、idx、. .ilk、imc、in \_ 、.ini、.manifest、jbf、. latex、.lib、local、m14、mac、.manifest、. map、。MAPIMail、.mmf、movie、mv、. mydocs、.ncb、.obj、oc \_ 、.ocx、.pch、.pdb、pf。 pma、. pmc、. >procmontrace.pml、pmr、.res、. rmp、.res、.rsp、.sbr、sc2、. \_ \_ sy、sys、.tlb、sym、>flightrecordercurrent.trc、simsun18030.ttc、ttf、vbx、. 集會、. wlt、. xix、. z96、.、.、.、。ZFSendToTarget.

## <a name="folder-exclusions"></a>資料夾排除專案

> [!TIP]
> 資料夾名稱不區分大小寫。

 

預設會將下列資料夾從索引中排除：



| 資料夾排除模式                                                              | 在 Windows 7 中的效果 | Windows Vista 中的效果 | Description                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------|---------------------|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *% 系統%* \\ProgramData \\ Microsoft \\ 搜尋 \\ 資料\\                                    | **已排除**        | 沒有影響               | 系統磁片磁碟機上的索引子資料。                                                                                                                                                                                          |
| *% 系統%* \\使用者使用者 \\ *名稱* \\ AppData\\                                              | **已排除**        | 沒有影響               | 使用者的應用程式資料 (包括系統磁片磁碟機上) 的暫存資料。<br/> 針對登入系統的每個使用者，會加入特定的排除模式，以排除其在索引中的應用程式資料。<br/> |
| *% 系統%* \\\\ \* \\ AppData \\ 本機 \\ Microsoft \\ Windows \\ 暫時性網際網路檔案的使用者\\ | **已排除**        | 沒有影響               | Windows 在系統磁片磁碟機上 Internet Explorer 暫時性網際網路檔案的預設位置。<br/> 如果 Internet Explorer 暫時性的網際網路檔案的位置已變更，則可能會將這些檔案編制索引。<br/>    |
| *% 系統%* \\Windows \\ CSC\\                                                            | **已排除**        | 沒有影響               | 如果開啟 Windows 系統目錄的索引，系統磁片磁碟機上 (的 CSC 資料夾) 仍會排除在編制索引之外。                                                                                           |
| *% 系統%* \\Windows \\ \* \\ Temp\\                                                       | **已排除**        | 沒有影響               | 系統磁片磁碟機上的 Windows 暫存資料。                                                                                                                                                                                     |
| *% 系統%* \\窗戶。\*\\                                                              | **已排除**        | 沒有影響               | 系統磁片磁碟機上的舊 Windows 安裝。                                                                                                                                                                             |
| *% 系統%* \\ProgramData\\                                                             | **已排除**        | **已排除**            | 請注意，共用的 [開始] 功能表子資料夾已編制索引。                                                                                                                                                                     |
| *% 系統%* \\使用者 \\ \* \\ AppData\\                                                      | **已排除**        | **已排除**            | 使用者的應用程式資料 (包含) 的暫存資料。                                                                                                                                                                              |
| *% 系統%* \\\\ \* \\ AppData \\ 本機 \\ Temp 的使用者\\                                         | **已排除**        | **已排除**            | 使用者的暫存資料。 如果使用者應用程式資料的索引已開啟，預設仍會將使用者暫存資料排除在編制索引之外。                                                                                           |
| *% 系統%* \\窗戶\\                                                                 | **已排除**        | **已排除**            | 系統磁片磁碟機上的作業系統檔案。                                                                                                                                                                                |
| *% 系統%* \\$Recycle Bin\\                                                            | **已排除**        | **已排除**            | 檔案在資源回收筒中的位置。                                                                                                                                                                                      |
| *% 系統%* \\建立\\                                                                   | 沒有影響           | **已排除**            | 在系統磁片磁碟機上。                                                                                                                                                                                                       |
| *% 系統%* \\已安裝的儲存機制\\                                                    | 沒有影響           | **已排除**            | 在系統磁片磁碟機上。                                                                                                                                                                                                       |
| *% 系統%* \\Program Files\\                                                           | 沒有影響           | **已排除**            | 在系統磁片磁碟機上。                                                                                                                                                                                                       |
| *% 系統%* \\Program Files (x86) \\                                                     | 沒有影響           | **已排除**            | 在系統磁片磁碟機上。                                                                                                                                                                                                       |
| \*\\臨時\\\*                                                                          | 沒有影響           | **已排除**            | Windows 暫存資料和其他名稱為 "temp" 的資料夾。                                                                                                                                                                  |
| *% 系統%* \\使用者 \\ 預設\\                                                          | 沒有影響           | **已排除**            | 預設使用者設定檔資料在系統磁片磁碟機上的位置。                                                                                                                                                             |
| \*\\窗戶。\*\\                                                                      | 沒有影響           | **已排除**            | 舊的 Windows 安裝和其他名稱開頭為 "Windows" 的資料夾。                                                                                                                                         |



 

## <a name="drive-exclusions"></a>磁片磁碟機排除

在 Windows 7 和 Windows Vista 上，預設不會編制卸載式磁片磁碟機的索引。

> [!Note]  
> 如果卸載式磁片磁碟機將本身報告為固定磁片磁碟機，您可以將它們新增至索引，即使它們實際上是卸載式也一樣。 資訊會保留在索引中，而 Windows Search 會在卸載式磁片重新插入時，進行增量編目以協調索引結果。 由於 USB 快閃磁片磁碟機本身是卸載式的，因此無法進行索引。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Search 中的編制索引、查詢和通知](-search-3x-wds-included-in-index.md)
</dt> <dt>

[Windows Search 中的編制索引進程](-search-indexing-process-overview.md)
</dt> <dt>

[在 Windows Search 中查詢進程](querying-process--windows-search-.md)
</dt> <dt>

[Windows Search 中的通知處理](-search-3x-wds-support.md)
</dt> <dt>

[URL 格式設定需求](url-formatting-requirements.md)
</dt> </dl>

 

 




