---
title: 'MCI_STATUS 命令 (Mmsystem .h) '
description: MCI \_ STATUS 命令會抓取有關 MCI 裝置的資訊。 所有裝置都會辨識此命令。 資訊會以 lpStatus 參數所識別之結構的 dwReturn 成員傳回。
ms.assetid: d1c3dff9-c66f-4525-aac1-4a15b43083e7
keywords:
- MCI_STATUS 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_STATUS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86553ac759a362c1ea4abb53a47d0e9376cbc526
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/12/2021
ms.locfileid: "104321252"
---
# <a name="mci_status-command"></a>MCI \_ 狀態命令

> [!NOTE]
> 無偏差的通訊-Microsoft 支援多樣化且 inclusionary 的環境。  本檔中有 ' 從屬 ' 這個字的參考。 Microsoft 的 [Bias-Free 通訊樣式指南](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) 會將此視為排他性行為單字。  這種用語是用來做為命令內所使用的用語。 為求一致，本檔包含此字。 當您在命令中更改這個字時，我們會將此檔修正為一致。

MCI \_ STATUS 命令會抓取有關 MCI 裝置的資訊。 所有裝置都會辨識此命令。 資訊會以 *lpStatus* 參數所識別之結構的 **dwReturn** 成員傳回。

若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_STATUS, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_STATUS_PARMS) lpStatus
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

<span id="lpStatus"></span><span id="lpstatus"></span><span id="LPSTATUS"></span>*lpStatus*
</dt> <dd>

[**MCI \_ 狀態 \_ PARMS**](mci-status-parms.md)結構的指標。 具有擴充命令集的 (裝置，可能會以裝置特定結構取代此結構。 ) 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

下列其他標準和命令特定旗標適用于所有支援 MCI 狀態的裝置 \_ ：

<dl> <dt>

<span id="MCI_STATUS_ITEM"></span><span id="mci_status_item"></span>MCI \_ 狀態 \_ 專案
</dt> <dd>

指定由 *lpStatus* 所識別之結構的 **dwItem** 成員包含常數，指定要取得的狀態專案。 下列常數會定義要在結構的 **dwReturn** 成員中傳回的狀態專案：

MCI \_ 狀態 \_ 目前的 \_ 追蹤

**DwReturn** 成員會設定為目前的曲目編號。 MCI 使用連續的追蹤號碼。

MCI \_ 狀態 \_ 長度

**DwReturn** 成員會設定為媒體總長度。

</dd> <dt>

<span id="MCI_STATUS_MODE"></span><span id="mci_status_mode"></span>MCI \_ 狀態 \_ 模式
</dt> <dd>

**DwReturn** 成員會設定為裝置的目前模式。 這些模式包括下列各項：

-   MCI \_ 模式 \_ 未 \_ 就緒
-   MCI \_ 模式 \_ 暫停
-   MCI \_ 模式 \_ 播放
-   MCI \_ 模式 \_ 停止
-   \_開啟 MCI 模式 \_
-   MCI \_ 模式 \_ 記錄
-   MCI \_ 模式 \_ 搜尋

</dd> <dt>

<span id="MCI_STATUS_NUMBER_OF_TRACKS"></span><span id="mci_status_number_of_tracks"></span>MCI \_ 狀態 \_ \_ 追蹤數目 \_
</dt> <dd>

**DwReturn** 成員會設定為可播放的曲目總數。

</dd> <dt>

<span id="MCI_STATUS_POSITION"></span><span id="mci_status_position"></span>MCI \_ 狀態 \_ 位置
</dt> <dd>

**DwReturn** 成員會設定為目前的位置。

</dd> <dt>

<span id="MCI_STATUS_READY"></span><span id="mci_status_ready"></span>MCI \_ 狀態 \_ 就緒
</dt> <dd>

如果裝置已備妥， **dwReturn** 成員會設定為 **TRUE** ;否則會設為 **FALSE** 。

</dd> <dt>

<span id="MCI_STATUS_TIME_FORMAT"></span><span id="mci_status_time_format"></span>MCI \_ 狀態 \_ 時間 \_ 格式
</dt> <dd>

**DwReturn** 成員會設定為裝置目前的時間格式。 時間格式包括：

-   MCI \_ 格式 \_ 位元組
-   MCI \_ 格式 \_ 框架
-   MCI \_ 格式 \_ HMS
-   MCI \_ 格式 \_ 毫秒
-   MCI \_ 格式 \_ MSF
-   MCI \_ 格式 \_ 範例
-   MCI \_ 格式 \_ TMSF

</dd> <dt>

<span id="MCI_STATUS_START"></span><span id="mci_status_start"></span>MCI \_ 狀態 \_ 開始
</dt> <dd>

取得媒體的開始位置。 若要取得開始位置，請將此旗標與 MCI \_ 狀態專案合併， \_ 並將 *lpStatus* 所識別之結構的 **dwItem** 成員設定為 mci \_ 狀態 \_ 位置。

</dd> <dt>

<span id="MCI_TRACK"></span><span id="mci_track"></span>MCI \_ 曲目
</dt> <dd>

指出狀態追蹤參數包含在 *lpStatus* 所識別之結構的 **dwTrack** 成員中。 您必須使用此旗標搭配 MCI \_ 狀態 \_ 位置或 mci \_ 狀態 \_ 長度常數。 搭配 MCI \_ 狀態位置使用時 \_ ，MCI TRACK 會取得 \_ 指定之追蹤的開始位置。搭配 MCI \_ 狀態長度使用時 \_ ，MCI TRACK 會取得指定的 \_ 曲目長度。MCI 使用連續的追蹤號碼。

</dd> </dl>

下列其他旗標會搭配 **cdaudio** 裝置類型使用。 當  \_ \_ 針對 *dwFlags* 參數指定了 MCI 狀態專案時，lpStatus 參數所指向之結構的 dwItem 成員會使用這些常數。

<dl> <dt>

<span id="MCI_CDA_STATUS_TYPE_TRACK"></span><span id="mci_cda_status_type_track"></span>MCI \_ CDA \_ 狀態 \_ 類型 \_ 追蹤
</dt> <dd>

**DwReturn** 成員會設定為下列其中一個值：

-   MCI \_ CDA \_ 追蹤 \_ 音訊
-   MCI \_ CDA \_ 追蹤 \_ 其他

若要使用此旗標， \_ 必須設定 MCI TRACK 旗標，且由 *lpStatus* 所識別之結構的 **dwTrack** 成員必須包含有效的曲目編號。

</dd> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI \_ 狀態 \_ 媒體 \_ 存在
</dt> <dd>

如果媒體插入裝置中， **dwReturn** 成員會設定為 **TRUE** 。否則會設為 **FALSE** 。

</dd> </dl>

下列其他旗標適用于 **digitalvideo** 裝置類型：

<dl> <dt>

<span id="MCI_DGV_STATUS_DISKSPACE"></span><span id="mci_dgv_status_diskspace"></span>MCI \_ DGV \_ 狀態 \_ 磁碟空間
</dt> <dd>

由 *lpStatus* 所識別之結構的 **lpstrDrive** 成員會指定磁片磁碟機，或在某些實作為路徑中指定磁片磁碟機。 MCI \_ STATUS 命令會傳回 *lpStatus* 所識別之結構的 **DwReturn** 成員中， [mci \_ RESERVE](mci-reserve.md)命令可取得的大約磁碟空間量。 磁碟空間是以目前時間格式的單位來測量。

</dd> <dt>

