---
title: 'MCI_SET 命令 (Mmsystem .h) '
description: MCI \_ SET 命令會設定裝置資訊。 CD 音訊、數位影片、MIDI sequencer、VCR、videodisc、影片重迭和波形音訊裝置都會辨識此命令。
ms.assetid: c527f9d6-2119-4274-98b7-dc892e9b70f9
keywords:
- MCI_SET 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_SET
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e1da0da94c0d970b607a29548c773fa9302d26d
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/12/2021
ms.locfileid: "106997290"
---
# <a name="mci_set-command"></a>MCI \_ SET 命令

> [!NOTE]
> 無偏差的通訊-Microsoft 支援多樣化且 inclusionary 的環境。  本檔中有 ' 從屬 ' 這個字的參考。 Microsoft 的 [Bias-Free 通訊樣式指南](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) 會將此視為排他性行為單字。  這種用語是用來做為命令內所使用的用語。 為求一致，本檔包含此字。 當您在命令中更改這個字時，我們會將此檔修正為一致。

MCI \_ SET 命令會設定裝置資訊。 CD 音訊、數位影片、MIDI sequencer、VCR、videodisc、影片重迭和波形音訊裝置都會辨識此命令。

若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SET, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SET_PARMS) lpSet
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

<span id="lpSet"></span><span id="lpset"></span><span id="LPSET"></span>*lpSet*
</dt> <dd>

[**MCI \_ 設定 \_ PARMS**](mci-set-parms.md)結構的指標。 具有擴充命令集的 (裝置，可能會以裝置特定結構取代此結構。 ) 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

下列其他旗標適用于所有支援 MCI 設定的裝置 \_ ：

<dl> <dt>

<span id="MCI_SET_AUDIO"></span><span id="mci_set_audio"></span>MCI \_ 組 \_ 音訊
</dt> <dd>

音訊頻道號碼會包含在由 *lpSet* 所識別之結構的 dwAudio 成員中。 此旗標必須與設定為 \_ \_ ON 或 mci \_ OFF 的 mci 一起使用 \_ 。 使用下列其中一個常數來表示通道號碼：

</dd> <dt>

<span id="MCI_SET_AUDIO_ALL"></span><span id="mci_set_audio_all"></span>MCI \_ 設定 \_ 音訊 \_ 全部
</dt> <dd>

所有音訊頻道。

</dd> <dt>

<span id="MCI_SET_AUDIO_LEFT"></span><span id="mci_set_audio_left"></span>剩餘的 MCI \_ 組 \_ 音訊 \_
</dt> <dd>

左聲道。

</dd> <dt>

<span id="MCI_SET_AUDIO_RIGHT"></span><span id="mci_set_audio_right"></span>MCI \_ 設定 \_ 音訊 \_ 許可權
</dt> <dd>

右聲道。

</dd> <dt>

<span id="MCI_SET_DOOR_CLOSED"></span><span id="mci_set_door_closed"></span>MCI \_ 設定 \_ 門 \_ 已關閉
</dt> <dd>

關閉媒體蓋 (是否有任何) 。

</dd> <dt>

<span id="MCI_SET_DOOR_OPEN"></span><span id="mci_set_door_open"></span>MCI \_ 設定 \_ 門 \_ 開啟
</dt> <dd>

開啟媒體蓋 (（如果有任何) ）。

</dd> <dt>

<span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>已 \_ 設定 \_ MCI
</dt> <dd>

停用指定的影片或音訊頻道。

</dd> <dt>

<span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ 設定 \_ 于
</dt> <dd>

啟用指定的影片或音訊頻道。

</dd> <dt>

<span id="MCI_SET_TIME_FORMAT"></span><span id="mci_set_time_format"></span>MCI \_ 設定 \_ 時間 \_ 格式
</dt> <dd>

時間格式參數會包含在 *lpSet* 所識別之結構的 **dwTimeFormat** 成員中。 下列旗標可搭配此旗標使用：

