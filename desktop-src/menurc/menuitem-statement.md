---
title: MENUITEM 語句
description: 定義功能表項目。
ms.assetid: b154211a-5267-4dcf-9e70-ac36671d10d3
keywords:
- MENUITEM 語句功能表和其他資源
topic_type:
- apiref
api_name:
- MENUITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da2051b326b2f2f37c9e24e03bcb5e5116cf290a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106967653"
---
# <a name="menuitem-statement"></a>MENUITEM 語句

定義功能表項目。

``` syntax
MENUITEM text, result, [optionlist]  
MENUITEM SEPARATOR
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*文本*
</dt> <dd>

功能表項目的名稱。

字串可以包含 escape 字元 **\\ t** **\\ 和。** **\\ T** 字元會在字串中插入索引標籤，用來對齊資料行中的文字。 只有在功能表中（而不是在功能表列中）使用 Tab 字元。  (如需功能表的詳細資訊，請參閱快顯 [**資源**](popup-resource.md)。 ) **\\ 一個** 字元，將緊接在上方的所有文字排在功能表列或快顯功能表上。

</dd> <dt>

<span id="result"></span><span id="RESULT"></span>*結果*
</dt> <dd>

數位，指定當使用者選取功能表項目時所產生的結果。 此參數會使用整數值。 功能表項目結果一律為整數;當使用者按一下功能表項目名稱時，結果會傳送到擁有功能表的視窗。

</dd> <dt>

<span id="optionlist"></span><span id="OPTIONLIST"></span>*optionlist*
</dt> <dd>

功能表項目的外觀。 這個選擇性參數會採用下列一或多個重新定義的功能表選項，並以逗號或空格分隔。



| 選項           | Description                                                                                                                                                           |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **檢查**      | 功能表項目旁邊有核取記號。                                                                                                                                |
| **灰色**       | 功能表項目一開始為非使用中，並顯示在功能表中的灰色或功能表文字色彩的淺色陰影。 此選項不能與 **非** 使用中的選項搭配使用。 |
| **説明**         | 識別說明專案。 此選項不會影響功能表項目的外觀。                                                                                 |
| **無效**     | 功能表項目隨即顯示，但無法選取。 此選項不能與 **灰色** 選項搭配使用。                                                              |
| **MENUBARBREAK** | 與 **MENUBREAK** 相同，不同之處在于針對快顯功能表，它會將新的資料行與舊的資料行與垂直線分開。                                             |
| **MENUBREAK**    | 將功能表項目放在靜態功能表列專案的新行上。 在功能表中，它會將功能表項目放在新的資料行中，而且資料行之間不會有分隔線。           |



 

</dd> <dt>

<span id="MENUITEM_SEPARATOR"></span><span id="menuitem_separator"></span>**MENUITEM 分隔符號**
</dt> <dd>

**Menuitem** 語句的 **menuitem 分隔符號** 形式會建立非作用中的功能表項目，做為功能表上兩個現用功能表項目之間的分隔線。

</dd> </dl>

## <a name="examples"></a>範例

下列範例將示範 **menuitem** 和 **menuitem 分隔符號** 語句的用法：

``` syntax
MENUITEM "&Roman", 206, CHECKED, GRAYED
MENUITEM SEPARATOR
MENUITEM "&Blackletter", 301
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**功能表**](menu-resource.md)
</dt> <dt>

[**彈出**](popup-resource.md)
</dt> </dl>

 

 