<span id="MCI_DGV_STATUS_INPUT"></span><span id="mci_dgv_status_input"></span>MCI \_ DGV \_ 狀態 \_ 輸入
</dt> <dd>

由 *lpStatus* 所識別之結構的 **dwItem** 成員所指定的常數會套用至輸入。

</dd> <dt>

<span id="MCI_DGV_STATUS_LEFT"></span><span id="mci_dgv_status_left"></span>剩餘的 MCI \_ DGV \_ 狀態 \_
</dt> <dd>

由 *lpStatus* 所識別之結構的 **dwItem** 成員所指定的常數會套用至左方音訊通道。

</dd> <dt>

<span id="MCI_DGV_STATUS_NOMINAL"></span><span id="mci_dgv_status_nominal"></span>MCI \_ DGV \_ 狀態 \_ 名義
</dt> <dd>

由 *lpStatus* 所識別之結構的 **dwItem** 成員所指定的常數會要求名義值，而不是目前的值。

</dd> <dt>

<span id="MCI_DGV_STATUS_OUTPUT"></span><span id="mci_dgv_status_output"></span>MCI \_ DGV \_ 狀態 \_ 輸出
</dt> <dd>

由 *lpStatus* 所識別之結構的 **dwItem** 成員所指定的常數會套用至輸出。

</dd> <dt>

<span id="MCI_DGV_STATUS_RECORD"></span><span id="mci_dgv_status_record"></span>MCI \_ DGV \_ 狀態 \_ 記錄
</dt> <dd>

針對 [MCI DGV STATUS frame rate] 旗標傳回的畫面播放速率 \_ \_ \_ \_ 是用於壓縮的速率。

</dd> <dt>

<span id="MCI_DGV_STATUS_REFERENCE"></span><span id="mci_dgv_status_reference"></span>MCI \_ DGV \_ 狀態 \_ 參考
</dt> <dd>

由 *lpStatus* 所識別之結構的 **dwReturn** 成員會傳回最接近 **dwReference** 成員中指定之框架之前的主要畫面格影像。

</dd> <dt>

<span id="MCI_DGV_STATUS_RIGHT"></span><span id="mci_dgv_status_right"></span>MCI \_ DGV \_ STATUS \_ RIGHT
</dt> <dd>

由 *lpStatus* 所識別之結構的 **dwItem** 成員所指定的常數會套用至正確的音訊通道。

</dd> </dl>

當   \_ \_ 針對 *dwFlags* 參數指定了 MCI 狀態專案時，會使用下列常數搭配 lpStatus 參數所指向之結構 dwItem 成員中的 digitalvideo 裝置類型。

<dl> <dt>

<span id="MCI_AVI_STATUS_AUDIO_BREAKS"></span><span id="mci_avi_status_audio_breaks"></span>MCI \_ AVI \_ 狀態 \_ 音訊 \_ 中斷
</dt> <dd>

**DwReturn** 成員會傳回最後一個 AVI 序列的音訊部分所中斷的次數。 當系統嘗試將音訊資料寫入設備磁碟機，併發現該驅動程式已經播放了所有可用的資料時，系統就會計算出一份音訊中斷的次數。 只有 MCIAVI 數位視訊驅動程式能辨識此旗標。

</dd> <dt>

<span id="MCI_AVI_STATUS_FRAMES_SKIPPED"></span><span id="mci_avi_status_frames_skipped"></span>已 \_ \_ 略過 MCI AVI 狀態 \_ 框架 \_
</dt> <dd>

**DwReturn** 成員會傳回播放最後一個 AVI 序列時未繪製的框架數目。 只有 MCIAVI 數位視訊驅動程式能辨識此旗標。

</dd> <dt>

<span id="MCI_AVI_STATUS_LAST_PLAY_SPEED"></span><span id="mci_avi_status_last_play_speed"></span>MCI \_ AVI \_ 狀態 \_ 上次 \_ 播放 \_ 速度
</dt> <dd>

**DwReturn** 成員會傳回一個值，表示最後一個 AVI 序列的實際播放時間與目標播放時間相符的程度。 值1000表示目標時間和實際時間相同。 例如，值為2000時，會指出 AVI 序列所花的時間比應該有兩倍的時間。 只有 MCIAVI 數位視訊驅動程式能辨識此旗標。

</dd> <dt>

<span id="MCI_DGV_STATUS_AUDIO"></span><span id="mci_dgv_status_audio"></span>MCI \_ DGV \_ 狀態 \_ 音訊
</dt> <dd>

**DwReturn** 成員會根據 \_ \_ \_ \_ [mci \_ set](mci-set.md)命令最新的 MCI set AUDIO 選項，將 mci 回傳或 mci OFF。 \_如果已啟用其中一或兩個喇叭，則會傳回 mci，否則會傳回 mci \_ 。

</dd> <dt>

<span id="MCI_DGV_STATUS_AUDIO_INPUT"></span><span id="mci_dgv_status_audio_input"></span>MCI \_ DGV \_ 狀態 \_ 音訊 \_ 輸入
</dt> <dd>

**DwReturn** 成員會傳回類比音訊信號的近似即時音訊層級。 大於1000的值表示有裁剪失真。 某些裝置只能在錄製音訊時決定此值。 此狀態值沒有相關聯的 **MCI \_ SET** 或 [mci \_ SETAUDIO](mci-setaudio.md) 命令。 此值與 WAVE-音訊命令 MCI \_ WAVE \_ 狀態層級相關，但以不同的方式來正規化 \_ 。

</dd> <dt>

<span id="MCI_DGV_STATUS_AUDIO_RECORD"></span><span id="mci_dgv_status_audio_record"></span>MCI \_ DGV \_ 狀態 \_ 音訊 \_ 記錄
</dt> <dd>

**DwReturn** 成員會 \_ \_ 依 \_ \_ \_ **mci \_ SETAUDIO** 命令的 mci DGV SETAUDIO 記錄旗標來反映狀態所設定的狀態，以傳回 mci 或 mci。

</dd> <dt>

<span id="MCI_DGV_STATUS_AUDIO_SOURCE"></span><span id="mci_dgv_status_audio_source"></span>MCI \_ DGV \_ 狀態 \_ 音訊 \_ 來源
</dt> <dd>

**DwReturn** 成員會傳回目前的音訊數位化器來源：

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_AVERAGE"></span><span id="mci_dgv_setaudio_average"></span>MCI \_ DGV \_ SETAUDIO \_ AVERAGE
</dt> <dd>

指定左右音訊頻道的平均值。

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_LEFT"></span><span id="mci_dgv_setaudio_left"></span>\_ \_ SETAUDIO \_ 剩下的 MCI DGV
</dt> <dd>

指定左聲道。

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_RIGHT"></span><span id="mci_dgv_setaudio_right"></span>MCI \_ DGV \_ SETAUDIO \_ RIGHT
</dt> <dd>

指定正確的音訊頻道。

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_STEREO"></span><span id="mci_dgv_setaudio_stereo"></span>MCI \_ DGV \_ SETAUDIO \_ 身歷聲
</dt> <dd>

指定身歷聲。

</dd> <dt>

<span id="MCI_DGV_STATUS_AUDIO_STREAM"></span><span id="mci_dgv_status_audio_stream"></span>MCI \_ DGV \_ 狀態 \_ 音訊 \_ 串流
</dt> <dd>

**DwReturn** 成員會傳回目前的音訊資料流程號碼。

</dd> <dt>

<span id="MCI_DGV_STATUS_AVGBYTESPERSEC"></span><span id="mci_dgv_status_avgbytespersec"></span>MCI \_ DGV \_ 狀態 \_ AVGBYTESPERSEC
</dt> <dd>

