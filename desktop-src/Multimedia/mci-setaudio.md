---
title: 'MCI_SETAUDIO 命令 (Mmsystem .h) '
description: MCI \_ SETAUDIO 命令會設定與音訊播放和捕捉相關聯的值。 數位影片和 VCR 裝置會辨識此命令。
ms.assetid: 78624596-e465-4ef1-8988-edcfe9a46f89
keywords:
- MCI_SETAUDIO 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_SETAUDIO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b882209b8a9debc2c01e4f5c6f852d418c1a5cd321a764af022d19c58fe32a21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117803395"
---
# <a name="mci_setaudio-command"></a>MCI \_ SETAUDIO 命令

MCI \_ SETAUDIO 命令會設定與音訊播放和捕捉相關聯的值。 數位影片和 VCR 裝置會辨識此命令。

若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SETAUDIO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSetAudio
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

MCI \_ 通知、mci \_ 等候或 mci \_ 測試。 如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。

</dd> <dt>

<span id="lpSetAudio"></span><span id="lpsetaudio"></span><span id="LPSETAUDIO"></span>*lpSetAudio*
</dt> <dd>

[**MCI \_ 泛型 \_ PARMS**](mci-generic-parms.md)結構的指標。 具有擴充命令集的 (裝置，可能會以裝置特定結構取代此結構。 ) 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

下列旗標適用于 **digitalvideo** 裝置類型：

<dl> <dt>

<span id="MCI_DGV_SETAUDIO_ALG"></span><span id="mci_dgv_setaudio_alg"></span>MCI \_ DGV \_ SETAUDIO \_ ALG
</dt> <dd>

*LpSetAudio* 所識別之結構的 **lpstrAlgorithm** 成員包含包含音訊壓縮演算法名稱的緩衝區位址。 壓縮演算法會由後續的 [mci \_ 保留](mci-reserve.md) 或 [MCI \_ 記錄](mci-record.md) 命令使用。 可用的演算法取決於裝置。 如果演算法與目前的檔案格式不相容，則檔案格式會變更為演算法的預設格式。

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_CLOCKTIME"></span><span id="mci_dgv_setaudio_clocktime"></span>MCI \_ DGV \_ SETAUDIO \_ CLOCKTIME
</dt> <dd>

指定的時間是以毫秒為單位，而在與 MCI DGV SETAUDIO 搭配使用時是絕對時間 \_ \_ \_ 。  (這次無法在工作區的播放中執行。 ) 

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_INPUT"></span><span id="mci_dgv_setaudio_input"></span>MCI \_ DGV \_ SETAUDIO \_ 輸入
</dt> <dd>

修改低音、高音或音量旗標，使其影響輸入信號，並修改所記錄的內容。 可能的話，這是監視輸入時的預設值。

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_ITEM"></span><span id="mci_dgv_setaudio_item"></span>MCI \_ DGV \_ SETAUDIO \_ 專案
</dt> <dd>

音訊常數指定于 *lpSetAudio* 所識別之結構的 **dwItem** 成員中。 常數可識別正在設定的值。 以下是定義的常數：

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_AVGBYTESPERSEC"></span><span id="mci_dgv_setaudio_avgbytespersec"></span>MCI \_ DGV \_ SETAUDIO \_ AVGBYTESPERSEC
</dt> <dd>

平均位元組數是在 *lpSetAudio* 所識別之結構的 **dwValue** 成員中指定。 此值會設定在 PCM (脈衝程式碼調製) 中播放或錄製的平均每秒位元組數，並 ADPCM (調適型差異脈衝程式碼調製) 格式。 檔案會以這種格式儲存。

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_BASS"></span><span id="mci_dgv_setaudio_bass"></span>MCI \_ DGV \_ SETAUDIO \_ 低音
</dt> <dd>

音訊低頻率層級會指定為 *lpSetAudio* 所識別之結構的 **dwValue** 成員中的因素。

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_BITSPERSAMPLE"></span><span id="mci_dgv_setaudio_bitspersample"></span>MCI \_ DGV \_ SETAUDIO \_ BITSPERSAMPLE
</dt> <dd>

依 *lpSetAudio* 所識別之結構的 **dwValue** 成員，指定每個樣本的位數。 此值會設定以 PCM 格式播放或錄製的每個樣本位數。 檔案會以這種格式儲存。

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_BLOCKALIGN"></span><span id="mci_dgv_setaudio_blockalign"></span>MCI \_ DGV \_ SETAUDIO \_ BLOCKALIGN
</dt> <dd>

