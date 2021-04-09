---
title: 'MCI_PLAY 命令 (Mmsystem .h) '
description: MCI \_ PLAY 命令會指示裝置開始傳輸輸出資料。 CD 音訊、數位影片、MIDI sequencer、videodisc、VCR 和波形音訊裝置都會辨識此命令。
ms.assetid: d912ab49-63f0-40a9-aa4c-f9463782b54c
keywords:
- MCI_PLAY 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_PLAY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f985a8d5d6be7ad42702afc898b3aaf437ef320
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844404"
---
# <a name="mci_play-command"></a>MCI \_ PLAY 命令

MCI \_ PLAY 命令會指示裝置開始傳輸輸出資料。 CD 音訊、數位影片、MIDI sequencer、videodisc、VCR 和波形音訊裝置都會辨識此命令。

若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_PLAY, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_PLAY_PARMS ) lpPlay
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

<span id="lpPlay"></span><span id="lpplay"></span><span id="LPPLAY"></span>*lpPlay*
</dt> <dd>

[**MCI \_ 播放 \_ PARMS**](mci-play-parms.md)結構的指標。 具有擴充命令集的 (裝置，可能會以裝置特定結構取代此結構。 ) 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

下列其他旗標適用于所有支援 MCI PLAY 的裝置 \_ ：

<dl> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ 來源
</dt> <dd>

起始位置會包含在 *lpPlay* 所識別之結構的 **dwFrom** 成員中。 指派給位置值的單位，會以 Mci 設定的 \_ \_ 時間格式旗標，以 \_ [mci \_ set](mci-set.md) 命令來指定。 如果 \_ 未指定來自的 MCI，開始位置會預設為目前的位置。

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ 至
</dt> <dd>

結束位置會包含在由 *lpPlay* 所識別之結構的 **dwTo** 成員中。 指派給位置值的單位是使用 mci \_ set \_ TIME \_ FORMAT 旗標來指定 \_ 。 如果 \_ 未指定 MCI 至，結束位置會預設為媒體的結尾。

</dd> </dl>

下列其他旗標適用于 **digitalvideo** 裝置類型：

<dl> <dt>

<span id="MCI_DGV_PLAY_REPEAT"></span><span id="mci_dgv_play_repeat"></span>MCI \_ DGV \_ 播放 \_ 重複
</dt> <dd>

當到達內容的結尾時，播放應該會一開始重新開機。

</dd> <dt>

<span id="MCI_DGV_PLAY_REVERSE"></span><span id="mci_dgv_play_reverse"></span>MCI \_ DGV \_ 播放 \_ 反向
</dt> <dd>

播放應以相反的方式進行。

</dd> <dt>

<span id="MCI_MCIAVI_PLAY_WINDOW"></span><span id="mci_mciavi_play_window"></span>MCI \_ MCIAVI \_ 播放 \_ 視窗
</dt> <dd>

在 (預設) 的裝置實例相關聯的視窗中，應該會進行播放。  (此旗標適用于 MCIAVI。WINSPOOL.DRV。 ) 

</dd> <dt>

<span id="MCI_MCIAVI_PLAY_FULLSCREEN"></span><span id="mci_mciavi_play_fullscreen"></span>MCI \_ MCIAVI \_ \_ 全螢幕播放
</dt> <dd>

播放應使用全螢幕顯示。 只有在播放壓縮或8位檔案時，才使用此旗標。

</dd> </dl>

針對數位影片裝置， *lpPlay* 會指向 [**MCI \_ DGV \_ PLAY \_ PARMS**](/previous-versions//dd743396(v=vs.85)) 結構。

下列其他旗標適用于 **vcr** 裝置類型：

<dl> <dt>

<span id="MCI_VCR_PLAY_AT"></span><span id="mci_vcr_play_at"></span>MCI \_ VCR \_ \_ 的播放位置
</dt> <dd>

*LpPlay* 所識別之結構的 **dwAt** 成員，包含整個命令開始的時間，或如果裝置是 cued，則在裝置到達 [MCI \_ 提示](mci-cue.md)命令所提供的 from 位置時。

</dd> <dt>

<span id="MCI_VCR_PLAY_REVERSE"></span><span id="mci_vcr_play_reverse"></span>MCI \_ VCR \_ \_ 反向播放
</dt> <dd>

播放應以相反的方式進行。

</dd> <dt>

<span id="MCI_VCR_PLAY_SCAN"></span><span id="mci_vcr_play_scan"></span>MCI \_ VCR \_ 播放 \_ 掃描
</dt> <dd>

在維護影片輸出時，播放應該盡可能快越好。

</dd> </dl>

若為 VCR 裝置， *lpPlay* 會指向 [**MCI \_ VCR \_ 播放 \_ PARMS**](mci-vcr-play-parms.md) 結構。

下列其他旗標適用于 **videodisc** 裝置類型：

<dl> <dt>

<span id="MCI_VD_PLAY_FAST"></span><span id="mci_vd_play_fast"></span>MCI \_ VD \_ \_ 快速播放
</dt> <dd>

快速播放。

</dd> <dt>

<span id="MCI_VD_PLAY_REVERSE"></span><span id="mci_vd_play_reverse"></span>MCI \_ VD \_ 播放 \_ 反向
</dt> <dd>

反向播放。

</dd> <dt>

<span id="MCI_VD_PLAY_SCAN"></span><span id="mci_vd_play_scan"></span>MCI \_ VD \_ PLAY \_ 掃描
</dt> <dd>

快速掃描。

</dd> <dt>

<span id="MCI_VD_PLAY_SLOW"></span><span id="mci_vd_play_slow"></span>MCI \_ VD \_ 播放 \_ 緩慢
</dt> <dd>

慢慢播放。

</dd> <dt>

<span id="MCI_VD_PLAY_SPEED"></span><span id="mci_vd_play_speed"></span>MCI \_ VD \_ 播放 \_ 速度
</dt> <dd>

播放速度會包含在 *lpPlay* 所識別之結構的 **dwSpeed** 成員中。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Mmsystem (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[MCI 命令](mci-commands.md)
</dt> </dl>

 