**DwReturn** 成員會傳回每秒用於錄製的平均位元組數。

</dd> <dt>

<span id="MCI_DGV_STATUS_BASS"></span><span id="mci_dgv_status_bass"></span>MCI \_ DGV \_ 狀態 \_ 低音
</dt> <dd>

**DwReturn** 成員會傳回目前的音訊低音等級。 使用 \_ \_ \_ 具有此旗標的 MCI DGV 狀態，以取得名義層級。

</dd> <dt>

<span id="MCI_DGV_STATUS_BITSPERPEL"></span><span id="mci_dgv_status_bitsperpel"></span>MCI \_ DGV \_ 狀態 \_ BITSPERPEL
</dt> <dd>

**DwReturn** 成員會傳回用於儲存已捕捉或已記錄資料之每個圖元的位數。

</dd> <dt>

<span id="MCI_DGV_STATUS_BITSPERSAMPLE"></span><span id="mci_dgv_status_bitspersample"></span>MCI \_ DGV \_ 狀態 \_ BITSPERSAMPLE
</dt> <dd>

**DwReturn** 成員會傳回裝置用來錄製的每個樣本位數。 這僅適用于支援 PCM 格式的裝置。

</dd> <dt>

<span id="MCI_DGV_STATUS_BLOCKALIGN"></span><span id="mci_dgv_status_blockalign"></span>MCI \_ DGV \_ 狀態 \_ BLOCKALIGN
</dt> <dd>

**DwReturn** 成員會傳回相對於輸入波形開頭的資料區塊對齊。

</dd> <dt>

<span id="MCI_DGV_STATUS_BRIGHTNESS"></span><span id="mci_dgv_status_brightness"></span>MCI \_ DGV \_ 狀態 \_ 亮度
</dt> <dd>

**DwReturn** 成員會傳回目前的影片亮度等級。 使用 \_ \_ \_ 具有此旗標的 MCI DGV 狀態，以取得名義層級。

</dd> <dt>

<span id="MCI_DGV_STATUS_COLOR"></span><span id="mci_dgv_status_color"></span>MCI \_ DGV \_ 狀態 \_ 色彩
</dt> <dd>

**DwReturn** 成員會傳回目前的色彩層級。 使用 \_ \_ \_ 具有此旗標的 MCI DGV 狀態，以取得名義層級。

</dd> <dt>

<span id="MCI_DGV_STATUS_CONTRAST"></span><span id="mci_dgv_status_contrast"></span>MCI \_ DGV \_ 狀態 \_ 對比
</dt> <dd>

**DwReturn** 成員會傳回目前的對比層級。 使用 \_ \_ \_ 具有此旗標的 MCI DGV 狀態，以取得名義層級。

</dd> <dt>

<span id="MCI_DGV_STATUS_FILEFORMAT"></span><span id="mci_dgv_status_fileformat"></span>MCI \_ DGV \_ 狀態 \_ >FILEFORMAT
</dt> <dd>

**DwReturn** 成員會傳回目前的檔案格式以進行錄製或儲存。

</dd> <dt>

<span id="MCI_DGV_STATUS_FILE_MODE"></span><span id="mci_dgv_status_file_mode"></span>MCI \_ DGV \_ 狀態 \_ 檔案 \_ 模式
</dt> <dd>

**DwReturn** 成員會傳回檔案作業的狀態：

MCI \_ DGV \_ 檔 \_ 模式 \_ 編輯

在剪下、複製、刪除、貼上和復原作業期間傳回。

MCI \_ DGV \_ 檔 \_ 模式 \_ 閒置

當檔案準備好進行下一項作業時傳回。

MCI \_ DGV \_ FILE \_ MODE \_ 載入

在載入檔案時傳回。

\_正在儲存 MCI DGV \_ 檔 \_ 模式 \_

在儲存檔案時傳回。

</dd> <dt>

<span id="MCI_DGV_STATUS_FILE_COMPLETION"></span><span id="mci_dgv_status_file_completion"></span>MCI \_ DGV \_ 狀態 \_ 檔案 \_ 完成
</dt> <dd>

**DwReturn** 成員會傳回負載、儲存、捕捉、剪下、複製、刪除、貼上或復原作業進度的估計百分比。  (的應用程式可以使用此功能來提供進度的視覺指標。 ) 所有數位視訊裝置都不支援此旗標。

</dd> <dt>

<span id="MCI_DGV_STATUS_FORWARD"></span><span id="mci_dgv_status_forward"></span>MCI \_ DGV \_ 狀態 \_ 轉寄
</dt> <dd>

如果裝置方向為轉寄或裝置未播放， **dwReturn** 成員會傳回 **TRUE** 。

</dd> <dt>

<span id="MCI_DGV_STATUS_FRAME_RATE"></span><span id="mci_dgv_status_frame_rate"></span>MCI \_ DGV \_ STATUS \_ FRAME \_ 速率
</dt> <dd>

**DwReturn** 成員必須搭配 mci \_ DGV \_ 狀態 \_ 名義、mci \_ DGV \_ 狀態 \_ 記錄或兩者一起使用。 與 MCI \_ DGV 狀態記錄搭配使用時 \_ \_ ，會傳回目前用來錄製的畫面播放速率。 搭配使用 MCI \_ DGV \_ 狀態 \_ 記錄和 mci \_ DGV 狀態時 \_ \_ ，會傳回與輸入視訊訊號相關聯的名義畫面播放速率。 與 MCI \_ DGV 狀態名義搭配使用時 \_ \_ ，會傳回與檔案相關聯的名義框架費率。 在所有情況下，單位都是每秒畫面格乘以1000。

</dd> <dt>

<span id="MCI_DGV_STATUS_GAMMA"></span><span id="mci_dgv_status_gamma"></span>MCI \_ DGV \_ 狀態 \_ GAMMA
</dt> <dd>

**DwReturn** 成員會傳回目前的 gamma 值。 使用 \_ \_ \_ 具有此旗標的 MCI DGV 狀態，以取得名義層級。

</dd> <dt>

<span id="MCI_DGV_STATUS_HPAL"></span><span id="mci_dgv_status_hpal"></span>MCI \_ DGV \_ 狀態 \_ HPAL
</dt> <dd>

**DwReturn** 成員會傳回目前調色板控制碼的 ASCII 十進位值。 控制碼包含在傳回值的低序位字中。

</dd> <dt>

<span id="MCI_DGV_STATUS_HWND"></span><span id="mci_dgv_status_hwnd"></span>MCI \_ DGV \_ 狀態 \_ HWND
</dt> <dd>

**DwReturn** 成員會針對與此設備磁碟機實例相關聯的目前明確或預設視窗控制碼，傳回 ASCII 十進位值。 控制碼包含在傳回值的低序位字中。

</dd> <dt>

<span id="MCI_DGV_STATUS_KEY_COLOR"></span><span id="mci_dgv_status_key_color"></span>MCI \_ DGV \_ STATUS \_ KEY \_ COLOR
</dt> <dd>

**DwReturn** 成員會傳回目前的按鍵色彩值。

</dd> <dt>

<span id="MCI_DGV_STATUS_KEY_INDEX"></span><span id="mci_dgv_status_key_index"></span>MCI \_ DGV \_ STATUS \_ KEY \_ INDEX
</dt> <dd>

**DwReturn** 成員會傳回目前的索引鍵索引值。

</dd> <dt>

<span id="MCI_DGV_STATUS_MONITOR"></span><span id="mci_dgv_status_monitor"></span>MCI \_ DGV \_ 狀態 \_ 監視
</dt> <dd>