</dd> <dt>

<span id="MCI_FORMAT_BYTES"></span><span id="mci_format_bytes"></span>MCI \_ 格式 \_ 位元組
</dt> <dd>

在 PCM (脈衝程式碼調製) 資料格式，將時間成員描述變更為輸入或輸出的位元組。 由 **waveaudio** 裝置類型辨識。

</dd> <dt>

<span id="MCI_FORMAT_FRAMES"></span><span id="mci_format_frames"></span>MCI \_ 格式 \_ 框架
</dt> <dd>

後續的命令將會使用框架。 由 **digitalvideo**、 **vcr** 和 **videodisc** 裝置類型辨識。

</dd> <dt>

<span id="MCI_FORMAT_HMS"></span><span id="mci_format_hms"></span>MCI \_ 格式 \_ HMS
</dt> <dd>

將時間格式變更為小時、分鐘和秒。 由 **vcr** 和 **videodisc** 裝置類型辨識。

</dd> <dt>

<span id="MCI_FORMAT_MILLISECONDS"></span><span id="mci_format_milliseconds"></span>MCI \_ 格式 \_ 毫秒
</dt> <dd>

將時間格式變更為毫秒。 所有裝置類型都能辨識。

</dd> <dt>

<span id="MCI_FORMAT_MSF"></span><span id="mci_format_msf"></span>MCI \_ 格式 \_ MSF
</dt> <dd>

將時間格式變更為分鐘、秒和框架。 **Cdaudio** 和 **vcr** 裝置類型的辨識。

</dd> <dt>

<span id="MCI_FORMAT_SAMPLES"></span><span id="mci_format_samples"></span>MCI \_ 格式 \_ 範例
</dt> <dd>

將時間格式變更為輸入或輸出的範例。 由 **waveaudio** 裝置類型辨識。

</dd> <dt>

<span id="MCI_FORMAT_SMPTE_24__MCI_FORMAT_SMPTE_25__and_MCI_FORMAT_SMPTE_30"></span><span id="mci_format_smpte_24__mci_format_smpte_25__and_mci_format_smpte_30"></span><span id="MCI_FORMAT_SMPTE_24__MCI_FORMAT_SMPTE_25__AND_MCI_FORMAT_SMPTE_30"></span>MCI \_ 格式 \_ \_ 的 SMPTE 24、 \_ MCI \_ 格式 \_ 的 smpte 25 以及 mci \_ 格式的 \_ smpte \_ 30
</dt> <dd>

將時間格式設定為24、25和30個框架 SMPTE (社會的運動圖片和電視工程師分別) 。 由 **sequencer** 和 **vcr** 裝置類型辨識。

</dd> <dt>

<span id="MCI_FORMAT_SMPTE_30DROP"></span><span id="mci_format_smpte_30drop"></span>MCI \_ 格式的 \_ SMPTE \_ 30DROP
</dt> <dd>

將時間格式設定為30個放置畫面的 SMPTE。 由 **sequencer** 和 **vcr** 裝置類型辨識。

</dd> <dt>

<span id="MCI_FORMAT_TMSF"></span><span id="mci_format_tmsf"></span>MCI \_ 格式 \_ TMSF
</dt> <dd>

變更時間格式以追蹤、分、秒和框架。  (MCI 使用連續的追蹤號碼。 ) 由 **cdaudio** 和 **vcr** 裝置類型辨識。

</dd> <dt>

<span id="MCI_SET_VIDEO"></span><span id="mci_set_video"></span>MCI \_ 設定 \_ 影片
</dt> <dd>

設定開啟或關閉的視訊訊號。 此旗標必須與 \_ 設定為 \_ ON 或 mci OFF 的 \_ mci 一起使用 \_ 。 沒有影片的裝置會傳回 MCIERR \_ 不支援 \_ 的功能。

</dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> </dl>

下列其他旗標適用于 **digitalvideo** 裝置類型：

<dl> <dt>

