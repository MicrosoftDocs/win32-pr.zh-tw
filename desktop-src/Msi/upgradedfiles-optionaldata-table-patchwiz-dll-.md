---
description: UpgradedFile \_ OptionalData 資料表包含有關已升級映射中特定檔案的資訊。 此資料表在修補程式建立資料庫中是選擇性的， ( pcp 檔案) 並由 UiCreatePatchPackageEx 函數使用。
ms.assetid: 8b96a83a-2bfa-47b7-bde0-896bdcc97d29
title: 'UpgradedFiles_OptionalData 資料表 (Patchwiz.dll) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2a648623e2a0cde11af34a3b948b4f2ac6fba59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194946"
---
# <a name="upgradedfiles_optionaldata-table-patchwizdll"></a>UpgradedFiles \_ OptionalData 資料表 (Patchwiz.dll) 

UpgradedFile \_ OptionalData 資料表包含有關已升級映射中特定檔案的資訊。 此資料表在修補程式建立資料庫中是選擇性的， ( pcp 檔案) 並由 [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) 函數使用。

UpgradedFile \_ OptionalData 資料表有下列資料行。



| Column                  | 類型    | 答案 | Nullable |
|-------------------------|---------|-----|----------|
| 已升級                | text    | Y   | N        |
| FTK                     | text    | Y   | N        |
| SymbolPaths             | text    |     | Y        |
| AllowIgnoreOnPatchError | 整數 |     | Y        |
| IncludeWholeFile        | 整數 |     | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>升級
</dt> <dd>

UpgradedImages 資料表的升級資料行的外鍵 [ (Patchwiz.dll) ](upgradedimages-table-patchwiz-dll-.md)。

</dd> <dt>

<span id="FTK"></span><span id="ftk"></span>FTK
</dt> <dd>

檔案資料表索引鍵。 已升級映射之 .msi 檔案的檔案 [資料表](file-table.md) 中的外鍵。 如果系列內的兩個或多個升級的映射具有相同的 FTK 值，則值必須參考相同的檔案。 多個升級映射所共用的檔案應該具有相同的 FTK，以將封包檔大小降到最低。

</dd> <dt>

<span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths
</dt> <dd>

此欄位中的值會加入至 [UpgradedImages 資料表 ](upgradedimages-table-patchwiz-dll-.md) 的 SymbolPaths 資料行中，以分號分隔的資料夾清單， (Patchwiz.dll 在產生修補程式時) ，而且可以用來新增特定檔案的符號檔。

</dd> <dt>

<span id="AllowIgnoreOnPatchError"></span><span id="allowignoreonpatcherror"></span><span id="ALLOWIGNOREONPATCHERROR"></span>AllowIgnoreOnPatchError
</dt> <dd>

設定為1，表示修補程式為不重要。 設定為0表示修補程式很重要。 如果 Windows Installer 在將此修補程式套用至 [FTK] 資料行中指定的檔案時發生問題，則此欄位中的值會決定錯誤訊息框是否包含 [ **略** 過] 按鈕，讓使用者能夠繼續進行修補程式。

</dd> <dt>

<span id="IncludeWholeFile"></span><span id="includewholefile"></span><span id="INCLUDEWHOLEFILE"></span>IncludeWholeFile
</dt> <dd>

如果應該安裝 FTK 資料行中指定的整個檔案，而不是建立二進位修補程式，請將設定為非零值。

</dd> </dl>

 

 



