---
description: 若要在您的應用程式中啟用 Windows Installer，您必須使用安裝程式函數。 本主題中的表格會依分類來識別函數。
ms.assetid: 05a16915-6b47-4d51-b62a-5a4d92b87e50
title: 安裝程式函數參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ab6a77bd3aa02be85f0d2a3cb11a864861535360f5741c6566f77e9fc1aa11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118630543"
---
# <a name="installer-function-reference"></a>安裝程式函數參考

若要在您的應用程式中啟用 Windows Installer，您必須使用安裝程式函數。 本主題中的表格會依分類來識別函數。

## <a name="user-interface-and-logging-functions"></a>消費者介面和記錄功能



| Name                                                     | 描述                                                                           |
|----------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)             | 啟用安裝程式的內部使用者介面。                                 |
| [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)             | 啟用以字串格式接收訊息的外部使用者介面處理常式。 |
| [**MsiSetExternalUIRecord**](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord) | 啟用以記錄格式接收訊息的外部使用者介面處理常式。 |
| [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga)                     | 設定呼叫進程中所有安裝的記錄模式。                       |



 

## <a name="handle-management-functions"></a>處理管理功能



| Name                                             | 描述                                                   |
|--------------------------------------------------|---------------------------------------------------------------|
| [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle)         | 關閉開啟的安裝控制碼。                           |
| [**MsiCloseAllHandles**](/windows/desktop/api/Msi/nf-msi-msicloseallhandles) | 關閉所有開啟的安裝控制碼。 請勿使用進行清除。 |



 

## <a name="installation-and-configuration-functions"></a>安裝和設定功能



| Name                                                                     | 描述                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsiAdvertiseProduct**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproducta)                       | 通告產品。                                                                                                                                                                                                        |
| [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa)                   | 通告產品。                                                                                                                                                                                                        |
| [**MsiAdvertiseScript**](/windows/desktop/api/Msi/nf-msi-msiadvertisescripta)                         | 將公告腳本檔案複製到指定的位置。                                                                                                                                                                    |
| [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta)                           | 安裝或移除應用程式或應用程式套件。                                                                                                                                                                     |
| [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)                       | 安裝或移除應用程式或應用程式套件。                                                                                                                                                                     |
| [**MsiConfigureProductEx**](/windows/desktop/api/Msi/nf-msi-msiconfigureproductexa)                   | 安裝或移除應用程式或應用程式套件。 您可以指定產品命令列。                                                                                                                            |
| [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)                       | 重新安裝或修復安裝。                                                                                                                                                                                       |
| [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea)                       | 設定功能的已安裝狀態。                                                                                                                                                                                 |
| [**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)                       | 驗證或修復功能。                                                                                                                                                                                               |
| [**MsiInstallMissingComponent**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta)         | 安裝遺失的元件。                                                                                                                                                                                                 |
| [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea)                   | 安裝遺失的檔案。                                                                                                                                                                                                      |
| [**MsiNotifySidChange**](/windows/desktop/api/Msi/nf-msi-msinotifysidchangea)                         | 使用使用者 sid 的變更，通知並更新 Windows Installer 的內部資訊。 從 Windows Installer 3.1 開始提供。                                                                                   |
| [**MsiProcessAdvertiseScript**](/windows/desktop/api/Msi/nf-msi-msiprocessadvertisescripta)           | 將公告腳本檔處理至指定的位置。                                                                                                                                                                 |
| [**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea)                 | 在指定的內容中新增或重新排序修補程式或產品的來源。                                                                                                                                                   |
| [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)             | 在指定的內容中新增或重新排序修補程式或產品的來源。 針對不存在於指定內容中的修補程式建立來源清單。 適用于 Windows Installer 3.0。                                |
| [**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)             | 在指定的內容中移除產品或修補程式的現有來源。 適用于 Windows Installer 3.0。                                                                                                               |
| [**MsiSourceListClearAll**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearalla)                   | 針對指定的產品實例，移除特定來源類型的所有現有來源。                                                                                                                                 |
| [**MsiSourceListClearAllEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa)               | 針對指定的產品實例，移除特定來源類型的所有現有來源。 適用于 Windows Installer 3.0。                                                                                            |
| [**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)     | 移除產品或修補程式目前來源的註冊，該來源會註冊為 "LastUsedSource" 屬性。 此函數不會影響已註冊的來源清單。                                      |
| [**MsiSourceListForceResolutionEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutionexa) | 移除產品或修補程式目前來源的註冊，該來源會註冊為 "LastUsedSource" 屬性。 此函數不會影響已註冊的來源清單。 適用于 Windows Installer 3.0。 |
| [**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa)                     | 抓取特定內容中產品或修補程式的來源清單相關資訊。                                                                                                                                    |
| [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)                     | 在指定的內容中，設定產品或修補程式最近使用的來源。 適用于 Windows Installer 3.0。                                                                                                       |
| [**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)       | 列舉針對修補程式或產品的媒體來源所註冊的磁片清單。 適用于 Windows Installer 3.0。                                                                                                    |
| [**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)           | 新增或更新已註冊產品或修補程式之媒體來源的磁片。 適用于 Windows Installer 3.0。                                                                                                            |
| [**MsiSourceListClearMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska)      | 針對特定內容中的產品或修補程式，在媒體來源下移除現有的已註冊磁片。 適用于 Windows Installer 3.0。                                                                                |
| [**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa)             | 列舉指定修補程式或產品的來源清單中的來源。 適用于 Windows Installer 3.0。                                                                                                              |



 