<span id="MCI_DGV_SET_FILEFORMAT"></span><span id="mci_dgv_set_fileformat"></span>MCI \_ DGV \_ SET \_ >FILEFORMAT
</dt> <dd>

檔案格式參數會包含在 *lpSet* 所識別之結構的 **dwFileFormat** 成員中。 若為數位視訊裝置，則會使用檔案格式來儲存或捕捉命令。 如果省略此參數，則可能會預設為設備磁碟機定義的格式。 如果指定的檔案格式與目前選取的演算法和品質相衝突，則會將它們變更為檔案格式的預設值。 以下是定義的檔案格式常數：

</dd> <dt>

<span id="MCI_DGV_FF_AVI"></span><span id="mci_dgv_ff_avi"></span>MCI \_ DGV \_ FF \_ AVI
</dt> <dd>

AVI 格式。

</dd> <dt>

<span id="MCI_DGV_FF_AVSS"></span><span id="mci_dgv_ff_avss"></span>MCI \_ DGV \_ FF \_ AVSS
</dt> <dd>

AVSS 格式。

</dd> <dt>

<span id="MCI_DGV_FF_DIB"></span><span id="mci_dgv_ff_dib"></span>MCI \_ DGV \_ FF \_ DIB
</dt> <dd>

DIB 格式。

</dd> <dt>

<span id="MCI_DGV_FF_JFIF"></span><span id="mci_dgv_ff_jfif"></span>MCI \_ DGV \_ FF \_ JFIF
</dt> <dd>

JFIF 格式。

</dd> <dt>

<span id="MCI_DGV_FF_JPEG"></span><span id="mci_dgv_ff_jpeg"></span>MCI \_ DGV \_ FF \_ JPEG
</dt> <dd>

JPEG 格式。

</dd> <dt>

<span id="MCI_DGV_FF_MPEG"></span><span id="mci_dgv_ff_mpeg"></span>MCI \_ DGV \_ FF \_ MPEG
</dt> <dd>

MPEG 格式。

</dd> <dt>

<span id="MCI_DGV_FF_RDIB"></span><span id="mci_dgv_ff_rdib"></span>MCI \_ DGV \_ FF \_ RDIB
</dt> <dd>

RLE DIB 格式。

</dd> <dt>

<span id="MCI_DGV_FF_RJPEG"></span><span id="mci_dgv_ff_rjpeg"></span>MCI \_ DGV \_ FF \_ RJPEG
</dt> <dd>

RJPEG 格式。

</dd> <dt>

<span id="MCI_DGV_SET_SEEK_EXACTLY"></span><span id="mci_dgv_set_seek_exactly"></span>MCI \_ DGV \_ \_ \_ 精確地設定搜尋
</dt> <dd>

設定用於定位的格式。 此旗標必須與設定為 \_ \_ ON 或 mci \_ OFF 的 mci 一起使用 \_ 。 如果 \_ \_ 指定了 mci 設定，則播放或錄製會精確地從旗標存取以 mci 指定的框架 \_ 。 如果要求的框架不是主要畫面格，這可能會增加一些額外的延遲。 如果 \_ \_ 指定了 MCI 設定，裝置將會搜尋在要求的框架之前的主要畫面格影像。 針對某些檔案和裝置，這可能是檔案的第一個畫面格。 此旗標的預設值是裝置相依的。

</dd> <dt>

<span id="MCI_DGV_SET_SPEED"></span><span id="mci_dgv_set_speed"></span>MCI \_ DGV \_ 設定 \_ 速度
</dt> <dd>

速度參數會包含在由 *lpSet* 所識別之結構的 **dwSpeed** 成員中。 速度會指定為名義畫面播放速率與所需畫面播放速率之間的比率，其中名義畫面播放速率會指定為1000。 半速度是500，而雙速度是2000。 允許的速度範圍也取決於裝置，也可能是檔案。

</dd> <dt>

