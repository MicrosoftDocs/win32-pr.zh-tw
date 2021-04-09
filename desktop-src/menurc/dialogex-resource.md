---
title: DIALOGEX 資源
description: 定義對話方塊。 |DIALOGEX 資源
ms.assetid: 3ff28b68-e8b4-444d-8e26-5119ed30e44e
keywords:
- DIALOGEX 資源功能表與其他資源
topic_type:
- apiref
api_name:
- DIALOGEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbd55bfb06b678742aa5e356c9e62b14229aa8d3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104196054"
---
# <a name="dialogex-resource"></a>DIALOGEX 資源

定義對話方塊。 語句會定義畫面上對話方塊的位置和維度，以及對話方塊的樣式。 它也會定義下列各項：

-   對話方塊本身以及對話方塊內控制項的說明識別碼。
-   針對對話方塊本身以及對話方塊內的控制項，使用 [**EXSTYLE**](exstyle-statement.md) 語句。
-   要在對話方塊中使用之字型的字型粗細和斜體設定。
-   對話方塊內控制項的控制項特定資料。
-   使用 **BEDIT**、 **IEDIT** 和 **HEDIT** 預先定義的系統類別名稱。

``` syntax
nameID DIALOGEX x, y, width, height [ , helpID] [optional-statements]  {control-statements}
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

識別對話方塊的唯一名稱或唯一的16位不帶正負號的整數值。

</dd> <dt>

<span id="x"></span><span id="X"></span>*X*
</dt> <dd>

對話方塊左側畫面上的位置，以對話方塊單位表示。

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Y*
</dt> <dd>

對話方塊頂端畫面上的位置，以對話方塊單位表示。

</dd> <dt>

<span id="width"></span><span id="WIDTH"></span>*寬度*
</dt> <dd>

對話方塊的寬度（以對話方塊單位為單位）。

</dd> <dt>

<span id="height"></span><span id="HEIGHT"></span>*高度*
</dt> <dd>

對話方塊的高度，以對話方塊單位為單位。

</dd> <dt>

<span id="helpID"></span><span id="helpid"></span><span id="HELPID"></span>*h*
</dt> <dd>

數值運算式，指出在 [**WM \_**](../shell/wm-help.md) 說明處理期間用來識別對話方塊的識別碼。

</dd> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*選用語句*
</dt> <dd>

對話方塊的選項。 這可以是零或多個下列語句。



| 陳述式                                                         | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **標題** "*text*"                                              | 對話方塊的標題列（如果有的話）。 如需詳細資訊，請參閱 [**CAPTION 語句**](caption-statement.md)。                                                                                                                                                                                                                                                                                                                                                            |
| **特性** *dword*                                       | 資源工具所使用的使用者定義 **DWORD** 值。 系統不會使用這個值。 如需詳細資訊，請參閱 [**特性語句**](characteristics-statement.md)。                                                                                                                                                                                                                                                                                               |
| **類別**_類別_                                                  | 以雙引號括住的16位不帶正負號的整數或字串 ( ") ，以識別對話方塊的類別。 如需詳細資訊，請參閱 [**CLASS 語句**](class-statement.md)。                                                                                                                                                                                                                                                                                     |
| **EXSTYLE** = *擴充樣式*                                    | 對話方塊的擴充視窗樣式。 如需詳細資訊，請參閱 [**EXSTYLE 語句**](exstyle-statement.md)。                                                                                                                                                                                                                                                                                                                                                                    |
| **字型** *Dialog**、"* font-family"、*權數*、*斜體*、*字元集* | 字型的點大小和字型。 針對 *權數*，請使用 WinGDI 中定義的 **FW \_ \** _ 值。 若為 _italic *，請指定 TRUE 以使用斜體字型，否則為 FALSE。 若為 *字元集*，請使用 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)結構之 **lfCharSet** 成員中定義的值。 若要取得對話方塊的最終字型，應用程式應指定 *字元集* 以及其他字型屬性。 如需詳細資訊，請參閱 [**字型語句**](font-statement.md)。 |
| **語言***語言*、*語言*                            | 對話方塊的語言。 如需詳細資訊，請參閱 [**LANGUAGE 語句**](language-statement.md)。                                                                                                                                                                                                                                                                                                                                                                               |
| **功能表** *menuname*                                               | 要使用的功能表。 此值為功能表的名稱或其整數識別碼。 如需詳細資訊，請參閱 [**功能表語句**](menu-statement.md)。                                                                                                                                                                                                                                                                                                                             |
| **樣式***樣式*                                                | 對話方塊的樣式。 如需詳細資訊，請參閱 [**STYLE 語句**](style-statement.md)。                                                                                                                                                                                                                                                                                                                                                                                       |
| **版本** *dword*                                               | 使用者定義的 **DWORD** 值。 此語句適用于其他資源工具，而且系統不會使用此語句。 如需詳細資訊，請參閱 [**版本聲明**](version-statement.md)。                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

<span id="control-statements"></span><span id="CONTROL-STATEMENTS"></span>*control 語句*
</dt> <dd>

**DIALOGEX** 資源的主體是由任意數目的控制語句所組成。 控制語句有四個系列： [泛型]、[靜態]、[按鈕] 和 [編輯]。 如需詳細資訊，請參閱＜備註＞。

</dd> </dl>

此外，也支援某些屬性以提供回溯相容性。 如需詳細資訊，請參閱 [一般資源屬性](common-resource-attributes.md)。

## <a name="remarks"></a>備註

可能包含在 **DIALOGEX** 語句中任何數值運算式中的有效作業如下：

-   新增 ( ' + ' ) 
-   減去 ( '-' ) 
-   一元減號 ( '-' ) 
-   一元未 ( ' ~ ' ) 
-   和 ( ' & ' ) 
-   或 ( ' \| ' ) 

資源的主體是由泛型、靜態、按鈕和編輯控制語句所組成。 雖然這兩個語句系列都使用不同的語法來定義其控制項的特定功能，但它們全都共用定義位置、大小、擴充樣式、說明識別碼和控制項特定資料的一般語法。 如需詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。

### <a name="generic-control-statements"></a>泛型控制項語句

``` syntax
CONTROL controlText, id, className, style
```

<dl> <dt>

<span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*
</dt> <dd>

控制項的視窗文字。 如需詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。

</dd> <dt>

<span id="id"></span><span id="ID"></span>*Id*
</dt> <dd>

控制識別碼。 如需詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。

</dd> <dt>

<span id="className"></span><span id="classname"></span><span id="CLASSNAME"></span>*className*
</dt> <dd>

類別的名稱。 這可能是以雙引號括住的字串 ( ") 或下列其中一個預先定義的系統類別： **按鈕**、 **靜態**、 **編輯**、 **LISTBOX**、 **捲軸** 或 **COMBOBOX**。

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*風格*
</dt> <dd>

您可以將包含在 .rc 檔中的 include 新增至 .rc 檔，以使用在 Winuser 中定義的視窗樣式 (明確 **\_ \* *的 WS _、_* BS \_ \* *_、_* SS \_ \* *_、_* ES \_ \* *_、_* 磅 \_ \* *_、_* SBS \_ \* *_ 和 _* CBS \_ \*** 樣式值： `#include "winuser.h"`) 。 如需詳細資訊，請參閱 [視窗樣式](/windows/desktop/winmsg/window-styles)。

