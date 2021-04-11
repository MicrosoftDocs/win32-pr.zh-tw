---
description: DuplicateFile 資料表包含要複製的檔案清單，可能會複製到與原始檔案不同的目錄，或是與相同的目錄不同的名稱。 原始檔案必須是 InstallFiles 動作所安裝的檔案。
ms.assetid: 7fe1b52d-4b06-48cd-afe5-2bd5495bb55e
title: DuplicateFile 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 766f28b7984aedfc682a2bf23378d46ee0519c65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026881"
---
# <a name="duplicatefile-table"></a>DuplicateFile 資料表

DuplicateFile 資料表包含要複製的檔案清單，可能會複製到與原始檔案不同的目錄，或是與相同的目錄不同的名稱。 原始檔案必須是 [InstallFiles 動作](installfiles-action.md)所安裝的檔案。

DuplicateFile 資料表具有下列資料行。



| Column      | 類型                         | 答案 | Nullable |
|-------------|------------------------------|-----|----------|
| FileKey     | [識別碼](identifier.md) | Y   | N        |
| 元件\_ | [識別碼](identifier.md) | N   | N        |
| 檔案\_      | [識別碼](identifier.md) | N   | N        |
| DestName    | [檔案名稱](filename.md)     | N   | Y        |
| DestFolder  | [識別碼](identifier.md) | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey
</dt> <dd>

主要索引鍵、非當地語系化的 token，識別唯一的 DuplicateFile 記錄。

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_
</dt> <dd>

[元件資料表](component-table.md)第一個資料行的外部索引鍵。 如果未選取索引鍵所識別的元件來進行安裝或移除，則不會在此 DuplicateFile 記錄上採取任何動作。

</dd> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>檔\_
</dt> <dd>

代表要複製之原始檔案的檔案 [資料表](file-table.md) 中的外鍵。

</dd> <dt>

<span id="DestName"></span><span id="destname"></span><span id="DESTNAME"></span>DestName
</dt> <dd>

要提供給重複檔案的可當地語系化名稱。 如果這個欄位是空白的，則會為目的地檔案提供與原始檔案相同的名稱。

</dd> <dt>

<span id="DestFolder"></span><span id="destfolder"></span><span id="DESTFOLDER"></span>DestFolder
</dt> <dd>

屬性的名稱，這個屬性是複製複製之檔案的完整路徑。 如果這個目錄與包含原始檔案的目錄相同，且建議的重複檔案名稱與原始檔案相同，則不會進行任何動作。

</dd> </dl>

## <a name="remarks"></a>備註

資料表是由 [DuplicateFiles 動作](duplicatefiles-action.md) 和 [RemoveDuplicateFiles 動作](removeduplicatefiles-action.md)來處理。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE18](ice18.md)  
[ICE32](ice32.md)  
</dl>

 

 



