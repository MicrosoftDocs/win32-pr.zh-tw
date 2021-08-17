---
title: 'SBM_SETPOS 訊息 (Winuser .h) '
description: 傳送 SBM \_ SETPOS 訊息來設定捲動方塊 (thumb 的位置) 並在要求時，重繪捲軸以反映捲動方塊的新位置。
ms.assetid: 6b3c16ba-1cdf-41ff-8546-ba98477af334
keywords:
- SBM_SETPOS 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- SBM_SETPOS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd753d8ef20d912cd5b50ba0932d54ed231ae19e032d21eb1de6492e5792e1d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119332221"
---
# <a name="sbm_setpos-message"></a>SBM \_ SETPOS 訊息

傳送 **SBM \_ SETPOS** 訊息來設定捲動方塊 (thumb 的位置) 並在要求時，重繪捲軸以反映捲動方塊的新位置。

應用程式不應直接傳送此訊息。 相反地，它們應該使用 [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) 函數。 視窗會透過其 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。 執行自訂捲軸控制項的應用程式必須回應這些訊息， **SetScrollPos** 函數才能正常運作。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定捲動方塊的新位置。 它必須在滾動範圍內。 如果這個參數超出滾動範圍，此值會向上或向下舍入為最接近的有效值。

</dd> <dt>

*lParam* 
</dt> <dd>

指定是否應該重新繪製捲軸，以反映新的捲動方塊位置。 如果此參數為 **TRUE**，則會重新繪製捲軸。 如果為 **FALSE**，則不會重新繪製捲軸。

</dd> </dl>

## <a name="return-value"></a>傳回值

**ComCtl32.dll 5.0 版**：如果捲動方塊的位置已變更，則傳回值是捲動方塊的先前位置;否則，它是零。

**ComCtl32.dll 版本 6.0**：捲動方塊的目前位置，不論是否已變更。

## <a name="remarks"></a>備註

如果對另一個函式的後續呼叫重新繪製捲軸控制項，將 *lParam* 參數設定為 **FALSE** 會很有用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**SBM \_ GETPOS**](sbm-getpos.md)
</dt> <dt>

[**SBM \_ GETRANGE**](sbm-getrange.md)
</dt> <dt>

[**SBM \_ SETRANGE**](sbm-setrange.md)
</dt> <dt>

[**SBM \_ SETRANGEREDRAW**](sbm-setrangeredraw.md)
</dt> </dl>

 

