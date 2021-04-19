---
description: " (控制項和屬性頁的列舉) "
ms.assetid: 2ac80d0f-94c2-4d70-a48a-1b0060f91902
title: WUA 控制項和屬性頁列舉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99c2058023d636e6680c36d6032e11f14727a3e7
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/02/2021
ms.locfileid: "106984918"
---
# <a name="wua-controls-and-property-pages-enumerations"></a>WUA 控制項和屬性頁列舉

Windows Update Agent (WUA) 會使用下表所列的列舉來表示作業的狀態。



| 列舉型別                                                                                  | 描述                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddServiceFlag**](/windows/win32/api/wuapi/ne-wuapi-addserviceflag)                                                     | 定義可以處理服務註冊的可能方式。                                                                                                                                                                                                         |
| [**AutoDownloadMode**](/windows/win32/api/wuapi/ne-wuapi-autodownloadmode)                                                 | 定義用來判斷自動更新是否會在判斷是否適用于電腦時自動下載更新的邏輯。                                                                                                                  |
| [**AutomaticUpdatesNotificationLevel**](/windows/win32/api/wuapi/ne-wuapi-automaticupdatesnotificationlevel)               | 定義提高許可權的使用者收到自動更新事件通知的可能方式。                                                                                                                                                                                        |
| [**AutomaticUpdatesPermissionType**](/windows/win32/api/wuapi/ne-wuapi-automaticupdatespermissiontype)                     | 定義設定 [**IAutomaticUpdatesSettings：： NotificationLevel**](/windows/win32/api/wuapi/ne-wuapi-automaticupdatesnotificationlevel) 屬性或或 [**IAutomaticUpdatesSettings2：： IncludeRecommendedUpdates**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-get_includerecommendedupdates) 屬性的可能方式。 |
| [**AutomaticUpdatesScheduledInstallationDay**](/windows/win32/api/wuapi/ne-wuapi-automaticupdatesscheduledinstallationday) | 定義自動更新安裝或卸載更新的星期幾。                                                                                                                                                                                                   |
| [**AutomaticUpdatesUserType**](/windows/win32/api/wuapi/ne-wuapi-automaticupdatesusertype)                                 | 描述使用者的類型。                                                                                                                                                                                                                                                           |
| [**AutoSelectionMode**](/windows/win32/api/wuapi/ne-wuapi-autoselectionmode)                                               | 定義邏輯，用來決定當使用者在 Windows Update 使用者介面中查看可用的更新時，是否會自動選取特定的更新。                                                                                                        |
| [**DeploymentAction**](/windows/win32/api/wuapi/ne-wuapi-deploymentaction)                                                 | 定義明確部署更新的動作。                                                                                                                                                                                                                        |
| [**DownloadPhase**](/windows/win32/api/wuapi/ne-wuapi-downloadphase)                                                       | 定義 [**IDownloadProgress：： CurrentUpdateDownloadPhase**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatedownloadphase) 屬性所傳回之目前更新的下載進度。                                                                                      |
| [**DownloadPriority**](/windows/win32/api/wuapi/ne-wuapi-downloadpriority)                                                 | 定義下載作業的可能優先順序。                                                                                                                                                                                                                             |
| [**InstallationImpact**](/windows/win32/api/wuapi/ne-wuapi-installationimpact)                                             | 定義可能因安裝或卸載更新而造成的影響層級。                                                                                                                                                                                     |
| [**InstallationRebootBehavior**](/windows/win32/api/wuapi/ne-wuapi-installationrebootbehavior)                             | 定義更新可能的重新開機行為。                                                                                                                                                                                                                                 |
| [**OperationResultCode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode)                                           | 定義更新上的下載、安裝、卸載或驗證操作的可能結果。                                                                                                                                                                               |
| [**SearchScope**](/windows/win32/api/wuapi/ne-wuapi-searchscope)                                                           | 指定搜尋應該傳回的各種更新：個別電腦更新、每一使用者更新或兩者。 每個使用者更新是專為影響單一使用者環境而設計的更新。 如需詳細資訊，請參閱 [**IUpdate4：:P eruser**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate4-get_peruser)。    |
| [**Serverselection.sqlpolicy**](/openspecs/windows_protocols/ms-uamg/07e2bfa4-6795-4189-b007-cc50b476181a)                                                   | 定義 Windows Update 可以操作的更新服務。 .                                                                                                                                                                                                                |
| [**UpdateEndpointAuthTokenType**](updateendpointauthtokentype.md)                           | 定義可用來向端點驗證的標記類型。                                                                                                                                                                                                      |
| [**UpdateEndpointType**](updateendpointtype.md)                                             | 定義可以用來連接到服務的端點類型。                                                                                                                                                                                                               |
| [**UpdateExceptionCoNtext**](/windows/win32/api/wuapi/ne-wuapi-updateexceptioncontext)                                     | 定義可以提供 [**IUpdateException**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateexception) 物件的內容。                                                                                                                                                                                  |
| [**UpdateLockdownOption**](/windows/win32/api/wuapi/ne-wuapi-updatelockdownoption)                                         | 定義 Windows Update 代理程式 (WUA) 物件可以從 Windows Update 存取的功能。                                                                                                                                                                                  |
| [**Character**](/windows/win32/api/wuapi/ne-wuapi-updateoperation)                                                   | 定義可以在更新時嘗試的作業。                                                                                                                                                                                                                            |
| [**UpdateServiceOption**](/windows/win32/api/wuapi/ne-wuapi-updateserviceoption)                                           | 定義移除掃描封裝服務之服務註冊的選項。                                                                                                                                                                                                    |
| [**UpdateServiceRegistrationState**](/windows/win32/api/wuapi/ne-wuapi-updateserviceregistrationstate)                     | 定義更新服務的可能狀態。                                                                                                                                                                                                                                    |
| [**UpdateType**](/windows/win32/api/wuapi/ne-wuapi-updatetype)                                                             | 指出更新是否為軟體更新或驅動程式更新。                                                                                                                                                                                                                  |



 

 

 



