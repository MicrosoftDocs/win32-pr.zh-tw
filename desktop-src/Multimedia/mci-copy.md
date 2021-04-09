---
title: 'MCI_COPY 命令 (Mmsystem .h) '
description: MCI \_ 複製命令會將資料複製到剪貼簿。 數位影片裝置辨識此命令。
ms.assetid: 41807920-3312-4cdb-82e6-6ab4b9b35162
keywords:
- MCI_COPY 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_COPY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4c27950b9599d0b565b982eb59755e4d3f2ea65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934436"
---
# <a name="mci_copy-command"></a>MCI \_ 複製命令

MCI \_ 複製命令會將資料複製到剪貼簿。 數位影片裝置辨識此命令。

若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_COPY, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_COPY_PARMS) lpCopy
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

<span id="lpCopy"></span><span id="lpcopy"></span><span id="LPCOPY"></span>*lpCopy*
</dt> <dd>

[**MCI \_ DGV \_ 複製 \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_copy_parms)結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

下列其他旗標適用于數位視訊裝置：

<dl> <dt>

<span id="MCI_DGV_COPY_AT"></span><span id="mci_dgv_copy_at"></span>MCI \_ DGV \_ 複製 \_ 位置
</dt> <dd>

矩形會包含在 *lpCopy* 所識別之結構的 **rc** 成員中。 矩形會指定要複製的每個畫面格的部分。 如果省略旗標，MCI 複製會複製 \_ 整個框架。

</dd> <dt>

<span id="MCI_DGV_COPY_AUDIO_STREAM"></span><span id="mci_dgv_copy_audio_stream"></span>MCI \_ DGV \_ 複製 \_ 音訊 \_ 串流
</dt> <dd>

音訊串流號碼包含在 *lpCopy* 所識別之結構的 **dwAudioStream** 成員中。 如果您使用此旗標，而且也想要複製影片，您也必須使用 MCI \_ DGV \_ 複製 \_ 影片旗標 \_ 。  (如果未指定任何旗標，則會複製所有音訊和影片資料流程中的資料。 ) 

</dd> <dt>

<span id="MCI_DGV_COPY_VIDEO_STREAM"></span><span id="mci_dgv_copy_video_stream"></span>MCI \_ DGV \_ 複製 \_ 影片 \_ 串流
</dt> <dd>

影片串流號碼包含在 *lpCopy* 所識別之結構的 **dwVideoStream** 成員中。 如果您使用此旗標，而且也想要複製音訊，您也必須使用 MCI \_ DGV \_ 複製 \_ 音訊 \_ 串流旗標。  (如果未指定任何旗標，則會複製所有音訊和影片資料流程中的資料。 ) 

</dd> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ 來源
</dt> <dd>

起始位置會包含在 *lpCopy* 所識別之結構的 **dwFrom** 成員中。 指派給位置值的單位，會以 Mci 設定的 \_ \_ 時間格式旗標，以 \_ [mci \_ set](mci-set.md) 命令來指定。

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ 至
</dt> <dd>

結束位置會包含在由 *lpCopy* 所識別之結構的 **dwTo** 成員中。 指派給位置值的單位，會以 MCI 設定的 \_ \_ 時間格式旗標，以 \_ mci \_ set 命令來指定。

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

 

