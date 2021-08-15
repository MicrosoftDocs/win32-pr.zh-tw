---
title: 'MCI_STOP 命令 (Mmsystem .h) '
description: MCI \_ 停止命令會停止所有播放和記錄順序、卸載所有播放緩衝區，並停止顯示影片影像。 CD 音訊、數位影片、MIDI sequencer、videodisc、VCR 和波形音訊裝置都會辨識此命令。
ms.assetid: e5ae20b3-7439-4314-8354-d06e83b29729
keywords:
- MCI_STOP 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_STOP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e02830dde544e025447cb72df6ff3720857985384ff6bd074c5e0718b114697c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118374600"
---
# <a name="mci_stop-command"></a>MCI \_ 停止命令

MCI \_ 停止命令會停止所有播放和記錄順序、卸載所有播放緩衝區，並停止顯示影片影像。 CD 音訊、數位影片、MIDI sequencer、videodisc、VCR 和波形音訊裝置都會辨識此命令。

若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_STOP, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpStop
);
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*
</dt> <dd>

要接收命令訊息之 MCI 裝置的裝置識別碼。

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

\_ \_ 針對數位-視頻和 VCR 裝置，mci 測試的 mci 通知、mci 等候或 \_ 。 如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。

</dd> <dt>

<span id="lpStop"></span><span id="lpstop"></span><span id="LPSTOP"></span>*lpStop*
</dt> <dd>

[**MCI \_ 泛型 \_ PARMS**](mci-generic-parms.md)結構的指標。 具有擴充命令集的 (裝置，可能會以裝置特定結構取代此結構。 ) 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

MCI \_ STOP 和 [mci \_ PAUSE](mci-pause.md) 命令之間的差異取決於裝置。 可能的話，MCI 會 \_ 暫停裝置操作，但讓裝置可以立即繼續播放。

針對 CD 音訊裝置，MCI 會 \_ 停止將目前的曲目位置重設為零; 相反地， [mci \_ PAUSE](mci-pause.md) 會維持目前的曲目位置，並預期裝置將繼續播放。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Mmsystem (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[MCI 命令](mci-commands.md)
</dt> </dl>

 

