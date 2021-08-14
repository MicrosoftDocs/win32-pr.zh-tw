---
description: IniLocator 資料表會保存使用 .ini 檔案搜尋檔案或目錄，或搜尋特定 .ini 專案本身所需的資訊。 .ini 檔案必須存在於預設的 Microsoft Windows 目錄中。
ms.assetid: 5a3c6077-34ef-48c8-b4e6-ecb1deb40f96
title: IniLocator 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5fae106340a953c59358c7c4108991d1510d49ea6d8940bcef72c538b7165ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946538"
---
# <a name="inilocator-table"></a>IniLocator 資料表

IniLocator 資料表會保存使用 .ini 檔案搜尋檔案或目錄，或搜尋特定 .ini 專案本身所需的資訊。 .ini 檔案必須存在於預設的 Microsoft Windows 目錄中。

IniLocator 資料表具有下列資料行。



| Column      | 類型                         | 答案 | Nullable |
|-------------|------------------------------|-----|----------|
| 簽名\_ | [識別碼](identifier.md) | Y   | N        |
| FileName    | [FileName](text.md)         | N   | N        |
| 區段     | [Text](text.md)             | N   | N        |
| 答案         | [Text](text.md)             | N   | N        |
| 欄位       | [整數](integer.md)       | N   | Y        |
| 類型        | [整數](integer.md)       | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>簽名\_
</dt> <dd>

簽章 [資料表](signature-table.md)的第一個資料行中的外部索引鍵。 簽章 \_ 代表唯一的簽章，而且也是在簽章資料表的第一個資料行中的外部索引鍵。 如果簽章資料表中有這個簽章，則搜尋是用於檔案。 如果簽章資料表中沒有此索引鍵，且 Type 資料行的值是 **msidbLocatorTypeRawValue**，則搜尋是針對 IniLocator 資料表所指定的 .ini 專案。 否則搜尋是針對 IniLocator 資料表所指定的目錄。

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>檔案名
</dt> <dd>

.ini 的檔案名。

</dd> <dt>

<span id="Section"></span><span id="section"></span><span id="SECTION"></span>部分
</dt> <dd>

.ini 檔案中的區段名稱。

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>關鍵
</dt> <dd>

區段內的索引鍵值。

</dd> <dt>

<span id="Field"></span><span id="field"></span><span id="FIELD"></span>領域
</dt> <dd>

.ini 行中的欄位。 如果欄位為 Null 或0，則會讀取整行。 此值必須是非負數。

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>類型
</dt> <dd>

值，這個值會判斷 .ini 值為檔案位置、目錄位置或原始 .ini 值。

下表列出有效的值。 如果不存在，則類型會設定為1。



| 常數                      | 十六進位 | Decimal | Description           |
|-------------------------------|-------------|---------|-----------------------|
| **msidbLocatorTypeDirectory** | 0x000       | 0       | 目錄位置。 |
| **msidbLocatorTypeFileName**  | 0x001       | 1       | 檔案位置。      |
| **msidbLocatorTypeRawValue**  | 0x002       | 2       | 原始的 .ini 值。     |



 

</dd> </dl>

## <a name="remarks"></a>備註

此資料表與 [AppSearch 資料表](appsearch-table.md)搭配使用。

此資料表的資料行通常不會當地語系化。 如果作者決定搜尋多種語言的產品，則每種語言的表格中都可以有個別的專案。

進度顯示或記錄的相關當地語系化文字會在 [ActionText 資料表](actiontext-table.md)中指定。

請參閱 [搜尋現有的應用程式、檔案、登錄專案或 .ini 檔專案](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 



