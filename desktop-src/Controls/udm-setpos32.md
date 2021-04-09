---
title: 'UDM_SETPOS32 訊息 (Commctrl .h) '
description: 設定具有32位精確度的上下按鈕控制項的位置。
ms.assetid: a337f2a1-0e3d-4ff4-a224-57b7f25c4bd0
keywords:
- UDM_SETPOS32 message Windows 控制項
topic_type:
- apiref
api_name:
- UDM_SETPOS32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0153305bb535a79dbed59e8d42a7c25157c30cd1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934699"
---
# <a name="udm_setpos32-message"></a>UDM \_ SETPOS32 訊息

設定具有32位精確度的上下按鈕控制項的位置。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

整數類型的變數，指定上下按鈕控制項的新位置。 如果參數超出控制項的指定範圍， *lParam* 會設為最接近的有效值。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回先前的位置。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**UDM \_ GETPOS**](udm-getpos.md)
</dt> <dt>

[**UDM \_ SETPOS**](udm-setpos.md)
</dt> <dt>

[**UDM \_ GETPOS32**](udm-getpos32.md)
</dt> </dl>

 

 





