---
title: POPUP 資源
description: 定義可以包含功能表項目和子功能表的功能表項目。
ms.assetid: afca21c7-605e-4354-b6ec-576b81389b69
keywords:
- 快顯視窗資源功能表與其他資源
topic_type:
- apiref
api_name:
- POPUP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f134b2d5801bc5003be6f45b42d13f1668c2e684b5f63fe0aed1f2c9c0400860
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952338"
---
# <a name="popup-resource"></a>POPUP 資源

定義可以包含功能表項目和子功能表的功能表項目。

``` syntax
POPUP text, [optionlist] {item-definitions ...}
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*文本*
</dt> <dd>

包含功能表名稱的字串。 此字串必須用雙引號括住 (**"**) 。

</dd> <dt>

<span id="optionlist"></span><span id="OPTIONLIST"></span>*optionlist*
</dt> <dd>

此參數會指定已重新定義的功能表選項，以指定功能表項目的外觀。 這個選擇性參數可以是下列其中一項或多項。



| 選項           | 描述                                                                                                                                                           |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **檢查**      | 功能表項目旁邊有核取記號。 最上層功能表的此選項無效。                                                                                 |
| **灰色**       | 功能表項目一開始為非使用中，並顯示在功能表中的灰色或功能表文字色彩的淺色陰影。 此選項不能與 **非** 使用中的選項搭配使用。 |
| **説明**         | 識別說明專案。 功能表項目放在功能表列上最右邊的位置。                                                                            |
| **無效**     | 功能表項目隨即顯示，但無法選取。 此選項不能與 **灰色** 選項搭配使用。                                                              |
| **MENUBARBREAK** | 與 **MENUBREAK** 相同，不同之處在于針對快顯功能表，它會將新的資料行與舊的資料行與垂直線分開。                                             |
| **MENUBREAK**    | 將功能表項目放在靜態功能表列專案的新行上。 在功能表中，它會將功能表項目放在新的資料行中，而且資料行之間不會有分隔線。           |



 

</dd> </dl>

此外，也支援某些屬性以提供回溯相容性。 如需詳細資訊，請參閱 [一般資源屬性](common-resource-attributes.md)。

## <a name="examples"></a>範例

下列範例示範如何使用 **POPUP** 語句：

``` syntax
chem MENU
{
    POPUP "&Elements"
    {
         MENUITEM "&Oxygen", 200
         MENUITEM "&Carbon", 201, CHECKED
         MENUITEM "&Hydrogen", 202
         MENUITEM SEPARATOR
         MENUITEM "&Sulfur", 203
         MENUITEM "Ch&lorine", 204
    } 
    POPUP "&Compounds"
    {
         POPUP "&Sugars"
         {
            MENUITEM "&Glucose", 301
            MENUITEM "&Sucrose", 302, CHECKED
            MENUITEM "&Lactose", 303, MENUBREAK
            MENUITEM "&Fructose", 304
         }
         POPUP "&Acids"
         {
              "&Hydrochloric", 401
              "&Sulfuric", 402
         }
    }
}
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**功能表**](menu-resource.md)
</dt> <dt>

[**MENUITEM**](menuitem-statement.md)
</dt> </dl>

 

 




