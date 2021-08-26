---
title: 'UDM_GETPOS 訊息 (Commctrl .h) '
description: 抓取具有16位精確度之上下按鈕控制項的目前位置。
ms.assetid: 5f395de0-11b3-44f8-9bf4-42e27ce88a0c
keywords:
- UDM_GETPOS 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- UDM_GETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e92ca5fe5d902980560b6879ac7c345230056987308a1e390b0af351281eac62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059778"
---
# <a name="udm_getpos-message"></a>UDM \_ GETPOS 訊息

抓取具有16位精確度之上下按鈕控制項的目前位置。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) 會設為零，而且 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) 會設定為控制項的目前位置。 如果發生錯誤， **HIWORD** 會設為非零值。

## <a name="remarks"></a>備註

處理此訊息時，上下按鈕控制項會根據好友視窗的標題來更新其目前位置。 如果沒有任何好友視窗，或標題指定無效或超出範圍的值，則會傳回一個錯誤。 此外，如果在沒有 ud [**\_ SETBUDDYINT**](up-down-control-styles.md) 樣式的情況下建立控制項，則會在傳回的 HIWORD 中設定錯誤旗標，即使它在傳回的 LOWORD 中傳回有效的位置值也一樣。

如果已針對具有 [**UDM \_ SETRANGE32**](udm-setrange32.md)的上下按鈕啟用32位的值，則此訊息只會傳回位置的較低16位。 若要取得完整的32位位置，請使用 [**UDM \_ GETPOS32**](udm-getpos32.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**UDM \_ GETRANGE**](udm-getrange.md)
</dt> <dt>

[**UDM \_ GETRANGE32**](udm-getrange32.md)
</dt> <dt>

[**UDM \_ SETPOS**](udm-setpos.md)
</dt> <dt>

[**UDM \_ SETRANGE32**](udm-setrange32.md)
</dt> </dl>

 