資料區塊對齊是在 *lpSetAudio* 所識別之結構的 **dwValue** 成員中指定。 此值會設定資料區塊相對於輸入波形資料開頭的對齊方式。

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_SAMPLESPERSEC"></span><span id="mci_dgv_setaudio_samplespersec"></span>MCI \_ DGV \_ SETAUDIO \_ SAMPLESPERSEC
</dt> <dd>

取樣率是在 *lpSetAudio* 所識別之結構的 **dwValue** 成員中指定。 此值會設定用 PCM 和 ADPCM 演算法播放和錄製的取樣率。 檔案會以這種格式儲存。

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_SOURCE"></span><span id="mci_dgv_setaudio_source"></span>MCI \_ DGV \_ SETAUDIO \_ 來源
</dt> <dd>

指定音訊輸入來源的常數會包含在由 *lpSetAudio* 所識別之結構的 **dwValue** 成員中。 下列是針對音訊輸入來源定義的常數：

MCI \_ DGV \_ SETAUDIO \_ 來源 \_ 平均

左右音訊頻道的平均值。

剩餘的 MCI \_ DGV \_ SETAUDIO \_ 來源 \_

左聲道。

MCI \_ DGV \_ SETAUDIO \_ 來源 \_ 右邊

右音訊頻道。

MCI \_ DGV \_ SETAUDIO \_ 來源 \_ 身歷聲

立體。

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_STREAM"></span><span id="mci_dgv_setaudio_stream"></span>MCI \_ DGV \_ SETAUDIO \_ STREAM
</dt> <dd>

音訊資料流程是在 *lpSetAudio* 所識別之結構的 **dwValue** 成員中指定。 整數值指定從工作區播放的音訊串流。 如果未指定資料流程，則會播放第一個實際交錯的音訊資料流程。

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_TREBLE"></span><span id="mci_dgv_setaudio_treble"></span>MCI \_ DGV \_ SETAUDIO \_ 高音
</dt> <dd>

音訊高頻率層級會指定為 *lpSetAudio* 所識別之結構的 **dwValue** 成員中的一個因素。

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_VOLUME"></span><span id="mci_dgv_setaudio_volume"></span>MCI \_ DGV \_ SETAUDIO \_ VOLUME
</dt> <dd>

其中一個或兩個音訊通道的音訊層級，會指定為 *lpSetAudio* 所識別之結構的 **dwValue** 成員中的一個因素。 如果左方和右邊的磁片區已設定為不同的值，則從左至右磁片區的比率大約是未變更。

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_LEFT"></span><span id="mci_dgv_setaudio_left"></span>\_ \_ SETAUDIO \_ 剩下的 MCI DGV
</dt> <dd>

在搭配使用的 MCI 設定時啟用左 \_ 聲道 \_ 。 當使用的 MCI 設定為 OFF 時，停用左聲道 \_ \_ 。 當此旗標搭配 MCI \_ DGV \_ SETAUDIO \_ VALUE 和 mci DGV SETAUDIO VOLUME 的組合使用時 \_ \_ \_ ，它會設定左方音訊頻道的音量。 當此旗標與 MCI \_ DGV SETAUDIO 來源搭配使用時 \_ \_ ，它會指定左方音訊頻道作為音訊輸入數位板的來源。

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_OVER"></span><span id="mci_dgv_setaudio_over"></span>MCI \_ DGV \_ SETAUDIO \_
</dt> <dd>

轉換長度參數會包含在由 *lpSetAudio* 所識別之結構的 **dwOver** 成員中。 [長度] 值會指定以目前時間格式的單位 (的時間長度，) 需要進行使用因素的變更。 如果未使用此旗標，則會立即進行變更。

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_QUALITY"></span><span id="mci_dgv_setaudio_quality"></span>MCI \_ DGV \_ SETAUDIO \_ 品質
</dt> <dd>

*LpSetAudio* 所識別之結構的 **lpstrQuality** 成員包含定義音訊品質的緩衝區位址。 緩衝區內的文字字串會指定音訊壓縮演算法的特性。

您 \_ \_ 可以使用 MCI DGV SETAUDIO \_ ALG 旗標來選取指定演算法的品質描述項。 如果省略此旗標，則會使用目前的演算法。

可用的演算法和描述項名稱取決於裝置。 每個裝置都會提供可用演算法的相關檔，以及適用描述項名稱的描述。 [MCI \_ QUALITY](mci-quality.md)命令可以定義其他描述項名稱。

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_RECORD"></span><span id="mci_dgv_setaudio_record"></span>MCI \_ DGV \_ SETAUDIO \_ 記錄
</dt> <dd>

