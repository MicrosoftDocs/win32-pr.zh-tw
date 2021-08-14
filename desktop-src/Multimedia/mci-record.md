---
title: 'MCI_RECORD 命令 (Mmsystem .h) '
description: MCI \_ 記錄命令會從目前位置或從某個指定位置開始記錄到另一個指定的位置。
ms.assetid: d3c4e8a3-7d81-428e-91d8-d8d63fc0aa02
keywords:
- MCI_RECORD 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_RECORD
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 327b9ed9b138b581bec17d8bfcfe19ae67bb07d59be2781af54e22a85e2133c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117803449"
---
# <a name="mci_record-command"></a>MCI \_ 記錄命令

[**MCI \_ 記錄**](mci-record-parms.md)命令會從目前位置或從某個指定位置開始記錄到另一個指定的位置。 VCR 和波形-音訊裝置會辨識此命令。 雖然數位視訊裝置和 MIDI sequencers 也會辨識此命令，但 MCIAVI 和 MCISEQ 驅動程式並不會執行此命令。

若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_RECORD, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_RECORD_PARMS) lpRecord
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

<span id="lpRecord"></span><span id="lprecord"></span><span id="LPRECORD"></span>*lpRecord*
</dt> <dd>

[**MCI \_ 記錄 \_ PARMS**](mci-record-parms.md)結構的指標。 具有擴充命令集的 (裝置，可能會以裝置特定結構取代此結構。 ) 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

當您使用 MCI  GETDEVCAPS 可以[ \_ ](mci-getdevcaps.md) \_ \_ \_ 記錄旗標呼叫 mci GETDEVCAPS 命令時，會傳回 TRUE 的裝置支援此命令。 針對 MCIWAVE 驅動程式，如果檔案已關閉而不儲存，則會捨棄檔案之後記錄的所有資料。

下列其他旗標適用于所有支援 MCI 記錄的裝置 \_ ：

<dl> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ 來源
</dt> <dd>

起始位置會包含在 *lpRecord* 所識別之結構的 **dwFrom** 成員中。 指派給位置值的單位，會以 Mci 設定的 \_ \_ 時間格式旗標，以 \_ [mci \_ set](mci-set.md) 命令來指定。 如果 \_ 未指定來自的 MCI，開始位置會預設為目前的位置。

</dd> <dt>

<span id="MCI_RECORD_INSERT"></span><span id="mci_record_insert"></span>MCI \_ 記錄 \_ 插入
</dt> <dd>

新記錄的資訊應該插入或貼到現有的資料中。 某些裝置可能不支援這種情況。 如果支援，這是預設值。

</dd> <dt>

<span id="MCI_RECORD_OVERWRITE"></span><span id="mci_record_overwrite"></span>MCI \_ 記錄 \_ 覆寫
</dt> <dd>

資料應覆寫現有的資料。 MCIWAVE。WINSPOOL.DRV 裝置會傳回 MCIERR \_ 不支援的函式以 \_ 回應此旗標。

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ 至
</dt> <dd>

結束位置會包含在由 *lpRecord* 所識別之結構的 **dwTo** 成員中。 指派給位置值的單位，會以 Mci 設定的 \_ \_ 時間格式旗標，以 \_ [mci \_ set](mci-set.md) 命令來指定。 如果 \_ 未指定 MCI 至，結束位置會預設為內容結尾。

</dd> </dl>

下列其他旗標適用于 **digitalvideo** 裝置類型：

<dl> <dt>

<span id="MCI_DGV_RECORD_AUDIO_STREAM"></span><span id="mci_dgv_record_audio_stream"></span>MCI \_ DGV \_ 錄製 \_ 音訊 \_ 串流
</dt> <dd>

音訊串流號碼包含在 *lpRecord* 所識別之結構的 **dwAudioStream** 成員中。 如果您省略此旗標，則會將音訊資料記錄到第一個實體資料流程中。

</dd> <dt>

<span id="MCI_DGV_RECORD_HOLD"></span><span id="mci_dgv_record_hold"></span>MCI \_ DGV \_ 記錄 \_ 保存
</dt> <dd>

錄製停止時，畫面將會保留最後一個影像，而且在發出 [MCI \_ 監視器](mci-monitor.md) 命令之前，將不會繼續顯示影片。

</dd> <dt>

<span id="MCI_DGV_RECORD_VIDEO_STREAM"></span><span id="mci_dgv_record_video_stream"></span>MCI \_ DGV \_ 錄製 \_ 影片 \_ 串流
</dt> <dd>

影片串流號碼包含在 *lpRecord* 所識別之結構的 **dwVideoStream** 成員中。 如果您省略此旗標，則會將影片資料記錄到第一個實體串流中。

</dd> <dt>

<span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI \_ DGV \_ RECT
</dt> <dd>

在 *lpRecord* 所識別之結構的 **rc** 成員中指定矩形。 矩形會指定外部輸入的區域，做為壓縮和儲存的圖元來源。 這個矩形預設為 DGV 所指定的矩形 (或預設) 由 mci \_ put 命令的 mci \_ PUT \_ 影片旗標。 [ \_ ](mci-put.md) 當其設定方式不同于影片矩形時，顯示的內容不是錄製的內容

</dd> </dl>

針對數位影片裝置， *lpRecord* 會指向 [**MCI \_ DGV \_ 記錄 \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_record_parms) 結構。

下列其他旗標適用于 **vcr** 裝置類型：

<dl> <dt>

<span id="MCI_VCR_RECORD_AT"></span><span id="mci_vcr_record_at"></span>MCI \_ VCR \_ 記錄 \_ 于
</dt> <dd>

*LpRecord* 所識別之結構的 **dwAt** 成員，包含整個命令開始的時間，或如果裝置是 cued，則會在裝置到達提示命令所提供的位置時。

</dd> <dt>

<span id="MCI_VCR_RECORD_INITIALIZE"></span><span id="mci_vcr_record_initialize"></span>MCI \_ VCR \_ 記錄 \_ 初始化
</dt> <dd>

將裝置搜尋至媒體的開頭，開始錄製空白的影片和音訊，以及記錄時間碼（如果可能的話）。

</dd> </dl>

若為 VCR 裝置， *lpRecord* 會指向 [**MCI \_ VCR \_ 記錄 \_ PARMS**](mci-vcr-record-parms.md) 結構。

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

[MCI 命令](mci-commands.md)
</dt> </dl>

 

