---
description: 核取方塊表格會列出核取方塊的值。
ms.assetid: 6881f358-74af-4160-ac69-36e848865ac0
title: 核取方塊表格
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 848769f9430681a8c37de0afd8d9d1fa8abfee2f833798ecbdc5271535f79da4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649868"
---
# <a name="checkbox-table"></a>核取方塊表格

核取方塊表格會列出核取方塊的值。

CheckBox 資料表具有下列資料行。



| Column   | 類型                         | 答案 | Nullable |
|----------|------------------------------|-----|----------|
| 屬性 | [識別碼](identifier.md) | Y   | N        |
| 值    | [格式 化](formatted.md)   | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>財產
</dt> <dd>

要系結至這個專案的命名屬性。

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>價值
</dt> <dd>

與這個專案相關聯的值字串。

</dd> </dl>

## <a name="remarks"></a>備註

如果選取此核取方塊，則對應的屬性會設定為指定的值。 如果未指定任何值，或此資料表不存在，則在選取核取方塊時，屬性會設定為其原始值。 如果原始值為 null，則屬性會設定為 "1"。

當建立控制項時， [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) 函式會格式化 Value 資料行的內容。 因此，它可以包含 **MsiFormatRecord** 函數可解讀的任何運算式。 只有在建立控制項時，才會格式化 Value 資料行，而且如果在控制項的存留期內修改了包含在運算式中的屬性，則不會更新此資料行。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
</dl>

 

 