指定錄製是否包含或排除音訊資料。 當結合的 MCI \_ 設定 \_ 為時，會記錄音訊資料。 當 \_ 將 MCI 設定為 \_ OFF 時，會排除音訊資料。 預設值包含音訊資料。

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_RIGHT"></span><span id="mci_dgv_setaudio_right"></span>MCI \_ DGV \_ SETAUDIO \_ RIGHT
</dt> <dd>

搭配使用設定的 MCI 時，可啟用正確的音訊通道 \_ \_ 。 當搭配使用的 MCI 設定為 OFF 時，會停用正確的音訊通道 \_ \_ 。 當此旗標搭配 MCI \_ DGV \_ SETAUDIO \_ VALUE 和 mci DGV SETAUDIO VOLUME 的組合使用時 \_ \_ \_ ，它會設定正確音訊通道的音量。

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_VALUE"></span><span id="mci_dgv_setaudio_value"></span>MCI \_ DGV \_ SETAUDIO \_ 值
</dt> <dd>

值是在 *lpSetAudio* 所識別之結構的 **dwValue** 成員中指定。 值的意義是由針對 MCI \_ DGV \_ SETAUDIO 專案旗標定義的常數所指定 \_ 。

</dd> <dt>

<span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>已 \_ 設定 \_ MCI
</dt> <dd>

停用指定的音訊通道。

</dd> <dt>

<span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ 設定 \_ 于
</dt> <dd>

啟用指定的音訊通道。

</dd> <dt>

<span id="MCI_SETAUDIO_OUTPUT"></span><span id="mci_setaudio_output"></span>MCI \_ SETAUDIO \_ 輸出
</dt> <dd>

修改低音、高音或音量旗標，讓它只修改播放的信號，而不是記錄的內容。 可能的話，這是監視輸入時的預設值。

</dd> </dl>

針對數位影片裝置， *lpSetAudio* 參數會指向 [**MCI \_ DGV \_ SETAUDIO \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setaudio_parmsa) 結構。

下列其他旗標適用于 **vcr** 裝置類型：

<dl> <dt>

<span id="MCI_VCR_SETAUDIO_RECORD"></span><span id="mci_vcr_setaudio_record"></span>MCI \_ VCR \_ SETAUDIO \_ 記錄
</dt> <dd>

將音訊錄製設定為 on 或 off，以搭配下列其中一個旗標使用：

MCI \_ 設定 \_ 于

錄製音訊。

已 \_ 設定 \_ MCI

錄製音訊。 您可能必須先關閉組合錄製 (使用 [mci \_ set](mci-set.md) 命令，並將 [mci \_ VCR \_ 組 \_ 組合 \_ 記錄] 旗標設為 [關閉]) ，然後才能關閉音訊錄製。

MCI \_ 曲目

*LpSetAudio* 所識別之結構的 **dwTrack** 成員會指定受命令影響的追蹤。

MCI \_ VCR \_ SETAUDIO \_ 來源

設定音訊來源。 此旗標必須與 MCI \_ VCR SETAUDIO 搭配 \_ 使用 \_ 以進行旗標。

MCI \_ VCR \_ SETAUDIO \_ 監視

設定音訊來源監視器。 此旗標必須與 MCI \_ VCR SETAUDIO 搭配 \_ 使用 \_ 以進行旗標。

MCI \_ VCR \_ SETAUDIO \_ 至

由 *lpSetAudio* 所識別之結構的 **dwTo** 成員，包含描述輸入或受監視輸入類型的常數。 它必須是下列其中一項：

<dl> <dd>

MCI \_ VCR \_ SRC \_ 類型 \_ 調諧器

類型為調諧器。

</dd> <dd>

MCI \_ VCR \_ SRC \_ 類型 \_ 行

類型為 line。

</dd> <dd>

MCI \_ VCR \_ SRC \_ 類型 \_ AUX

類型為輔助。

</dd> <dd>

MCI \_ VCR \_ SRC \_ 類型 \_ 泛型

類型為泛型。

</dd> <dd>

MCI \_ VCR \_ SRC \_ 類型 \_ 靜音

類型為靜音。 這只能與 MCI \_ VCR \_ SETAUDIO 來源旗標搭配使用 \_ 。

</dd> <dd>

MCI \_ VCR \_ SRC \_ 類型 \_ 輸出

類型為 output。

</dd> <dd>

MCI \_ VCR \_ SETAUDIO \_ 號碼

LpSetAudio 所識別之結構的 dwNumber 成員包含要使用的 dwTo 成員) 中所指定類型的音訊輸入 (。

</dd> </dl> </dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> </dl>

若為 VCR 裝置， *lpSetAudio* 參數會指向 [**MCI \_ VCR \_ SETAUDIO \_ PARMS**](mci-vcr-setaudio-parms.md) 結構。

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

 

