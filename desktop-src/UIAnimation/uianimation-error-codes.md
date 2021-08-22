---
title: 'Windows動畫錯誤碼 (Winerror.h .h) '
description: 如果發生錯誤，Windows 動畫會以 HRESULT 值傳回程序代碼。 本節提供 Windows 動畫特定的錯誤碼清單。 如需一般 COM 錯誤碼的清單，請參閱 COM 錯誤碼。
ms.assetid: 38f15d61-d415-4c7d-b454-5144fc7c9b1e
topic_type:
- apiref
api_name:
- UI_E_CREATE_FAILED
- UI_E_SHUTDOWN_CALLED
- UI_E_ILLEGAL_REENTRANCY
- UI_E_OBJECT_SEALED
- UI_E_VALUE_NOT_SET
- UI_E_VALUE_NOT_DETERMINED
- UI_E_INVALID_OUTPUT
- UI_E_BOOLEAN_EXPECTED
- UI_E_DIFFERENT_OWNER
- UI_E_AMBIGUOUS_MATCH
- UI_E_FP_OVERFLOW
- UI_E_WRONG_THREAD
- UI_E_STORYBOARD_ACTIVE
- UI_E_STORYBOARD_NOT_PLAYING
- UI_E_START_KEYFRAME_AFTER_END
- UI_E_END_KEYFRAME_NOT_DETERMINED
- UI_E_LOOPS_OVERLAP
- UI_E_TRANSITION_ALREADY_USED
- UI_E_TRANSITION_NOT_IN_STORYBOARD
- UI_E_TRANSITION_ECLIPSED
- UI_E_TIME_BEFORE_LAST_UPDATE
- UI_E_TIMER_CLIENT_ALREADY_CONNECTED
api_location:
- winerror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44d725874de9c511558cef6ebbe8652905a7f5dac6372230385eaa3253ba3454
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513658"
---
# <a name="windows-animation-error-codes"></a>Windows動畫錯誤碼

如果發生錯誤，Windows 動畫會以 **HRESULT** 值傳回程序代碼。 本節提供 Windows 動畫特定的錯誤碼清單。 如需一般 COM 錯誤碼的清單，請參閱 [Com 錯誤碼](/windows/desktop/com/com-error-codes)。

<dl> <dt>

<span id="UI_E_CREATE_FAILED"></span><span id="ui_e_create_failed"></span>**UI \_ E \_ 建立 \_ 失敗**
</dt> <dd> <dl> <dt>

0x802A0001
</dt> <dt>



無法建立物件。


</dt> </dl> </dd> <dt>

<span id="UI_E_SHUTDOWN_CALLED"></span><span id="ui_e_shutdown_called"></span>**UI \_ E \_ 關機 \_ 呼叫**
</dt> <dd> <dl> <dt>

0x802A0002
</dt> <dt>



已在動畫管理員上呼叫 [**Shutdown**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) 方法，導致動畫管理員關閉，以及建立的所有動畫變數和分鏡腳本。

> [!Note]  
> 在 [**關閉**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown)之後，任何動畫物件都不能呼叫任何方法。

 


</dt> </dl> </dd> <dt>

<span id="UI_E_ILLEGAL_REENTRANCY"></span><span id="ui_e_illegal_reentrancy"></span>**UI \_ E 不 \_ 合法的 \_ 重新進入**
</dt> <dd> <dl> <dt>

0x802A0003
</dt> <dt>



這種回呼類型無法呼叫這個方法。


</dt> </dl> </dd> <dt>

<span id="UI_E_OBJECT_SEALED"></span><span id="ui_e_object_sealed"></span>**UI \_ E \_ 物件 \_ 密封**
</dt> <dd> <dl> <dt>

0x802A0004
</dt> <dt>



此物件已密封，因此不再允許這項變更。


</dt> </dl> </dd> <dt>

<span id="UI_E_VALUE_NOT_SET"></span><span id="ui_e_value_not_set"></span>**\_ \_ \_ 未設定 UI E \_ 值**
</dt> <dd> <dl> <dt>

0x802A0005
</dt> <dt>



要求的值從未設定過，因此無法取出。


</dt> </dl> </dd> <dt>

<span id="UI_E_VALUE_NOT_DETERMINED"></span><span id="ui_e_value_not_determined"></span>**UI \_ E \_ 值 \_ 未 \_ 判斷**
</dt> <dd> <dl> <dt>

0x802A0006
</dt> <dt>



無法判斷要求的值。


</dt> </dl> </dd> <dt>

<span id="UI_E_INVALID_OUTPUT"></span><span id="ui_e_invalid_output"></span>**UI \_ E \_ 不正確 \_ 輸出**
</dt> <dd> <dl> <dt>

0x802A0007
</dt> <dt>



回呼傳回了不正確輸出參數。


</dt> </dl> </dd> <dt>

<span id="UI_E_BOOLEAN_EXPECTED"></span><span id="ui_e_boolean_expected"></span>**\_需要 UI E \_ 布林值 \_**
</dt> <dd> <dl> <dt>

0x802A0008
</dt> <dt>



回呼傳回的成功碼不是 S \_ OK 或 \_ FALSE。


</dt> </dl> </dd> <dt>

<span id="UI_E_DIFFERENT_OWNER"></span><span id="ui_e_different_owner"></span>**UI \_ E \_ 不同的 \_ 擁有者**
</dt> <dd> <dl> <dt>

