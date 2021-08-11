---
title: 加速器資源
description: 定義應用程式的一個或多個加速器。 加速器是應用程式所定義的按鍵，可讓使用者快速地執行工作。
ms.assetid: 5953ee2d-b7a7-45d2-8445-4cba1207e272
keywords:
- 加速器資源功能表與其他資源
topic_type:
- apiref
api_name:
- ACCELERATORS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e7ba2d19bbab6346f7a62afe56269f762cd94f7ef1730654fb6ac1abf317e4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118235737"
---
# <a name="accelerators-resource"></a>加速器資源

定義應用程式的一個或多個加速器。 加速器是應用程式所定義的按鍵，可讓使用者快速地執行工作。

``` syntax
acctablename ACCELERATORS [optional-statements] {event, idvalue, [type] [options]... }
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="acctablename"></span><span id="ACCTABLENAME"></span>*acctablename*
</dt> <dd>

識別資源的唯一名稱或16位不帶正負號的整數值。

</dd> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*選用語句*
</dt> <dd>

下列零或多個語句。



| 陳述式                                                        | 描述                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**特性**](characteristics-statement.md) *dword*     | 有關可供讀取和寫入資源檔的工具使用之資源的使用者定義資訊。 如需詳細資訊，請參閱 [**特性**](characteristics-statement.md)。 |
| [**語言**](language-statement.md)*語言*、*語言* | 指定資源的語言。 如需詳細資訊，請參閱 [**語言**](language-statement.md)。                                                                              |
| [**版本**](version-statement.md) *dword*                     | 資源的使用者定義版本號碼，可供讀取和寫入資源檔的工具使用。 如需詳細資訊，請參閱 [**版本**](version-statement.md)。              |



 

</dd> <dt>

<span id="event"></span><span id="EVENT"></span>*事件*
</dt> <dd>

要作為加速器使用的按鍵。 它可以是下列任何一個字元類型。



| 類型                    | 描述                                                                                                                                                                                                                                  |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "*char*"                | 用雙引號括住的單一字元 ( ") 。 字元前面可以加上插入號 (^) ，表示字元是控制字元。                                                                                  |
| *字元*             | 代表字元的整數值。 *型* 別參數必須是 **ASCII**。                                                                                                                                                           |
| *虛擬機器碼字元* | 代表虛擬機器碼的整數值。 您可以藉由在雙引號中放置大寫字母或數位來指定英數位元的虛擬機器碼 (例如 "9" 或 "C" ) 。 *型* 別參數必須是 **VIRTKEY**。 |



 

</dd> <dt>

<span id="idvalue"></span><span id="IDVALUE"></span>*idvalue*
</dt> <dd>

識別快速鍵的16位不帶正負號的整數值。

</dd> <dt>

<span id="type"></span><span id="TYPE"></span>*類型*
</dt> <dd>

只有當 *事件* 參數是 *字元* 或 *虛擬金鑰字元* 時才需要。 *類型* 參數會指定 **ASCII** 或 **VIRTKEY**;*事件* 的整數值會據以解讀。 當指定 **VIRTKEY** 且 *事件* 包含字串時， *事件* 必須為大寫。

</dd> <dt>

<span id="options"></span><span id="OPTIONS"></span>*選項*
</dt> <dd>

定義加速器的選項。 這個參數可以是下列一或多個值。



| 選項                             | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **NOINVERT**                       | 指定使用快速鍵時，不會反白顯示最上層功能表項目。 當您針對未對應至功能表項目的動作定義快速鍵時，這會很有用。 如果省略 **NOINVERT** ，當使用快速鍵時，最上層的功能表項目會反白顯示 (可能的) 。 這個屬性已過時，而且只是為了與針對16位 Windows 所設計資源檔的回溯相容性而保留。 |
| **ALT**                            | 只有在 ALT 鍵關閉時，才會啟用快速鍵。 只適用于虛擬機器碼。                                                                                                                                                                                                                                                                                                                                            |
| **轉變**                          | 只有在 SHIFT 鍵已關閉時，才會啟用快速鍵。 僅適用于虛擬機器碼                                                                                                                                                                                                                                                                                                                                           |
| [**控制**](control-control.md) | 將字元定義為控制字元 (只有在控制項索引鍵) 關閉時，才會啟用快速鍵。 這與使用插入號 (^) 在 *事件* 參數中的快速鍵之前，會有相同的效果。 僅適用于虛擬機器碼                                                                                                                                                                                           |



 

</dd> </dl>

此外，也支援某些屬性以提供回溯相容性。 如需詳細資訊，請參閱 [一般資源屬性](common-resource-attributes.md)。

## <a name="remarks"></a>備註

[**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora)函式可用來將應用程式佇列中的加速器訊息轉譯為 [**Wm \_ 命令**](./wm-command.md)或 [**wm \_ SYSCOMMAND**](./wm-syscommand.md)訊息。

## <a name="examples"></a>範例

下列範例示範快速鍵的使用。

``` syntax
1 ACCELERATORS
{
  "^C",  IDDCLEAR         ; control C
  "K",   IDDCLEAR         ; shift K
  "k",   IDDELLIPSE, ALT  ; alt k
  98,    IDDRECT, ASCII   ; b
  66,    IDDSTAR, ASCII   ; B (shift b)
  "g",   IDDRECT          ; g
  "G",   IDDSTAR          ; G (shift G)
  VK_F1, IDDCLEAR, VIRTKEY                ; F1
  VK_F1, IDDSTAR, CONTROL, VIRTKEY        ; control F1
  VK_F1, IDDELLIPSE, SHIFT, VIRTKEY       ; shift F1
  VK_F1, IDDRECT, ALT, VIRTKEY            ; alt F1
  VK_F2, IDDCLEAR, ALT, SHIFT, VIRTKEY    ; alt shift F2
  VK_F2, IDDSTAR, CONTROL, SHIFT, VIRTKEY ; ctrl shift F2
  VK_F2, IDDRECT, ALT, CONTROL, VIRTKEY   ; alt control F2
}
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[使用鍵盤加速器](./using-keyboard-accelerators.md)
</dt> <dt>

[**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[**特徵**](characteristics-statement.md)
</dt> <dt>

[**對話 框**](dialog-resource.md)
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

 

 