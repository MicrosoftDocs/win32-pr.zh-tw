---
description: ModuleDependency 資料表會保留此合併模組正常運作所需的其他合併模組清單。
ms.assetid: 36418331-bec7-40c9-8fdf-fe4b958a1443
title: ModuleDependency 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08d527ba5874c8fffb0234dbf8f041f424b7bf9aecff5e8f29005324f2a17fdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118628580"
---
# <a name="moduledependency-table"></a>ModuleDependency 資料表

ModuleDependency 資料表會保留此合併模組正常運作所需的其他合併模組清單。 下表啟用合併或驗證工具，以確保所需的合併模組實際上包含在使用者的安裝程式資料庫中。 此工具會在安裝程式資料庫中，透過參考此資料表與 ModuleSignature 資料表的方式進行檢查。

ModuleDependency 資料表具有下列資料行。



| Column           | 類型                         | 答案 | Nullable |
|------------------|------------------------------|-----|----------|
| ModuleID         | [識別碼](identifier.md) | Y   | N        |
| ModuleLanguage   | [整數](integer.md)       | Y   | N        |
| RequiredID       | [識別碼](identifier.md) | Y   | N        |
| RequiredLanguage | [整數](integer.md)       | Y   | N        |
| RequiredVersion  | [版本](version.md)       |     | Y        |



 

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

<span id="RequiredID"></span><span id="requiredid"></span><span id="REQUIREDID"></span>RequiredID
</dt> <dd>

ModuleID 中 merge 模組所需之合併模組的識別碼。

</dd> <dt>

<span id="RequiredLanguage"></span><span id="requiredlanguage"></span><span id="REQUIREDLANGUAGE"></span>RequiredLanguage
</dt> <dd>

RequiredID 中合併模組的數位語言識別項。 RequiredLanguage 資料行可以指定單一語言的語言識別項，例如美國英文的1033，或指定語言群組的語言識別項，例如任何英文的9。 如果欄位包含群組語言識別項，則在該群組中具有語言代碼的任何合併模組都會滿足相依性。 如果 RequiredLanguage 設定為0，則任何填入其他需求的合併模組都會滿足相依性。

</dd> <dt>

<span id="RequiredVersion"></span><span id="requiredversion"></span><span id="REQUIREDVERSION"></span>RequiredVersion
</dt> <dd>

RequiredID 中的合併模組版本。 如果此欄位為 Null，任何版本都會填滿相依性。

</dd> </dl>

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE25](ice25.md)  
</dl>

 

 



