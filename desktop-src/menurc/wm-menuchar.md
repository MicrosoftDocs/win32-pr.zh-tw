---
title: 'WM_MENUCHAR 訊息 (Winuser .h) '
description: 當功能表在使用中，且使用者按下未對應至任何助憶鍵或快速鍵的按鍵時傳送。 這則訊息會傳送至擁有功能表的視窗。
ms.assetid: de6c91bb-80fd-44b2-8d96-d016477a6547
keywords:
- WM_MENUCHAR 訊息功能表和其他資源
topic_type:
- apiref
api_name:
- WM_MENUCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d276418636857fb7ce76159111b8e8b24519235823225fccb68fa1523b4137d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117869607"
---
# <a name="wm_menuchar-message"></a>WM \_ MENUCHAR 訊息

當功能表在使用中，且使用者按下未對應至任何助憶鍵或快速鍵的按鍵時傳送。 這則訊息會傳送至擁有功能表的視窗。


```C++
#define WM_MENUCHAR                     0x0120
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

低序位字組指定對應至使用者所按下之按鍵的字元碼。

高序位字組指定現用功能表類型。 此參數可以是下列其中一個值。



| 值                                                                                                                                                                                                                 | 意義                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <dt>**MF \_快顯視窗**</dt> <dt>0x00000010L</dt> </dl>       | 下拉式選單、子功能表或快捷方式功能表。<br/> |
| <span id="MF_SYSMENU"></span><span id="mf_sysmenu"></span><dl> <dt>**MF \_SYSMENU**</dt> <dt>0x00002000L</dt> </dl> | [視窗] 功能表。<br/>                             |



 

</dd> <dt>

*lParam* 
</dt> <dd>

現用功能表的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

處理此訊息的應用程式應該在傳回值的高序位字中傳回下列其中一個值。



| 傳回碼/值                                                                                                                                  | 描述                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**MNC \_關閉**</dt> <dt>1</dt> </dl>   | 通知系統應該關閉使用中的功能表。<br/>                                                                                                                      |
| <dl> <dt>**MNC \_執行**</dt> <dt>2</dt> </dl> | 通知系統應該選擇傳回值的低序位字組中指定的專案。 擁有者視窗會收到 [**WM \_ 命令**](wm-command.md) 訊息。<br/> |
| <dl> <dt>**MNC \_忽略**</dt> <dt>0</dt> </dl>  | 通知系統應該捨棄使用者所按下的字元，並在系統喇叭上建立短暫的嗶聲。<br/>                                                       |
| <dl> <dt>**MNC \_選取**</dt> <dt>3</dt> </dl>  | 通知系統應選取傳回值的低序位字組中指定的專案。 <br/>                                                                       |



 

## <a name="remarks"></a>備註

如果高序位字組包含0或1，則會忽略低序位字組。

當使用快速鍵來選取顯示點陣圖的功能表項目時，應用程式應該處理此訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

**概念**
</dt> <dt>

[鍵盤加速器](keyboard-accelerators.md)
</dt> </dl>

 

