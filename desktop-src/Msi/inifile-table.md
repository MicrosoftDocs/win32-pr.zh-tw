---
description: IniFile 資料表包含應用程式在 .ini 檔中所需設定的 .ini 資訊。
ms.assetid: fdb1a627-da6b-4da1-87a7-7f1c94d3836e
title: IniFile 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4cd12c02fa0123ac9e1a763b4e725681e6c6b1d51a331a1efea9916b5ac4cbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946565"
---
# <a name="inifile-table"></a>IniFile 資料表

IniFile 資料表包含應用程式在 .ini 檔中所需設定的 .ini 資訊。

IniFile 資料表具有下列資料行。



| Column      | 類型                         | 答案 | Nullable |
|-------------|------------------------------|-----|----------|
| IniFile     | [識別碼](identifier.md) | Y   | N        |
| FileName    | [FileName](text.md)         | N   | N        |
| DirProperty | [識別碼](identifier.md) | N   | Y        |
| 區段     | [格式 化](formatted.md)   | N   | N        |
| 答案         | [格式 化](formatted.md)   | N   | N        |
| 值       | [格式 化](formatted.md)   | N   | N        |
| 動作      | [整數](integer.md)       | N   | N        |
| 元件\_ | [識別碼](identifier.md) | N   | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="IniFile"></span><span id="inifile"></span><span id="INIFILE"></span>IniFile
</dt> <dd>

此資料表的索引鍵。

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>檔案名
</dt> <dd>

要在其中寫入資訊的 .ini 檔案名的可當地語系化名稱。

</dd> <dt>

<span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty
</dt> <dd>

屬性的名稱，這個屬性的值會解析為包含 .ini 檔案之資料夾的完整路徑。 屬性可以是 [目錄資料表](directory-table.md)中目錄的名稱、 [AppSearch 資料表](appsearch-table.md)所設定的屬性，或是表示完整路徑的任何其他屬性。 如果此欄位保留空白，則會在具有 [**WindowsFolder**](windowsfolder.md) 屬性所指定完整路徑的資料夾中建立 .ini 檔案。

</dd> <dt>

<span id="Section"></span><span id="section"></span><span id="SECTION"></span>部分
</dt> <dd>

可當地語系化的 .ini 檔案區段。

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>關鍵
</dt> <dd>

區段內的可當地語系化 .ini 檔案索引鍵。

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>價值
</dt> <dd>

要寫入的可當地語系化值。

</dd> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>行動
</dt> <dd>

要進行的修改類型。



| 常數                         | 十六進位 | Decimal | 修改                                                                     |
|----------------------------------|-------------|---------|----------------------------------------------------------------------------------|
| **msidbIniFileActionAddLine**    | 0x000       | 0       | 建立或更新 .ini 專案。                                                 |
| **msidbIniFileActionCreateLine** | 0x001       | 1       | 只有在專案不存在時，才會建立 .ini 專案。                   |
| **msidbIniFileActionAddTag**     | 0x003       | 3       | 建立新的專案，或將新的逗號分隔值附加至現有的專案。 |



 

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_
</dt> <dd>

在 [元件資料表](component-table.md) 的第一個資料行中，外部索引鍵參考控制 .ini 值安裝的元件。

</dd> </dl>

## <a name="remarks"></a>備註

當對應的元件已選取要安裝為本機或從來源執行時，就會寫出 .ini 的檔案資訊。

當執行 [WriteIniValues 動作](writeinivalues-action.md) 或 [RemoveIniValues 動作](removeinivalues-action.md) 時，就會參考此資料表。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
[ICE88](ice88.md)  
[ICE91](ice91.md)  
</dl>

 

 



