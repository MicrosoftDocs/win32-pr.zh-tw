---
title: 功能表資源
description: 定義功能表資源的內容。 |功能表資源
ms.assetid: fcb420b6-d42e-4044-89ee-028eed1f21ee
keywords:
- 功能表資源功能表與其他資源
topic_type:
- apiref
api_name:
- MENU
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c2b73afb5ef0547cbbccd8e5fdd87d7581edcaf19d5d73bc49ea3151166d882
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119601938"
---
# <a name="menu-resource"></a>功能表資源

定義功能表資源的內容。 功能表資源是一組資訊，可定義應用程式功能表的外觀和功能。 功能表是一種特殊的輸入工具，可讓使用者選取命令，並從功能表項目清單中開啟子功能表。

``` syntax
menuID MENU  [optional-statements]  {item-definitions ... }
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="menuID"></span><span id="menuid"></span><span id="MENUID"></span>*menuID*
</dt> <dd>

識別功能表的編號。 此值為1到65535範圍內的唯一字串或唯一的16位不帶正負號的整數值。

</dd> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*選用語句*
</dt> <dd>

這個參數可以是下列其中零個語句。



| 陳述式                                                        | 描述                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**特性**](characteristics-statement.md) *dword*     | 有關可供讀取和寫入資源檔的工具使用之資源的使用者定義資訊。 如需詳細資訊，請參閱 [**特性**](characteristics-statement.md)。 |
| [**語言**](language-statement.md)*語言*、*語言* | 資源的語言。 如需詳細資訊，請參閱 [**語言**](language-statement.md)。                                                                                            |
| [**版本**](version-statement.md) *dword*                     | 資源的使用者定義版本號碼，可供讀取和寫入資源檔的工具使用。 如需詳細資訊，請參閱 [**版本**](version-statement.md)。              |



 

</dd> </dl>

此外，也支援某些屬性以提供回溯相容性。 如需詳細資訊，請參閱 [一般資源屬性](common-resource-attributes.md)。

## <a name="examples"></a>範例

以下是完整 **功能表** 語句的範例：

``` syntax
sample MENU
{
     MENUITEM "&Soup", 100
     MENUITEM "S&alad", 101
     POPUP "&Entree"
     {
          MENUITEM "&Fish", 200
          MENUITEM "&Chicken", 201, CHECKED
          POPUP "&Beef"
          {
               MENUITEM "&Steak", 301
               MENUITEM "&Prime Rib", 302
          }
     }
     MENUITEM "&Dessert", 103
}
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[使用功能表](./using-menus.md)
</dt> <dt>

[**加速器**](accelerators-resource.md)
</dt> <dt>

[**特徵**](characteristics-statement.md)
</dt> <dt>

[**語言**](language-statement.md)
</dt> <dt>

[**MENUEX**](menuex-resource.md)
</dt> <dt>

[**MENUITEM**](menuitem-statement.md)
</dt> <dt>

[**彈出**](popup-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[**版本**](version-statement.md)
</dt> </dl>

 

 
