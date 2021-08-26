---
description: RemoveIniFile 資料表包含應用程式從 .ini 檔案中刪除所需的資訊。
ms.assetid: 702cf86e-02f4-4ea7-8573-b500ac550aae
title: RemoveIniFile 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6aca38f320a8cb548faf00d284cff4c934e127a44cbaf7ca5b96013fac80d63
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074578"
---
# <a name="removeinifile-table"></a>RemoveIniFile 資料表

RemoveIniFile 資料表包含應用程式從 .ini 檔案中刪除所需的資訊。

RemoveIniFile 資料表具有下列資料行。



| Column        | 類型                         | 答案 | Nullable |
|---------------|------------------------------|-----|----------|
| RemoveIniFile | [識別碼](identifier.md) | Y   | N        |
| FileName      | [FileName](text.md)         | N   | N        |
| DirProperty   | [識別碼](identifier.md) | N   | Y        |
| 區段       | [格式 化](formatted.md)   | N   | N        |
| 答案           | [格式 化](formatted.md)   | N   | N        |
| 值         | [格式 化](formatted.md)   | N   | Y        |
| 動作        | [整數](integer.md)       | N   | N        |
| 元件\_   | [識別碼](identifier.md) | N   | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="RemoveIniFile"></span><span id="removeinifile"></span><span id="REMOVEINIFILE"></span>RemoveIniFile
</dt> <dd>

此資料表的索引鍵。

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>檔案名
</dt> <dd>

要在其中刪除資訊的 .ini 檔案名。

</dd> <dt>

<span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty
</dt> <dd>

屬性的名稱，其值會假設解析為要移除之 .ini 檔案的資料夾完整路徑。 屬性可以是 [目錄資料表](directory-table.md)中目錄的名稱、 [AppSearch 資料表](appsearch-table.md)所設定的屬性，或是表示完整路徑的任何其他屬性。

</dd> <dt>

<span id="Section"></span><span id="section"></span><span id="SECTION"></span>部分
</dt> <dd>

可當地語系化的 .ini 檔案區段。

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>關鍵
</dt> <dd>

區段下的可當地語系化 .ini 檔案索引鍵。

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>價值
</dt> <dd>

要刪除的可當地語系化值。 當 Action 為4時，此值為必要項。

</dd> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>行動
</dt> <dd>

要進行的修改類型。



| 常數                         | 十六進位 | Decimal | 意義                          |
|----------------------------------|-------------|---------|----------------------------------|
| **msidbIniFileActionRemoveLine** | 0x002       | 2       | 刪除 .ini 專案。              |
| **msidbIniFileActionRemoveTag**  | 0x004       | 4       | 從 .ini 專案中刪除標記。 |



 

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_
</dt> <dd>

[元件資料表](component-table.md)的第一個資料行中的外部索引鍵，該元件會參考控制 .ini 值刪除的元件。

</dd> </dl>

## <a name="remarks"></a>備註

當已選取要安裝的對應元件時，就會刪除 .ini 檔案資訊，不論是在本機或從來源執行都是如此。

當 [RemoveIniValues 動作](removeinivalues-action.md) 執行時，就會參考此資料表。

如果目錄資料 \_ 行指定為 null，則 ini 檔案的位置會是預設 Windows ini 位置，也就是 Windows 目錄。

從區段移除最後一個值會刪除該區段。 除了移除所有的值以外，沒有其他方法可刪除整個區段。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE40](ice40.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 



