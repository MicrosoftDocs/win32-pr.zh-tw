---
title: 'TBM_SETPAGESIZE 訊息 (Commctrl .h) '
description: 設定捲軸的滑杆為了回應鍵盤輸入而移動的邏輯位置數目，例如或按鍵，或滑鼠輸入，例如在並排條通道中按一下。
ms.assetid: 34edb868-4b6b-4b3f-b315-3ce39346b134
keywords:
- TBM_SETPAGESIZE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TBM_SETPAGESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87cf41547a996e9726002101998ea859b7dbc6cc3e7ed3f87927fdae8bdadd2f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046098"
---
# <a name="tbm_setpagesize-message"></a>TBM \_ >setpagesize method 訊息

設定捲軸的滑杆為了回應鍵盤輸入而移動的邏輯位置數目，例如或按鍵，或滑鼠輸入，例如在並排條通道中按一下。 邏輯位置是捲軸的最小值與最大滑杆位置之間的整數增量。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

新的頁面大小。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回指定先前頁面大小的32位值。

## <a name="remarks"></a>備註

當您收到滾動頁的鍵盤或滑鼠輸入時，這些頁首也會將具有 TB PAGEUP 和 TB PAGEDOWN 通知碼的 [**wm \_ HSCROLL**](wm-hscroll.md) 或 [**WM \_ VSCROLL**](wm-vscroll.md) 訊息傳送 \_ \_ 至其父視窗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TBM \_ GETPAGESIZE**](tbm-getpagesize.md)
</dt> </dl>

 

 





