---
description: TypeLib 資料表包含需要放在類型程式庫登錄註冊中的資訊。
ms.assetid: 86b827ed-e707-4627-9488-78eafb444d32
title: TypeLib 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 862bc37e325f8c615e8158cfa431c927841f6b33c403c804726cea8fee6f0469
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499998"
---
# <a name="typelib-table"></a>TypeLib 資料表

TypeLib 資料表包含需要放在類型程式庫登錄註冊中的資訊。

TypeLib 資料表具有下列資料行。



| Column      | 類型                               | 答案 | Nullable |
|-------------|------------------------------------|-----|----------|
| LibID       | [GUID](guid.md)                   | Y   | N        |
| 語言    | [整數](integer.md)             | Y   | N        |
| 元件\_ | [識別碼](identifier.md)       | Y   | N        |
| 版本     | [DoubleInteger](doubleinteger.md) | N   | Y        |
| 描述 | [Text](text.md)                   | N   | Y        |
| 目錄\_ | [識別碼](identifier.md)       | N   | Y        |
| 特徵\_   | [識別碼](identifier.md)       | N   | N        |
| Cost        | [DoubleInteger](doubleinteger.md) | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="LibID"></span><span id="libid"></span><span id="LIBID"></span>LibID
</dt> <dd>

識別程式庫的 GUID。

</dd> <dt>

<span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>語言
</dt> <dd>

類型程式庫的語言。 此值必須是非負數。

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_
</dt> <dd>

在 [元件資料表](component-table.md)的第一個資料行中的外部索引鍵。 此資料行會識別屬於功能的元件， \_ 其金鑰檔是要註冊的類型程式庫。

</dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>版本
</dt> <dd>

這是程式庫的版本。 主要和次要版本會以四個位元組整數值進行編碼。 次要版本是在較低的八位。 主要版本是在中間的十六位。

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>描述
</dt> <dd>

程式庫的可當地語系化描述。

</dd> <dt>

<span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>目錄\_
</dt> <dd>

在 [目錄資料表](directory-table.md)的第一個資料行中的外部索引鍵。 這個資料行會識別類型程式庫的說明路徑。 在廣告期間會忽略此資料行。

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>特徵\_
</dt> <dd>

在 [功能資料表](feature-table.md)的第一個資料行中的外部索引鍵。 這個資料行會指定必須安裝才能操作類型程式庫的功能。

</dd> <dt>

<span id="Cost"></span><span id="cost"></span><span id="COST"></span>成本
</dt> <dd>

與類型程式庫註冊相關聯的成本（以位元組為單位）。 這必須是非負數或 null。

</dd> </dl>

## <a name="remarks"></a>備註

當執行 [RegisterTypeLibraries 動作](registertypelibraries-action.md) 或 [UnregisterTypeLibraries 動作](unregistertypelibraries-action.md) 時，就會參考此資料表。

安裝程式會將所有類型程式庫註冊資訊寫入 HKEY \_ 本機 \_ 電腦 (HKLM) 登錄位置。 即使是針對個別使用者安裝也是如此。 類型程式庫無法在 (HKCU) 的每個使用者位置註冊。

使用 TypeLib 資料表時，強烈建議使用安裝套件作者。 相反地，他們應該使用 [登錄表來](registry-table.md) 註冊類型程式庫。 避免自行註冊的原因包括：

-   如果使用 TypeLib 資料表的安裝失敗，而且必須回復，則回復可能不會將電腦還原到復原之前存在的相同狀態。 復原之前註冊的類型程式庫可能不會在復原後註冊。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE19](ice19.md)  
[ICE32](ice32.md)  
</dl>

 

 



