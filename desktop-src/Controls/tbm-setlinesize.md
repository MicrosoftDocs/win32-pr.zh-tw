---
title: 'TBM_SETLINESIZE 訊息 (Commctrl .h) '
description: 設定從箭號按鍵（例如，或按鍵）回應鍵盤輸入時，會將這些捲軸滑杆移動的邏輯位置數目。 邏輯位置是捲軸的最小值與最大滑杆位置之間的整數增量。
ms.assetid: 7fe3f9b8-2ddf-4460-882f-6be439f83daa
keywords:
- TBM_SETLINESIZE message Windows 控制項
topic_type:
- apiref
api_name:
- TBM_SETLINESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec898ed09b20f15023ef04a399f5644df746e495
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934043"
---
# <a name="tbm_setlinesize-message"></a>TBM \_ SETLINESIZE 訊息

設定從箭號按鍵（例如，或按鍵）回應鍵盤輸入時，會將這些捲軸滑杆移動的邏輯位置數目。 邏輯位置是捲軸的最小值與最大滑杆位置之間的整數增量。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

新行大小。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回指定前一行大小的32位值。

## <a name="remarks"></a>備註

行大小的預設設定為1。

當使用者按下方向鍵時，此項資訊也會將具有 TB 組合和 TB LINEDOWN 通知碼的 [**wm \_ HSCROLL**](wm-hscroll.md) 或 [**WM \_ VSCROLL**](wm-vscroll.md) 訊息傳送 \_ \_ 至其父視窗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TBM \_ GETLINESIZE**](tbm-getlinesize.md)
</dt> </dl>

 

 





