---
title: 'EM_SETMARGINS 訊息 (Winuser .h) '
description: 設定編輯控制項的左邊界和右邊界的寬度。 訊息會重新繪製控制項，以反映新的邊界。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。
ms.assetid: 23eb6c9e-3cf9-4c90-b33e-8da84034b49b
keywords:
- EM_SETMARGINS 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETMARGINS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 396bba6dda0f6dbd132b9f67fa5a1ef012758bbf7cf8fa9517b656dcf164c94c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048358"
---
# <a name="em_setmargins-message"></a>EM \_ SETMARGINS 訊息

設定編輯控制項的左邊界和右邊界的寬度。 訊息會重新繪製控制項，以反映新的邊界。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要設定的邊界。 這個參數可以是下列一或多個值。



| 值                                                                                                                                                            | 意義                                                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EC_LEFTMARGIN"></span><span id="ec_leftmargin"></span><dl> <dt>**EC \_ LEFTMARGIN**</dt> </dl>    | 設定左邊界。<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="EC_RIGHTMARGIN"></span><span id="ec_rightmargin"></span><dl> <dt>**EC \_ RIGHTMARGIN**</dt> </dl> | 設定右邊界。<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="EC_USEFONTINFO"></span><span id="ec_usefontinfo"></span><dl> <dt>**EC \_ USEFONTINFO**</dt> </dl> | **Rich edit 控制項：** 將左邊界和右邊界設定為使用控制項目前字型的文字度量計算的窄寬度。 如果未針對控制項設定字型，則邊界會設定為零。 *LParam* 參數會被忽略。 <br/> **編輯控制項：** 在 *wParam* 參數中無法使用 **EC \_ USEFONTINFO** 值。 它只能用在 *lParam* 參數中。<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會指定左邊界的新寬度（以圖元為單位）。 如果 *wParam* 不包含 **EC \_ LEFTMARGIN**，則會忽略此值。

**編輯控制項及豐富的編輯3.0 和更新版本：**[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))可以指定 **EC \_ USEFONTINFO** 值，將左邊界設定為使用控制項目前字型的文字度量來計算的窄寬度。 如果未針對控制項設定字型，則邊界會設定為零。

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定右邊界的新寬度（以圖元為單位）。 如果 *wParam* 不包含 **EC \_ RIGHTMARGIN**，則會忽略此值。

**編輯控制項及豐富的編輯3.0 和更新版本：**[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))可以指定 **EC \_ USEFONTINFO** 值，將右邊界設定為使用控制項目前字型的文字度量來計算的窄寬度。 如果未針對控制項設定字型，則邊界會設定為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息不會傳回值。

## <a name="remarks"></a>備註

**編輯控制項：** 您無法在 *wParam* 參數中使用 **EC \_ USEFONTINFO** ，但可以在 *lParam* 參數中使用它。

**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。 所有 rich edit 版本都支援在 *wParam* 參數中使用 **EC \_ USEFONTINFO** 。 不過，只有 Microsoft Rich Edit 3.0 和更新版本支援在 *lParam* 參數中使用 **EC \_ USEFONTINFO** 。 如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ GETMARGINS**](em-getmargins.md)
</dt> </dl>

 