0x802A0009
</dt> <dt>



這個物件所擁有的參數是由不同的物件所擁有。


</dt> </dl> </dd> <dt>

<span id="UI_E_AMBIGUOUS_MATCH"></span><span id="ui_e_ambiguous_match"></span>**UI \_ E \_ 模糊 \_ 相符**
</dt> <dd> <dl> <dt>

0x802A000A
</dt> <dt>



有一個以上的專案符合搜尋準則。


</dt> </dl> </dd> <dt>

<span id="UI_E_FP_OVERFLOW"></span><span id="ui_e_fp_overflow"></span>**UI \_ E \_ FP \_ 溢位**
</dt> <dd> <dl> <dt>

0x802A000B
</dt> <dt>



發生浮點溢位。


</dt> </dl> </dd> <dt>

<span id="UI_E_WRONG_THREAD"></span><span id="ui_e_wrong_thread"></span>**UI \_ E \_ 錯誤的 \_ 執行緒**
</dt> <dd> <dl> <dt>

0x802A000C
</dt> <dt>



您只能從建立物件的執行緒呼叫這個方法。


</dt> </dl> </dd> <dt>

<span id="UI_E_STORYBOARD_ACTIVE"></span><span id="ui_e_storyboard_active"></span>**UI E 分鏡腳本 \_ \_ \_ 活動**
</dt> <dd> <dl> <dt>

0x802A0101
</dt> <dt>



分鏡腳本目前為排程。


</dt> </dl> </dd> <dt>

<span id="UI_E_STORYBOARD_NOT_PLAYING"></span><span id="ui_e_storyboard_not_playing"></span>**UI E 分鏡腳本 \_ \_ \_ 未 \_ 播放**
</dt> <dd> <dl> <dt>

0x802A0102
</dt> <dt>



腳本未播放。


</dt> </dl> </dd> <dt>

<span id="UI_E_START_KEYFRAME_AFTER_END"></span><span id="ui_e_start_keyframe_after_end"></span>**UI \_ E \_ \_ \_ 在結束後 \_ 啟動主要畫面格**
</dt> <dd> <dl> <dt>

0x802A0103
</dt> <dt>



開始的主要畫面格可能會在結束主要畫面格之後發生。


</dt> </dl> </dd> <dt>

<span id="UI_E_END_KEYFRAME_NOT_DETERMINED"></span><span id="ui_e_end_keyframe_not_determined"></span>**UI \_ E 結束主要畫面格 \_ \_ \_ 未 \_ 判定**
</dt> <dd> <dl> <dt>

0x802A0104
</dt> <dt>



可能無法判斷達到開始主要畫面格的結束主要畫面格時間。


</dt> </dl> </dd> <dt>

<span id="UI_E_LOOPS_OVERLAP"></span><span id="ui_e_loops_overlap"></span>**UI \_ E \_ 迴圈重 \_ 迭**
</dt> <dd> <dl> <dt>

0x802A0105
</dt> <dt>



兩個重複的分鏡腳本部分可能會重迭。


</dt> </dl> </dd> <dt>

<span id="UI_E_TRANSITION_ALREADY_USED"></span><span id="ui_e_transition_already_used"></span>**\_ \_ \_ 已使用 UI E \_ 轉換**
</dt> <dd> <dl> <dt>

0x802A0106
</dt> <dt>



轉換已加入至不同的分鏡腳本，或已新增至已完成播放且已發行的分鏡腳本。


</dt> </dl> </dd> <dt>

<span id="UI_E_TRANSITION_NOT_IN_STORYBOARD"></span><span id="ui_e_transition_not_in_storyboard"></span>**UI \_ E \_ 轉換 \_ 不 \_ 在分鏡腳本中 \_**
</dt> <dd> <dl> <dt>

0x802A0107
</dt> <dt>



轉換尚未新增至任何分鏡腳本。


</dt> </dl> </dd> <dt>

<span id="UI_E_TRANSITION_ECLIPSED"></span><span id="ui_e_transition_eclipsed"></span>**UI \_ E \_ 轉換 \_ ECLIPSED**
</dt> <dd> <dl> <dt>

0x802A0108
</dt> <dt>



轉換可能會 eclipse 腳本中的另一個轉換開始。


</dt> </dl> </dd> <dt>

<span id="UI_E_TIME_BEFORE_LAST_UPDATE"></span><span id="ui_e_time_before_last_update"></span>**\_ \_ \_ \_ 上次 \_ 更新前的 UI E 時間**
</dt> <dd> <dl> <dt>

0x802A0109
</dt> <dt>



指定的時間早于傳遞至上次更新的時間。


</dt> </dl> </dd> <dt>

<span id="UI_E_TIMER_CLIENT_ALREADY_CONNECTED"></span><span id="ui_e_timer_client_already_connected"></span>**UI \_ E \_ 計時器 \_ 用戶端 \_ 已 \_ 連線**
</dt> <dd> <dl> <dt>

0x802A010A
</dt> <dt>



此用戶端已連接到計時器。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7，僅適用于 Windows vista \[ 桌面應用程式的 Windows vista 和平臺更新\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                       |
| 標頭<br/>                   | <dl> <dt>Winerror.h。h</dt> </dl>           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Windows動畫參考](windows-animation-reference.md)
</dt> </dl>

 

