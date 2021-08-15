---
description: 標準合併模組中需要有下列資料表。
ms.assetid: 2af6cea0-6d93-4aa5-a708-d305f11986ef
title: 合併模組資料庫資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 201b4af776ae0b68fd4330dca8240390e5731950fdaba5a734f48d887db5be84
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580638"
---
# <a name="merge-module-database-tables"></a>合併模組資料庫資料表

標準合併模組中需要有下列資料表。



| 資料表名稱                                       | 註解                                                                                          |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [元件](component-table.md)                 | 需要 ()                                                                                        |
| [目錄](directory-table.md)                 | 需要 ()                                                                                        |
| [FeatureComponents](featurecomponents-table.md) | 需要 ()                                                                                        |
| [檔案](file-table.md)                           | 需要 ()                                                                                        |
| [ModuleSignature](modulesignature-table.md)     |  (需要合併到安裝程式資料庫) 。 列出識別合併模組的資訊。 |
| [ModuleComponents](modulecomponents-table.md)   |  (需要合併到安裝程式資料庫) 。 列出合併模組中的所有元件。     |



 

下列資料表只會出現在合併模組或其他安裝程式資料庫（已與合併模組合併）中。



| 資料表名稱                                     | 註解                                                                                                     |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [ModuleDependency](moduledependency-table.md) | 合併到安裝程式資料庫。 列出此合併模組所需的其他合併模組。                |
| [ModuleExclusion](moduleexclusion-table.md)   | 合併到安裝程式資料庫。 列出與此合併模組不相容的其他合併模組。 |



 

下列 ModuleSequence 資料表只會出現在合併模組中。



| 資料表名稱                                                             | 註解                                                                                   |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [ModuleAdminUISequence](moduleadminuisequence-table.md)               | 將動作合併至 [AdminUISequence 資料表](adminuisequence-table.md)。               |
| [ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md)     | 將動作合併至 [AdminExecuteSequence 資料表](adminexecutesequence-table.md)。     |
| [ModuleAdvtUISequence](moduleadvtuisequence-table.md)                 | 請勿使用此資料表。 如需詳細資訊，請參閱 [AdvtUISequence 資料表](advtuisequence-table.md)。 |
| [ModuleAdvtExecuteSequence](moduleadvtexecutesequence-table.md)       | 將動作合併至 [AdvtExecuteSequence 資料表](advtexecutesequence-table.md)。       |
| [ModuleIgnoreTable](moduleignoretable-table.md)                       | 列出模組中未合併到 .msi 檔案中的資料表。                        |
| [ModuleInstallUISequence](moduleinstalluisequence-table.md)           | 將動作合併至 [InstallUISequence 資料表](installuisequence-table.md)。           |
| [ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md) | 將動作合併至 [InstallExecuteSequence 資料表](installexecutesequence-table.md)。 |



 

每個可設定的合併模組都需要下列資料表。 需要 Mergemod.dll 2.0 或更新版本，才能建立可設定的合併模組。 如需詳細資訊，請參閱可設定的 [合併模組](configurable-merge-modules.md)。



| 資料表名稱                                                 | 註解                                                                                                                                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ModuleSubstitution 資料表](modulesubstitution-table.md)   |  (需要) 此資料表不會合並到目標安裝資料庫中。 指定目標資料庫中可設定的欄位，並為每個欄位的設定提供範本。 |
| [ModuleConfiguration 資料表](moduleconfiguration-table.md) |  (需要) 此資料表不會合並到目標安裝資料庫中。 識別模組的可設定屬性。                                                                 |



 

下列安裝程式資料表不能出現在標準合併模組中。

-   [BBControl](bbcontrol-table.md)
-   [廣告 牌](billboard-table.md)
-   [CCPSearch](ccpsearch-table.md)
-   [錯誤](error-table.md)
-   [功能](feature-table.md)
-   [LaunchCondition 資料表](launchcondition-table.md)
-   [媒體](media-table.md)
-   [修補](patch-table.md)
-   [升級](upgrade-table.md)

下列安裝程式資料表在合併模組中是選擇性的。

-   [ActionText](actiontext-table.md)
-   [AdminExecuteSequence](adminexecutesequence-table.md)
-   [AdminUISequence](adminuisequence-table.md)
-   [AdvtExecuteSequence](advtexecutesequence-table.md)
-   [AdvtUISequence](advtuisequence-table.md)
-   [AppId](appid-table.md)
-   [AppSearch](appsearch-table.md)
-   [BindImage](bindimage-table.md)
-   [CheckBox](checkbox-table.md)
-   [類別](class-table.md)
-   [ComboBox](combobox-table.md)
-   [CompLocator](complocator-table.md)
-   [控制](control-table.md)
-   [ControlCondition](controlcondition-table.md)
-   [CreateFolder](createfolder-table.md)
-   [CustomAction](customaction-table.md)
-   [對話方塊](dialog-table.md)
-   [DrLocator](drlocator-table.md)
-   [DuplicateFile](duplicatefile-table.md)
-   [環境](environment-table.md)
-   [EventMapping](eventmapping-table.md)
-   [延伸模組](extension-table.md)
-   [Font](font-table.md)
-   [圖示](icon-table.md)
-   [IniFile](inifile-table.md)
-   [IniLocator](inilocator-table.md)
-   [InstallExecuteSequence](installexecutesequence-table.md)
-   [InstallUISequence](installuisequence-table.md)
-   [ListBox](listbox-table.md)
-   [ListView](listview-table.md)
-   [MIME](mime-table.md)
-   [MoveFile](movefile-table.md)
-   [ODBCAttribute](odbcattribute-table.md)
-   [ODBCDataSource](odbcdatasource-table.md)
-   [ODBCDriver](odbcdriver-table.md)
-   [ODBCSourceAttribute](odbcsourceattribute-table.md)
-   [ODBCTranslator](odbctranslator-table.md)
-   [ProgID 資料表](progid-table.md)
-   [屬性](property-table.md)
-   [PublishComponent](publishcomponent-table.md)
-   [RadioButton](radiobutton-table.md)
-   [登錄資料表](registry-table.md)
-   [RegLocator](reglocator-table.md)
-   [RemoveFile](removefile-table.md)
-   [RemoveIniFile](removeinifile-table.md)
-   [RemoveRegistry](removeregistry-table.md)
-   [ReserveCost](reservecost-table.md)
-   [SelfReg](selfreg-table.md)
-   [ServiceControl](servicecontrol-table.md)
-   [ServiceInstall](serviceinstall-table.md)
-   [快速鍵](shortcut-table.md)
-   [簽名](signature-table.md)
-   [文本](textstyle-table.md)
-   [類型](typelib-table.md)
-   [UIText](uitext-table.md)
-   [動詞命令](verb-table.md)

 

 



