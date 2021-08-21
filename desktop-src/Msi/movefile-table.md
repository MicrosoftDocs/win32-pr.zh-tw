---
description: 此資料表包含要從指定的來原始目錄移動或複製到指定之目的地目錄的檔案清單。
ms.assetid: 9ba47bdc-90c8-444a-ba8b-71c723b54556
title: MoveFile 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49d90afe8a5fb950f2e6fdb96ba0f8af4f8969226a5dc219bc9cd0598481beb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945093"
---
# <a name="movefile-table"></a>MoveFile 資料表

此資料表包含要從指定的來原始目錄移動或複製到指定之目的地目錄的檔案清單。

MoveFile 資料表具有下列資料行。



| Column       | 類型                         | 答案 | Nullable |
|--------------|------------------------------|-----|----------|
| FileKey      | [識別碼](identifier.md) | Y   | N        |
| 元件\_  | [識別碼](identifier.md) | N   | N        |
| SourceName   | [Text](text.md)             | N   | Y        |
| DestName     | [檔案名稱](filename.md)     | N   | Y        |
| SourceFolder | [識別碼](identifier.md) | N   | Y        |
| DestFolder   | [識別碼](identifier.md) | N   | N        |
| 選項      | [整數](integer.md)       | N   | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey
</dt> <dd>

可唯一識別特定 MoveFile 記錄的主鍵。

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_
</dt> <dd>

[元件資料表](component-table.md)中的外部索引鍵。 如果未選取此索引鍵所參考的元件來進行安裝或移除，則不會在此 MoveFile 專案上採取任何動作。

</dd> <dt>

<span id="SourceName"></span><span id="sourcename"></span><span id="SOURCENAME"></span>SourceName
</dt> <dd>

此資料行包含要移動或複製之來源檔案的可當地語系化名稱。 此資料行可以保留空白。 請參閱 SourceFolder 資料行的描述。 此欄位必須包含長檔名，而且可能包含萬用字元 (\* 和？ ) 。

</dd> <dt>

<span id="DestName"></span><span id="destname"></span><span id="DESTNAME"></span>DestName
</dt> <dd>

此資料行包含在移動或複製原始檔案之後，提供給原始檔案的可當地語系化名稱。 如果這個欄位是空白的，則會將目的地檔案的名稱與來源檔案相同。

</dd> <dt>

<span id="SourceFolder"></span><span id="sourcefolder"></span><span id="SOURCEFOLDER"></span>SourceFolder
</dt> <dd>

此資料行包含屬性的名稱，這個屬性的值會解析為來原始目錄的完整路徑。 如果 [不完整] 資料行保留空白，則會假設 SourceFolder 資料行中命名的屬性包含原始程式檔本身的完整路徑 (包括檔案名) 。

</dd> <dt>

<span id="DestFolder"></span><span id="destfolder"></span><span id="DESTFOLDER"></span>DestFolder
</dt> <dd>

屬性的名稱，這個屬性的值會解析為目的地目錄的完整路徑。

</dd> <dt>

<span id="Options"></span><span id="options"></span><span id="OPTIONS"></span>選項
</dt> <dd>

指定操作模式的整數值。



| 常數                     | 十六進位 | Decimal | 意義               |
|------------------------------|-------------|---------|-----------------------|
| (無)                       | 0x000       | 0       | 複製來源檔案。 |
| **msidbMoveFileOptionsMove** | 0x001       | 1       | 移動原始檔。 |



 

</dd> </dl>

## <a name="remarks"></a>備註

如果在 \* MoveFile 資料表的 [未使用] 資料行中輸入 "" 萬用字元，並在 DestName 資料行中指定目的地檔案名，則所有移動或複製的檔案都會保留來源中的名稱。

此資料表是由 [MoveFiles 動作](movefiles-action.md)處理。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE18](ice18.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE85](ice85.md)  
</dl>

 

 



