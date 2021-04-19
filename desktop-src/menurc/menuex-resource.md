---
title: MENUEX 資源
description: 定義功能表資源的內容。 |MENUEX 資源
ms.assetid: a83e1e78-2af4-4257-906e-7eb6d98bcbc8
keywords:
- MENUEX 資源功能表與其他資源
topic_type:
- apiref
api_name:
- MENUEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ed379fb97d2795a166571fb48cde2c233021a33
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106979866"
---
# <a name="menuex-resource"></a>MENUEX 資源

定義功能表資源的內容。 功能表資源是一組資訊，可定義應用程式功能表的外觀和功能。 功能表是一種特殊的輸入工具，可讓使用者選取命令，並從功能表項目清單中開啟子功能表。 它也會定義下列各項：

-   功能表上的說明識別碼。
-   功能表上的識別碼。
-   使用 **MFT \_ \** _ 類型旗標和 _*MFS \_ \**_ 狀態旗標。 如需這些旗標的詳細資訊，請參閱 [_ *MENUITEMINFO* *](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)結構。

``` syntax
menuID MENUEX{ [{[MENUITEM itemText [,[id][, [type][, state]]]] | 
    POPUP itemText [,[id][, [type][, [state][, helpID]]]] { popupBody } } . . .]}
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="MENUITEM"></span><span id="menuitem"></span>[**MENUITEM**](menuitem-statement.md)
</dt> <dd>

定義功能表項目。

<dl> <dt>

<span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*itemText*
</dt> <dd>

字串，包含功能表項目的文字。 如需詳細資訊，請參閱 [**MENUITEM**](menuitem-statement.md)。

</dd> <dt>

<span id="id"></span><span id="ID"></span>*Id*
</dt> <dd>

指出功能表項目識別碼的數值運算式。

</dd> <dt>

<span id="type"></span><span id="TYPE"></span>*類型*
</dt> <dd>

數值運算式，指出要使用預先定義的 MFT 類型值之功能表項目的類型 \_ \* ，在 .rc 檔中加入下列語句：`#include "winuser.h"`

</dd> <dt>

<span id="state"></span><span id="STATE"></span>*狀態*
</dt> <dd>

數值運算式，指出要使用預先定義的 MFS 狀態值之功能表項目的狀態 \_ \* ，在您的中加入下列語句。RC 檔案：`#include "winuser.h"`

</dd> </dl> </dd> <dt>

<span id="POPUP"></span><span id="popup"></span>[**彈出**](popup-resource.md)
</dt> <dd>

定義具有與其相關聯之子功能表的功能表項目。

<dl> <dt>

<span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*itemText*
</dt> <dd>

字串，包含功能表項目的文字。

</dd> <dt>

<span id="id"></span><span id="ID"></span>*Id*
</dt> <dd>

指出功能表項目識別碼的數值運算式。

</dd> <dt>

<span id="type"></span><span id="TYPE"></span>*類型*
</dt> <dd>

數值運算式，指出要使用預先定義的 MFT 類型值之功能表項目的類型 \_ \* ，請在您的中包含下列語句。RC 檔案：`#include "winuser.h"`

</dd> <dt>

<span id="state"></span><span id="STATE"></span>*狀態*
</dt> <dd>

數值運算式，指出要使用預先定義的 MFS 狀態值之功能表項目的狀態 \_ \* ，在 .rc 檔中加入下列語句：`#include "winuser.h"`

</dd> <dt>

<span id="helpID"></span><span id="helpid"></span><span id="HELPID"></span>*h*
</dt> <dd>

數值運算式，指出在 [**WM \_**](../shell/wm-help.md) 說明處理期間用來識別功能表的識別碼。

</dd> </dl> </dd> <dt>

<span id="popupBody"></span><span id="popupbody"></span><span id="POPUPBODY"></span>*popupBody*
</dt> <dd>

包含 [**MENUITEM**](menuitem-statement.md) 和 [**POPUP**](popup-resource.md) 語句的任何組合。

</dd> </dl>

此外，也支援某些屬性以提供回溯相容性。 如需詳細資訊，請參閱 [一般資源屬性](common-resource-attributes.md)。

## <a name="remarks"></a>備註

可包含在 **MENUEX** 語句中任何數值運算式內的有效算術和布耳運算如下所示：

-   新增 ( ' + ' ) 
-   減去 ( '-' ) 
-   一元減號 ( '-' ) 
-   一元未 ( ' ~ ' ) 
-   和 ( ' & ' ) 
-   或 ( ' \| ' ) 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[使用功能表](./using-menus.md)
</dt> <dt>

[**加速器**](accelerators-resource.md)
</dt> <dt>

[**特徵**](characteristics-statement.md)
</dt> <dt>

[**對話 框**](dialog-resource.md)
</dt> <dt>

[**語言**](language-statement.md)
</dt> <dt>

[**功能表**](menu-resource.md)
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

 

 
