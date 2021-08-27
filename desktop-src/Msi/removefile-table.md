---
description: RemoveFile 資料表包含 RemoveFiles 動作要移除的檔案清單。 將此資料表的 FileName 資料行設定為 Null，可支援移除空的資料夾。
ms.assetid: 8b3cb0e3-ccc0-4030-8f57-aa124c3b5588
title: RemoveFile 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12cf63e9b7616eb033a696da2ad29cb4310e6dc0dc56279ef465c3c549cb5437
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082598"
---
# <a name="removefile-table"></a>RemoveFile 資料表

RemoveFile 資料表包含 [RemoveFiles 動作](removefiles-action.md)要移除的檔案清單。 將此資料表的 FileName 資料行設定為 Null，可支援移除空的資料夾。

RemoveFile 資料表具有下列資料行。



| Column      | 類型                                     | 答案 | Nullable |
|-------------|------------------------------------------|-----|----------|
| FileKey     | [識別碼](identifier.md)             | Y   | N        |
| 元件\_ | [識別碼](identifier.md)             | N   | N        |
| FileName    | [WildCardFilename](wildcardfilename.md) | N   | Y        |
| DirProperty | [識別碼](identifier.md)             | N   | N        |
| InstallMode | [整數](integer.md)                   | N   | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey
</dt> <dd>

用來識別這個特定資料表專案的主要索引鍵。

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_
</dt> <dd>

[元件資料表](component-table.md)的第一個資料行的外部索引鍵。 此欄位會參考控制要移除之檔案的元件。

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>檔案名
</dt> <dd>

此資料行包含要移除之檔案的可當地語系化名稱。 如果這個資料行是 null，則如果指定的資料夾是空的，則會將它移除。 所有符合萬用字元的檔案都將從指定的目錄中移除。

</dd> <dt>

<span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty
</dt> <dd>

屬性的名稱，其值會被假設解析為要移除之檔案資料夾的完整路徑。 屬性可以是 [目錄資料表](directory-table.md)中目錄的名稱、 [AppSearch 資料表](appsearch-table.md)所設定的屬性，或是表示完整路徑的任何其他屬性。

</dd> <dt>

<span id="InstallMode"></span><span id="installmode"></span><span id="INSTALLMODE"></span>InstallMode
</dt> <dd>

必須是下列其中一個值。



| 常數                                | 十六進位 | Decimal | 描述                                                                                                   |
|-----------------------------------------|-------------|---------|---------------------------------------------------------------------------------------------------------------|
| **msidbRemoveFileInstallModeOnInstall** | 0x001       | 1       | 只有在 (msiInstallStateLocal 或 msiInstallStateSource) 安裝相關聯的元件時，才移除。 |
| **msidbRemoveFileInstallModeOnRemove**  | 0x002       | 2       | 只有在 (msiInstallStateAbsent) 移除相關聯的元件時，才移除。                           |
| **msidbRemoveFileInstallModeOnBoth**    | 0x003       | 3       | 在上述任一情況下移除。                                                                          |



 

</dd> </dl>

## <a name="remarks"></a>備註

此資料表中的檔案參考是由 [RemoveFiles 動作](removefiles-action.md)處理。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE18](ice18.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE64](ice64.md)  
</dl>

 

 