**DwReturn** 成員會傳回常數，指出目前簡報的來源。 以下是定義的常數：

MCI \_ DGV \_ 監視 \_ 檔案

檔案是來源。

MCI \_ DGV \_ 監視 \_ 輸入

輸入為來源。

</dd> <dt>

<span id="MCI_DGV_STATUS_MONITOR_METHOD"></span><span id="mci_dgv_status_monitor_method"></span>MCI \_ DGV \_ STATUS \_ 監視 \_ 方法
</dt> <dd>

**DwReturn** 成員會傳回常數，指出用於輸入監視的方法。 以下是定義的常數：

MCI \_ DGV \_ 方法 \_ 直接

直接輸入監視。

MCI \_ DGV \_ 方法 \_ 文章

輸入後監視。

MCI \_ DGV \_ 方法 \_ 預先

預先輸入監視。

</dd> <dt>

<span id="MCI_DGV_STATUS_PAUSE_MODE"></span><span id="mci_dgv_status_pause_mode"></span>MCI \_ DGV \_ 狀態 \_ 暫停 \_ 模式
</dt> <dd>

如果裝置在播放時暫停， **dwReturn** 成員會傳回 mci \_ 模式 \_ ， \_ 如果裝置在錄製時暫停，則會傳回 mci 模式 \_ 記錄。 此命令會傳回 MCIERR \_ NONAPPLICABLE 函式， \_ 以在裝置未暫停時傳回錯誤。

</dd> <dt>

<span id="MCI_DGV_STATUS_SAMPLESPERSECOND"></span><span id="mci_dgv_status_samplespersecond"></span>MCI \_ DGV \_ 狀態 \_ SAMPLESPERSECOND
</dt> <dd>

**DwReturn** 成員會傳回每秒記錄的樣本數。

</dd> <dt>

<span id="MCI_DGV_STATUS_SEEK_EXACTLY"></span><span id="mci_dgv_status_seek_exactly"></span>MCI \_ DGV \_ 狀態 \_ \_ 精確搜尋
</dt> <dd>

**DwReturn** 成員會傳回 **TRUE** 或 **FALSE** ，指出是否已設定搜尋確切格式。  (的應用程式可以使用 [mci \_ set](mci-set.md) 命令搭配 mci \_ DGV \_ set \_ SEEK 確切旗標來設定此格式 \_ 。 ) 

</dd> <dt>

<span id="MCI_DGV_STATUS_SHARPNESS"></span><span id="mci_dgv_status_sharpness"></span>MCI \_ DGV \_ 狀態 \_ 清晰度
</dt> <dd>

**DwReturn** 成員會傳回目前的清晰度層級。 使用 \_ \_ \_ 具有此旗標的 MCI DGV 狀態，以取得名義層級。

</dd> <dt>

<span id="MCI_DGV_STATUS_SIZE"></span><span id="mci_dgv_status_size"></span>MCI \_ DGV \_ 狀態 \_ 大小
</dt> <dd>

**DwReturn** 成員會傳回保留工作區將保留之壓縮資料的大約播放持續時間。 持續時間單位為目前的時間格式。 如果沒有保留的磁碟空間，則會傳回零。 傳回的大小為近似值，因為壓縮資料的精確磁碟空間無法在資料壓縮後才進行預測。

</dd> <dt>

<span id="MCI_DGV_STATUS_SMPTE"></span><span id="mci_dgv_status_smpte"></span>MCI \_ DGV \_ 狀態 \_ SMPTE
</dt> <dd>

**DwReturn** 成員會傳回與工作區中目前位置相關聯的 SMPTE 時間碼。

</dd> <dt>

<span id="MCI_DGV_STATUS_SPEED"></span><span id="mci_dgv_status_speed"></span>MCI \_ DGV \_ 狀態 \_ 速度
</dt> <dd>

**DwReturn** 成員會傳回目前的播放速度。

</dd> <dt>

<span id="MCI_DGV_STATUS_STILL_FILEFORMAT"></span><span id="mci_dgv_status_still_fileformat"></span>MCI \_ DGV \_ 狀態 \_ 仍 \_ >FILEFORMAT
</dt> <dd>

**DwReturn** 成員會傳回 [MCI \_ CAPTURE](mci-capture.md)命令的目前檔案格式。

</dd> <dt>

<span id="MCI_DGV_STATUS_TINT"></span><span id="mci_dgv_status_tint"></span>MCI \_ DGV \_ 狀態 \_ 淡色
</dt> <dd>

**DwReturn** 成員會傳回目前的影片色調層級。 使用 \_ \_ \_ 具有此旗標的 MCI DGV 狀態，以取得名義層級。

</dd> <dt>

<span id="MCI_DGV_STATUS_TREBLE"></span><span id="mci_dgv_status_treble"></span>MCI \_ DGV \_ 狀態 \_ 高音
</dt> <dd>

**DwReturn** 成員會傳回目前的音訊高音層級。 使用 \_ \_ \_ 具有此旗標的 MCI DGV 狀態，以取得名義層級。

</dd> <dt>

<span id="MCI_DGV_STATUS_UNSAVED"></span><span id="mci_dgv_status_unsaved"></span>未儲存的 MCI \_ DGV \_ 狀態 \_
</dt> <dd>

如果工作區中有記錄的資料可能由於 [mci \_ 關閉](mci-close.md)、 [mci \_ 負載](mci-load.md)、 [mci \_ 記錄](mci-record.md)、 [Mci \_ 保留](mci-reserve.md)、 [mci \_ 剪](mci-cut.md)下、mci [ \_ 刪除](mci-delete.md)或 [mci \_ 貼](mci-paste.md)上命令而遺失， **dwReturn** 成員會傳回 **TRUE** 。 否則，成員會傳回 **FALSE** 。

</dd> <dt>

<span id="MCI_DGV_STATUS_VIDEO"></span><span id="mci_dgv_status_video"></span>MCI \_ DGV \_ 狀態 \_ 影片
</dt> <dd>

 \_ 如果啟用影片或停用 mci，dwReturn 成員會傳回 mci \_ 。

</dd> <dt>

<span id="MCI_DGV_STATUS_VIDEO_RECORD"></span><span id="mci_dgv_status_video_record"></span>MCI \_ DGV \_ 狀態 \_ 影片 \_ 記錄
</dt> <dd>

**DwReturn** 成員會將 mci 回傳 \_ 或 mci \_ OFF，以反映 \_ \_ \_ [mci \_ SETVIDEO](mci-setvideo.md)命令的 mci DGV SETVIDEO 記錄旗標所設定的狀態。

</dd> <dt>

<span id="MCI_DGV_STATUS_VIDEO_SOURCE"></span><span id="mci_dgv_status_video_source"></span>MCI \_ DGV \_ 狀態 \_ 影片 \_ 來源
</dt> <dd>

**DwReturn** 成員會傳回常數，指出由 \_ \_ \_ **mci \_ SETVIDEO** 命令的 mci DGV SETVIDEO 來源旗標所設定的影片來源類型。

</dd> <dt>

<span id="MCI_DGV_STATUS_VIDEO_SRC_NUM"></span><span id="mci_dgv_status_video_src_num"></span>MCI \_ DGV \_ 狀態 \_ 影片 \_ SRC \_ NUM
</dt> <dd>

**DwReturn** 成員會傳回目前作用中的影片輸入來源類型內的數位。

</dd> <dt>

<span id="MCI_DGV_STATUS_VIDEO_STREAM"></span><span id="mci_dgv_status_video_stream"></span>MCI \_ DGV \_ 狀態 \_ 影片 \_ 串流
</dt> <dd>

