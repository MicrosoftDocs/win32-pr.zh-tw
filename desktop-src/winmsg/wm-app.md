---
description: 用來定義私用訊息（通常是以 WM \_ 應用程式 + x 形式），其中 x 是整數值。
ms.assetid: fdb549df-426f-4af5-9c17-6e8730e4abc0
title: 'WM_APP (Winuser) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4998f8240b08d248a75b375bb813ba02cd02344e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193707"
---
# <a name="wm_app"></a>WM \_ 應用程式

用來定義私用訊息（通常是以 **WM \_ 應用程式** x 形式）， + 其中 *x* 是整數值。

``` syntax
#define WM_APP                          0x8000
```

## <a name="remarks"></a>備註

**WM \_ 應用程式** 常數可用來區分保留給系統使用的訊息值，以及可供應用程式用來在私用視窗類別內傳送訊息的值。 以下是可用的訊息編號範圍。



| 範圍                                                 | 意義                                                        |
|-------------------------------------------------------|----------------------------------------------------------------|
| 0到 [**WM \_ 使用者**](wm-user.md) -1<br/>   | 保留供系統使用的訊息。<br/>            |
| [**WM \_使用者**](wm-user.md) 透過0x7FFF<br/> | 私用視窗類別使用的整數訊息。<br/> |
| **WM \_** 透過0xBFFF 的應用程式<br/>                 | 應用程式可使用的訊息。<br/>         |
| 0xC000 至0xFFFF<br/>                      | 應用程式所使用的字串訊息。<br/>            |
| 大於0xFFFF<br/>                        | 由系統所保留。<br/>                             |



 

第一個範圍中的訊息編號 (0 到 [**WM \_ 使用者**](wm-user.md) -1) 是由系統所定義。 此範圍中未明確定義的值是由系統所保留。

第二個範圍中的訊息編號 ([**WM \_ 使用者**](wm-user.md) 透過 0x7FFF) 可以由應用程式定義和使用，以在私用視窗類別內傳送訊息。 這些值不能用來定義整個應用程式中有意義的訊息，因為某些預先定義的視窗類別已經在這個範圍中定義值。 例如，[ **按鈕**]、[ **編輯**]、[ **LISTBOX**] 和 [ **COMBOBOX** ] 等預先定義的控制項類別，都可能會使用這些值。 除非應用程式已設計為交換訊息，並將相同意義附加至訊息編號，否則不應將此範圍中的訊息傳送至其他應用程式。

第三個範圍中的訊息編號 (0x8000 到 0xBFFF) 可供應用程式用來作為私用訊息。 此範圍內的訊息不會與系統訊息發生衝突。

第四個範圍內的訊息編號 (0xC000 至 0xFFFF) 是在執行時間定義，而應用程式會呼叫 [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) 函式來取得字串的訊息編號。 所有註冊相同字串的應用程式都可以使用相關聯的訊息編號來交換訊息。 不過，實際的訊息編號不是常數，而且在不同的會話之間不能假設是相同的。

系統會保留第五個範圍 (大於 0xFFFF) 的訊息編號。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

[**WM \_ 使用者**](wm-user.md)
</dt> <dt>

**概念**
</dt> <dt>

[訊息和訊息佇列](messages-and-message-queues.md)
</dt> </dl>

 

 