<span id="MCI_DGV_SET_STILL"></span><span id="mci_dgv_set_still"></span>\_ \_ 尚未設定 MCI \_ DGV
</dt> <dd>

搭配 MCI \_ DGV \_ set >fileformat 使用時 \_ ，mci \_ 集會設定用於 capture 命令的檔案格式。

</dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> </dl>

針對數位影片裝置， *lpSet* 參數會指向 [**MCI \_ DGV \_ SET \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_set_parms) 結構。

下列其他旗標會搭配 **sequencer** 裝置類型使用：

<dl> <dt>

<span id="MCI_SEQ_FORMAT_SONGPTR"></span><span id="mci_seq_format_songptr"></span>MCI \_ SEQ \_ 格式 \_ SONGPTR
</dt> <dd>

將時間格式設定為歌曲指標單位。

</dd> <dt>

<span id="MCI_SEQ_SET_MASTER"></span><span id="mci_seq_set_master"></span>MCI \_ SEQ \_ SET \_ MASTER
</dt> <dd>

將 sequencer 設定為同步處理資料的來源，並指出在 *lpSet* 所識別之結構的 **dwMaster** 成員中指定同步處理的類型。 MCISEQ 傳回 MCIERR \_ 不支援 \_ 的函數。 以下是針對同步處理類型定義的常數：

</dd> <dt>

<span id="MCI_SEQ_MIDI"></span><span id="mci_seq_midi"></span>MCI \_ SEQ \_ MIDI
</dt> <dd>

Sequencer 會傳送 MIDI 格式同步處理資料。

</dd> <dt>

<span id="MCI_SEQ_SMPTE"></span><span id="mci_seq_smpte"></span>MCI \_ SEQ \_ SMPTE
</dt> <dd>

Sequencer 會傳送 SMPTE 格式的同步處理資料。

</dd> <dt>

<span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI \_ SEQ \_ 無
</dt> <dd>

Sequencer 不會傳送同步處理資料。

</dd> <dt>

<span id="MCI_SEQ_SET_OFFSET"></span><span id="mci_seq_set_offset"></span>MCI \_ SEQ \_ SET \_ OFFSET
</dt> <dd>

將序列的 SMPTE 位移變更為由 *lpSet* 所識別之結構的 **dwOffset** 成員所指定的。 這只會影響具有 SMPTE 除法類型的序列。

</dd> <dt>

<span id="MCI_SEQ_SET_PORT"></span><span id="mci_seq_set_port"></span>MCI \_ SEQ \_ 設定 \_ 埠
</dt> <dd>

將序列的輸出 MIDI 埠設定為 *lpSet* 所識別結構之 **dwPort** 成員中的 MIDI 裝置識別碼所指定的。 裝置會關閉先前的埠 (如果有任何) ，然後嘗試開啟並使用新的埠。 如果失敗，則會傳回錯誤，並重新開啟先前使用的埠 (如果有任何) 。 針對埠定義了下列常數：

</dd> <dt>

<span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI \_ SEQ \_ 無
</dt> <dd>

關閉先前使用的埠 (是否有任何) 。 如果埠已開啟，sequencer 的行為就會完全相同，但不會傳送任何 MIDI 訊息。

</dd> <dt>

<span id="MIDI_MAPPER"></span><span id="midi_mapper"></span>MIDI \_ 對應程式
</dt> <dd>

將開啟的埠設定為 MIDI 對應程式。

</dd> <dt>

<span id="MCI_SEQ_SET_SLAVE"></span><span id="mci_seq_set_slave"></span>MCI \_ SEQ \_ SET \_ 從屬
</dt> <dd>

設定 sequencer 以接收同步處理資料，並指出同步處理的類型是在由 *lpSet* 所識別之結構的 **dwSlave** 成員中指定。 MCISEQ 傳回 MCIERR \_ 不支援 \_ 的函數。 以下是針對同步處理類型定義的常數：

</dd> <dt>

<span id="MCI_SEQ_FILE"></span><span id="mci_seq_file"></span>MCI \_ SEQ \_ 檔案
</dt> <dd>

