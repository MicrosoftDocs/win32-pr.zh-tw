---
title: 'UDM_SETPOS 訊息 (Commctrl .h) '
description: 設定具有16位精確度之上下按鈕控制項的目前位置。
ms.assetid: e7c8b55f-3a4f-47e7-8c7d-e47509f27f1d
keywords:
- UDM_SETPOS message Windows 控制項
topic_type:
- apiref
api_name:
- UDM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b409f9e7468e3add89248b61b7b563ac592f0dcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104760"
---
# <a name="udm_setpos-message"></a>UDM \_ SETPOS 訊息

設定具有16位精確度之上下按鈕控制項的目前位置。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

上下按鈕控制項的新位置。 如果參數超出控制項的指定範圍， *lParam* 會設為最接近的有效值。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是先前的位置。

## <a name="remarks"></a>備註

此訊息僅支援16位的位置。 如果已針對具有 [**UDM \_ SETRANGE32**](udm-setrange32.md)的上下控制項啟用32位值，請使用 [**udm \_ SETPOS32**](udm-setpos32.md)。

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

[**UDM \_ GETRANGE**](udm-getrange.md)
</dt> <dt>

[**UDM \_ GETPOS**](udm-getpos.md)
</dt> </dl>

 

 





