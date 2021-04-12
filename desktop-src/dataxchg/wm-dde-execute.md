---
title: 'WM_DDE_EXECUTE 訊息 (的) '
description: 動態資料交換 (DDE) 用戶端應用程式會將 WM \_ DDE \_ 執行訊息張貼至 dde 伺服器應用程式，以將字串傳送至要以一連串命令的形式處理的伺服器。
ms.assetid: 23c18a57-83ee-4fd3-a5bc-71645bda34eb
keywords:
- WM_DDE_EXECUTE 訊息資料交換
topic_type:
- apiref
api_name:
- WM_DDE_EXECUTE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 957b5cadcd2383d535aa67258725bafff57ab4f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384785"
---
# <a name="wm_dde_execute-message"></a>WM \_ DDE \_ 執行訊息

動態資料交換 (DDE) 用戶端應用程式會將 **WM \_ DDE \_ 執行** 訊息張貼至 dde 伺服器應用程式，以將字串傳送至要以一連串命令的形式處理的伺服器。 伺服器應用程式預期會在回應中公佈一則 [**WM 的 \_ DDE \_ ACK**](wm-dde-ack.md) 訊息。

若要張貼此訊息，請使用下列參數呼叫 [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) 函數。


```C++
#define WM_DDE_EXECUTE     0x03E8
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

張貼訊息之用戶端視窗的控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>

包含參考 ANSI 或 Unicode 命令字串的全域記憶體物件，視交談中涉及的 windows 類型而定。

</dd> </dl>

## <a name="remarks"></a>備註

命令字串是以 null 終止的字串，其中包含一個或多個以單一括弧括住的 opcode 字串 (\[ \]) 。 每個 opcode 字串都有下列語法，其中 *參數* 清單是選擇性的：

*opcode 參數*

*Opcode* 是任何應用程式定義的單一 token。 它不能包含空格、逗號、括弧、方括弧或引號。

[ *參數* ] 清單可以包含任何應用程式定義的值或值。 多個參數會以逗號分隔，而整個參數清單會以括弧括住。 參數不能包含逗號或括弧，除非在加上引號的字串內。 如果括弧或括弧字元要出現在加上引號的字串中，則不需要加倍，如同舊規則下的案例。

以下是有效的命令字串：


```
[connect][download(query1,results.txt)][disconnect] 
[query("sales per employee for each district")] 
[open("sample.xlm")][run("r1c1")] 
[quote_case("This is a "" character")] 
[bracket_or_paren_case("()s or []s should be no problem.")] 
```



請注意，在舊規則下，括弧和括弧必須加倍，如下所示：


```
[bracket_or_paren_case("(())s or [[]]s should be no problem.")] 
```



伺服器應該能夠以任一形式剖析命令。

只有當用戶端和伺服器視窗的控制碼造成 [**IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) 函數傳回 **TRUE** 時，才應該使用 Unicode 執行字串。

### <a name="posting"></a>張貼

用戶端應用程式會藉由呼叫 [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) 函數來配置全域記憶體物件。

當您處理伺服器張貼至 **wm dde \_ \_ 執行** 訊息的「 [**wm \_ dde \_**](wm-dde-ack.md)通知」訊息時，用戶端應用程式必須刪除 **wm \_ dde \_ ack** 訊息所傳回的物件。

### <a name="receiving"></a>接收

伺服器應用程式會張貼 [**WM \_ DDE \_**](wm-dde-ack.md) 通知訊息，以回應正面或負面。 伺服器應重複使用全域記憶體物件。

除非子通訊協定另有指定，否則伺服器不應張貼 [**WM \_ DDE \_**](wm-dde-ack.md) 通知訊息，直到執行命令字串指定的所有動作都完成為止。 這項規則的唯一例外狀況是當字串導致伺服器終止交談時。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                 |
| 標頭<br/>                   | <dl> <dt> (包含 Windows. h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode)
</dt> <dt>

[**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[**WM \_ DDE \_ ACK**](wm-dde-ack.md)
</dt> <dt>

**概念**
</dt> <dt>

[關於動態資料交換](about-dynamic-data-exchange.md)
</dt> </dl>

 

