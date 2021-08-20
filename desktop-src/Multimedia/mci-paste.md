---
title: 'MCI_PASTE 命令 (Mmsystem .h) '
description: MCI \_ 貼上命令會將剪貼簿中的資料貼入檔案中。 數位影片裝置辨識此命令。
ms.assetid: cad5799a-08ef-4e34-803a-415b937d8fbd
keywords:
- MCI_PASTE 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_PASTE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bdc7b27838236b09952a009f1cb8c7d60091afb6634bbd74fad213f013f6e2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138229"
---
# <a name="mci_paste-command"></a>MCI \_ 貼上命令

MCI \_ 貼上命令會將剪貼簿中的資料貼入檔案中。 數位影片裝置辨識此命令。

若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_PASTE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_PASTE_PARMS) lpPaste
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

<span id="lpPaste"></span><span id="lppaste"></span><span id="LPPASTE"></span>*lpPaste*
</dt> <dd>

[**MCI \_ DGV \_ 貼上 \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_paste_parms)結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

下列其他旗標適用于數位視訊裝置：

<dl> <dt>

<span id="MCI_DGV_PASTE_AT"></span><span id="mci_dgv_paste_at"></span>MCI \_ DGV \_ 貼 \_ 在
</dt> <dd>

矩形會包含在 *lpPaste* 所識別之結構的 **rc** 成員中。 矩形的前兩個值會指定框架內的點，以放置剪貼簿資訊。 如果矩形高度和寬度為非零值，當剪貼簿的內容貼到框架中時，剪貼簿的內容會調整為這些維度。 如果省略旗標，則會將 MCI \_ 貼上預設為整個框架矩形。

</dd> <dt>

<span id="MCI_DGV_PASTE_AUDIO_STREAM"></span><span id="mci_dgv_paste_audio_stream"></span>MCI \_ DGV \_ 貼上 \_ 音訊 \_ 串流
</dt> <dd>

音訊串流號碼包含在 *lpPaste* 所識別之結構的 **dwAudioStream** 成員中。 如果剪貼簿中只有一個音訊串流，則會將音訊資料貼入指定的資料流程。 如果剪貼簿中有一個以上的音訊串流，資料流程就會指出資料流程順序的起始數位。 如果您使用此旗標，而且也想要貼上影片，您也必須使用 MCI \_ DGV \_ 貼上影片的旗標 \_ \_ 。  (如果未指定任何旗標，則會從第一個音訊和影片串流開始貼上所有音訊和影片串流。 每個貼上的資料流程都會保留其原始資料流程號碼。 ) 

</dd> <dt>

<span id="MCI_DGV_PASTE_INSERT"></span><span id="mci_dgv_paste_insert"></span>MCI \_ DGV \_ 貼上 \_ 插入
</dt> <dd>

剪貼簿資料應插入至現有的工作區中，位於 MCI 所指定的位置， \_ 以進行旗標。 在插入點之後，任何現有的資料都會移至工作區，以騰出空間。 此為預設值。

</dd> <dt>

<span id="MCI_DGV_PASTE_OVERWRITE"></span><span id="mci_dgv_paste_overwrite"></span>MCI \_ DGV \_ 貼上 \_ 覆寫
</dt> <dd>

剪貼簿資料應取代已存在於工作區中的資料。 工作區資料會在插入點之後取代。

</dd> <dt>

<span id="MCI_DGV_PASTE_VIDEO_STREAM"></span><span id="mci_dgv_paste_video_stream"></span>MCI \_ DGV \_ 貼上 \_ 影片 \_ 串流
</dt> <dd>

影片串流號碼包含在 *lpPaste* 所識別之結構的 **dwVideoStream** 成員中。 如果剪貼簿中只有一個影片串流，則會將影片資料貼入指定的資料流程。 如果剪貼簿中有一個以上的影片串流，資料流程就會指出資料流程順序的起始數位。 如果您使用此旗標，而且也想要貼上音訊，您也必須使用 MCI \_ DGV \_ 貼上 \_ 音訊 \_ 串流旗標。  (如果未指定任何旗標，則會從第一個音訊和影片串流開始貼上所有音訊和影片串流。 每個貼上的資料流程都會保留其原始資料流程號碼。 ) 

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ 至
</dt> <dd>

Position 值會包含在 *lpPaste* 所識別之結構的 **dwTo** 成員中。 Position 值指定開始將資料貼入工作區的位置。 如果省略此旗標，位置就會預設為目前的位置。

</dd> </dl>

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

 

