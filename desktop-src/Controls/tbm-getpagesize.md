---
title: 'TBM_GETPAGESIZE 訊息 (Commctrl .h) '
description: 抓取捲軸的滑杆為了回應鍵盤輸入（例如或按鍵）或滑鼠輸入而移動的邏輯位置數目，例如在並排條的通道中按一下。
ms.assetid: f0c5feac-2723-440e-96c0-dac37b0531ed
keywords:
- TBM_GETPAGESIZE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TBM_GETPAGESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1aa3ef3412fd00c18972b62d4d868ff1dbc97cb4787693b3746281b4884706e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046498"
---
# <a name="tbm_getpagesize-message"></a>TBM \_ GETPAGESIZE 訊息

抓取捲軸的滑杆為了回應鍵盤輸入（例如或按鍵）或滑鼠輸入而移動的邏輯位置數目，例如在並排條的通道中按一下。 邏輯位置是捲軸的最小值與最大滑杆位置之間的整數增量。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回指定頁尾頁面大小的32位值。

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

[**TBM \_ >SETPAGESIZE METHOD**](tbm-setpagesize.md)
</dt> </dl>

 

 





