---
description: ModuleExclusion 資料表會保留相同安裝程式資料庫中不相容的其他合併模組清單。
ms.assetid: c28d9afa-152c-43b5-9892-7a38fae8c593
title: ModuleExclusion 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8fb4cc136937d5a01bd16a42c138532dd524ee1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104386265"
---
# <a name="moduleexclusion-table"></a>ModuleExclusion 資料表

ModuleExclusion 資料表會保留相同安裝程式資料庫中不相容的其他合併模組清單。 此資料表會啟用合併或驗證工具，以檢查衝突的合併模組是否未在使用者的安裝程式資料庫中合併。 此工具會在安裝程式資料庫中使用 ModuleSignature 資料表來交叉參考此資料表，以進行檢查。

ModuleExclusion 資料表具有下列資料行。



| Column             | 類型                         | 答案 | Nullable |
|--------------------|------------------------------|-----|----------|
| ModuleID           | [識別碼](identifier.md) | Y   | N        |
| ModuleLanguage     | [整數](integer.md)       | Y   | N        |
| ExcludedID         | [識別碼](identifier.md) | Y   | N        |
| ExcludedLanguage   | [整數](integer.md)       | Y   | N        |
| ExcludedMinVersion | [版本](version.md)       |     | Y        |
| ExcludedMaxVersion | [版本](version.md)       |     | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID
</dt> <dd>

合併模組的識別碼。 這是 [ModuleSignature 資料表](modulesignature-table.md)中的外鍵。

</dd> <dt>

<span id="ModuleLanguage"></span><span id="modulelanguage"></span><span id="MODULELANGUAGE"></span>ModuleLanguage
</dt> <dd>

ModuleID 中合併模組的十進位語言識別項。 這是 [ModuleSignature 資料表](modulesignature-table.md)中的外鍵。

</dd> <dt>

<span id="ExcludedID"></span><span id="excludedid"></span><span id="EXCLUDEDID"></span>ExcludedID
</dt> <dd>

已排除合併模組的識別碼。

</dd> <dt>

<span id="ExcludedLanguage"></span><span id="excludedlanguage"></span><span id="EXCLUDEDLANGUAGE"></span>ExcludedLanguage
</dt> <dd>

ExcludedID 中合併模組的數位語言識別項。 ExcludedLanguage 資料行可以指定單一語言的語言識別項，例如美國英文的1033，或指定語言群組的語言識別項，例如任何英文的9。 ExcludedLanguage 資料行可接受負的語言識別項。 ExcludedLanguage 資料行中值的意義如下所示。



| ExcludedLanguage | 意義                                                              |
|------------------|----------------------------------------------------------------------|
| > 0           | 排除 ExcludedLanguage 所指定的語言識別項。              |
| = 0              | 排除無語言識別項。                                             |
| < 0           | 除了 ExcludedLanguage 指定的語言識別項之外，請排除所有語言識別項。 |



 

</dd> <dt>

<span id="ExcludedMinVersion"></span><span id="excludedminversion"></span><span id="EXCLUDEDMINVERSION"></span>ExcludedMinVersion
</dt> <dd>

從範圍中排除的最小版本。 如果 ExcludedMinVersion 欄位為 Null，則會排除 ExcludedMaxVersion 之前的所有版本。 如果 ExcludedMinVersion 和 ExcludedMaxVersion 都是 Null，則不會根據版本進行排除。

</dd> <dt>

<span id="ExcludedMaxVersion"></span><span id="excludedmaxversion"></span><span id="EXCLUDEDMAXVERSION"></span>ExcludedMaxVersion
</dt> <dd>

從範圍中排除的最大版本。 如果 ExcludedMaxVersion 欄位為 Null，則會排除 ExcludedMinVersion 之後的所有版本。 如果 ExcludedMinVersion 和 ExcludedMaxVersion 都是 Null，則不會根據版本進行排除。

</dd> </dl>

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE25](ice25.md)  
</dl>

 

 



