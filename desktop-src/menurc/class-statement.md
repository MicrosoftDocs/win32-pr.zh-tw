---
title: CLASS 語句
description: 定義對話方塊的類別。
ms.assetid: 7c4325fe-66a4-4bb2-9c99-04b3ff590e7a
keywords:
- 類別語句功能表和其他資源
topic_type:
- apiref
api_name:
- CLASS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d31eba66a1e4527a24a55a24e4623f3c49dc204
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933172"
---
# <a name="class-statement"></a>CLASS 語句

定義對話方塊的類別。

**CLASS** 語句會出現在 [**對話方塊**](dialog-resource.md)語句的 main 之前的選擇性區段中。 如果未指定任何類別，則會使用標準對話方塊類別。

``` syntax
CLASS class
```

<dl> <dt>

<span id="class"></span><span id="CLASS"></span>*類*
</dt> <dd>

以雙引號括住的16位不帶正負號的整數或字串 ( ") ，以識別對話方塊的類別。 如果類別的視窗程式未處理傳送給它的訊息，則必須呼叫 [**DefDlgProc**](/windows/win32/api/winuser/nf-winuser-defdlgprocw) 函式，以確保正確處理所有訊息的對話方塊。 私用類別可以使用 **DefDlgProc** 做為預設視窗程式。 類別必須向設定為 **DLGWINDOWEXTRA** 的 [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)結構的 **cbWndExtra** 成員註冊。

</dd> </dl>

## <a name="remarks"></a>備註

**類別** 語句應該只用于特殊的案例，因為它會覆寫對話方塊的正常處理。 **CLASS** 語句會將對話方塊轉換成指定類別的視窗;這可能會產生非預期的結果，視類別而定。 請勿使用這個語句所定義的控制項類別名稱。

## <a name="examples"></a>範例

下列範例示範如何使用 **CLASS** 語句：

``` syntax
CLASS "myclass" 
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DefDlgProc**](/windows/win32/api/winuser/nf-winuser-defdlgprocw)
</dt> <dt>

[**對話 框**](dialog-resource.md)
</dt> </dl>

 

 