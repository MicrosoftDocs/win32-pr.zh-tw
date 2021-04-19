---
description: 下列安裝程式 API 函式會搭配 INF 檔案使用。
ms.assetid: fb4263fc-5f59-460a-a7d9-93f10729c02a
title: INF 檔案設定函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24944f19938217d40ff4a7eaebbfb638c26e4afb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984622"
---
# <a name="inf-file-setup-functions"></a>INF 檔案設定函數

下列安裝程式 API 函式會搭配 INF 檔案使用。



| 函式                                                                         | 描述                                                                                                                                                                                            |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetupCloseInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile)                                   | 釋出資源並關閉 INF 控制碼。                                                                                                                                                             |
| [**SetupDecompressOrCopyFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupdecompressorcopyfilea)                   | 複製檔案，並視需要將它解壓縮。                                                                                                                                                      |
| [**SetupFindFirstLine**](/windows/desktop/api/Setupapi/nf-setupapi-setupfindfirstlinea)                                 | 尋找 INF 檔案區段中的第一行，如果指定了金鑰，就會找到符合該金鑰的第一行。 它會更新 [**INFCONTEXT**](/windows/desktop/api/Setupapi/ns-setupapi-infcontext)結構的 **行** 成員。 |
| [**SetupFindNextLine**](/windows/desktop/api/Setupapi/nf-setupapi-setupfindnextline)                                   | 傳回區段中相對於指定 [**INFCONTEXT**](/windows/desktop/api/Setupapi/ns-setupapi-infcontext)結構的 **行** 成員的下一行。                                                                    |
| [**SetupFindNextMatchLine**](/windows/desktop/api/Setupapi/nf-setupapi-setupfindnextmatchlinea)                         | 傳回區段中相對於符合指定索引鍵之指定 [**INFCONTEXT**](/windows/desktop/api/Setupapi/ns-setupapi-infcontext)的 **行** 成員的下一行。                                                 |
| [**SetupGetBinaryField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetbinaryfield)                               | 從其欄位為二進位格式的行中取出資料。                                                                                                                                          |
| [**SetupGetFieldCount**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetfieldcount)                                 | 傳回線條中的欄位數目。                                                                                                                                                                |
| [**SetupGetFileCompressionInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetfilecompressioninfoa)               | 從 INF 檔案抓取檔案壓縮資訊。                                                                                                                                               |
| [**SetupGetInfFileList**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinffilelista)                               | 取得指定目錄中的 INF 檔案類型清單。                                                                                                                                        |
| [**SetupGetInfInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinfinformationa)                         | 傳回 [**INFCONTEXT**](/windows/desktop/api/Setupapi/ns-setupapi-infcontext)或檔案名) 的 **行** 成員 (之 INF 檔案的相關資訊。                                                                                     |
| [**SetupGetIntField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetintfield)                                     | 傳回 INF 檔案中某一行的指定整數位段。                                                                                                                                          |
| [**SetupGetLineByIndex**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinebyindexa)                               | 針對指定之區段中指定索引處的行，更新 [**INFCONTEXT**](/windows/desktop/api/Setupapi/ns-setupapi-infcontext)的 **行** 成員。                                                                     |
| [**SetupGetLineCount**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinecounta)                                   | 傳回指定區段中的行數。                                                                                                                                                  |
| [**SetupGetLineText**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinetexta)                                     | 從 INF 檔案抓取指定行的內容。                                                                                                                                            |
| [**SetupGetMultiSzField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetmultiszfielda)                             | 從 INF 檔案中的行指定欄位開始，傳回字串清單。                                                                                                                   |
| [**SetupGetSourceFileLocation**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourcefilelocationa)                 | 取得來源磁片序數和路徑 (相對於來源檔案所在的來源根目錄)                                                                                                        |
| [**SetupGetSourceFileSize**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourcefilesizea)                         | 取得 INF 檔案中個別原始程式檔或 **複製** 檔案區段的檔案大小。                                                                                                           |
| [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa)                                 | 抓取來源的路徑、標記檔案或描述。                                                                                                                                             |
| [**SetupGetStringField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetstringfielda)                               | 傳回 INF 檔案中某一行的指定字串欄位。                                                                                                                                           |
| [**SetupGetTargetPath**](/windows/desktop/api/Setupapi/nf-setupapi-setupgettargetpatha)                                 | 取得 INF 檔案中 **複製** 檔案區段的目標路徑。                                                                                                                                      |
| [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)                                     | 安裝檔案。                                                                                                                                                                                       |
| [**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)                                 | 安裝檔案並傳回變數，指出檔案是否正在使用中。                                                                                                                  |
| [**SetupInstallFilesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona)       | 將 [ **複製** 檔案]、[ **刪除** 檔案] 和 [ **重新命名** 檔案] 區段中指定的所有檔案排入佇列，以供 **安裝** 區段所列出。                                                       |
| [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)                 | 執行 INF 檔案 **安裝** 區段中指定的指示詞。                                                                                                                                  |
| [**SetupInstallServicesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallservicesfrominfsectiona) | 執行服務安裝和刪除作業，如 INF 檔案的 **服務** 區段中所指定。                                                                                            |
| [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea)                         | 開啟 INF 檔案，並將它附加到現有的 INF 控制碼。                                                                                                                                             |
| [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea)                                     | 開啟 INF 檔案，並傳回其控制碼。                                                                                                                                                          |
| [**SetupOpenMasterInf**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenmasterinf)                                 | 開啟 INF 檔案，其中包含系統隨附之檔案的檔案和配置資訊。                                                                                                        |
| [**SetupQueryInfFileInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinffileinformationa)             | 查詢 INF 資訊結構相關的 INF 檔案名。                                                                                                                               |
| [**SetupQueryInfVersionInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinfversioninformationa)       | 查詢 INF 資訊結構以取得其中一個構成 INF 檔案的版本資訊。                                                                                                      |
| [**SetupSetDirectoryId**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetdirectoryida)                               | 將新的目錄識別碼與特定目錄產生關聯。                                                                                                                                     |



 

 

 



