---
title: 'BCM_SETSPLITINFO 訊息 (Commctrl .h) '
description: 設定分割按鈕控制項的資訊。 明確地傳送此訊息，或使用按鈕 \_ SetSplitInfo 宏。
ms.assetid: 609b8972-9616-4850-a72c-2f87ce19f563
keywords:
- BCM_SETSPLITINFO 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- BCM_SETSPLITINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17332ce5f10fa612d739598222e4973000961435fa525190a650adaa9aa9fc4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921418"
---
# <a name="bcm_setsplitinfo-message"></a>BCM \_ SETSPLITINFO 訊息

設定分割按鈕控制項的資訊。 明確地傳送此訊息，或使用 [**按鈕 \_ SetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_setsplitinfo) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

必須為零。

</dd> <dt>

*lParam* \[在\]
</dt> <dd>

[**按鈕 \_ SPLITINFO**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo)結構的指標，其中包含分割按鈕的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

此訊息只能搭配 [**BS \_ SPLITBUTTON**](button-styles.md) 和 [**BS \_ DEFSPLITBUTTON**](button-styles.md) 按鈕樣式使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[按鈕樣式](button-styles.md)
</dt> <dt>

**概念**
</dt> <dt>

[按鈕類型](button-types-and-styles.md)
</dt> </dl>

 

 





