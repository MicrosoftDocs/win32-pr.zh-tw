---
title: 'TBM_SETPAGESIZE 訊息 (Commctrl .h) '
description: 設定捲軸的滑杆為了回應鍵盤輸入而移動的邏輯位置數目，例如或按鍵，或滑鼠輸入，例如在並排條通道中按一下。
ms.assetid: 34edb868-4b6b-4b3f-b315-3ce39346b134
keywords:
- TBM_SETPAGESIZE message Windows 控制項
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
ms.openlocfilehash: ec5d8a396bb605b4276346e84e7b46bfbefe0657
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025326"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TBM \_ GETPAGESIZE**](tbm-getpagesize.md)
</dt> </dl>

 

 





