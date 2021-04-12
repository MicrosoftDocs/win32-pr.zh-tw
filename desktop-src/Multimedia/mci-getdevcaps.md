---
title: 'MCI_GETDEVCAPS 命令 (Mmsystem .h) '
description: MCI \_ GETDEVCAPS 命令會捕獲裝置的靜態資訊。
ms.assetid: a839006f-ea57-4595-9208-cfc465c95298
keywords:
- MCI_GETDEVCAPS 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_GETDEVCAPS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85abb0354d36979741d0b292dd9def469cec0049
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509419"
---
# <a name="mci_getdevcaps-command"></a>MCI \_ GETDEVCAPS 命令

MCI \_ GETDEVCAPS 命令會捕獲裝置的靜態資訊。 所有裝置都會辨識此命令。 適用于此命令的參數和旗標取決於選取的裝置。 資訊會以 *lpCapsParms* 所識別之結構的 **dwReturn** 成員傳回。

若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_GETDEVCAPS, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GETDEVCAPS_PARMS) lpCapsParms
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

<span id="lpCapsParms"></span><span id="lpcapsparms"></span><span id="LPCAPSPARMS"></span>*lpCapsParms*
</dt> <dd>

[**MCI \_ GETDEVCAPS \_ PARMS**](mci-getdevcaps-parms.md)結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

下列其他標準和命令特定旗標適用于所有支援 MCI GETDEVCAPS 的裝置 \_ ：

<dl> <dt>

<span id="MCI_GETDEVCAPS_COMPOUND_DEVICE"></span><span id="mci_getdevcaps_compound_device"></span>MCI \_ GETDEVCAPS \_ 複合 \_ 裝置
</dt> <dd>

如果裝置使用必須明確開啟和關閉的資料儲存體， **dwReturn** 成員會設定為 **TRUE** 。否則會設為 **FALSE** 。

</dd> <dt>

<span id="MCI_GETDEVCAPS_DEVICE_TYPE"></span><span id="mci_getdevcaps_device_type"></span>MCI \_ GETDEVCAPS \_ 裝置 \_ 類型
</dt> <dd>

**DwReturn** 成員會設定為 [ [MCI 裝置類型](mci-device-types.md)] 中所列的其中一個值。

</dd> <dt>

<span id="MCI_GETDEVCAPS_HAS_AUDIO"></span><span id="mci_getdevcaps_has_audio"></span>MCI \_ GETDEVCAPS \_ 有 \_ 音訊
</dt> <dd>

如果裝置有音訊輸出， **dwReturn** 成員會設定為 **TRUE** ;否則會設為 **FALSE** 。

</dd> <dt>

<span id="MCI_GETDEVCAPS_HAS_VIDEO"></span><span id="mci_getdevcaps_has_video"></span>MCI \_ GETDEVCAPS \_ 有 \_ 影片
</dt> <dd>

如果裝置有影片輸出， **dwReturn** 成員會設定為 **TRUE** 。否則會設為 **FALSE** 。 例如，針對支援 videodisc 命令集的裝置，此成員會設定為 **TRUE** 。

</dd> <dt>

<span id="MCI_GETDEVCAPS_ITEM"></span><span id="mci_getdevcaps_item"></span>MCI \_ GETDEVCAPS \_ 專案
</dt> <dd>

指定 [**MCI \_ GETDEVCAPS \_ PARMS**](mci-getdevcaps-parms.md)結構的 **dwItem** 成員包含下列其中一個常數：

</dd> <dt>

<span id="MCI_GETDEVCAPS_CAN_EJECT"></span><span id="mci_getdevcaps_can_eject"></span>MCI \_ GETDEVCAPS \_ 可以 \_ 退出
</dt> <dd>

如果裝置可以退出媒體， **dwReturn** 成員會設定為 **TRUE** 。否則，它會設為 **FALSE**。

</dd> <dt>

<span id="MCI_GETDEVCAPS_CAN_PLAY"></span><span id="mci_getdevcaps_can_play"></span>MCI \_ GETDEVCAPS \_ 可以 \_ 播放
</dt> <dd>

如果裝置可以播放媒體， **dwReturn** 成員會設定為 **TRUE** 。否則，它會設為 **FALSE**。 如果裝置指定 **為 TRUE**，表示裝置支援 [Mci \_ PAUSE](mci-pause.md) 和 [mci \_ STOP](mci-stop.md) 命令，以及 [mci \_ PLAY](mci-play.md) 命令。

</dd> <dt>

