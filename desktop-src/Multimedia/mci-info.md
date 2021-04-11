---
title: 'MCI_INFO 命令 (Mmsystem .h) '
description: MCI \_ INFO 命令會從裝置取出字串資訊。
ms.assetid: aed3fed3-87b9-4673-9171-4f57770d765c
keywords:
- MCI_INFO 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_INFO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9f6ba5be1c2a4ce94b880a87a468c594bc5b676
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105708"
---
# <a name="mci_info-command"></a>MCI \_ 資訊命令

MCI \_ INFO 命令會從裝置取出字串資訊。 所有裝置都會辨識此命令。 資訊會以 *lpInfo* 所識別之結構的 **lpstrReturn** 成員傳回。 **DwRetSize** 成員會指定傳回之資料的緩衝區長度。

若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_INFO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_INFO_PARMS) lpInfo
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

<span id="lpInfo"></span><span id="lpinfo"></span><span id="LPINFO"></span>*lpInfo*
</dt> <dd>

[**MCI \_ 資訊 \_ PARMS**](mci-info-parms.md)結構的指標。 具有擴充命令集的 (裝置，可能會以裝置特定結構取代此結構。 ) 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

下列其他標準和命令特定旗標適用于所有支援 MCI 資訊的裝置 \_ ：

<dl> <dt>

<span id="MCI_INFO_PRODUCT"></span><span id="mci_info_product"></span>MCI \_ 資訊 \_ 產品
</dt> <dd>

取得與裝置相關聯之硬體的描述。 裝置應該提供識別驅動程式和所使用硬體的描述。

</dd> </dl>

下列其他旗標適用于 **cdaudio** 裝置類型：

<dl> <dt>

<span id="MCI_INFO_MEDIA_IDENTITY"></span><span id="mci_info_media_identity"></span>MCI \_ 資訊 \_ 媒體身分 \_ 識別
</dt> <dd>

針對目前已在正在進行查詢的播放程式中載入的音訊 CD 產生唯一識別碼。 此旗標會傳回16個十六進位數位的字串。

</dd> <dt>

<span id="MCI_INFO_MEDIA_UPC"></span><span id="mci_info_media_upc"></span>MCI \_ 資訊 \_ 媒體 \_ UPC
</dt> <dd>

產生在音訊 CD 上編碼 (UPC) 的通用產品程式碼。 UPC 是數位的字串。 它可能不適用於所有 Cd。

</dd> </dl>

下列其他旗標適用于 **digitalvideo** 裝置類型：

<dl> <dt>

<span id="MCI_DGV_INFO_ITEM"></span><span id="mci_dgv_info_item"></span>MCI \_ DGV \_ 資訊 \_ 專案
</dt> <dd>

常數，表示所需的資訊會包含在 *lpInfo* 所識別之結構的 **dwItem** 成員中。 下列常數是針對數位視訊裝置所定義：

</dd> <dt>

<span id="MCI_DGV_INFO_AUDIO_ALG"></span><span id="mci_dgv_info_audio_alg"></span>MCI \_ DGV \_ 資訊 \_ 音訊 \_ ALG
</dt> <dd>

傳回目前音訊壓縮演算法的名稱。

</dd> <dt>

<span id="MCI_DGV_INFO_AUDIO_QUALITY"></span><span id="mci_dgv_info_audio_quality"></span>MCI \_ DGV \_ 資訊 \_ 音訊 \_ 品質
</dt> <dd>

傳回目前音訊品質描述項的名稱。

</dd> <dt>

<span id="MCI_DGV_INFO_STILL_ALG"></span><span id="mci_dgv_info_still_alg"></span>MCI \_ DGV \_ 資訊 \_ 還是 \_ ALG
</dt> <dd>

傳回目前靜止影像壓縮演算法的名稱。

</dd> <dt>

<span id="MCI_DGV_INFO_STILL_QUALITY"></span><span id="mci_dgv_info_still_quality"></span>MCI \_ DGV \_ 資訊 \_ 仍為 \_ 品質
</dt> <dd>

傳回目前靜止影像品質描述項的名稱。

</dd> <dt>

<span id="MCI_DGV_INFO_USAGE"></span><span id="mci_dgv_info_usage"></span>MCI \_ DGV \_ 資訊 \_ 使用方式
</dt> <dd>

傳回字串，描述可能由視覺效果的擁有者或工作區中的資料所造成的使用限制。

</dd> <dt>

<span id="MCI_DGV_INFO_VIDEO_ALG"></span><span id="mci_dgv_info_video_alg"></span>MCI \_ DGV \_ 資訊 \_ 影片 \_ ALG
</dt> <dd>