設定 sequencer 以接收包含在 MIDI 檔案中的同步處理資料。

</dd> <dt>

<span id="MCI_SEQ_MIDI"></span><span id="mci_seq_midi"></span>MCI \_ SEQ \_ MIDI
</dt> <dd>

設定 sequencer 以接收 MIDI 同步處理資料。

</dd> <dt>

<span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI \_ SEQ \_ 無
</dt> <dd>

將 sequencer 設定為忽略 MIDI 資料流程中的同步處理資料。

</dd> <dt>

<span id="MCI_SEQ_SMPTE"></span><span id="mci_seq_smpte"></span>MCI \_ SEQ \_ SMPTE
</dt> <dd>

設定 sequencer 以接收 SMPTE 同步處理資料。

</dd> <dt>

<span id="MCI_SEQ_SET_TEMPO"></span><span id="mci_seq_set_tempo"></span>MCI \_ SEQ \_ SET \_ 節奏
</dt> <dd>

將 MIDI 序列的節奏變更為 *lpSet* 所指向之結構的 **dwTempo** 成員所指定的。 若為除法別為 PPQN 的序列，則會在每分鐘的節拍中指定節奏;針對具有範圍類型為 SMPTE 的序列，節奏是以每秒的畫面格來指定。

</dd> </dl>

針對 sequencer 裝置， *lpSet* 參數會指向 [**MCI \_ SEQ \_ SET \_ PARMS**](mci-seq-set-parms.md) 結構。

下列其他旗標適用于 **vcr** 裝置類型：

<dl> <dt>

<span id="MCI_VCR_SET_ASSEMBLE_RECORD"></span><span id="mci_vcr_set_assemble_record"></span>MCI \_ VCR \_ 組 \_ 組合 \_ 記錄
</dt> <dd>

