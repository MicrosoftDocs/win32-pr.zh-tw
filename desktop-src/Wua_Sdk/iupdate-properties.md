---
description: IUpdate 介面會定義下列屬性。
ms.assetid: d87544f1-a107-440f-8ce0-77d9f2d90578
title: IUpdate 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b93db8e7d8d6786e3f3f827d9eb2e9f97c43aae4781edf0a05fcf6d03e8fb1f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859858"
---
# <a name="iupdate-properties"></a>IUpdate 屬性

[**IUpdate**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate)介面會定義下列屬性。



| 屬性                                                                           | 描述                                                                                                                                                                         |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutoSelectOnWebSites**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_autoselectonwebsites)                       | 取得布林值，這個值會指出是否將更新標記為 Windows Update 自動選取。                                                                   |
| [**BundledUpdates**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_bundledupdates)                                   | 取得介面，其中包含更新之配套更新的已排序清單的相關資訊。                                                                           |
| [**CanRequireSource**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_canrequiresource)                               | 取得布林值，指出是否需要更新的來源媒體以進行安裝或卸載。                                                          |
| [**類別**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_categories)                                           | 取得介面，其中包含更新所屬的類別集合。                                                                                             |
| [**期限**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_deadline)                                               | 取得必須安裝更新的日期。                                                                                                                                |
| [**DeltaCompressedContentAvailable**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_deltacompressedcontentavailable) | 取得布林值，指出伺服器上是否有差異壓縮的內容可供更新。                                                                       |
| [**DeltaCompressedContentPreferred**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_deltacompressedcontentpreferred) | 取得布林值，這個值會指出是否要在下載時偏好差異壓縮的內容，並在有差異壓縮的內容時，安裝或卸載更新。 |
| [**DeploymentAction**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_deploymentaction)                               | 取得已部署更新的動作。                                                                                                                                   |
| [**描述**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_description)                                         | 取得更新的當地語系化描述。                                                                                                                                       |
| [**DownloadContents**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_downloadcontents)                               | 取得更新下載內容的相關檔案資訊。                                                                                                                    |
| [**DownloadPriority**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_downloadpriority)                               | 取得更新的建議下載優先權。                                                                                                                                 |
| [**EulaAccepted**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_eulaaccepted)                                       | 取得布林值，這個值會指出是否接受電腦的與更新相關聯的 Microsoft 軟體授權條款。                                 |
| [**EulaText**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_eulatext)                                               | 取得與更新相關聯之 Microsoft 軟體授權條款的完整當地語系化文字。                                                                           |
| [**HandlerID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_handlerid)                                             | 取得更新的安裝處理常式。                                                                                                                                             |
| [**身分識別**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_identity)                                               | 取得包含更新之唯一識別碼的介面。                                                                                                                |
| [**映像**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_image)                                                     | 取得介面，其中包含與更新相關聯之影像的相關資訊。                                                                                      |
| [**InstallationBehavior**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_installationbehavior)                       | 取得包含更新安裝選項的介面。                                                                                                             |
| [**IsBeta**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_isbeta)                                                   | 取得布林值，指出更新是否為搶鮮版（Beta）。                                                                                                           |
| [**IsDownloaded**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_isdownloaded)                                       | 取得布林值，指出是否在電腦上快取所有更新內容。                                                                                       |
| [**IsHidden**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden)                                               | 取得布林值，指出使用者是否隱藏更新。                                                                                                          |
| [**IsInstalled**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_isinstalled)                                         | 取得布林值，指出是否在執行搜尋時，將更新安裝在電腦上。                                                                     |
| [**IsMandatory**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ismandatory)                                         | 取得布林值，指出更新的安裝是否為強制性。                                                                                            |
| [**IsUninstallable**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_isuninstallable)                                 | 取得布林值，指出使用者是否可以從電腦卸載更新。                                                                                        |
| [**KBArticleIDs**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_kbarticleids)                                       | 取得與更新相關聯之 Microsoft 知識庫文章識別碼的集合。                                                                                      |
| [**語言**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_languages)                                              | 取得介面，其中包含更新所支援的語言。                                                                                                     |
| [**LastDeploymentChangeTime**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_lastdeploymentchangetime)               | 在部署更新的伺服器上，取得更新的上次發行日期（以國際標準時間 (UTC) 日期和時間）。                                               |
| [**MaxDownloadSize**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_maxdownloadsize)                                 | 取得更新的下載大小上限。                                                                                                                                       |
| [**MinDownloadSize**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_mindownloadsize)                                 | 取得更新的最小下載大小。                                                                                                                                       |
| [**MoreInfoUrls**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_moreinfourls)                                       | 取得特定語言字串的集合，這些字串會指定有關更新詳細資訊的超連結。                                                                    |
| [**MsrcSeverity**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_msrcseverity)                                       | 取得更新的 Microsoft Security Response Center 嚴重性分級。                                                                                                          |
| [**RecommendedCPUSpeed**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_recommendedcpuspeed)                         | 取得用來安裝更新的建議 CPU 速度，以 mhz (MHz) 。                                                                                                      |
| [**RecommendedHardDiskSpace**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_recommendedharddiskspace)               | 取得安裝更新之前，應該可在硬碟上使用的建議可用空間。 可用空間的指定單位為 mb (MB) 。                             |
| [**RecommendedMemory**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_recommendedmemory)                             | 取得在安裝更新之前，應該在電腦上使用的建議實體記憶體大小。 實體記憶體大小的指定單位為 mb (MB) 。         |
| [**ReleaseNotes**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_releasenotes)                                       | 取得更新的當地語系化版本資訊。                                                                                                                                    |
| [**SecurityBulletinIDs**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_securitybulletinids)                         | 取得字串值的集合，其中包含與更新相關聯的資訊安全佈告欄識別碼。                                                                      |
| [**SupersededUpdateIDs**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_supersededupdateids)                         | 取得更新識別碼的集合。 此識別碼集合會指定更新所取代的更新。                                                    |
| [**SupportUrl**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_supporturl)                                           | 取得更新之語言特定支援資訊的超連結。                                                                                                       |
| [**標題**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_title)                                                     | 取得更新的當地語系化標題。                                                                                                                                             |
| [**類型**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_type)                                                       | 取得更新的型別。                                                                                                                                                        |
| [**UninstallationBehavior**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_uninstallationbehavior)                   | 取得包含更新之卸載選項的介面。                                                                                                          |
| [**UninstallationNotes**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_uninstallationnotes)                         | 取得更新的卸載附注。                                                                                                                                       |
| [**UninstallationSteps**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_uninstallationsteps)                         | 取得包含更新之卸載步驟的介面。                                                                                                            |



 

 

 