傳回目前視訊壓縮演算法的名稱。

</dd> <dt>

<span id="MCI_DGV_INFO_VIDEO_QUALITY"></span><span id="mci_dgv_info_video_quality"></span>MCI \_ DGV \_ 資訊 \_ 影片 \_ 品質
</dt> <dd>

傳回目前影片品質描述項的名稱。

</dd> <dt>

<span id="MCI_INFO_VERSION"></span><span id="mci_info_version"></span>MCI \_ 資訊 \_ 版本
</dt> <dd>

傳回設備磁碟機和硬體的版本層級。 設備磁碟機開發人員必須記錄所傳回字串的語法。

</dd> <dt>

<span id="MCI_DGV_INFO_TEXT"></span><span id="mci_dgv_info_text"></span>MCI \_ DGV \_ 資訊 \_ 文字
</dt> <dd>

取得視窗標題。

</dd> <dt>

<span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>MCI \_ 資訊 \_ 檔案
</dt> <dd>

取得以 [MCI \_ OPEN](mci-open.md) 或 [mci \_ LOAD](mci-load.md) 命令指定之最後一個檔案的路徑和檔案名。 如果未指定檔案，裝置會傳回以 null 結束的字串。 只有傳回 **TRUE** 給 mci \_ GETDEVCAPS \_ 使用 \_ [mci \_ GETDEVCAPS](mci-getdevcaps.md) 命令的 [檔案] 旗標的裝置才支援此旗標。

</dd> </dl>

針對數位影片裝置， *lpInfo* 會指向 [**MCI \_ DGV \_ INFO \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_info_parmsa) 結構。

下列其他旗標適用于 **sequencer** 裝置類型：

<dl> <dt>

<span id="MCI_INFO_COPYRIGHT"></span><span id="mci_info_copyright"></span>MCI \_ 資訊 \_ 著作權
</dt> <dd>

從著作權中繼活動取得 MIDI 檔案的著作權注意事項。

</dd> <dt>

<span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>MCI \_ 資訊 \_ 檔案
</dt> <dd>

取得目前檔案的檔案名。 只有 **當您** 使用 mci GETDEVCAPS [使用檔案] 旗標呼叫 [mci \_ GETDEVCAPS](mci-getdevcaps.md) 命令時，裝置才會支援此旗標 \_ \_ \_ 。

</dd> <dt>

<span id="MCI_INFO_NAME"></span><span id="mci_info_name"></span>MCI \_ 資訊 \_ 名稱
</dt> <dd>

從 sequence/track name 中繼事件取得序列名稱。

</dd> </dl>

下列其他旗標適用于 **vcr** 裝置類型：

<dl> <dt>

<span id="MCI_VCR_INFO_VERSION"></span><span id="mci_vcr_info_version"></span>MCI \_ VCR \_ 資訊 \_ 版本
</dt> <dd>

設定 [**MCI \_ INFO \_ PARMS**](mci-info-parms.md)結構的 **lpstrReturn** 成員，以指向版本號碼。 也會將 **dwRetSize** 成員設定為等於指向之字串的長度。

</dd> </dl>

下列其他旗標 **適用于重迭裝置類型** ：

<dl> <dt>

<span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>MCI \_ 資訊 \_ 檔案
</dt> <dd>

取得目前檔案的檔案名。 只有傳回 **TRUE** 給 mci \_ GETDEVCAPS \_ 使用 \_ [mci \_ GETDEVCAPS](mci-getdevcaps.md) 命令的 [檔案] 旗標的裝置才支援此旗標。

</dd> <dt>

<span id="MCI_OVLY_INFO_TEXT"></span><span id="mci_ovly_info_text"></span>MCI \_ OVLY \_ 資訊 \_ 文字
</dt> <dd>

取得與影片重迭裝置相關聯之視窗的標題。

</dd> </dl>

下列其他旗標適用于 **waveaudio** 裝置類型：

<dl> <dt>

<span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>MCI \_ 資訊 \_ 檔案
</dt> <dd>

取得目前檔案的檔案名。 **當您** 使用 mci GETDEVCAPS [使用檔案] 旗標呼叫 [mci \_ GETDEVCAPS](mci-getdevcaps.md)命令時，裝置會支援此旗標 \_ \_ \_ 。

</dd> <dt>

<span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI \_ WAVE \_ 輸入
</dt> <dd>

取得目前輸入的產品名稱。

</dd> <dt>

<span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI \_ WAVE \_ 輸出
</dt> <dd>

取得目前輸出的產品名稱，且其值為裝置特定。

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

 

