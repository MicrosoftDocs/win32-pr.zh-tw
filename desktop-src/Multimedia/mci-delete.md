---
title: 'MCI_DELETE 命令 (Mmsystem .h) '
description: MCI \_ DELETE 命令會移除檔案中的資料。 數位-視頻和波形-音訊裝置辨識此命令。
ms.assetid: cf7fae86-e81e-4006-9755-fd01f81aeb62
keywords:
- MCI_DELETE 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_DELETE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8c1b9f81712c842e06085c323ca2110c8e06784
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934685"
---
# <a name="mci_delete-command"></a>MCI \_ 刪除命令

MCI \_ DELETE 命令會移除檔案中的資料。 數位-視頻和波形-音訊裝置辨識此命令。

若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_DELETE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpDelete
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

\_ \_ 適用于數位視訊裝置、mci 測試的 mci 通知、mci 等待或 \_ 。 如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。

</dd> <dt>

<span id="lpDelete"></span><span id="lpdelete"></span><span id="LPDELETE"></span>*lpDelete*
</dt> <dd>

[**MCI \_ 泛型 \_ PARMS**](mci-generic-parms.md)結構的指標。 具有擴充命令集的 (裝置，可能會以裝置特定結構取代此結構。 ) 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

下列旗標適用于 **digitalvideo** 裝置類型：

<dl> <dt>

<span id="MCI_DGV_DELETE_AT"></span><span id="mci_dgv_delete_at"></span>MCI \_ DGV \_ 刪除 \_ 于
</dt> <dd>

矩形會包含在 *lpDelete* 所識別之結構的 **rc** 成員中。 矩形會指定要刪除之每個畫面格的部分。 使用這個旗標時，框架會保留在工作區中，而矩形所指定的區域會變成黑色。 如果省略旗標，則 MCI \_ 刪除會預設為整個畫面格，並從工作區中移除框架。

</dd> <dt>

<span id="MCI_DGV_DELETE_AUDIO_STREAM"></span><span id="mci_dgv_delete_audio_stream"></span>MCI \_ DGV \_ 刪除 \_ 音訊 \_ 串流
</dt> <dd>

音訊串流號碼包含在 *lpDelete* 所識別之結構的 **dwAudioStream** 成員中。 如果您使用此旗標，而且也想要刪除影片，您也必須使用 MCI \_ DGV \_ delete \_ 影片旗標 \_ 。  (如果未指定任何旗標，則會刪除所有音訊和影片資料流程中的資料。 ) 

</dd> <dt>

<span id="MCI_DGV_DELETE_VIDEO_STREAM"></span><span id="mci_dgv_delete_video_stream"></span>MCI \_ DGV \_ 刪除 \_ 影片 \_ 串流
</dt> <dd>

影片串流號碼包含在 *lpDelete* 所識別之結構的 **dwVideoStream** 成員中。 如果您使用此旗標，而且也想要刪除音訊，您也必須使用 MCI \_ DGV \_ delete \_ 音訊 \_ 串流旗標。  (如果未指定任何旗標，則會刪除所有音訊和影片資料流程中的資料。 ) 

</dd> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ 來源
</dt> <dd>

起始位置會包含在 *lpDelete* 所識別之結構的 **dwFrom** 成員中。 指派給位置值的單位，會以 Mci 設定的 \_ \_ 時間格式旗標，以 \_ [mci \_ set](mci-set.md) 命令來指定。

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ 至
</dt> <dd>

結束位置會包含在由 *lpDelete* 所識別之結構的 **dwTo** 成員中。 指派給位置值的單位是使用 mci \_ set \_ TIME \_ FORMAT 旗標來指定 \_ 。

</dd> </dl>

針對數位影片裝置， *lpDelete* 參數會指向 [**MCI \_ DGV \_ 刪除 \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_delete_parms) 結構。

下列旗標適用于 **waveaudio** 裝置類型：

<dl> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ 來源
</dt> <dd>

起始位置會包含在 *lpDelete* 所識別之結構的 **dwFrom** 成員中。 指派給位置值的單位是使用 mci \_ set \_ TIME \_ FORMAT 旗標來指定。 [ \_ ](mci-set.md)

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ 至
</dt> <dd>

結束位置會包含在由 *lpDelete* 所識別之結構的 **dwTo** 成員中。 指派給位置值的單位是使用 mci \_ set \_ TIME \_ FORMAT 旗標來指定 \_ 。

</dd> </dl>

針對波形音訊裝置， *lpDelete* 參數會指向 [**MCI \_ WAVE \_ DELETE \_ PARMS**](mci-wave-delete-parms.md) 結構。

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

 