**DwReturn** 成員會傳回目前的視頻串流號碼。

</dd> <dt>

<span id="MCI_DGV_STATUS_VOLUME"></span><span id="mci_dgv_status_volume"></span>MCI \_ DGV \_ 狀態 \_ 磁片區
</dt> <dd>

**DwReturn** 成員會將磁片區的平均值傳回給左邊和右邊的喇叭。 使用 \_ \_ \_ 具有此旗標的 MCI DGV 狀態，以取得名義層級。

</dd> <dt>

<span id="MCI_DGV_STATUS_WINDOW_VISIBLE"></span><span id="mci_dgv_status_window_visible"></span>[MCI \_ DGV \_ 狀態 \_ ] 視窗 \_ 可見
</dt> <dd>

如果視窗不是隱藏的， **dwReturn** 成員會傳回 **TRUE** 。

</dd> <dt>

<span id="MCI_DGV_STATUS_WINDOW_MINIMIZED"></span><span id="mci_dgv_status_window_minimized"></span>\_ \_ \_ 最小化 MCI DGV 狀態視窗 \_
</dt> <dd>

如果視窗最小化， **dwReturn** 成員會傳回 **TRUE** 。

</dd> <dt>

<span id="MCI_DGV_STATUS_WINDOW_MAXIMIZED"></span><span id="mci_dgv_status_window_maximized"></span>\_最大化的 MCI DGV \_ 狀態 \_ 視窗 \_
</dt> <dd>

如果視窗最大化， **dwReturn** 成員會傳回 **TRUE** 。

</dd> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI \_ 狀態 \_ 媒體 \_ 存在
</dt> <dd>

**DwReturn** 成員會傳回 **TRUE**。

</dd> </dl>

針對數位影片裝置， *lpStatus* 參數會指向 [**MCI \_ DGV \_ STATUS \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_status_parmsa) 結構。

下列其他旗標會搭配 **sequencer** 裝置類型使用。 當  \_ \_ 針對 *dwFlags* 參數指定了 MCI 狀態專案時，lpStatus 參數所指向之結構的 dwItem 成員會使用這些常數。

<dl> <dt>

<span id="MCI_SEQ_STATUS_DIVTYPE"></span><span id="mci_seq_status_divtype"></span>MCI \_ SEQ \_ STATUS \_ DIVTYPE
</dt> <dd>

**DwReturn** 成員會設定為下列其中一個值，表示序列的目前除法類型：

-   MCI \_ SEQ \_ DIV \_ PPQN
-   MCI \_ SEQ \_ DIV （ \_ SMPTE \_ 24）
-   MCI \_ SEQ \_ DIV 的 \_ SMPTE \_ 25
-   MCI \_ SEQ \_ DIV \_ \_ 30
-   MCI \_ SEQ \_ DIV \_ SMPTE \_ 30DROP

</dd> <dt>

<span id="MCI_SEQ_STATUS_MASTER"></span><span id="mci_seq_status_master"></span>MCI \_ SEQ \_ 狀態 \_ 主機
</dt> <dd>

**DwReturn** 成員會設定為主要作業所使用的同步處理類型。

</dd> <dt>

<span id="MCI_SEQ_STATUS_OFFSET"></span><span id="mci_seq_status_offset"></span>MCI \_ SEQ \_ 狀態 \_ 位移
</dt> <dd>

**DwReturn** 成員會設定為序列的目前 SMPTE 位移。

</dd> <dt>

<span id="MCI_SEQ_STATUS_PORT"></span><span id="mci_seq_status_port"></span>MCI \_ SEQ \_ 狀態 \_ 埠
</dt> <dd>

**DwReturn** 成員會設定為序列所使用之目前埠的 MIDI 裝置識別碼。

</dd> <dt>

<span id="MCI_SEQ_STATUS_SLAVE"></span><span id="mci_seq_status_slave"></span>MCI \_ SEQ \_ 狀態 \_ 從屬
</dt> <dd>

**DwReturn** 成員會設定為用於從屬作業的同步處理類型。

</dd> <dt>

<span id="MCI_SEQ_STATUS_TEMPO"></span><span id="mci_seq_status_tempo"></span>MCI \_ SEQ \_ STATUS \_ 節奏
</dt> <dd>

**DwReturn** 成員會設定為 PPQN 檔案在每分鐘的每分鐘的最新節奏，或每秒的每秒畫面格數。

</dd> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI \_ 狀態 \_ 媒體 \_ 存在
</dt> <dd>

如果媒體插入裝置中， **dwReturn** 成員會設定為 **TRUE** 。否則會設為 **FALSE** 。

</dd> </dl>

下列其他旗標會搭配 **vcr** 裝置類型使用。 當  \_ \_ 針對 *dwFlags* 參數指定了 MCI 狀態專案時，lpStatus 參數所指向之結構的 dwItem 成員會使用這些常數。

<dl> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI \_ 狀態 \_ 媒體 \_ 存在
</dt> <dd>

如果媒體插入裝置中， **dwReturn** 成員會設定為 **TRUE** 。否則會設為 **FALSE** 。

</dd> <dt>

<span id="MCI_VCR_STATUS_ASSEMBLE_RECORD"></span><span id="mci_vcr_status_assemble_record"></span>MCI \_ VCR \_ 狀態 \_ 組合 \_ 記錄
</dt> <dd>

如果組合模式為開啟， **dwReturn** 成員會設定為 **TRUE** ;否則會設為 **FALSE** 。

</dd> <dt>

<span id="MCI_VCR_STATUS_AUDIO_MONITOR"></span><span id="mci_vcr_status_audio_monitor"></span>MCI \_ VCR \_ 狀態 \_ 音訊 \_ 監視器
</dt> <dd>

**DwReturn** 成員會設定為常數，表示目前選取的音訊監視器類型。

</dd> <dt>

<span id="MCI_VCR_STATUS_AUDIO_MONITOR_NUMBER"></span><span id="mci_vcr_status_audio_monitor_number"></span>MCI \_ VCR \_ 狀態 \_ 音訊 \_ 監視器 \_ 編號
</dt> <dd>

**DwReturn** 成員會設定為目前選取之音訊監視器類型的數目。

</dd> <dt>

<span id="MCI_VCR_STATUS_AUDIO_RECORD"></span><span id="mci_vcr_status_audio_record"></span>MCI \_ VCR \_ 狀態 \_ 音訊 \_ 記錄
</dt> <dd>

如果指定了下一個 [記錄] 命令，則 **dwReturn** 成員會設定為 **TRUE** ，否則會記錄音訊。否則會設為 **FALSE** 。 如果您 \_ 在此命令的 *dwFlags* 參數中指定 MCI TRACK， **dwTrack** 就會包含此查詢適用的曲目。

</dd> <dt>

<span id="MCI_VCR_STATUS_AUDIO_SOURCE"></span><span id="mci_vcr_status_audio_source"></span>MCI \_ VCR \_ 狀態 \_ 音訊 \_ 來源
</dt> <dd>

**DwReturn** 成員會設定為常數，表示目前的音訊來源類型。

</dd> <dt>

<span id="MCI_VCR_STATUS_AUDIO_SOURCE_NUMBER"></span><span id="mci_vcr_status_audio_source_number"></span>MCI \_ VCR \_ 狀態 \_ 音訊 \_ 來源 \_ 編號
</dt> <dd>

**DwReturn** 成員會設定為目前選取之音訊來源類型的編號。

</dd> <dt>

