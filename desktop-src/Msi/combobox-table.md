---
description: 下拉式方塊的行不會被視為個別控制項;它們是做為控制項的單一下拉式方塊的一部分。 下表列出每個下拉式方塊的值。
ms.assetid: 1d3566ac-e95d-48ed-bce4-fb4604d5f762
title: ComboBox 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e209ac8a7c27c36fd5c1bbd3c97822617c48f5c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979945"
---
# <a name="combobox-table"></a>ComboBox 資料表

下拉式方塊的行不會被視為個別控制項;它們是做為控制項的單一下拉式方塊的一部分。 下表列出每個下拉式方塊的值。

ComboBox 資料表具有下列資料行。



| Column   | 類型                         | 答案 | Nullable |
|----------|------------------------------|-----|----------|
| 屬性 | [識別碼](identifier.md) | Y   | N        |
| 單    | [整數](integer.md)       | Y   | N        |
| 值    | [格式 化](formatted.md)   | N   | N        |
| Text     | [Text](text.md)             | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>財產
</dt> <dd>

要系結至這個專案的命名屬性。 系結至相同屬性的所有專案都會變成相同下拉式方塊的一部分。

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>以
</dt> <dd>

正整數，用來決定出現在單一下拉式方塊清單中的專案順序。 整數不需要是連續的。 如果下拉式方塊定義為已排序，則所有專案都應該有 Order 值。 如果下拉式列示方塊定義為未排序，則會忽略此資料行。

僅限正數。

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>價值
</dt> <dd>

與這個專案相關聯的值字串。 選取此下拉式方塊行，就會將屬性) 中指定的相關屬性 (設定為此值。

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>文本
</dt> <dd>

要指派給專案的可見、可當地語系化文字。 如果遺漏此專案或整個資料行，則文字會預設為 [值] 中的專案。

</dd> </dl>

## <a name="remarks"></a>備註

[**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)函式會在建立控制項時將值和文字欄位的內容格式化，因此可以包含 **MsiFormatRecord** 函數可以解讀的任何運算式。 只有在建立控制項時，才會進行格式化，而且如果在控制項的存留期內修改了包含在運算式中的屬性，則不會更新。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE46](ice46.md)  
</dl>

 

 



