---
description: 若要重現範例修補程式套件，您需要能夠建立和編輯 Windows Installer 修補套件的軟體工具。
ms.assetid: 0653d8f6-89b0-4c56-ae51-3c7cb7df2909
title: 建立修補程式建立屬性檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50873fd508aa9f31435bd401284d38d13310991e150b28f4e24e5ec27f505dc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118379403"
---
# <a name="creating-a-patch-creation-properties-file"></a>建立修補程式建立屬性檔

若要重現範例修補程式套件，您需要能夠建立和編輯 Windows Installer 修補套件的軟體工具。 您可以從獨立軟體廠商取得數個修補套件建立工具。 下列各節所討論的範例會使用名為 Orca 的 Windows Installer 資料庫編輯器來撰寫修補程式建立屬性檔 (. pcp 延伸) 。 pcp 檔案可與公用程式[Msimsp.exe](msimsp-exe.md)和[Patchwiz.dll](patchwiz-dll.md)一起使用，以產生 Windows Installer 修補套件 ( .msp 延伸) 。 [Windows Installer 開發人員的 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中會提供 Orca、Msimsp.exe 和 Patchwiz.dll。

SDK 也會提供空白的 patch 建立屬性檔 pcp。 製作 pcp 的複本，並重新命名此複製 MNP2000. pcp。 使用 Orca 或其他資料庫編輯器，在 MNP2000. pcp 的 Properties 資料表中輸入下列資料。 Properties 資料表包含 patch 封裝的全域設定。

[Properties 資料表](properties-table-patchwiz-dll-.md)



| Name                               | 值                                  |
|------------------------------------|----------------------------------------|
| AllowProductCodeMismatches         | 1                                      |
| AllowProductVersionMajorMismatches | 1                                      |
| ApiPatchingSymbolFlags             | 0x00000000                             |
| DontRemoveTempFolderWhenFinished   | 1                                      |
| IncludeWholeFilesOnly              | 0                                      |
| ListOfPatchGUIDsToReplace          |                                        |
| ListOfTargetProductCodes           | \*                                     |
| PatchGUID                          | {5406B219-A1AC-4BC4-8695-72292C8195AC} |
| PatchOutputPath                    | c： \\ .msp 輸出                         |
| PatchSourceList                    | PatchSourceList                        |



 

使用資料庫編輯器，將下列資料輸入 MNP2000. pcp 的 ImageFamilies 資料表中。 ImageFamilies 資料表包含修補期間要新增至 [媒體資料表](media-table.md) 的資訊。

[ImageFamilies 資料表](imagefamilies-table-patchwiz-dll-.md)



| 系列  | MediaSrcPropName | MediaDiskId | FileSequenceStart | DiskPrompt | VolumeLabel |
|---------|------------------|-------------|-------------------|------------|-------------|
| MNPapps | MNPSrcPropName   | 2           | 1000              |            |             |



 

將下列資料輸入 MNP2000. pcp 的 UpgradedImages 資料表中。 UpgradedImages 資料表包含您在 [規劃小型更新修補程式](planning-a-small-update-patch.md)時所建立的升級映射相關資訊。

[UpgradedImages 資料表](upgradedimages-table-patchwiz-dll-.md)



| 已升級   | MsiPath                                           | PatchMsiPath | SymbolPaths | 系列  |
|------------|---------------------------------------------------|--------------|-------------|---------|
| 已 \_ 修正的 MNP | C： \\ Note \_ Installer \\ 修補程式 \\ 升級 \\MNP2000.msi |              |             | MNPapps |



 

將下列資料輸入 MNP2000. pcp 的 TargetImages 資料表中。 TargetImages 資料表包含目標影像的相關資訊。

[TargetImages 資料表](targetimages-table-patchwiz-dll-.md)



| 目標     | MsiPath                                         | SymbolPaths | 已升級   | 單 | ProductValidateFlags | IgnoreMissingSrcFiles |
|------------|-------------------------------------------------|-------------|------------|-------|----------------------|-----------------------|
| MNP \_ 錯誤 | C： \\ Note \_ Installer \\ 修補 \\ 目標 \\MNP2000.msi |             | 已 \_ 修正的 MNP | 1     |                      | 0                     |



 

針對範例修補程式套件，請將下列資料表保留在 MNP2000 中。 pcp 空白。

[UpgradedFiles \_ OptionalData 資料表](upgradedfiles-optionaldata-table-patchwiz-dll-.md)

[FamilyFileRanges 資料表](familyfileranges-table-patchwiz-dll-.md)

[TargetFiles \_ OptionalData 資料表](targetfiles-optionaldata-table-patchwiz-dll-.md)

[ExternalFiles 資料表](externalfiles-table-patchwiz-dll-.md)

[UpgradedFilesToIgnore 資料表](upgradedfilestoignore-table-patchwiz-dll-.md)

[繼續](generating-a-patch-package.md)

 

 