<span id="MCI_VCR_STATUS_CLOCK"></span><span id="mci_vcr_status_clock"></span>MCI \_ VCR \_ 狀態 \_ 時鐘
</dt> <dd>

**DwReturn** 成員會設定為目前的時鐘值（以總時鐘遞增）。

</dd> <dt>

<span id="MCI_VCR_STATUS_CLOCK_ID"></span><span id="mci_vcr_status_clock_id"></span>MCI \_ VCR \_ 狀態 \_ 時鐘 \_ 識別碼
</dt> <dd>

**DwReturn** 成員會設定為可唯一描述使用中時鐘的數位。

</dd> <dt>

<span id="MCI_VCR_STATUS_COUNTER_FORMAT"></span><span id="mci_vcr_status_counter_format"></span>MCI \_ VCR \_ 狀態 \_ 計數器 \_ 格式
</dt> <dd>

**DwReturn** 成員會設定為描述目前計數器格式的常數。 如需詳細資訊，請參閱 \_ \_ \_ [MCI \_ set](mci-set.md) 命令的 mci set TIME FORMAT 旗標。

</dd> <dt>

<span id="MCI_VCR_STATUS_COUNTER_RESOLUTION"></span><span id="mci_vcr_status_counter_resolution"></span>MCI \_ VCR \_ 狀態 \_ 計數器 \_ 解析
</dt> <dd>

**DwReturn** 成員會設定為描述計數器解析的常數，而且是下列其中一個值：

-   MCI \_ VCR \_ 計數器 \_ RES \_ 框架：計數器具有框架的解析度。
-   MCI \_ VCR \_ 計數器 \_ RES \_ seconds：計數器的解決方式為秒。
-   MCI \_ VCR \_ 狀態 \_ 計數器 \_ 值：在目前的計數器時間格式中， **dwReturn** 成員會設定為目前的計數器讀取。

</dd> <dt>

<span id="MCI_VCR_STATUS_FRAME_RATE"></span><span id="mci_vcr_status_frame_rate"></span>MCI \_ VCR \_ 狀態 \_ 幀 \_ 速率
</dt> <dd>

**DwReturn** 成員會設定為裝置目前的原生畫面播放速率。

</dd> <dt>

<span id="MCI_VCR_STATUS_INDEX"></span><span id="mci_vcr_status_index"></span>MCI \_ VCR \_ 狀態 \_ 索引
</dt> <dd>

**DwReturn** 成員會設定為常數，以描述螢幕上顯示的目前內容，而且是下列其中一項：

-   MCI \_ VCR \_ 索引 \_ 計數器
-   MCI \_ VCR \_ 索引 \_ 日期
-   MCI \_ VCR \_ 索引 \_ 時間
-   MCI \_ VCR \_ 索引時間 \_ 碼

</dd> <dt>

<span id="MCI_VCR_STATUS_INDEX_ON"></span><span id="mci_vcr_status_index_on"></span>\_上的 MCI VCR \_ 狀態 \_ 索引 \_
</dt> <dd>

如果螢幕上顯示開啟， **dwReturn** 成員會設定為 **TRUE** 。否則會設為 **FALSE** 。

</dd> <dt>

<span id="MCI_VCR_STATUS_MEDIA_TYPE"></span><span id="mci_vcr_status_media_type"></span>MCI \_ VCR \_ 狀態 \_ 媒體 \_ 類型
</dt> <dd>

**DwReturn** 成員會設定為下列其中一項：

-   MCI \_ VCR \_ 媒體 \_ 8
-   MCI \_ VCR \_ 媒體 \_ HI8
-   MCI \_ VCR \_ 媒體 \_ VHS
-   MCI \_ VCR \_ 媒體 \_ SVHS
-   MCI \_ VCR \_ 媒體搶鮮版（ \_ BETA）
-   MCI \_ VCR \_ 媒體 \_ EDBETA
-   MCI \_ VCR \_ 媒體 \_ 其他

</dd> <dt>

<span id="MCI_VCR_STATUS_NUMBER"></span><span id="mci_vcr_status_number"></span>MCI \_ VCR \_ 狀態 \_ 號碼
</dt> <dd>

當您搭配使用此旗標與 MCI \_ VCR \_ 狀態 \_ 調諧器 \_ 通道旗標時，dwNumber 成員會設定為邏輯調諧器號碼。

</dd> <dt>

<span id="MCI_VCR_STATUS_NUMBER_OF_AUDIO_TRACKS"></span><span id="mci_vcr_status_number_of_audio_tracks"></span>\_ \_ \_ \_ \_ 音訊 \_ 曲目的 MCI VCR 狀態數位
</dt> <dd>

**DwReturn** 成員會設定為可獨立選取的曲目數目。

</dd> <dt>

<span id="MCI_VCR_STATUS_NUMBER_OF_VIDEO_TRACKS"></span><span id="mci_vcr_status_number_of_video_tracks"></span>\_ \_ \_ \_ \_ 影片 \_ 曲目的 MCI VCR 狀態編號
</dt> <dd>

**DwReturn** 成員會設定為可獨立選取的影片曲目數目。

</dd> <dt>

<span id="MCI_VCR_STATUS_PAUSE_TIMEOUT"></span><span id="mci_vcr_status_pause_timeout"></span>MCI \_ VCR \_ 狀態 \_ 暫停 \_ 超時
</dt> <dd>

**DwReturn** 成員會設定為 pause 命令的最長持續時間（以毫秒為單位）。 傳回值為零表示不會進行任何超時。

</dd> <dt>

<span id="MCI_VCR_STATUS_PLAY_FORMAT"></span><span id="mci_vcr_status_play_format"></span>MCI \_ VCR \_ 狀態 \_ 播放 \_ 格式
</dt> <dd>

**DwReturn** 成員會設定為下列其中一項：

-   MCI \_ VCR \_ 格式 \_ EP
-   MCI \_ VCR \_ 格式 \_ LP
-   其他的 MCI \_ VCR \_ 格式 \_
-   MCI \_ VCR \_ 格式 \_ SP

</dd> <dt>

<span id="MCI_VCR_STATUS_POSTROLL_DURATION"></span><span id="mci_vcr_status_postroll_duration"></span>MCI \_ VCR \_ 狀態 \_ POSTROLL \_ 持續期間
</dt> <dd>

**DwReturn** 成員會設定為以目前時間格式在停止的位置之後將播放的磁帶長度。 若要從停止或暫停命令煞車 VCR 磁帶傳輸，這是必要的。

</dd> <dt>

<span id="MCI_VCR_STATUS_POWER_ON"></span><span id="mci_vcr_status_power_on"></span>MCI \_ VCR \_ 狀態 \_ 開啟 \_
</dt> <dd>

如果開啟電源， **dwReturn** 成員會設定為 **TRUE** ;否則會設為 **FALSE** 。

</dd> <dt>

<span id="MCI_VCR_STATUS_PREROLL_DURATION"></span><span id="mci_vcr_status_preroll_duration"></span>MCI \_ VCR \_ 狀態 \_ \_ 持續時間
</dt> <dd>

**DwReturn** 成員會設定為將在其啟動所在位置之前播放的磁帶長度（以目前的時間格式）。 這是穩定 VCR 輸出的必要項。

</dd> <dt>

<span id="MCI_VCR_STATUS_RECORD_FORMAT"></span><span id="mci_vcr_status_record_format"></span>MCI \_ VCR \_ 狀態 \_ 記錄 \_ 格式
</dt> <dd>

**DwReturn** 成員會設定為下列其中一項：

