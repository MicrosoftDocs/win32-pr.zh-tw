---
description: ICE 用來驗證安裝套件。 本主題中的表格會識別每一冰。 如需用來驗證合併模組之 ICEMs 的詳細資訊，請參閱合併模組 ICE 參考。
ms.assetid: f287c1cf-c464-42a3-985d-f892db5e1f5f
title: ICE 參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53c249692150923ebd7752c2c69e306ebcc69d2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975159"
---
# <a name="ice-reference"></a>ICE 參考

ICE 用來驗證安裝套件。 本主題中的表格會識別每一冰。 如需用來驗證合併模組之 ICEMs 的詳細資訊，請參閱 [合併模組 ICE 參考](merge-module-ice-reference.md)。



| 冰                   | Description                                                                                                                                                                                                                                             |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ICE01](ice01.md)    | 簡單的霜淇淋機制測試。                                                                                                                                                                                                                           |
| [ICE02](ice02.md)    | 檔案元件的迴圈參考測試，Registry-Component KeyPaths。                                                                                                                                                                                |
| [ICE03](ice03.md)    | 基本資料和外鍵驗證。                                                                                                                                                                                                                  |
| [ICE04](ice04.md)    | 針對 [媒體資料表](media-table.md)的 LastSequence 號碼驗證檔案序號。                                                                                                                                                 |
| [ICE05](ice05.md)    | 驗證特定資料表中的「必要」專案。                                                                                                                                                                                                  |
| [ICE06](ice06.md)    | 驗證資料庫中遺失的資料行或資料表。 您 \_ 必須在資料庫中找到驗證資料表中定義的任何資料行。                                                                                                                     |
| [ICE07](ice07.md)    | 驗證是否已將字型安裝至 FontsFolder。                                                                                                                                                                                                  |
| [ICE08](ice08.md)    | 檢查元件資料表的 [元件 Id] 資料行中是否有重複的 Guid。                                                                                                                                                                            |
| [ICE09](ice09.md)    | 驗證是否已針對每個標示為要安裝的元件，將永久位設定為 SystemFolder。                                                                                                                                              |
| [ICE10](ice10.md)    | 確保子系和父系之間的公告功能狀態是相容的。                                                                                                                                                                        |
| [ICE12](ice12.md)    | 驗證類型35和類型51自訂動作及其在順序資料表中的位置。                                                                                                                                                                |
| [ICE13](ice13.md)    | 驗證對話未列為執行順序資料表中的動作。 對話方塊動作只能在使用者介面順序資料表中使用。                                                                                                 |
| [ICE14](ice14.md)    | 驗證功能父系沒有設定 msidbFeatureAttributesFollowParent 位。 也會驗證在相同記錄中，功能和功能父資料行中的專案 \_ 不相同。                                              |
| [ICE15](ice15.md)    | 驗證 MIME 資料表中的每個專案和延伸模組資料表中的對應延伸之間是否有迴圈參考。                                                                                                                |
| [ICE16](ice16.md)    | 驗證屬性資料表中的 ProductName 是否長度不超過63個字元。                                                                                                                                                       |
| [ICE17](ice17.md)    | 驗證控制資料表中的控制項類型相依性。 涵蓋按鈕、RadioButtonGroups、清單方塊、Listview 和下拉式方塊。                                                                                                                  |
| [ICE18](ice18.md)    | 驗證元件資料表的 KeyPath 資料行是否為 null。 在此情況下，金鑰路徑是目錄。                                                                                                                                         |
| [ICE19](ice19.md)    | 驗證廣告資料表： Class、TypeLib、Extension、PublishComponents 和快捷方式。                                                                                                                                                           |
| [ICE20](ice20.md)    | 驗證所需的對話方塊是否在對話方塊資料表中。                                                                                                                                                                                            |
| [ICE21](ice21.md)    | 驗證元件資料表中的所有元件都對應至 FeatureComponents 資料表中的功能。                                                                                                                                                   |
| [ICE22](ice22.md)    | 驗證 \_ PublishComponent 資料表中的功能和元件資料 \_ 行。                                                                                                                                                                     |
| [ICE23](ice23.md)    | 驗證所有對話方塊中控制項的定位順序。                                                                                                                                                                                                |
| [ICE24](ice24.md)    | 驗證屬性資料表中的特定屬性。                                                                                                                                                                                                     |
| [ICE25](ice25.md)    | 驗證合併模組相依性和合併模組排除項。                                                                                                                                                                                         |
| [ICE26](ice26.md)    | 驗證順序資料表中所需和禁止的動作。                                                                                                                                                                                       |
| [ICE27](ice27.md)    | 驗證順序資料表的組織和順序。                                                                                                                                                                                            |
| [ICE28](ice28.md)    | 驗證不得以 ForceReboot 分隔的動作。                                                                                                                                                                                            |
| [ICE29](ice29.md)    | 如果截斷為62個字元的限制，則會驗證您的資料流程名稱是否維持唯一。                                                                                                                                                                  |
| [ICE30](ice30.md)    | 驗證封裝含相同檔案的元件安裝，在相同的目錄中永遠不會安裝檔案一次以上。                                                                                                                 |
| [ICE31](ice31.md)    | 驗證控制資料表的文字資料行中所列的文字樣式。                                                                                                                                                                               |
| [ICE32](ice32.md)    | 比較資料行定義，以驗證索引鍵和外鍵的大小與類型相同。                                                                                                                                                   |
| [ICE33](ice33.md)    | 檢查登錄表中是否有屬於其他資料表的專案。                                                                                                                                                                                      |
| [ICE34](ice34.md)    | 驗證每個選項按鈕群組都有預設值。                                                                                                                                                                                              |
| [ICE35](ice35.md)    | 驗證封包檔中的任何檔案無法設定為從來源執行。                                                                                                                                                                      |
| [ICE36](ice36.md)    | 驗證圖示表格中所列的圖示是否用於類別、ProgID 或快速鍵資料表中。                                                                                                                                                        |
| [ICE38](ice38.md)    | 驗證安裝在使用者設定檔之下的元件，會使用 HKCU 下的登錄機碼作為其金鑰路徑。                                                                                                                                           |
| [ICE39](ice39.md)    | 驗證資料庫的摘要資訊資料流程。                                                                                                                                                                                               |
| [ICE40](ice40.md)    | 執行各種其他檢查。                                                                                                                                                                                                                  |
| [ICE41](ice41.md)    | 驗證延伸模組和類別資料表中的專案會參考屬於參考功能的元件。                                                                                                                                       |
| [ICE42](ice42.md)    | 檢查類別資料表專案沒有將 .exe 檔案設定為 InProc 值，而且只有 LocalServer 的內容具有引數和 DefInProc 值。                                                                                                    |
| [ICE43](ice43.md)    | 檢查非公告的快捷方式是否位於具有 HKCU 登錄機碼的元件中做為金鑰路徑。                                                                                                                                                        |
| [ICE44](ice44.md)    | 檢查 ControlEvent 資料表中的對話方塊事件 (NewDialog、SpawnDialog、SpawnWaitDialog) 參考對話方塊資料表中的有效對話。                                                                                                              |
| [ICE45](ice45.md)    | 檢查已設定的保留位。                                                                                                                                                                                                                  |
| [ICE46](ice46.md)    | 檢查自訂屬性，其大小寫與已定義的屬性不同。                                                                                                                                                                    |
| [ICE47](ice47.md)    | 檢查每項功能是否有超過1600個元件的功能。                                                                                                                                                                                        |
| [ICE48](ice48.md)    | 檢查已硬式編碼至本機路徑的目錄。                                                                                                                                                                                              |
| [ICE49](ice49.md)    | 檢查 \_ 登錄表中的非 REG SZ 預設值。                                                                                                                                                                                            |
| [ICE50](ice50.md)    | 檢查公告的快捷方式是否有正確的圖示和內容功能表。                                                                                                                                                                                  |
| [ICE51](ice51.md)    | 檢查 SIMSUN18030.TTC/TTF 字型是否沒有標題，但所有其他字型都有。                                                                                                                                                                              |
| [ICE52](ice52.md)    | 檢查 AppSearch 資料表中的非公用屬性。                                                                                                                                                                                                |
| [ICE53](ice53.md)    | 檢查是否有寫入私用安裝程式資訊或原則值的登錄專案。                                                                                                                                                                  |
| [ICE54](ice54.md)    | 使用隨附的檔案做為金鑰路徑檔案來檢查元件。                                                                                                                                                                                     |
| [ICE55](ice55.md)    | 檢查 LockPermission 物件是否存在且具有有效的許可權。                                                                                                                                                                                    |
| [ICE56](ice56.md)    | 驗證 .msi 檔案的目錄結構是否具有單一有效的根目錄。                                                                                                                                                                        |
| [ICE57](ice57.md)    | 驗證個別的元件不會混用每一電腦和每個使用者的資料。                                                                                                                                                                          |
| [ICE58](ice58.md)    | 檢查您的 [媒體資料表](media-table.md) 是否沒有超過80個數據列。                                                                                                                                                                        |
| [ICE59](ice59.md)    | 檢查公告的快捷方式是否屬於快捷方式的目標功能所安裝的元件。                                                                                                                                         |
| [ICE60](ice60.md)    | 檢查檔案 [資料表](file-table.md) 中的檔案是否不是字型並且具有版本，也會有語言。                                                                                                                                 |
| [ICE61](ice61.md)    | 檢查 [升級資料表](upgrade-table.md)。                                                                                                                                                                                                          |
| [ICE62](ice62.md)    | 針對可能會導致非預期行為的資料，執行 [IsolatedComponent 資料表](isolatedcomponent-table.md) 的廣泛檢查。                                                                                                                    |
| [ICE63](ice63.md)    | 檢查是否有適當的 RemoveExistingProducts 動作順序。                                                                                                                                                                                      |
| [ICE64](ice64.md)    | 檢查是否已在漫遊案例中移除使用者設定檔中的新目錄。                                                                                                                                                                       |
| [ICE65](ice65.md)    | 檢查 [環境資料表](environment-table.md) 是否沒有不正確前置詞或附加值。                                                                                                                                               |
| [ICE66](ice66.md)    | 使用資料庫中的資料表，來判斷您的資料庫應該使用哪一個架構。                                                                                                                                                                     |
| [ICE67](ice67.md)    | 檢查非公告快捷方式的目標是否屬於與快捷方式本身相同的元件，或目標群組件的屬性確定不會變更安裝位置。                                         |
| [ICE68](ice68.md)    | 檢查安裝所需的所有自訂動作類型是否有效。                                                                                                                                                                               |
| [ICE69](ice69.md)    | 檢查格式字串中 $componentkey 格式的所有子字串都 \[ \] 不會交互參照元件。                                                                                                                                   |
| [ICE70](ice70.md)    | 確認已正確指定登錄專案的整數值。                                                                                                                                                                              |
| [ICE71](ice71.md)    | 確認 [媒體資料表](media-table.md) 包含 DiskId 等於1的專案。                                                                                                                                                              |
| [ICE72](ice72.md)    | 確保 [AdvtExecuteSequence 資料表](advtexecutesequence-table.md) 中唯一使用的自訂動作為類型19、類型35和類型51自訂動作。                                                                                           |
| [ICE73](ice73.md)    | 確認您的套件未重複使用 Windows Installer SDK 範例的封裝碼或產品代碼。 如需詳細資訊，請參閱 [封裝程式碼](package-codes.md) 和 [產品代碼](product-codes.md)。                                     |
| [ICE74](ice74.md)    | 確認 [**FASTOEM**](fastoem.md) 屬性尚未撰寫至 [屬性資料表](property-table.md)。                                                                                                                              |
| [ICE75](ice75.md)    | 確認使用已安裝的檔案做為其來源的所有自訂動作類型，都會在 [CostFinalize 動作](costfinalize-action.md)之後排序。                                                                                                |
| [ICE76](ice76.md)    | 確認 [BindImage 資料表](bindimage-table.md) 中沒有任何檔案參考 SFP (WFP) 目錄。                                                                                                                                                      |
| [ICE77](ice77.md)    | 確認腳本內自訂動作會在 [InstallInitialize 動作](installinitialize-action.md) 之後，以及 [InstallFinalize 動作](installfinalize-action.md)之前排序。                                                            |
| [ICE78](ice78.md)    | 確認 [AdvtUISequence 資料表](advtuisequence-table.md) 不存在或空白。                                                                                                                                                   |
| [ICE79](ice79.md)    | 使用 [Condition](condition.md) 資料類型，驗證在資料庫欄位中輸入之元件和功能的參考。                                                                                                                          |
| [ICE80](ice80.md)    | 驗證 [**範本摘要**](template-summary.md) 屬性和 [**頁面計數摘要**](page-count-summary.md) 屬性是否正確地指定了64位元件或自訂動作腳本的存在。                                        |
| [ICE81](ice81.md)    | 驗證 [MsiDigitalCertificate 資料表](msidigitalcertificate-table.md)、 [MsiDigitalSignature 資料表](msidigitalsignature-table.md) 和 [MsiPackageCertificate 資料表](msipackagecertificate-table.md)。                                            |
| [ICE82](ice82.md)    | 驗證 [InstallExecuteSequence 資料表](installexecutesequence-table.md)。                                                                                                                                                                         |
| [ICE83](ice83.md)    | 驗證 [MsiAssembly 資料表](msiassembly-table.md)。                                                                                                                                                                                               |
| [ICE84](ice84.md)    | 檢查順序資料表，以確認所需的 [標準動作](standard-actions.md) 未設定條件。                                                                                                                                |
| [ICE85](ice85.md)    | 驗證 [MoveFile 資料表](movefile-table.md) 的 [未使用] 資料行是否為有效的完整檔案名。                                                                                                                                             |
| [ICE86](ice86.md)    | 如果封裝使用 [條件](condition.md)類型之資料庫資料行中的 [**AdminUser**](adminuser.md)屬性，就會發出警告。                                                                                                             |
| [ICE87](ice87.md)    | 驗證 [屬性資料表](property-table.md)中未撰寫下列屬性。                                                                                                                                             |
| [ICE88](ice88.md)    | 驗證 [IniFile 資料表](inifile-table.md)的 DirProperty 資料行。                                                                                                                                                                                 |
| [ICE89](ice89.md)    | 驗證 progid 資料表中 Progid 父資料行中的值， \_ 是否為 progid 資料表中 progid 資料行的有效外鍵。 [](progid-table.md)                                                                                                |
| [ICE90](ice90.md)    | 如果發現快捷方式的目錄已指定為公用屬性，則會張貼警告。                                                                                                                                                        |
| [ICE91](ice91.md)    | 如果檔案、.ini 檔案或快捷方式檔案已安裝到每個使用者設定檔目錄中，但不因 [**ALLUSERS**](allusers.md) 屬性而異，則會張貼警告。                                                                            |
| [ICE92](ice92.md)    | 確認沒有元件識別碼 GUID 的元件也未指定為永久元件。 確認沒有任何元件同時具有 **msidbComponentAttributesPermanent** 和 **msidbComponentAttributesUninstallOnSupersedence** 屬性。 |
| [ICE93](ice93.md)    | 如果自訂動作使用的名稱與標準動作相同，則會發出警告。                                                                                                                                                                            |
| [ICE94](ice94.md)    | 如果有任何 unadvertised 快捷方式指向全域組件快取中的元件檔案，就會發出警告。                                                                                                                                     |
| [ICE95](ice95.md)    | 檢查 [Control table](control-table.md) 和 [BBControl 資料表](bbcontrol-table.md) ，以確認該佈告欄控制項符合所有公告欄。                                                                                             |
| [ICE96](ice96.md)    | 確認已在[AdvtExecuteSequence 資料表](advtexecutesequence-table.md)中輸入[PublishFeatures 動作](publishfeatures-action.md)和[PublishProduct 動作](publishproduct-action.md)。                                        |
| [ICE97](ice97.md)    | 確認兩個元件沒有將共用元件隔離到相同的目錄。                                                                                                                                                                   |
| [ICE98](ice98.md)    | 驗證 ODBC 資料來源的 [ODBCDataSource 資料表](odbcdatasource-table.md) 的描述欄位。                                                                                                                                         |
| [ICE99](ice99.md)    | 確認 [目錄](directory-table.md) 資料表中未輸入的屬性名稱，重複了針對 Windows Installer 公開或私用所保留的名稱。                                                                                 |
| [ICE100](ice-100.md) | 檢查 [MsiEmbeddedUI](msiembeddedui-table.md) 和 [MsiEmbeddedChainer](msiembeddedchainer-table.md) 資料表的撰寫。                                                                                                                     |
| [ICE101](ice-101.md) | 檢查 [功能](feature-table.md) 資料表的 [功能] 資料行中沒有任何值超過38個字元的最大長度。                                                                                                                         |
| [ICE102](ice-102.md) | 驗證 [MsiServiceConfig](msiserviceconfig-table.md) 和 [MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md) 資料表。                                                                                                     |
| [ICE103](ice-103.md) | 驗證 [MsiPrint](msiprint-controlevent.md) 和 [MsiLaunchApp](msilaunchapp-controlevent.md) 控制項事件。                                                                                                                                   |
| [ICE104](ice-104.md) | 驗證 [MsiLockPermissionsEx](msilockpermissionsex-table.md) 和 [LockPermissions](lockpermissions-table.md) 資料表。                                                                                                                            |
| [ICE105](ice-105.md) | 驗證封裝是否已撰寫成要安裝在每個使用者的內容中。                                                                                                                                                                     |



 

 

 



