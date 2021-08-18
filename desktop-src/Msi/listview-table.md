---
description: Listview 的行不會被視為個別控制項，但它們是做為控制項的 listview 的一部分。 ListView 資料表會定義所有 listview 的值。
ms.assetid: 0da4eab9-cabc-4bcc-8267-4aa1cd79e78b
title: ListView 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a84ebab6c90486283c3dd8d4731cc0b7f3aff11a5459a0e93496bab83d7c277
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013076"
---
# <a name="listview-table"></a>ListView 資料表

Listview 的行不會被視為個別控制項，但它們是做為控制項的 listview 的一部分。 ListView 資料表會定義所有 listview 的值。

ListView 資料表具有下列資料行。



| Column   | 類型                         | 答案 | Nullable |
|----------|------------------------------|-----|----------|
| 屬性 | [識別碼](identifier.md) | Y   | N        |
| 單    | [整數](integer.md)       | Y   | N        |
| 值    | [格式 化](formatted.md)   | N   | N        |
| Text     | [格式 化](formatted.md)   | N   | Y        |
| 二 進 制\_ | [識別碼](identifier.md) | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>財產
</dt> <dd>

要系結至這個專案的命名屬性。 所有系結至相同屬性的專案都會變成相同 listview 的一部分。

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>以
</dt> <dd>

正整數，用來決定出現在單一 listview 清單中的專案順序。 整數不需要是連續的。 如果 listview 定義為已排序，則所有專案都應該有排序值。 如果 listview 定義為未排序，則會忽略此資料行。

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>價值
</dt> <dd>

與這個專案相關聯的值字串。 選取該行會將相關聯的屬性設定為此值。

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>文本
</dt> <dd>

要指派給專案的可見、可當地語系化文字。 如果遺漏此專案或整個資料行，則文字會預設為 [值] 中的對應專案。

</dd> <dt>

<span id="Binary_"></span><span id="binary_"></span><span id="BINARY_"></span>二 進 制\_
</dt> <dd>

圖示的影像資料。 這是 [二進位資料表](binary-table.md)的外鍵。

</dd> </dl>

## <a name="remarks"></a>備註

[**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)函式會在建立控制項時將值和文字欄位的內容格式化，因此可以包含 MsiFormatRecord 函數可以解讀的任何運算式。 只有在建立控制項時，才會進行格式化，而且如果在控制項的存留期間修改了包含在運算式中的屬性，則不會更新。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE32](ice32.md)  
</dl>

 

 