-   MCI \_ VCR \_ 格式 \_ EP
-   MCI \_ VCR \_ 格式 \_ LP
-   其他的 MCI \_ VCR \_ 格式 \_
-   MCI \_ VCR \_ 格式 \_ SP

</dd> <dt>

<span id="MCI_VCR_STATUS_SPEED"></span><span id="mci_vcr_status_speed"></span>MCI \_ VCR \_ 狀態 \_ 速度
</dt> <dd>

**DwReturn** 成員會設定為目前的速度。 如需詳細資訊，請參閱 \_ \_ \_ [MCI \_ set](mci-set.md) 命令的 mci VCR 設定速度旗標。

</dd> <dt>

<span id="MCI_VCR_STATUS_TIME_MODE"></span><span id="mci_vcr_status_time_mode"></span>MCI \_ VCR \_ 狀態 \_ 時間 \_ 模式
</dt> <dd>

**DwReturn** 成員會設定為下列其中一項：

-   MCI \_ VCR \_ 時間 \_ 計數器
-   MCI \_ VCR \_ 時間 \_ 偵測
-   MCI \_ VCR \_ 時間時間 \_ 碼

如需詳細資訊，請參閱 \_ \_ \_ \_ [mci \_ set](mci-set.md) 命令的 mci VCR 設定時間模式旗標。

</dd> <dt>

<span id="MCI_VCR_STATUS_TIME_TYPE"></span><span id="mci_vcr_status_time_type"></span>MCI \_ VCR \_ 狀態 \_ 時間 \_ 類型
</dt> <dd>

