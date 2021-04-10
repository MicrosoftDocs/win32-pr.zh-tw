---
description: 清單方塊的行不會被視為個別控制項，但它們是作為控制項的清單方塊的一部分。 ListBox 資料表會定義所有清單方塊的值。
ms.assetid: 1963adcf-f682-4371-ab44-f91e90105dc0
title: ListBox 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f60fb6ac48860c7893b0320b54e6e54dcf1691
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944532"
---
# <a name="listbox-table"></a>ListBox 資料表

清單方塊的行不會被視為個別控制項，但它們是作為控制項的清單方塊的一部分。 ListBox 資料表會定義所有清單方塊的值。

ListBox 資料表具有下列資料行。



| Column   | 類型                         | 答案 | Nullable |
|----------|------------------------------|-----|----------|
| 屬性 | [識別碼](identifier.md) | Y   | N        |
| 單    | [整數](integer.md)       | Y   | N        |
| 值    | [格式 化](formatted.md)   | N   | N        |
| Text     | [格式 化](formatted.md)   | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>財產
</dt> <dd>

要系結至這個專案的命名屬性。 所有系結至相同屬性的專案都會變成相同清單方塊的一部分。

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>以
</dt> <dd>

正整數，用來決定出現在單一清單方塊中的專案順序。 如果清單方塊定義為已排序，則所有專案都應該有 Order 值。 整數不需要是連續的。 如果清單方塊定義為未排序，則會忽略此資料行。

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>價值
</dt> <dd>

與這個專案相關聯的值字串。 選取該行會將相關聯的屬性設定為此值。

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>文本
</dt> <dd>

要指派給專案的可當地語系化、可見文字。 如果遺漏此專案或整個資料行，則文字會預設為 [值] 中的對應專案。

</dd> </dl>

## <a name="remarks"></a>備註

[**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)函式會在建立控制項時將值和文字欄位的內容格式化，因此可以包含 **MsiFormatRecord** 函數可以解讀的任何運算式。 只有在建立控制項時，才會進行格式化，而且如果在控制項的存留期間修改了包含在運算式中的屬性，則不會更新。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE20](ice20.md)  
[ICE46](ice46.md)  
</dl>

 

 



