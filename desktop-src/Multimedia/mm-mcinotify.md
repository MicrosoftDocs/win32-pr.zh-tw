---
title: 'MM_MCINOTIFY 訊息 (Mmsystem .h) '
description: MM \_ MCINOTIFY 訊息會通知應用程式，MCI 裝置已完成操作。 MCI 裝置只會在使用 MCI 通知旗標時傳送此訊息 \_ 。
ms.assetid: a0840130-2969-4ce5-b098-3e45401eebb1
keywords:
- MM_MCINOTIFY 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- MM_MCINOTIFY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc03ab0406542472871f35ca3ff619d4d9a6f35725b9322a4c11bc73bc29a5aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807508"
---
# <a name="mm_mcinotify-message"></a>MM \_ MCINOTIFY 訊息

**MM \_ MCINOTIFY** 訊息會通知應用程式，MCI 裝置已完成操作。 MCI 裝置只會在使用 MCI 通知旗標時傳送此訊息 \_ 。


```C++
MM_MCINOTIFY 
wParam = (WPARAM) wFlags 
lParam = (LONG) lDevID
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="wFlags"></span><span id="wflags"></span><span id="WFLAGS"></span>*wFlags*
</dt> <dd>

通知的原因。 系統會定義下列值：



| 需求 | 值 |
|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MCI \_ 通知已 \_ 中止    | 裝置收到命令，導致無法符合目前的條件來起始回呼函式。 如果新的命令中斷目前的命令，而且它也要求通知，則裝置只會傳送此訊息，而不會將 MCI \_ 通知 \_ 取代 |
| MCI \_ 通知 \_ 失敗    | 裝置執行命令時發生裝置錯誤。                                                                                                                                                                                                            |
| MCI \_ 通知 \_ 成功 | 已符合起始回呼函數的條件。                                                                                                                                                                                                                 |
| 已 \_ 取代 MCI 通知 \_ | 裝置收到另一個命令，並已設定「通知」旗標，且目前已取代初始回呼函式的條件。                                                                                                                           |



 

</dd> <dt>

<span id="lDevID"></span><span id="ldevid"></span><span id="LDEVID"></span>*lDevID*
</dt> <dd>

起始回呼函數的裝置識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

如需 MCI 通知旗標的詳細資訊 \_ ，請參閱 [通知旗](the-notify-flag.md)標。

\_ \_ 當命令的動作完成時，裝置會以 **MM \_ MCINOTIFY** 傳回 MCI 通知成功旗標。 例如，當裝置完成播放時，CD 音訊裝置會使用此旗標來取得 [**play**](play.md) ( [**MCI \_ play**](mci-play.md)) 命令的通知。 只有當 **播放** 命令到達指定的結束位置或到達媒體的結尾時，才會成功。 同樣地， [**搜尋**](seek.md) ( [**mci \_ 搜尋**](mci-seek.md)) 和 [**記錄**](record.md) ( [**mci \_ 記錄**](mci-record.md)) 命令不會讓 mci \_ 通知 \_ 成功，直到到達指定的結束位置或到達媒體的結尾為止。

裝置 \_ \_ 只會在收到命令以防止通知條件出現時，才會以 **MM \_ MCINOTIFY** 傳回 MCI 通知已中止旗標。 例如， [**播放**](play.md) 命令不會中止先前 **播放** 命令的通知，前提是新的命令不會變更播放方向或變更結束位置。 [**搜尋**](seek.md)和 [**記錄**](record.md)命令的行為類似。 \_ \_ 當使用 [**pause**](pause.md) ( [**MCI \_ pause**](mci-pause.md)) 命令暫停播放或錄製時，mci 也不會傳送 mci 通知。 傳送 [**resume**](resume.md) ( [**MCI \_ resume**](mci-resume.md)) 命令可讓它們繼續符合回呼條件。

當您的應用程式要求命令的通知時，請檢查 [**mciSendString**](/previous-versions//dd757161(v=vs.85)) 或 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數的錯誤傳回。 如果這些函式遇到錯誤並傳回非零值，則 MCI 不會設定命令的通知。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Mmsystem (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[MCI 訊息](mci-messages.md)
</dt> <dt>

[**暫停**](pause.md)
</dt> <dt>

[**玩**](play.md)
</dt> <dt>

[**記錄**](record.md)
</dt> <dt>

[**恢復**](resume.md)
</dt> <dt>

[**尋求**](seek.md)
</dt> </dl>

 

