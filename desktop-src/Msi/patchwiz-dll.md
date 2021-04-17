---
description: 若要產生修補程式套件，建議您使用修補程式建立工具，例如 Msimsp.exe 和 Patchwiz.dll。
ms.assetid: aca3bbd2-440a-405f-bddc-5f9cc831b811
title: Patchwiz.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6dc1135a9e2c09bb8a96e041f77bae39f0057ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195265"
---
# <a name="patchwizdll"></a>Patchwiz.dll

若要產生修補程式套件，建議您使用修補程式建立工具，例如 [Msimsp.exe](msimsp-exe.md) 和 Patchwiz.dll。 Patchwiz.dll 版本4.0 與使用舊版 Patchwiz.dll 撰寫的套件和修補程式相容。 Patchwiz.dll 工具僅適用于 [Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)。

Patchwiz.dll 4.0 版有一個新的函式（ [UiCreatePatchPackageEx (Patchwiz.dll) ](uicreatepatchpackageex--patchwiz-dll-.md)），可延伸 [UiCreatePatchPackage (Patchwiz.dll) ](uicreatepatchpackage-patchwiz-dll-.md)的功能。 這些函式會取得修補程式建立屬性檔 ( pcp 檔案) 並產生安裝 [程式修補套件](patch-packages.md)。

Pcp 檔案是二進位資料庫檔案，其格式與 Windows Installer 資料庫 ( .msi 檔案) 相同，但使用不同的資料庫架構。 因此，您可以使用安裝程式資料庫所使用的相同工具來撰寫 pcp 檔案。

您可以使用資料表編輯器（例如 [Orca.exe](orca-exe.md) ）來建立 pcp 檔案，並將資訊輸入 Windows Installer SDK 所提供的 pcp 資料庫 pcp。 如需詳細資訊，請參閱 [小型更新修補範例](a-small-update-patching-example.md)。

每個 pcp 檔案都需要下列資料庫資料表：

-   [屬性資料表 (Patchwiz.dll) ](properties-table-patchwiz-dll-.md)
-   [ImageFamilies 資料表 (Patchwiz.dll) ](imagefamilies-table-patchwiz-dll-.md)
-   [UpgradedImages 資料表 (Patchwiz.dll) ](upgradedimages-table-patchwiz-dll-.md)
-   [TargetImages 資料表 (Patchwiz.dll) ](targetimages-table-patchwiz-dll-.md)

下列資料庫資料表是選擇性的：

-   [UpgradedFiles \_ OptionalData 資料表 (Patchwiz.dll) ](upgradedfiles-optionaldata-table-patchwiz-dll-.md)
-   [FamilyFileRanges 資料表 (Patchwiz.dll) ](familyfileranges-table-patchwiz-dll-.md)
-   [TargetFiles \_ OptionalData 資料表 (Patchwiz.dll) ](targetfiles-optionaldata-table-patchwiz-dll-.md)
-   [ExternalFiles 資料表 (Patchwiz.dll) ](externalfiles-table-patchwiz-dll-.md)
-   [UpgradedFilesToIgnore 資料表 (Patchwiz.dll) ](upgradedfilestoignore-table-patchwiz-dll-.md)

在 pcp 檔案中，如果 MinimumRequiredMsiVersion 等於 [屬性](properties-table-patchwiz-dll-.md) 表中的300，則需要下表。

-   [PatchMetadata 資料表 (Patchwiz.dll) ](patchmetadata-table--patchwiz-dll-.md)

> [!Note]  
> 如果 MinimumRequiredMsiVersion 不等於300，則資料表是選擇性的。

 

使用 Windows Installer 3.0 發行的 Patchwiz.dll 版本可以自動產生修補程式順序資訊，並將其新增至新修補程式的 [MsiPatchSequence 資料表](msipatchsequence-table.md) 。 您可以使用 [PatchSequence 資料表](patchsequence-table--patchwiz-dll-.md) ，以手動方式將修補程式排序資訊新增至 MsiPatchSequence 資料表。 如需詳細資訊，請參閱 [產生修補程式順序資訊](generating-patch-sequence-information---patchwiz-dll-.md)。

從 Patchwiz.dll 版本2.0 開始，您可以使用 [修補資訊快取 (Patchwiz.dll) ](patch-information-caching-patchwiz-dll-.md)來提高後續修補建立的速度。

針對您的目標和升級映射二進位檔使用公用符號，可減少大約一半的二進位修補程式大小。 如需詳細資訊，請參閱 [使用符號來減少二進位修補程式大小](using-symbols-to-reduce-binary-patch-size.md)。

您可以指定要保留目標檔案的特定區域，使其在修補期間遭到覆寫，並保留這些區域中的資訊。 如需詳細資訊，請參閱 [修補檔案的選取區域](patching-selected-regions-of-a-file.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[已發行的版本、工具和可轉散發套件](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