**DwReturn** 成員會設定為常數，以描述 [play](play.md)、 [record](record.md)、 [seek](seek.md)等) 所使用 (目前的時間類型，而且是下列其中一項：

</dd> <dt>

<span id="MCI_VCR_TIME_COUNTER"></span><span id="mci_vcr_time_counter"></span>MCI \_ VCR \_ 時間 \_ 計數器
</dt> <dd>

計數器正在使用中。

</dd> <dt>

<span id="MCI_VCR_TIME_TIMECODE"></span><span id="mci_vcr_time_timecode"></span>MCI \_ VCR \_ 時間時間 \_ 碼
</dt> <dd>

時間碼正在使用中。

</dd> <dt>

<span id="MCI_VCR_STATUS_TIMECODE_PRESENT"></span><span id="mci_vcr_status_timecode_present"></span>\_存在 MCI VCR 狀態的時間 \_ \_ 碼 \_
</dt> <dd>

如果時間碼出現在內容中的目前位置， **dwReturn** 成員會設定為 **TRUE** ;否則會設為 **FALSE** 。

</dd> <dt>

<span id="MCI_VCR_STATUS_TIMECODE_RECORD"></span><span id="mci_vcr_status_timecode_record"></span>MCI \_ VCR \_ 狀態時間 \_ 碼 \_ 記錄
</dt> <dd>

如果指定了下一個記錄命令，則 **dwReturn** 成員會設定為 **TRUE** ，否則會記錄時間碼。否則會設為 **FALSE** 。

</dd> <dt>

<span id="MCI_VCR_STATUS_TIMECODE_TYPE"></span><span id="mci_vcr_status_timecode_type"></span>MCI \_ VCR \_ 狀態時間 \_ 碼 \_ 類型
</dt> <dd>

**DwReturn** 成員會設定為常數，描述裝置直接支援的時間碼類型，而且是下列其中一項：

-   MCI \_ VCR 時間 \_ 碼 \_ 類型 \_ NONE：此裝置不使用時間碼。
-   MCI \_ VCR 時間 \_ 碼 \_ 類型 \_ OTHER：此裝置使用未指定的時間碼。
-   MCI \_ VCR 時間 \_ 碼 \_ 類型 \_ SMPTE：此裝置使用的是 smpte 時間碼。
-   MCI \_ VCR 時間 \_ 碼 \_ 類型 \_ SMPTE \_ 捨棄：此裝置使用的是 SMPTE drop 時間碼。

</dd> <dt>

<span id="MCI_VCR_STATUS_TUNER_CHANNEL"></span><span id="mci_vcr_status_tuner_channel"></span>MCI \_ VCR \_ 狀態 \_ 調諧器 \_ 頻道
</dt> <dd>

**DwReturn** 成員會設定為目前的頻道號碼。 如果您 \_ \_ \_ 在此命令的 *DWFLAGS* 參數中指定 MCI VCR 狀態號碼， **dwNumber** 就會包含此命令適用的邏輯調諧器號碼。

</dd> <dt>

<span id="MCI_VCR_STATUS_VIDEO_MONITOR"></span><span id="mci_vcr_status_video_monitor"></span>MCI \_ VCR \_ 狀態 \_ 影片 \_ 監視
</dt> <dd>

**DwReturn** 成員會設定為常數，表示目前選取的影片監視器類型。

</dd> <dt>

<span id="MCI_VCR_STATUS_VIDEO_MONITOR_NUMBER"></span><span id="mci_vcr_status_video_monitor_number"></span>MCI \_ VCR \_ 狀態 \_ 影片 \_ 監視器 \_ 編號
</dt> <dd>

**DwReturn** 成員會設定為目前所選影片監視器類型的編號。

</dd> <dt>

<span id="MCI_VCR_STATUS_VIDEO_RECORD"></span><span id="mci_vcr_status_video_record"></span>MCI \_ VCR \_ 狀態 \_ 影片 \_ 記錄
</dt> <dd>

如果指定了下一個記錄命令，則 **dwReturn** 成員會設定為 **TRUE** ，如果影片將會錄製;否則會設為 **FALSE** 。 如果您 \_ 在此命令的 *dwFlags* 參數中指定 MCI TRACK， **dwTrack** 就會包含此查詢適用的曲目。

</dd> <dt>

<span id="MCI_VCR_STATUS_VIDEO_SOURCE"></span><span id="mci_vcr_status_video_source"></span>MCI \_ VCR \_ 狀態 \_ 影片 \_ 來源
</dt> <dd>

**DwReturn** 成員會設定為常數，指出目前選取的影片來源類型。

</dd> <dt>

<span id="MCI_VCR_STATUS_VIDEO_SOURCE_NUMBER"></span><span id="mci_vcr_status_video_source_number"></span>MCI \_ VCR \_ 狀態 \_ 影片 \_ 來源 \_ 編號
</dt> <dd>

**DwReturn** 成員會設定為目前所選影片來源類型的編號。

</dd> <dt>

<span id="MCI_VCR_STATUS_WRITE_PROTECTED"></span><span id="mci_vcr_status_write_protected"></span>MCI \_ VCR \_ 狀態 \_ 寫入 \_ 受保護
</dt> <dd>

如果媒體有寫入保護， **dwReturn** 成員會設定為 **TRUE** ;否則會設為 **FALSE** 。

</dd> </dl>

若為 VCR 裝置， *lpStatus* 參數會指向 [**MCI \_ VCR \_ 狀態 \_ PARMS**](mci-vcr-status-parms.md) 結構。

\_ \_ 除非已使用[mci \_ SET](mci-set.md)命令明確變更長度，否則使用 mci STATUS LENGTH 旗標來決定媒體的長度一律會傳回2小時的 VCR 裝置。

下列其他旗標會搭配覆迭 **裝置類型** 使用。 當  \_ \_ 針對 *dwFlags* 參數指定了 MCI 狀態專案時，lpStatus 參數所指向之結構的 dwItem 成員會使用這些常數。

<dl> <dt>

<span id="MCI_OVLY_STATUS_HWND"></span><span id="mci_ovly_status_hwnd"></span>MCI \_ OVLY \_ 狀態 \_ HWND
</dt> <dd>

**DwReturn** 成員會設定為與影片重迭裝置相關聯的視窗控制碼。

</dd> <dt>

<span id="MCI_OVLY_STATUS_STRETCH"></span><span id="mci_ovly_status_stretch"></span>MCI \_ OVLY \_ 狀態 \_ 延展
</dt> <dd>

如果已啟用延展， **dwReturn** 成員會設定為 **TRUE** ;否則會設為 **FALSE** 。

</dd> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI \_ 狀態 \_ 媒體 \_ 存在
</dt> <dd>

如果媒體插入裝置中， **dwReturn** 成員會設定為 **TRUE** 。否則會設為 **FALSE** 。

</dd> </dl>

下列其他旗標會搭配 **videodisc** 裝置類型使用。 當  \_ \_ 針對 *dwFlags* 參數指定了 MCI 狀態專案時，lpStatus 參數所指向之結構的 dwItem 成員會使用這些常數。

<dl> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI \_ 狀態 \_ 媒體 \_ 存在
</dt> <dd>

如果媒體插入裝置中， **dwReturn** 成員會設定為 **TRUE** 。否則會設為 **FALSE** 。

</dd> <dt>

<span id="MCI_STATUS_MODE"></span><span id="mci_status_mode"></span>MCI \_ 狀態 \_ 模式
</dt> <dd>

**DwReturn** 成員會設定為裝置的目前模式。 Videodisc 裝置除了可傳回的 \_ \_ 常數之外，還可以傳回 MCI VD 模式 \_ 公園常數，如 *dwFlags* 參數所述。

</dd> <dt>

<span id="MCI_VD_STATUS_DISC_SIZE"></span><span id="mci_vd_status_disc_size"></span>MCI \_ VD \_ 狀態 \_ 光碟 \_ 大小
</dt> <dd>

**DwReturn** 成員會設定為載入的光碟大小（以英寸為單位） (8 或 12) 。

</dd> <dt>

<span id="MCI_VD_STATUS_FORWARD"></span><span id="mci_vd_status_forward"></span>MCI \_ VD \_ 狀態 \_ 轉寄
</dt> <dd>

如果向前播放， **dwReturn** 成員會設定為 **TRUE** ;否則會設為 **FALSE** 。

MCI videodisc 裝置不支援此旗標。

</dd> <dt>

<span id="MCI_VD_STATUS_MEDIA_TYPE"></span><span id="mci_vd_status_media_type"></span>MCI \_ VD \_ 狀態 \_ 媒體 \_ 類型
</dt> <dd>

**DwReturn** 成員會設定為所插入媒體的媒體類型。 可以傳回下列媒體類型：

MCI \_ VD \_ MEDIA \_ CAV

MCI \_ VD \_ MEDIA \_ CLV

MCI \_ VD \_ \_ 其他媒體

</dd> <dt>

<span id="MCI_VD_STATUS_SIDE"></span><span id="mci_vd_status_side"></span>MCI \_ VD \_ 狀態 \_ 端
</dt> <dd>

**DwReturn** 成員設定為1或2，表示已載入光碟的哪一端。 並非所有 videodisc 裝置都支援此旗標。

</dd> <dt>

<span id="MCI_VD_STATUS_SPEED"></span><span id="mci_vd_status_speed"></span>MCI \_ VD \_ 狀態 \_ 速度
</dt> <dd>

**DwReturn** 成員會設定為每秒畫面格的播放速度。 MCIPIONR。WINSPOOL.DRV 設備磁碟機會傳回 MCIERR \_ 不支援的函式 \_ 。

</dd> </dl>

下列其他旗標會搭配 **waveaudio** 裝置類型使用。 當  \_ \_ 針對 *dwFlags* 參數指定了 MCI 狀態專案時，lpStatus 參數所指向之結構的 dwItem 成員會使用這些常數。

<dl> <dt>

<span id="MCI_WAVE_FORMATTAG"></span><span id="mci_wave_formattag"></span>MCI \_ WAVE \_ FORMATTAG
</dt> <dd>

**DwReturn** 成員會設定為目前用來播放、錄製和儲存的格式標記。

</dd> <dt>

<span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI \_ WAVE \_ 輸入
</dt> <dd>

**DwReturn** 成員會設定為用於錄製的 wave 輸入裝置。 如果沒有使用中的裝置，且未明確設定任何裝置，則錯誤會傳回 MCIERR \_ WAVE \_ INPUTUNSPECIFIED。

</dd> <dt>

<span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI \_ WAVE \_ 輸出
</dt> <dd>

**DwReturn** 成員會設定為用於播放的 wave 輸出裝置。 如果沒有使用中的裝置，且未明確設定任何裝置，則錯誤會傳回 MCIERR \_ WAVE \_ OUTPUTUNSPECIFIED。

</dd> <dt>

<span id="MCI_WAVE_STATUS_AVGBYTESPERSEC"></span><span id="mci_wave_status_avgbytespersec"></span>MCI \_ WAVE \_ 狀態 \_ AVGBYTESPERSEC
</dt> <dd>

**DwReturn** 成員會設定為目前每秒用來播放、錄製和儲存的位元組。

</dd> <dt>

<span id="MCI_WAVE_STATUS_BITSPERSAMPLE"></span><span id="mci_wave_status_bitspersample"></span>MCI \_ WAVE \_ 狀態 \_ BITSPERSAMPLE
</dt> <dd>

**DwReturn** 成員會設定為每個樣本的目前位數，用來播放、錄製和儲存 PCM 格式的資料。

</dd> <dt>

<span id="MCI_WAVE_STATUS_BLOCKALIGN"></span><span id="mci_wave_status_blockalign"></span>MCI \_ WAVE \_ 狀態 \_ BLOCKALIGN
</dt> <dd>

**DwReturn** 成員會設定為目前用來播放、錄製和儲存的區塊對齊。

</dd> <dt>

<span id="MCI_WAVE_STATUS_CHANNELS"></span><span id="mci_wave_status_channels"></span>MCI \_ WAVE \_ 狀態 \_ 通道
</dt> <dd>

**DwReturn** 成員會設定為目前用來播放、錄製和儲存的通道計數。

</dd> <dt>

<span id="MCI_WAVE_STATUS_LEVEL"></span><span id="mci_wave_status_level"></span>MCI \_ WAVE \_ 狀態 \_ 層級
</dt> <dd>

**DwReturn** 成員會設定為 PCM 格式化資料的目前記錄或播放層級。 此值會以8或16位值傳回，視使用的樣本大小而定。 右側或 mono 通道層級會以低序位字組傳回。 左聲道層級會以高序位字的方式傳回。

</dd> <dt>

<span id="MCI_WAVE_STATUS_SAMPLESPERSEC"></span><span id="mci_wave_status_samplespersec"></span>MCI \_ WAVE \_ 狀態 \_ SAMPLESPERSEC
</dt> <dd>

**DwReturn** 成員會設定為每秒用來播放、錄製和儲存的最新樣本。

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
</dt> <dt>

[MCI \_ 剪下](mci-cut.md)
</dt> <dt>

[MCI \_ 刪除](mci-delete.md)
</dt> <dt>

[MCI \_ 貼上](mci-paste.md)
</dt> <dt>

[MCI \_ 保留](mci-reserve.md)
</dt> <dt>

[MCI \_ 組](mci-set.md)
</dt> <dt>

[玩](play.md)
</dt> <dt>

[記錄](record.md)
</dt> <dt>

[尋求](seek.md)
</dt> </dl>

 