## <a name="component-specific-functions"></a>Component-Specific 函式



| Name                                                                     | 描述                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya)                         | 安裝並傳回元件的完整元件路徑。                                                                                                                                                                 |
| [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)                       | 安裝並傳回元件的完整元件路徑。                                                                                                                                                                  |
| [**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta)     | 安裝並傳回合格元件的完整元件路徑。                                                                                                                                                        |
| [**MsiProvideQualifiedComponentEx**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa) | 安裝並傳回產品所發佈之合格元件的完整元件路徑。                                                                                                                         |
| [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha)                       | 傳回已安裝元件的完整路徑或登錄機碼。                                                                                                                                                              |
| [**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa)                   | 將完整路徑或登錄機碼傳給使用者帳戶和安裝內容上已安裝的元件。 **[Windows Installer 4.5 及更早版本](not-supported-in-windows-installer-4-5.md)：** 不支援。<br/> |
| [**MsiLocateComponent**](/windows/desktop/api/Msi/nf-msi-msilocatecomponenta)                         | 傳回已安裝元件的完整路徑（沒有產品代碼）。                                                                                                                                                       |
| [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea)                 | 傳回元件的已安裝狀態。 可以查詢在目前使用者以外的使用者帳戶下安裝之產品實例的元件。 適用于 Windows Installer 3.0 或更新版本。                        |



 

## <a name="application-only-functions"></a>Application-Only 函式



| Name                                             | 描述                                                            |
|--------------------------------------------------|------------------------------------------------------------------------|
| [**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) | 從安裝精靈儲存使用者資訊。                   |
| [**MsiUseFeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea)           | 遞增功能的使用計數，並指出安裝狀態。 |
| [**MsiUseFeatureEx**](/windows/desktop/api/Msi/nf-msi-msiusefeatureexa)       | 遞增功能的使用計數，並指出安裝狀態。 |
| [**MsiGetProductCode**](/windows/desktop/api/Msi/nf-msi-msigetproductcodea)   | 使用元件程式碼傳回產品代碼。                         |



 

## <a name="system-status-functions"></a>系統狀態函數



| Name                                                             | 描述                                                                                                                                                                                                                       |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa)                       | 列舉已公告的產品。                                                                                                                                                                                                   |
| [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)                   | 列舉指定內容中已公告或已安裝產品的所有實例。 適用于 Windows Installer 3.0 或更新版本。                                                                                    |
| [**MsiEnumRelatedProducts**](/windows/desktop/api/Msi/nf-msi-msienumrelatedproductsa)         | 列舉具有指定升級程式碼的目前已安裝產品。                                                                                                                                                          |
| [**MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa)                       | 列舉已發行的功能。                                                                                                                                                                                                    |
| [**MsiEnumComponents**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa)                   | 列舉已安裝的元件。                                                                                                                                                                                              |
| [**MsiEnumComponentsEx**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa)               | 列舉跨使用者帳戶和安裝內容的已安裝元件。 **[Windows Installer 4.5 及更早版本](not-supported-in-windows-installer-4-5.md)：** 不支援。<br/>                                 |
| [**MsiEnumClients**](/windows/desktop/api/Msi/nf-msi-msienumclientsa)                         | 列舉已安裝元件的用戶端。                                                                                                                                                                                 |
| [**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)                     | 列舉跨使用者帳戶和安裝內容之已安裝元件的用戶端。 **[Windows Installer 4.5 及更早版本](not-supported-in-windows-installer-4-5.md)：** 不支援。<br/>                    |
| [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa) | 列舉元件的公告限定詞。                                                                                                                                                                             |
| [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea)             | 傳回功能的已安裝狀態。                                                                                                                                                                                         |
| [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa)         | 傳回產品功能的已安裝狀態。 可以查詢在目前使用者以外的使用者帳戶下安裝之產品實例的功能。 適用于 Windows Installer 3.0 或更新版本。                        |
| [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea)             | 傳回應用程式或應用程式套件的已安裝狀態。                                                                                                                                                              |
| [**MsiGetFeatureUsage**](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea)                 | 傳回功能的使用計量。                                                                                                                                                                                              |
| [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)                   | 傳回已發行和已安裝產品的產品資訊。                                                                                                                                                                 |
| [**MsiGetProductInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa)               | 傳回已公告和已安裝產品的產品資訊。 可以在目前使用者以外的使用者帳戶下，取得所安裝之產品實例的資訊。 適用于 Windows Installer 3.0 或更新版本。 |
| [**MsiGetUserInfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa)                         | 針對已安裝的產品傳回已註冊的使用者資訊。                                                                                                                                                                     |



 

