---
description: PublishComponent 資料表會將元件資料表中所列的元件與限定詞文字字串和分類識別碼 GUID 建立關聯。
ms.assetid: 4a6be647-3e73-47a1-acfa-7d6d0a2fb2f4
title: PublishComponent 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c0abd7567e8327aa36a120fd5a13115cb191e1660566e9d480446295dca53cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118376381"
---
# <a name="publishcomponent-table"></a>PublishComponent 資料表

PublishComponent 資料表會將 [元件資料表](component-table.md) 中所列的元件與限定詞文字字串和分類識別碼 GUID 建立關聯。 具有以這種方式群組在一起之平行功能的元件，稱為合格元件。 請參閱 [合格元件](qualified-components.md)。 這會在參考元件時，為安裝程式提供單一層級間接取值的方法。 請參閱 [使用限定的元件](using-qualified-components.md)。

PublishComponent 資料表具有下列資料行。



| Column      | 類型                         | 答案 | Nullable |
|-------------|------------------------------|-----|----------|
| ComponentId | [GUID](guid.md)             | Y   | N        |
| Qualifier   | [Text](text.md)             | Y   | N        |
| 元件\_ | [識別碼](identifier.md) | Y   | N        |
| AppData     | [Text](text.md)             | N   | Y        |
| 特徵\_   | [識別碼](identifier.md) | N   | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>ComponentId
</dt> <dd>

字串 [GUID](guid.md) ，表示正在群組在一起的元件類別。 請注意，這個資料行的標題會誤導。 這是限定元件類別的 GUID，而且與 [元件資料表](component-table.md)的 [元件] 資料行中顯示的 guid 不同。 這裡是指提供元件功能給外部用戶端的伺服器，而不是元件本身。

</dd> <dt>

<span id="Qualifier"></span><span id="qualifier"></span><span id="QUALIFIER"></span>限定 符
</dt> <dd>

符合 [元件] 資料行中之值的文字字串。 辨識符號是用來區別相同元件的多個表單，例如以多種語言所執行的元件。 這些是 [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)所傳回的辨識符號文字字串。

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_
</dt> <dd>

在 [元件資料表](component-table.md)的第一個資料行中的外部索引鍵。 此識別碼會參考元件資料表中的限定元件記錄。

</dd> <dt>

<span id="AppData"></span><span id="appdata"></span><span id="APPDATA"></span>AppData
</dt> <dd>

描述此記錄之限定元件的選擇性可當地語系化文字。 此字串通常是由應用程式進行剖析，並且可以向使用者顯示。 它應該描述限定的元件。 您可以使用 [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)來取出。

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>特徵\_
</dt> <dd>

在 [功能資料表](feature-table.md)的第一個資料行中的外部索引鍵。 這是使用此合格元件的功能。

</dd> </dl>

## <a name="remarks"></a>備註

當執行 [PublishComponents 動作](publishcomponents-action.md) 或 [UnpublishComponents 動作](unpublishcomponents-action.md) 時，就會參考此資料表。

請注意，此資料表的名稱會誤導。 撰寫公告不需要此資料表。 請參閱 [元件資料表](component-table.md) 和 [功能表](feature-table.md) 的屬性資料行，以取得如何設定要公告的元件安裝狀態的相關資訊。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE19](ice19.md)  
[ICE22](ice22.md)  
[ICE32](ice32.md)  
</dl>

 

 