</dd> </dl>

### <a name="static-control-statements"></a>靜態控制語句

``` syntax
staticClass controlText, id
```

<dl> <dt>

<span id="staticClass"></span><span id="staticclass"></span><span id="STATICCLASS"></span>*staticClass*
</dt> <dd>

**LTEXT**、 **RTEXT** 或 **CTEXT**。

</dd> <dt>

<span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*
</dt> <dd>

控制項的視窗文字。 如需詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。

</dd> <dt>

<span id="id"></span><span id="ID"></span>*Id*
</dt> <dd>

控制識別碼。 如需詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。

</dd> </dl>

### <a name="button-control-statements"></a>Button 控制項語句

``` syntax
buttonClass controlText, id
```

<dl> <dt>

<span id="buttonClass"></span><span id="buttonclass"></span><span id="BUTTONCLASS"></span>*buttonClass*
</dt> <dd>

**AUTO3STATE**、 **AUTOCHECKBOX**、 **AUTORADIOBUTTON**、 **CHECKBOX**、 **PUSHBOX**、 **按鈕**、 **選項按鈕**、 **STATE3** 或 **USERBUTTON**。

</dd> <dt>

<span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*
</dt> <dd>

控制項的視窗文字。 如需詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。

</dd> <dt>

<span id="id"></span><span id="ID"></span>*Id*
</dt> <dd>

控制識別碼。 如需詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。

</dd> </dl>

### <a name="edit-control-statements"></a>編輯控制語句

``` syntax
editClass id
```

<dl> <dt>

<span id="editClass"></span><span id="editclass"></span><span id="EDITCLASS"></span>*editClass*
</dt> <dd>

**EDITTEXT**、 **BEDIT**、 **HEDIT** 或 **IEDIT**。

</dd> <dt>

<span id="id"></span><span id="ID"></span>*Id*
</dt> <dd>

控制識別碼。 如需詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。

</dd> </dl>

## <a name="see-also"></a>另請參閱

<dl> <dt>

[使用對話方塊](../dlgbox/using-dialog-boxes.md)
</dt> <dt>

[**加速器**](accelerators-resource.md)
</dt> <dt>

[**特徵**](characteristics-statement.md)
</dt> <dt>

[**控制**](control-control.md)
</dt> <dt>

[**CreateDialog**](/windows/win32/api/winuser/nf-winuser-createdialoga)
</dt> <dt>

[**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[**對話方塊**](/windows/win32/api/winuser/nf-winuser-dialogboxa)
</dt> <dt>

[**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[**語言**](language-statement.md)
</dt> <dt>

[**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> <dt>

[功能表](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[**版本**](version-statement.md)
</dt> </dl>

 

 