<span id="MCI_GETDEVCAPS_CAN_RECORD"></span><span id="mci_getdevcaps_can_record"></span>MCI \_ GETDEVCAPS \_ 可以 \_ 記錄
</dt> <dd>

如果裝置支援錄製， **dwReturn** 成員會設定為 **TRUE** 。否則，它會設為 **FALSE**。 如果裝置指定 **為 TRUE**，表示裝置支援 mci \_ PAUSE 和 mci \_ STOP 命令，以及 [mci \_ 記錄](mci-record.md) 命令。

</dd> <dt>

<span id="MCI_GETDEVCAPS_CAN_SAVE"></span><span id="mci_getdevcaps_can_save"></span>MCI \_ GETDEVCAPS \_ 可以 \_ 節省
</dt> <dd>

如果裝置可以儲存檔案， **dwReturn** 成員會設定為 **TRUE** ;否則，它會設為 **FALSE**。

</dd> <dt>

<span id="MCI_GETDEVCAPS_USES_FILES"></span><span id="mci_getdevcaps_uses_files"></span>MCI \_ GETDEVCAPS \_ 使用 \_ 檔案
</dt> <dd>

如果裝置需要檔案名， **dwReturn** 成員會設定為 **TRUE** ;否則會設為 **FALSE** 。 只有複合裝置會使用檔案。

</dd> </dl>

下列旗標可指定于 **digitalvideo** 裝置類型的 [**MCI \_ GETDEVCAPS \_ PARMS**](mci-getdevcaps-parms.md)的 **dwItem** 成員中：

<dl> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_dgv_getdevcaps_can_freeze"></span>MCI \_ DGV \_ GETDEVCAPS \_ 可以 \_ 凍結
</dt> <dd>

如果裝置可以凍結畫面格， **dwReturn** 成員會設定為 **TRUE** 。否則，它會設為 **FALSE**。

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_LOCK"></span><span id="mci_dgv_getdevcaps_can_lock"></span>MCI \_ DGV \_ GETDEVCAPS \_ 可以 \_ 鎖定
</dt> <dd>

如果裝置可以鎖定， **dwReturn** 成員會設定為 **TRUE** ;否則，它會設為 **FALSE**。

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_dgv_getdevcaps_can_reverse"></span>MCI \_ DGV \_ GETDEVCAPS \_ 可以 \_ 反轉
</dt> <dd>

如果裝置可以反向播放， **dwReturn** 成員會設定為 **TRUE** ;否則，它會設為 **FALSE**。

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_STR_IN"></span><span id="mci_dgv_getdevcaps_can_str_in"></span>MCI \_ DGV \_ GETDEVCAPS \_ 可以是 \_ STR \_
</dt> <dd>

如果裝置可以延展輸入， **dwReturn** 成員會設定為 **TRUE** 。否則，它會設為 **FALSE**。

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_dgv_getdevcaps_can_stretch"></span>MCI \_ DGV \_ GETDEVCAPS \_ 可以 \_ 延展
</dt> <dd>

如果裝置可以延展影像， **dwReturn** 成員會設定為 **TRUE** 。否則，它會設為 **FALSE**。

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_TEST"></span><span id="mci_dgv_getdevcaps_can_test"></span>MCI \_ DGV \_ GETDEVCAPS \_ 可以 \_ 測試
</dt> <dd>

如果裝置可以執行測試， **dwReturn** 成員會設定為 **TRUE** 。否則，它會設為 **FALSE**。

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_HAS_STILL"></span><span id="mci_dgv_getdevcaps_has_still"></span>MCI \_ DGV \_ GETDEVCAPS \_ \_ 還在
</dt> <dd>

如果裝置可以顯示仍是影像， **dwReturn** 成員會設定為 **TRUE** 。否則，它會設為 **FALSE**。

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_dgv_getdevcaps_max_windows"></span>MCI \_ DGV \_ GETDEVCAPS \_ MAX \_ WINDOWS
</dt> <dd>

**DwReturn** 成員會設定為裝置可同時處理的最大視窗數目。

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_MAXIMUM_RATE"></span><span id="mci_dgv_getdevcaps_maximum_rate"></span>MCI \_ DGV \_ GETDEVCAPS \_ 最大 \_ 速率
</dt> <dd>

**DwReturn** 成員會設定為裝置的最大播放速率（以每秒畫面格數為單位）。

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_MINIMUM_RATE"></span><span id="mci_dgv_getdevcaps_minimum_rate"></span>MCI \_ DGV \_ GETDEVCAPS \_ 最低 \_ 費率
</dt> <dd>

