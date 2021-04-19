---
title: 對話方塊資源
description: 定義對話方塊。 |對話方塊資源
ms.assetid: d166fb7d-0fe5-4e48-a545-19acc0ff80f1
keywords:
- 對話方塊資源功能表與其他資源
topic_type:
- apiref
api_name:
- DIALOG
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc7a1aef314406340c42c6a4aca40b76f91ac353
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106997335"
---
# <a name="dialog-resource"></a>對話方塊資源

定義對話方塊。 語句會定義畫面上對話方塊的位置和維度，以及對話方塊的樣式。

> [!Note]  
> **對話方塊** 是過時的資源識別碼。 新的應用程式應該使用 [**DIALOGEX**](dialogex-resource.md)。

 

``` syntax
nameID DIALOG x, y, width, height  [optional-statements] {control-statement  . . . }
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

識別對話方塊的唯一名稱或唯一的16位不帶正負號的整數值。

</dd> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*選用語句*
</dt> <dd>

對話方塊的選項。 這可以是零或多個下列語句。



| 陳述式                                                        | 描述                                                                                                                                                                                  |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**標題**](caption-statement.md) "*text*"                    | 對話方塊的標題列（如果有的話）。 如需詳細資訊，請參閱 [**標題**](caption-statement.md)。                                                                             |
| [**特性**](characteristics-statement.md) *dword*     | 資源工具所使用的使用者定義 **DWORD** 值。 系統不會使用這個值。 如需詳細資訊，請參閱 [**特性**](characteristics-statement.md)。                |
| [**類別**](class-statement.md)*類別*                         | 以雙引號括住的16位不帶正負號的整數或字串 ( ") ，以識別對話方塊的類別。 如需詳細資訊，請參閱 [**類別**](class-statement.md)。      |
| **EXSTYLE =** *擴充樣式*                                   | 對話方塊的擴充視窗樣式。 如需詳細資訊，請參閱 [**EXSTYLE**](exstyle-statement.md)。                                                                                     |
| **字型** *dialog*、 *字型*                                 | 字型的點大小和字型。 如需詳細資訊，請參閱 [**字型**](font-statement.md)。                                                                                              |
| [**語言**](language-statement.md)*語言*、*語言* | 對話方塊的語言。 如需詳細資訊，請參閱 [**語言**](language-statement.md)。                                                                                                |
| **功能表** *menuname*                                              | 要使用的功能表。 此值為功能表的名稱或其整數識別碼。                                                                                                        |
| [**樣式**](style-statement.md)*樣式*                        | 對話方塊的樣式。 如需詳細資訊，請參閱 [**樣式**](style-statement.md)。                                                                                                        |
| [**版本**](version-statement.md) *dword*                     | 使用者定義的 **DWORD** 值。 此語句適用于其他資源工具，而且系統不會使用此語句。 如需詳細資訊，請參閱 [**版本**](version-statement.md)。 |



 

</dd> </dl>

此外，也支援某些屬性以提供回溯相容性。 如需詳細資訊，請參閱 [一般資源屬性](common-resource-attributes.md)。

## <a name="remarks"></a>備註

[**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)函式會傳回對話方塊基礎單位（以圖元為單位）。 座標的確切意義取決於 [**style**](style-statement.md) option 語句所定義的樣式。 針對子樣式對話方塊，除非對話方塊的樣式為 **DS \_ ABSALIGN**，否則座標會相對於父視窗的原點，而在此情況下，座標是相對於顯示畫面的原點。

請勿使用 **WS \_ 子** 樣式搭配強制回應對話方塊。 [**對話方塊**](/windows/win32/api/winuser/nf-winuser-dialogboxa)函式一律會停用新建立之對話方塊的父/擁有者。 停用父視窗時，會隱含停用其子視窗。 由於子樣式對話方塊的父視窗已停用，因此子樣式對話方塊也是如此。

如果對話方塊具有 **DS \_ ABSALIGN** 樣式，則其左上角的對話座標是相對於螢幕原點，而不是父視窗的左上角。 當您希望對話方塊在顯示的特定部分中啟動時，您通常會使用這種樣式，不論父視窗在螢幕上的哪個位置。

[名稱 **] 對話方塊** 也可以當做 [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) 函式的類別名稱參數，用來建立具有對話方塊屬性的視窗。

## <a name="examples"></a>範例

以下示範 **DIALOG** 語句的用法：

``` syntax
#include <windows.h>

ErrorDialog DIALOG  10, 10, 300, 110
STYLE WS_POPUP | WS_BORDER
CAPTION "Error!" 
{
    CTEXT "Select One:", 1, 10, 10, 280, 12
    PUSHBUTTON "&Retry", 2, 75, 30, 60, 12
    PUSHBUTTON "&Abort", 3, 75, 50, 60, 12
    PUSHBUTTON "&Ignore", 4, 75, 80, 60, 12
}
```

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

[**功能表**](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[**版本**](version-statement.md)
</dt> </dl>

 

 
