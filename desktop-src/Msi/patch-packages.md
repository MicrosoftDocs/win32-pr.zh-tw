---
description: Windows Installer 修補程式 ( .msp 檔) 是用來將更新傳遞至 Windows Installer 應用程式的檔案。
ms.assetid: f59736d7-0b5a-466c-ab60-f210ccccb07f
title: 修補套件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56b4bb5b7e182c8118f5a40c45be440784b92099
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692483"
---
# <a name="patch-packages"></a>修補套件

Windows Installer 修補程式 ( .msp 檔) 是用來將更新傳遞至 Windows Installer 應用程式的檔案。 修補程式是獨立套件，其中包含更新應用程式所需的所有資訊。  ( .msp 檔) 的修補套件可能會比整個更新應用程式的 Windows Installer 套件 () .msi 檔案更小。 如需將較小的更新傳遞給應用程式的詳細資訊，請參閱 [減少修補程式大小](reducing-patch-size.md)。

修補套件包含應用程式的實際更新，並描述應用程式可接收修補程式的版本。 修補套裝程式含至少兩個資料庫轉換。 一個轉換會更新應用程式安裝資料庫中的資訊。 另一個轉換會新增安裝程式用來修補檔案的資訊。 安裝程式會使用轉換所提供的資訊來套用修補檔案，這些檔案儲存在修補程式套件的封包檔資料流程中。 Patch 封裝沒有像安裝封裝 ( .msi 檔案的資料庫。 ) 

從 Windows Installer 版本3.0 開始，修補封裝可以包含描述修補程式順序的資訊，相對於 [MsiPatchSequence](msipatchsequence-table.md) 資料表中的其他更新以及 [MsiPatchMetadata](msipatchmetadata-table.md) 資料表中的其他描述性資訊。

使用者可以從網路管理映射安裝應用程式和更新。 雖然修補套件可以套用至系統管理安裝，但提供更新的建議方法是讓使用者安裝原始的應用程式，然後將修補程式套用到其電腦上的本機應用程式實例。 這樣可讓使用者與系統管理映射保持同步。 如果將修補程式套用至系統管理安裝，該系統管理安裝的所有用戶端都必須重新安裝，並重新安裝應用程式才能接收更新。 在使用者 recaches 並重新安裝之前，使用者無法視需要安裝，也無法從修補的系統管理安裝修複安裝。

從 Windows Installer 3.0 開始，非系統管理員可以在修補程式核准為受系統管理員信任之後，將修補程式套用到每位使用者管理的應用程式。 如需如何進行此作業的詳細資訊，請參閱 [修補 Per-User 受控應用程式](patching-per-user-managed-applications.md)。 另一種方法是使用最低許可權的使用者帳戶修補。

> [!Note]  
> 如果已設定 [AllowLockdownPatch](allowlockdownpatch.md) 原則，非系統管理員的使用者就可以在以較高的許可權執行安裝時，將修補程式套用至現有的應用程式。 不建議使用此方法，因為它可讓未受信任的修補程式套用至可使用較高許可權執行的應用程式。

 

修補程式套件由下列元件組成。 如需修補套件之結構的詳細資訊，請參閱 [建立修補程式套件](creating-a-patch-package.md)。

## <a name="summary-information-stream"></a>摘要資訊串流

Patch 封裝的摘要資訊資料流程會提供有關修補的身分識別和用途的資訊。

摘要資訊串流最少包含下列各項：

-   可唯一識別修補程式的 GUID。 此修補程式的 GUID 會附加至先前修補程式所取代的 Guid 清單。
-   此修補程式之有效目標的產品代碼清單（以分號分隔）。
-   以分號分隔的轉換 substorage 名稱清單（以其處理的順序排列）。
-   此修補程式的來源清單（以分號分隔）。

## <a name="transform-substorage"></a>轉換 Substorage

修補套件包含可新增或移除檔案、登錄專案、使用者介面和自訂的轉換。 轉換會以 substorages 的形式包含在套件中。 修補套件包含每個目標資料庫的兩個轉換。 其中一個轉換是安裝資料庫的實際更新，並從安裝封裝的原始和更新映射之間的差異產生。 其他轉換會將專案新增至 [Patch](patch-table.md)、 [PatchPackage](patchpackage-table.md)、 [Media](media-table.md)、 [InstallExecuteSequence](installexecutesequence-table.md)和 [AdminExecuteSequence](adminexecutesequence-table.md) 資料表。 Substorage 中的資訊會將它系結至特定的 [**UpgradeCode**](upgradecode.md)、 [**ProductCode**](productcode.md)、 [**ProductVersion**](productversion.md)和 [**ProductLanguage**](productlanguage.md)。 可以套用至多個目標的 patch 封裝包含一對以上的轉換。

## <a name="cabinet-file-stream"></a>封包檔串流

修補程式中包含的封包檔資料流程可以包含這些類型的檔案：

-   修補檔案，其中包含將舊版本檔案變更為新版本所需的資訊。 單一修補檔案可用來更新一或多個舊版本的檔案。
-   新增至應用程式的其他檔案不存在於舊版本中。
-   整個取代檔案。 在很罕見的情況下，檔案的新版本小於更新舊版本檔案所需的修補程式時，新的檔案可以包含在完整的檔案中。 這些是安裝在舊版本上的新檔案。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立修補程式套件](creating-a-patch-package.md)
</dt> </dl>

 

 