**DwReturn** 成員會設定為裝置的最小播放速率（以每秒畫面格數為單位）。

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_PALETTES"></span><span id="mci_dgv_getdevcaps_palettes"></span>MCI \_ DGV \_ GETDEVCAPS \_ 調色板
</dt> <dd>

如果裝置可以傳回檔色板控制碼， **dwReturn** 成員會設定為 **TRUE** 。否則，它會設為 **FALSE**。

</dd> </dl>

您可以在適用于 **vcr** 裝置類型的 [**MCI \_ GETDEVCAPS \_ PARMS**](mci-getdevcaps-parms.md)的 **dwItem** 成員中指定下列旗標：

<dl> <dt>

<span id="MCI_GETDEVCAPS_CLOCK_INCREMENT_RATE"></span><span id="mci_getdevcaps_clock_increment_rate"></span>MCI \_ GETDEVCAPS \_ 時鐘 \_ 遞增 \_ 率
</dt> <dd>

**DwReturn** 成員會設定為每秒的遞增數目。

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_DETECT_LENGTH"></span><span id="mci_vcr_getdevcaps_can_detect_length"></span>MCI \_ VCR \_ GETDEVCAPS \_ 可以偵測 \_ 到 \_ 長度
</dt> <dd>

如果裝置能夠偵測媒體的長度， **dwReturn** 成員會設定為 **TRUE** 。否則，它會設為 **FALSE**。

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_vcr_getdevcaps_can_freeze"></span>MCI \_ VCR \_ GETDEVCAPS \_ 可以 \_ 凍結
</dt> <dd>

如果裝置能夠凍結輸出影像， **dwReturn** 成員會設定為 **TRUE** 。否則，它會設為 **FALSE**。

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_MONITOR_SOURCES"></span><span id="mci_vcr_getdevcaps_can_monitor_sources"></span>MCI \_ VCR \_ GETDEVCAPS \_ 可以 \_ 監視 \_ 來源
</dt> <dd>

如果裝置能夠監視來源， **dwReturn** 成員會設定為 **TRUE** ;否則，它會設為 **FALSE**。

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_PREROLL"></span><span id="mci_vcr_getdevcaps_can_preroll"></span>MCI \_ VCR \_ GETDEVCAPS \_ 可以預先進行 \_
</dt> <dd>

如果裝置可以預先進行， **dwReturn** 成員會設定為 **TRUE** ;否則，它會設為 **FALSE**。

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_PREVIEW"></span><span id="mci_vcr_getdevcaps_can_preview"></span>MCI \_ VCR \_ GETDEVCAPS \_ 可以 \_ 預覽
</dt> <dd>

如果裝置能夠進行預覽， **dwReturn** 成員會設定為 **TRUE** ;否則，它會設為 **FALSE**。

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vcr_getdevcaps_can_reverse"></span>MCI \_ VCR \_ GETDEVCAPS \_ 可以 \_ 反轉
</dt> <dd>

如果裝置能夠反向播放， **dwReturn** 成員會設定為 **TRUE** ;否則，它會設為 **FALSE**。

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_TEST"></span><span id="mci_vcr_getdevcaps_can_test"></span>MCI \_ VCR \_ GETDEVCAPS \_ 可以 \_ 測試
</dt> <dd>

如果裝置能夠測試， **dwReturn** 成員會設定為 **TRUE** ;否則，它會設為 **FALSE**。

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_HAS_CLOCK"></span><span id="mci_vcr_getdevcaps_has_clock"></span>MCI \_ VCR \_ GETDEVCAPS \_ 有 \_ 時鐘
</dt> <dd>

如果裝置支援外部時鐘， **dwReturn** 成員會設定為 **TRUE** 。否則，它會設為 **FALSE**。

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_HAS_TIMECODE"></span><span id="mci_vcr_getdevcaps_has_timecode"></span>MCI \_ VCR \_ GETDEVCAPS \_ 有時間 \_ 碼
</dt> <dd>

如果裝置具有時間碼功能或這項功能未知， **dwReturn** 成員會設定為 **TRUE** 。否則，它會設為 **FALSE**。

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_NUMBER_OF_MARKS"></span><span id="mci_vcr_getdevcaps_number_of_marks"></span>MCI \_ VCR \_ GETDEVCAPS \_ \_ 標記數目 \_
</dt> <dd>