## <a name="product-query-functions"></a>產品查詢函數



| Name                                                               | 描述                                                                            |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta)                           | 開啟要與存取資料庫的函數搭配使用的產品。                    |
| [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea)                           | 開啟要與存取資料庫的函式搭配使用的封裝。                    |
| [**MsiOpenPackageEx**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa)                       | 開啟要與存取資料庫的函式搭配使用的封裝。                    |
| [**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda)               | 檢查產品是否以較高的許可權安裝。                      |
| [**MsiGetProductInfoFromScript**](/windows/desktop/api/Msi/nf-msi-msigetproductinfofromscripta) | 傳回安裝程式指令檔的產品資訊。                              |
| [**MsiGetProductProperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya)             | 抓取產品資料庫中的屬性。                                          |
| [**MsiGetShortcutTarget**](/windows/desktop/api/Msi/nf-msi-msigetshortcuttargeta)               | 檢查快捷方式，並傳回其產品、功能名稱和元件（如果有的話）。 |
| [**MsiGetFeatureInfo**](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa)                     | 傳回功能的描述性資訊。                                         |
| [**MsiVerifyPackage**](/windows/desktop/api/Msi/nf-msi-msiverifypackagea)                       | 確認指定的檔案是安裝套件。                             |



 

## <a name="patching-functions"></a>修補函式



| Name                                                                   | 描述                                                                                                                                                        |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)                                 | 叫用安裝並套用修補套件。                                                                                                               |
| [**MsiEnumPatches**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)                    | 傳回套用至產品的每個修補程式的 GUID，以及適用于產品的每個修補程式的轉換清單。                                  |
| [**MsiGetPatchInfo**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoa)                             | 傳回修補程式的相關資訊。                                                                                                                                 |
| [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)                           | 從產品卸載修補程式。 適用于 Windows Installer 3.0。                                                                                             |
| [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea)         | 判斷一組修補程式和產品的最佳應用程式順序。 適用于 Windows Installer 3.0。                                                     |
| [**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa)             | 將一或多個修補程式套用至產品。 適用于 Windows Installer 3.0。                                                                                       |
| [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)                           | 列舉針對特定內容中的產品套用的所有修補程式，或在所有內容中套用的所有修補程式。 適用于 Windows Installer 3.0。                                   |
| [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista)                     | 當提供 .msp 檔的清單時，此函式會抓取相容修補程式可更新的檔案清單。 適用于 Windows Installer 4.0。 |
| [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)                         | 查詢指定產品之指定修補程式的相關資訊。 適用于 Windows Installer 3.0。                                     |
| [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)               | 從修補程式中解壓縮資訊。 適用于 Windows Installer 3.0。                                                                                             |
| [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) | 決定更新產品或產品集所需的最佳修補集。 適用于 Windows Installer 3.0。                                            |



 

## <a name="file-query-functions"></a>檔案查詢函數



| Name                                                                     | 描述                                                                                                 |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha)                                 | 取得檔案的路徑，並傳回該檔案的128位雜湊。                                           |
| [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa) | 採用經過數位簽署的檔案路徑，並傳回檔案的簽署者憑證和雜湊。 |
| [**MsiGetFileVersion**](/windows/desktop/api/Msi/nf-msi-msigetfileversiona)                           | 傳回版本字串和語言字串。                                                             |



 

## <a name="transaction-management-functions"></a>交易管理函數



| Name                                               | 描述                                                                                                                                                                                         |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsiBeginTransaction**](/windows/desktop/api/Msi/nf-msi-msibegintransactiona) | 啟動多套件安裝的交易處理，並傳回交易的識別碼。 從 Windows Installer 4.5 開始，可以使用此函數。                    |
| [**MsiJoinTransaction**](/windows/desktop/api/Msi/nf-msi-msijointransaction)   | 要求 Windows Installer 讓目前的進程成為安裝多套件安裝的交易擁有者。 從 Windows Installer 4.5 開始，可以使用此函數。 |
| [**MsiEndTransaction**](/windows/desktop/api/Msi/nf-msi-msiendtransaction)     | 認可或復原屬於交易的所有安裝。 從 Windows Installer 4.5 開始，可以使用此函數。                                                          |



 

## <a name="database-functions"></a>資料庫函數

除了上表中所識別的 Windows Installer 函數以外，您還可以使用[資料庫](database-functions.md)函式區段中所述的資料庫存取函式，操作安裝資料庫中的資訊。

## <a name="installer-structures"></a>安裝程式結構

此外，安裝資料庫中的某些資訊是使用 [安裝程式結構](installer-structures.md) 一節中所述的結構來處理。

 

 