將裝置設定為 [組合]、[插入] 和 [) ] 時， (組合或插入模式中記錄。 使用下列其中一個旗標：

</dd> <dt>

<span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ 設定 \_ 于
</dt> <dd>

在上設定組合記錄，並關閉插入記錄。 記錄所有的影片、音訊和時間碼追蹤。

</dd> <dt>

<span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>已 \_ 設定 \_ MCI
</dt> <dd>

將組合記錄關閉，然後開啟插入記錄。 當組合記錄關閉時，可以選取影片、音訊和時間碼的個別曲目來進行錄製。

</dd> <dt>

<span id="MCI_VCR_SET_CLOCK"></span><span id="mci_vcr_set_clock"></span>MCI \_ VCR \_ 設定 \_ 時鐘
</dt> <dd>

*LpSet* 所識別之結構的 **dwClock** 成員包含新的時鐘時間。

</dd> <dt>

<span id="MCI_VCR_SET_COUNTER_FORMA"></span><span id="mci_vcr_set_counter_forma"></span>MCI \_ VCR \_ 組 \_ 計數器 \_ 估價
</dt> <dd>

*LpSet* 所識別之結構的 **dwCounterFormat** 成員包含常數，指定狀態計數器要使用的新計數器時間格式。 如需有效的常數清單，請參閱 \_ \_ \_ 此命令的其他旗標清單中的 MCI 設定時間格式。

</dd> <dt>

<span id="MCI_VCR_SET_COUNTER_VALUE"></span><span id="mci_vcr_set_counter_value"></span>MCI \_ VCR \_ 設定 \_ 計數器 \_ 值
</dt> <dd>

*LpSet* 所識別之結構的 **dwCounterValue** 成員包含新的計數器值。

</dd> <dt>

<span id="MCI_VCR_SET_INDEX"></span><span id="mci_vcr_set_index"></span>MCI \_ VCR \_ 設定 \_ 索引
</dt> <dd>

*LpSet* 所識別之結構的 **dwIndex** 成員包含一個常數，表示螢幕上顯示的內容，而且必須是下列其中一項：

</dd> <dt>

<span id="MCI_VCR_INDEX_COUNTER"></span><span id="mci_vcr_index_counter"></span>MCI \_ VCR \_ 索引 \_ 計數器
</dt> <dd>

顯示計數器。

</dd> <dt>

<span id="MCI_VCR_INDEX_DATE"></span><span id="mci_vcr_index_date"></span>MCI \_ VCR \_ 索引 \_ 日期
</dt> <dd>

顯示日期。

</dd> <dt>

<span id="MCI_VCR_INDEX_TIME"></span><span id="mci_vcr_index_time"></span>MCI \_ VCR \_ 索引 \_ 時間
</dt> <dd>

顯示時間。

</dd> <dt>

<span id="MCI_VCR_INDEX_TIMECODE"></span><span id="mci_vcr_index_timecode"></span>MCI \_ VCR \_ 索引時間 \_ 碼
</dt> <dd>

顯示時間碼。

如需詳細資訊，請參閱 [MCI \_ INDEX](mci-index.md) 命令。

</dd> <dt>

<span id="MCI_VCR_SET_PAUSE_TIMEOUT"></span><span id="mci_vcr_set_pause_timeout"></span>MCI \_ VCR \_ 設定 \_ 暫停 \_ 超時
</dt> <dd>

*LpSet* 所識別之結構的 **dwPauseTimeout** 成員包含 pause 命令的最長持續時間（以毫秒為單位）。

</dd> <dt>

<span id="MCI_VCR_SET_POSTROLL_DURATION"></span><span id="mci_vcr_set_postroll_duration"></span>MCI \_ VCR \_ SET \_ POSTROLL \_ DURATION
</dt> <dd>

*LpSet* 所識別之結構的 **dwPostrollDuration** 成員包含的磁帶長度（以目前的時間格式），在發出 stop 或 pause 命令時，需要用來煞車 VCR 傳輸。

</dd> <dt>

<span id="MCI_VCR_SET_POWER"></span><span id="mci_vcr_set_power"></span>MCI \_ VCR \_ 設定 \_ 電源
</dt> <dd>

設定開啟或關閉電源。 必須搭配下列其中一個旗標使用：

</dd> <dt>

<span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>已 \_ 設定 \_ MCI
</dt> <dd>

關閉電源。

</dd> <dt>

<span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ 設定 \_ 于
</dt> <dd>

開啟電源。

</dd> <dt>

<span id="MCI_VCR_SET_PREROLL_DURATION"></span><span id="mci_vcr_set_preroll_duration"></span>MCI \_ VCR \_ 設定預先進行 \_ \_ 持續時間
</dt> <dd>

由 *lpSet* 所識別之結構的 **dwPrerollDuration** 成員包含以目前時間格式表示的磁帶長度，以穩定 VCR 輸出。

</dd> <dt>

<span id="MCI_VCR_SET_RECORD_FORMAT"></span><span id="mci_vcr_set_record_format"></span>MCI \_ VCR \_ 設定 \_ 記錄 \_ 格式
</dt> <dd>

*LpSet* 所識別之結構的 **dwRecordFormat** 成員包含描述記錄速度的常數，其必須是下列其中一項：

</dd> <dt>

<span id="MCI_VCR_FORMAT_EP"></span><span id="mci_vcr_format_ep"></span>MCI \_ VCR \_ 格式 \_ EP
</dt> <dd>

速度較慢的記錄。

</dd> <dt>

<span id="MCI_VCR_FORMAT_LP"></span><span id="mci_vcr_format_lp"></span>MCI \_ VCR \_ 格式 \_ LP
</dt> <dd>

以中度慢的記錄。

</dd> <dt>

<span id="MCI_VCR_FORMAT_SP"></span><span id="mci_vcr_format_sp"></span>MCI \_ VCR \_ 格式 \_ SP
</dt> <dd>

標準速度的記錄。

</dd> <dt>

<span id="MCI_VCR_SET_SPEED"></span><span id="mci_vcr_set_speed"></span>MCI \_ VCR \_ 設定 \_ 速度
</dt> <dd>

由 *lpSet* 所識別之結構的 **dwSpeed** 成員包含新的速度設定，其中1000是正常的速度、2000是雙速度，而500是半速度等等。

</dd> <dt>

<span id="MCI_VCR_SET_TAPE_LENGTH"></span><span id="mci_vcr_set_tape_length"></span>MCI \_ VCR \_ 設定 \_ 磁帶 \_ 長度
</dt> <dd>

*LpSet* 所識別之結構的 **dwTapeLength** 成員包含磁帶的新長度（前提是磁帶的長度無法偵測）。

</dd> <dt>

<span id="MCI_VCR_SET_TIME_MODE"></span><span id="mci_vcr_set_time_mode"></span>MCI \_ VCR \_ 設定 \_ 時間 \_ 模式
</dt> <dd>

*LpSet* 所識別之結構的 **dwTimeMode** 成員包含一個常數，表示新的位置時間模式。 以下是有效的常數：

</dd> <dt>

<span id="MCI_VCR_TIME_COUNTER"></span><span id="mci_vcr_time_counter"></span>MCI \_ VCR \_ 時間 \_ 計數器
</dt> <dd>

強制裝置以獨佔方式使用計數器。

</dd> <dt>

<span id="MCI_VCR_TIME_DETECT"></span><span id="mci_vcr_time_detect"></span>MCI \_ VCR \_ 時間 \_ 偵測
</dt> <dd>

每次將新的磁帶插入裝置，或模式從尚未就緒變更為就緒時，裝置應該會嘗試判斷磁帶上是否有可用的時間碼。 如果有時間碼可用，請在所有指定位置的後續命令中使用時間碼。 否則，請使用計數器。

</dd> <dt>

<span id="MCI_VCR_TIME_TIMECODE"></span><span id="mci_vcr_time_timecode"></span>MCI \_ VCR \_ 時間時間 \_ 碼
</dt> <dd>

強制裝置僅使用時間碼。

</dd> <dt>

<span id="MCI_VCR_SET_TRACKING"></span><span id="mci_vcr_set_tracking"></span>MCI \_ VCR \_ 組 \_ 追蹤
</dt> <dd>

使用微調調整來微調 VCR 磁帶傳輸的速度，而且必須搭配下列其中一個旗標使用：

</dd> <dt>

<span id="MCI_VCR_PLUS"></span><span id="mci_vcr_plus"></span>MCI \_ VCR \_ PLUS
</dt> <dd>

增加磁帶傳送速率。

</dd> <dt>

<span id="MCI_VCR_MINUS"></span><span id="mci_vcr_minus"></span>MCI \_ VCR \_ 減號
</dt> <dd>

減少磁帶傳送速率。

</dd> <dt>

<span id="MCI_VCR_RESET"></span><span id="mci_vcr_reset"></span>MCI \_ VCR \_ 重設
</dt> <dd>

將追蹤調整傳回到零。

</dd> </dl>

若為 VCR 裝置， *lpSet* 參數會指向 [**MCI \_ VCR \_ 組 \_ PARMS**](mci-vcr-set-parms.md) 結構。

下列其他旗標適用于 **videodisc** 裝置類型：

<dl> <dt>

<span id="MCI_VD_FORMAT_TRACK"></span><span id="mci_vd_format_track"></span>MCI \_ VD \_ 格式 \_ 追蹤
</dt> <dd>

變更追蹤的時間格式。 MCI 使用連續的追蹤號碼。

</dd> </dl>

下列其他旗標適用于 **waveaudio** 裝置類型：

<dl> <dt>

<span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI \_ WAVE \_ 輸入
</dt> <dd>

將用於記錄的輸入設定為 *lpSet* 所識別之結構的 **wInput** 成員。

</dd> <dt>

<span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI \_ WAVE \_ 輸出
</dt> <dd>

設定用來播放 *lpSet* 所識別結構之 **wOutput** 成員的輸出。

</dd> <dt>

<span id="MCI_WAVE_SET_ANYINPUT"></span><span id="mci_wave_set_anyinput"></span>MCI \_ WAVE \_ 設定 \_ ANYINPUT
</dt> <dd>

任何與目前格式相容的 wave 輸入都可以用來錄製。

</dd> <dt>

<span id="MCI_WAVE_SET_ANYOUTPUT"></span><span id="mci_wave_set_anyoutput"></span>MCI \_ WAVE \_ 設定 \_ ANYOUTPUT
</dt> <dd>

任何與目前格式相容的 wave 輸出都可用於播放。

</dd> <dt>

<span id="MCI_WAVE_SET_AVGBYTESPERSEC"></span><span id="mci_wave_set_avgbytespersec"></span>MCI \_ WAVE \_ 設定 \_ AVGBYTESPERSEC
</dt> <dd>

設定用來播放、錄製和儲存至 *lpSet* 所識別結構之 **nAvgBytesPerSec** 成員的每秒位元組數。

</dd> <dt>

<span id="MCI_WAVE_SET_BITSPERSAMPLE"></span><span id="mci_wave_set_bitspersample"></span>MCI \_ WAVE \_ 設定 \_ BITSPERSAMPLE
</dt> <dd>

設定用來播放、錄製和儲存至 *lpSet* 所識別之 PCM 資料格式 **nBitsPerSample** 成員的每個樣本位數。

</dd> <dt>

<span id="MCI_WAVE_SET_BLOCKALIGN"></span><span id="mci_wave_set_blockalign"></span>MCI \_ WAVE \_ 設定 \_ BLOCKALIGN
</dt> <dd>

設定用來播放、錄製和儲存至 *lpSet* 所識別結構之 **nBlockAlign** 成員的區塊對齊。

</dd> <dt>

<span id="MCI_WAVE_SET_CHANNELS"></span><span id="mci_wave_set_channels"></span>MCI \_ WAVE \_ 設定 \_ 通道
</dt> <dd>

通道的數目會以 *lpSet* 所識別之結構的 **nChannels** 成員表示。

</dd> <dt>

<span id="MCI_WAVE_SET_FORMATTAG"></span><span id="mci_wave_set_formattag"></span>MCI \_ WAVE \_ 設定 \_ FORMATTAG
</dt> <dd>

設定用來播放、錄製和儲存至 *lpSet* 所識別結構之 **wFormatTag** 成員的格式類型。 指定 WAVE \_ 格式 \_ PCM 會將格式變更為 pcm。

</dd> <dt>

<span id="MCI_WAVE_SET_SAMPLESPERSEC"></span><span id="mci_wave_set_samplespersec"></span>MCI \_ WAVE \_ 設定 \_ SAMPLESPERSEC
</dt> <dd>

設定用來播放、錄製和儲存至 *lpSet* 所識別結構之 **nSamplesPerSec** 成員的每秒樣本數。

</dd> </dl>

針對 wave 音訊裝置， *lpSet* 參數會指向 [**MCI \_ WAVE \_ 設定 \_ PARMS**](mci-wave-set-parms.md) 結構。

在儲存資料的檔案建立時，會定義多個波形音訊資料的屬性。 這些屬性會描述如何在檔案中結構化資料，而且在錄製開始之後就無法變更。 下列旗標清單會識別這些屬性：

-   MCI \_ WAVE \_ 設定 \_ AVGBYTESPERSEC
-   MCI \_ WAVE \_ 設定 \_ BITSPERSAMPLE
-   MCI \_ WAVE \_ 設定 \_ BLOCKALIGN
-   MCI \_ WAVE \_ 設定 \_ 通道
-   MCI \_ WAVE \_ 設定 \_ FORMATTAG
-   MCI \_ WAVE \_ 設定 \_ SAMPLESPERSEC

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

 

