---
description: Windows Installer 具有下列標準動作。
ms.assetid: 219b5eb6-501f-4e30-b398-4ed5e0cdf2ab
title: 標準動作參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5104c39639ff2bc7b504996467cf707eb52bb014
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192307"
---
# <a name="standard-actions-reference"></a>標準動作參考

Windows Installer 具有下列標準動作。



| 動作名稱                                                     | 動作的簡短描述                                                                                                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [管理員](admin-action.md)                                       | 用於系統管理安裝的最上層動作。                                                                                                                   |
| [做廣告](advertise-action.md)                               | 呼叫以安裝或移除已公告元件的最上層動作。                                                                                                         |
| [AllocateRegistrySpace](allocateregistryspace-action.md)       | 驗證 [**AVAILABLEFREEREG**](availablefreereg.md) 所指定的可用空間是否存在於登錄中。                                                               |
| [AppSearch](appsearch-action.md)                               | 搜尋先前版本的產品，並判斷是否已安裝升級。                                                                                        |
| [BindImage](bindimage-action.md)                               | 將可執行檔系結至匯入的 Dll。                                                                                                                                           |
| [CCPSearch](ccpsearch-action.md)                               | 會在執行升級安裝之前，使用檔案簽章來驗證是否已在系統上安裝合格產品。                                              |
| [CostFinalize](costfinalize-action.md)                         | 結束 [CostInitialize 動作](costinitialize-action.md)開始的內部安裝成本處理常式。                                                               |
| [CostInitialize](costinitialize-action.md)                     | 開始安裝成本處理常式。                                                                                                                                      |
| [CreateFolders](createfolders-action.md)                       | 為元件建立空的資料夾。                                                                                                                                         |
| [CreateShortcuts](createshortcuts-action.md)                   | 建立快捷方式。                                                                                                                                                            |
| [DeleteServices](deleteservices-action.md)                     | 移除系統服務。                                                                                                                                                      |
| [DisableRollback](disablerollback-action.md)                   | 停用其餘安裝的復原。                                                                                                                      |
| [DuplicateFiles](duplicatefiles-action.md)                     | InstallFiles 動作所安裝的重複檔案。                                                                                                                        |
| [ExecuteAction](executeaction-action.md)                       | 檢查 [**EXECUTEACTION**](executeaction.md) 屬性，以判斷哪一個最上層動作開始執行序列，然後執行該動作。                          |
| [FileCost](filecost-action.md)                                 | 使用安裝程式初始化磁片成本計算。 在執行 CostFinalize 動作之前，不會完成磁片的成本。                                                |
| [FindRelatedProducts](findrelatedproducts-action.md)           | 偵測 [升級資料表](upgrade-table.md) 與已安裝產品之間的對應。                                                                                 |
| [ForceReboot](forcereboot-action.md)                           | 用於動作順序，以提示使用者在安裝期間重新開機系統。                                                                           |
| [安裝](install-action.md)                                   | 呼叫以安裝或移除元件的最上層動作。                                                                                                                    |
| [InstallAdminPackage](installadminpackage-action.md)           | 將安裝程式資料庫複製到系統管理安裝點。                                                                                                       |
| [InstallExecute](installexecute-action.md)                     | 執行包含動作順序中所有作業的腳本，這些作業是從安裝開始或上次 InstallFinalize 動作開始。 不會結束交易。   |
| [InstallFiles](installfiles-action.md)                         | 將檔案從來源複製到目的地目錄。                                                                                                                    |
| [InstallFinalize](installfinalize-action.md)                   | 執行包含動作順序中所有作業的腳本，這些作業是從安裝開始或上次 InstallFinalize 動作開始。 標示交易結束。 |
| [InstallInitialize](installinitialize-action.md)               | 標示交易的開頭。                                                                                                                                         |
| [InstallSFPCatalogFile](installsfpcatalogfile-action.md)       | InstallSFPCatalogFile 動作會安裝 Windows Me 用於 Windows 檔案保護的目錄。                                                                        |
| [InstallValidate](installvalidate-action.md)                   | 確認具有屬性化成本的所有磁片區都有足夠的空間可進行安裝。                                                                                   |
| [IsolateComponents](isolatecomponents-action.md)               | 處理 [IsolatedComponent 資料表](isolatedcomponent-table.md)                                                                                                          |
| [LaunchConditions](launchconditions-action.md)                 | 評估 LaunchCondition 資料表中包含的一組條件陳述式，必須全部評估為 True，才能繼續安裝。                          |
| [MigrateFeatureStates](migratefeaturestates-action.md)         | 將目前的功能狀態遷移至暫止的安裝。                                                                                                                  |
| [MoveFiles](movefiles-action.md)                               | 尋找現有的檔案，並將這些檔案移動或複製到新的位置。                                                                                                     |
| [MsiConfigureServices](msiconfigureservices-action.md)         | 設定系統的服務。 **[Windows Installer 4.5 及更早版本](not-supported-in-windows-installer-4-5.md)：** 不支援。<br/>                           |
| [MsiPublishAssemblies 動作](msipublishassemblies-action.md)  | 管理要安裝的 common language runtime 元件和 Win32 元件的公告。                                                                |
| [MsiUnpublishAssemblies](msiunpublishassemblies-action.md)     | 管理要移除之 common language runtime 元件和 Win32 元件的公告。                                                                  |
| [InstallODBC](installodbc-action.md)                           | 安裝 ODBC 驅動程式、轉譯程式和資料來源。                                                                                                                     |
| [InstallServices](installservices-action.md)                   | 向系統註冊服務。                                                                                                                                          |
| [PatchFiles](patchfiles-action.md)                             | 查詢 Patch 資料表，以判斷要將哪些修補程式套用至特定檔案，然後執行檔案的位元組並存修補。                                       |
| [ProcessComponents](processcomponents-action.md)               | 註冊元件、其金鑰路徑和元件用戶端。                                                                                                                 |
| [PublishComponents](publishcomponents-action.md)               | 通告 PublishComponent 資料表中指定的元件。                                                                                                            |
| [PublishFeatures](publishfeatures-action.md)                   | 將每個功能的功能狀態寫入系統登錄                                                                                                             |
| [PublishProduct](publishproduct-action.md)                     | 使用系統發佈產品資訊。                                                                                                                                |
| [RegisterClassInfo](registerclassinfo-action.md)               | 管理系統的 COM 類別資訊註冊。                                                                                                            |
| [RegisterComPlus](registercomplus-action.md)                   | RegisterComPlus 動作會註冊 COM + 應用程式。                                                                                                                       |
| [RegisterExtensionInfo](registerextensioninfo-action.md)       | 向系統註冊延伸模組的相關資訊。                                                                                                                      |
| [RegisterFonts](registerfonts-action.md)                       | 向系統註冊已安裝的字型。                                                                                                                                    |
| [RegisterMIMEInfo](registermimeinfo-action.md)                 | 向系統註冊 MIME 資訊。                                                                                                                                   |
| [RegisterProduct](registerproduct-action.md)                   | 向安裝程式註冊產品資訊，並將安裝程式資料庫儲存在本機電腦上。                                                                     |
| [RegisterProgIdInfo](registerprogidinfo-action.md)             | 向系統註冊 OLE ProgId 資訊。                                                                                                                             |
| [RegisterTypeLibraries](registertypelibraries-action.md)       | 向系統註冊類型程式庫。                                                                                                                                     |
| [RegisterUser](registeruser-action.md)                         | 註冊使用者資訊，以識別產品的使用者。                                                                                                                 |
| [RemoveDuplicateFiles](removeduplicatefiles-action.md)         | 刪除 DuplicateFiles 動作所安裝的檔案。                                                                                                                         |
| [RemoveEnvironmentStrings](removeenvironmentstrings-action.md) | 修改環境變數的值。                                                                                                                                 |
| [RemoveExistingProducts](removeexistingproducts-action.md)     | 移除已安裝的產品版本。                                                                                                                                      |
| [RemoveFiles](removefiles-action.md)                           | 移除 InstallFiles 動作先前安裝的檔案。                                                                                                                |
| [RemoveFolders](removefolders-action.md)                       | 移除連結至設定要移除之元件的空白資料夾。                                                                                                                 |
| [RemoveIniValues](removeinivalues-action.md)                   | 刪除與 IniFile 資料表中指定之元件相關聯的 .ini 檔案資訊。                                                                                     |
| [RemoveODBC](removeodbc-action.md)                             | 移除 ODBC 資料來源、轉譯程式和驅動程式。                                                                                                                          |
| [RemoveRegistryValues](removeregistryvalues-action.md)         | 移除從登錄表建立的應用程式登錄機碼。                                                                                            |
| [RemoveShortcuts](removeshortcuts-action.md)                   | 管理已選取要卸載其功能的已公告快捷方式移除。                                                                                   |
| [ResolveSource](resolvesource-action.md)                       | 決定來源位置並設定 [**SourceDir**](sourcedir.md) 屬性。                                                                                          |
| [RMCCPSearch](rmccpsearch-action.md)                           | 會在執行升級安裝之前，使用檔案簽章來驗證是否已在系統上安裝合格產品。                                              |
| [ScheduleReboot](schedulereboot-action.md)                     | 提示使用者在安裝結束時重新開機系統。                                                                                                         |
| [SelfRegModules](selfregmodules-action.md)                     | 處理 SelfReg 資料表中的模組，並在安裝時加以註冊。                                                                                              |
| [SelfUnregModules](selfunregmodules-action.md)                 | 將 SelfReg 資料表中已設定要卸載的模組取消註冊。                                                                                                  |
| [SEQUENCE](sequence-action.md)                                 | 在 [**SEQUENCE**](sequence.md) 屬性指定的資料表中執行動作。                                                                                           |
| [SetODBCFolders 動作](setodbcfolders-action.md)              | 檢查系統是否有現有的 ODBC 驅動程式，並為新的 ODBC 驅動程式設定目標目錄。                                                                                   |
| [StartServices](startservices-action.md)                       | 啟動系統服務。                                                                                                                                                       |
| [StopServices](stopservices-action.md)                         | 停止系統服務。                                                                                                                                                        |
| [UnpublishComponents](unpublishcomponents-action.md)           | 從 PublishComponent 資料表管理元件的 unadvertisement，並移除已發行元件的相關資訊。                                                 |
| [UnpublishFeatures](unpublishfeatures-action.md)               | 從系統登錄移除選取狀態和功能元件對應資訊。                                                                               |
| [UnregisterClassInfo](unregisterclassinfo-action.md)           | 管理從系統登錄移除 COM 類別的工作。                                                                                                                  |
| [UnregisterComPlus](unregistercomplus-action.md)               | UnregisterComPlus 動作會從登錄中移除 COM + 應用程式。                                                                                                     |
| [UnregisterExtensionInfo](unregisterextensioninfo-action.md)   | 管理從系統移除擴充功能相關資訊的功能。                                                                                                         |
| [UnregisterFonts](unregisterfonts-action.md)                   | 從系統移除已安裝字型的註冊資訊。                                                                                                       |
| [UnregisterMIMEInfo](unregistermimeinfo-action.md)             | 從系統登錄取消註冊 MIME 相關的資訊。                                                                                                                |
| [UnregisterProgIdInfo](unregisterprogidinfo-action.md)         | 管理將 OLE ProgId 資訊與系統的註冊。                                                                                                         |
| [UnregisterTypeLibraries](unregistertypelibraries-action.md)   | 使用系統取消註冊類型程式庫。                                                                                                                                   |
| [ValidateProductID](validateproductid-action.md)               | 將 [ [**ProductID**](productid.md) ] 屬性設定為 [完整產品識別碼]。                                                                                                  |
| [WriteEnvironmentStrings](writeenvironmentstrings-action.md)   | 修改環境變數的值。                                                                                                                                 |
| [WriteIniValues](writeinivalues-action.md)                     | 寫入 .ini 檔案資訊。                                                                                                                                                 |
| [WriteRegistryValues](writeregistryvalues-action.md)           | 設定登錄資訊。                                                                                                                                                 |



 

 

 




