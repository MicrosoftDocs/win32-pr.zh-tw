---
title: 'WM_INITDIALOG 訊息 (Winuser .h) '
description: 在對話方塊顯示之前，立即傳送至對話方塊程式。 對話方塊程式通常會使用這個訊息來初始化控制項，並執行任何其他會影響對話方塊外觀的初始作業。
ms.assetid: bc4f4718-1dab-48db-ae3b-5a81a7be2644
keywords:
- WM_INITDIALOG 訊息對話方塊
topic_type:
- apiref
api_name:
- WM_INITDIALOG
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64646075bc3d5c90076d6c1ca0d61f80111c90ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965738"
---
# <a name="wm_initdialog-message"></a>WM \_ INITDIALOG 訊息

在對話方塊顯示之前，立即傳送至對話方塊程式。 對話方塊程式通常會使用這個訊息來初始化控制項，並執行任何其他會影響對話方塊外觀的初始作業。


```C++
#define WM_INITDIALOG                   0x0110
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

控制項的控制碼，可接收預設鍵盤焦點。 只有在對話方塊程式傳回 **TRUE** 時，系統才會指派預設的鍵盤焦點。

</dd> <dt>

*lParam* 
</dt> <dd>

其他初始資料。 這項資料會在用來建立對話方塊的 [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)、 [**CreateDialogParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogparama)、 [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)或 [**DialogBoxParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama)函數的呼叫中，當做 *lParam* 參數傳遞給系統。 針對屬性工作表，此參數是用來建立頁面之 [**PROPSHEETPAGE**](/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2) 結構的指標。 如果使用任何其他對話方塊建立函式，則此參數為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

對話方塊程式應該會傳回 **TRUE** ，以指示系統將鍵盤焦點設定為 *wParam* 所指定的控制項。 否則，它應該會傳回 **FALSE** ，以防止系統設定預設的鍵盤焦點。

對話方塊程式應該會直接傳回值。 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)函數所設定的 **DWL \_ MSGRESULT** 值會被忽略。

## <a name="remarks"></a>備註

接收預設鍵盤焦點的控制項一律是對話方塊中可見、未停用，且具有 **WS \_ TABSTOP** 樣式的第一個控制項。 當對話方塊程式傳回 **TRUE** 時，系統會檢查控制項，以確定該程式未停用該程式。 如果已停用，系統會將鍵盤焦點設定為可見、未停用，且具有 **WS \_ TABSTOP** 的下一個控制項。

只有當應用程式已將鍵盤焦點設定為對話方塊的其中一個控制項時，才會傳回 **FALSE** 。

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

[**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[**CreateDialogParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogparama)
</dt> <dt>

[**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[**DialogBoxParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama)
</dt> <dt>

[**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus)
</dt> <dt>

**概念**
</dt> <dt>

[對話方塊](dialog-boxes.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**PROPSHEETPAGE**](/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2)
</dt> </dl>

 