**DwReturn** 成員會設定為 (99) 的標記數目。

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_SEEK_ACCURACY"></span><span id="mci_vcr_getdevcaps_seek_accuracy"></span>MCI \_ VCR \_ GETDEVCAPS \_ 搜尋 \_ 精確度
</dt> <dd>

**DwReturn** 成員會設定為裝置的搜尋精確度。

</dd> </dl>

下列旗標可在「 [**MCI \_ GETDEVCAPS \_ PARMS**](mci-getdevcaps-parms.md)的 **dwItem** 成員中，針對重 **迭裝置類型** 指定：

<dl> <dt>

<span id="MCI_OVLY_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_ovly_getdevcaps_can_freeze"></span>MCI \_ OVLY \_ GETDEVCAPS \_ 可以 \_ 凍結
</dt> <dd>

如果裝置可以凍結映射， **dwReturn** 成員會設定為 **TRUE** 。否則，它會設為 **FALSE**。

</dd> <dt>

<span id="MCI_OVLY_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_ovly_getdevcaps_can_stretch"></span>MCI \_ OVLY \_ GETDEVCAPS \_ 可以 \_ 延展
</dt> <dd>

如果裝置可以延展影像以填滿框架， **dwReturn** 成員會設定為 **TRUE** 。否則，它會設為 **FALSE**。

</dd> <dt>

<span id="MCI_OVLY_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_ovly_getdevcaps_max_windows"></span>MCI \_ OVLY \_ GETDEVCAPS \_ MAX \_ WINDOWS
</dt> <dd>

**DwReturn** 成員會設定為裝置可同時處理的最大視窗數目。

</dd> </dl>

下列旗標可指定于 **videodisc** 裝置類型的 [**MCI \_ GETDEVCAPS \_ PARMS**](mci-getdevcaps-parms.md)的 **dwItem** 成員中：

<dl> <dt>

<span id="MCI_VD_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vd_getdevcaps_can_reverse"></span>MCI \_ VD \_ GETDEVCAPS \_ 可以 \_ 反轉
</dt> <dd>

如果 videodisc 播放程式可以反向播放， **dwReturn** 成員會設定為 **TRUE** ;否則，它會設為 **FALSE**。 有些玩家可以反向播放 CLV 光碟以及 CAV 光碟。

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_CAV"></span><span id="mci_vd_getdevcaps_cav"></span>MCI \_ VD \_ GETDEVCAPS \_ CAV
</dt> <dd>

與其他專案結合時，會指定傳回信息適用于 CAV 格式 videodiscs。 如果未插入任何 videodisc，則這是預設值。

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_CLV"></span><span id="mci_vd_getdevcaps_clv"></span>MCI \_ VD \_ GETDEVCAPS \_ CLV
</dt> <dd>

與其他專案結合時，會指定傳回信息適用于 CLV 格式 videodiscs。

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_FAST_RATE"></span><span id="mci_vd_getdevcaps_fast_rate"></span>MCI \_ VD \_ GETDEVCAPS \_ FAST \_ RATE
</dt> <dd>

**DwReturn** 成員會設定為每秒畫面格的標準快速播放速率。

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_NORMAL_RATE"></span><span id="mci_vd_getdevcaps_normal_rate"></span>MCI \_ VD \_ GETDEVCAPS \_ 一般 \_ 費率
</dt> <dd>

**DwReturn** 成員會設定為每秒畫面格的正常播放速率。

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_SLOW_RATE"></span><span id="mci_vd_getdevcaps_slow_rate"></span>MCI \_ VD \_ GETDEVCAPS \_ 低速 \_ 率
</dt> <dd>

**DwReturn** 成員會設定為每秒畫面格的標準慢速播放速率。

</dd> </dl>

下列旗標可指定于 **waveaudio** 裝置類型的 [**MCI \_ GETDEVCAPS \_ PARMS**](mci-getdevcaps-parms.md)的 **dwItem** 成員中：

<dl> <dt>

<span id="MCI_WAVE_GETDEVCAPS_INPUT"></span><span id="mci_wave_getdevcaps_input"></span>MCI \_ WAVE \_ GETDEVCAPS \_ 輸入
</dt> <dd>

**DwReturn** 成員會設定為錄製) 裝置 (的波形輸入總數。

</dd> <dt>

<span id="MCI_WAVE_GETDEVCAPS_OUTPUT"></span><span id="mci_wave_getdevcaps_output"></span>MCI \_ WAVE \_ GETDEVCAPS \_ 輸出
</dt> <dd>

**DwReturn** 成員會設定為 (播放) 裝置的波形輸出總數。

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

 

