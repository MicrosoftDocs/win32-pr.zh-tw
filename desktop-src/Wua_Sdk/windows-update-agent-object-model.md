---
description: 使用 Windows Update Agent (WUA) 的程式設計人員一開始會先將 Wuapi.dll 的參考加入至 (、Microsoft Visual C++ 或 c Visual Basic 中的目前專案) ， \# 或在 c 或 c + + 專案中參考 Wuapi 和 Wuguid。
ms.assetid: ec9cbb0b-b5d4-41f2-8a25-143130d08a3b
title: Windows更新代理程式物件模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e32b60f9306dfae5910418ddc07353a421e0325c0953fb1f47994ad007ded5ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855441"
---
# <a name="windows-update-agent-object-model"></a>Windows更新代理程式物件模型

使用 Windows Update Agent (WUA) 的程式設計人員一開始會先將 Wuapi.dll 的參考加入至 (、Microsoft Visual C++ 或 c Visual Basic 中的目前專案) ， \# 或在 c 或 c + + 專案中參考 Wuapi 和 Wuguid。 使用 WUA API 的第一個步驟，是從適當的 coclass 建立物件，以建立其中一個介面的實例。

下圖描述 WUA 物件模型。 如需詳細資訊，請參閱「[WUA 物件和相關聯](#wua-objects-and-associated-tasks)的工作」一節。 如需所有 WUA 介面的完整清單，請參閱 [介面](interfaces.md)。

![windows update 代理程式物件模型](images/wua-object-model.png)

## <a name="wua-objects-and-associated-tasks"></a>WUA 物件和相關聯的工作

下表列出 WUA 物件和與 WUA 物件相關聯的一般工作。



| Object                                                                | 描述                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutomaticUpdates**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdates)                         | 開始、暫停或繼續自動更新。                                                                                                                                                                                                  |
| [**AutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings)         | 取得或設定安裝更新的日期和時間。 指定使用者如何收到自動更新事件的通知。                                                                                                                          |
| [**類別**](/windows/desktop/api/Wuapi/nn-wuapi-icategory)                                         | 取得更新類別的相關資訊，包括名稱、識別碼、描述、擁有者和預定產品。 取得屬於此分類的更新集合。 取出父系或子類別的集合。 |
| [**CategoryCollection**](/windows/desktop/api/Wuapi/nn-wuapi-icategorycollection)                     | 存取 Category 物件的集合。                                                                                                                                                                                                    |
| [**DownloadResult**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadresult)                             | 取得下載結果的相關資訊。                                                                                                                                                                                        |
| [**InstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationresult)                     | 取得安裝或卸載結果的相關資訊。 判斷是否需要重新開機系統才能完成安裝或卸載。                                                                  |
| [**>.searchresult**](/windows/desktop/api/Wuapi/nn-wuapi-isearchresult)                                 | 取得搜尋類別或更新結果的相關資訊。 透過搜尋來抓取目的地電腦上找到的分類集合。 取出搜尋所找到的更新集合。                     |
| [**SystemInformation**](/windows/desktop/api/Wuapi/nn-wuapi-isysteminformation)                       | 取得目的地電腦上 OEM 硬體和系統重新開機需求的相關資訊。                                                                                                                                        |
| [**更新**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate)                                             | 取得更新的大部分資訊，包括配套更新、來源需求、身分識別、描述、卸載選項、下載優先順序、大小和期限。                                                                |
| [**UpdateCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatecollection)                         | 存取更新物件的集合。                                                                                                                                                                                                      |
| [**UpdateDownloader**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader)                         | 開始非同步或同步下載與更新相關聯的檔案。                                                                                                                                            |
| [**UpdateDownloadResult**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloadresult)                 | 取得一項更新下載結果的相關資訊。                                                                                                                                                                       |
| [**UpdateException**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateexception)                           | 取得發生更新錯誤時所擲回之例外狀況的描述和內容。                                                                                                                                            |
| [**UpdateExceptionCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateexceptioncollection)       | 存取 UpdateException 物件的集合。                                                                                                                                                                                             |
| [**UpdateHistoryEntry**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentry)                     | 取得已安裝或卸載之更新的相關資訊，包括已處理的應用程式、日期和描述。                                                                                                    |
| [**UpdateHistoryEntryCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentrycollection) | 存取 UpdateHistoryEntry 物件的集合。                                                                                                                                                                                          |
| [**UpdateInstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstallationresult)         | 取得有關安裝或卸載更新結果的資訊。                                                                                                                                                  |
| [**UpdateInstaller**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller)                           | 啟動非同步或同步安裝或卸載更新。 啟動互動式對話順序，引導使用者完成安裝更新的步驟。                                                              |
| [**UpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher)                             | 依準則搜尋伺服器上的更新，例如更新類型、識別碼或類別目錄。                                                                                                                                            |
| [**UpdateSession**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession)                               | 啟動會話以搜尋、下載、安裝或卸載應用程式的更新。                                                                                                                                                  |
| [**WebProxy**](/windows/desktop/api/Wuapi/nn-wuapi-iwebproxy)                                         | 取得並設定 HTTP proxy 設定。                                                                                                                                                                                                       |



 

 

 



