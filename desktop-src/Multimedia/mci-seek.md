---
title: 'MCI_SEEK 命令 (Mmsystem .h) '
description: MCI \_ 搜尋命令會儘快變更內容中的目前位置。
ms.assetid: 5ffab964-a28d-4dc2-ac04-da501cd34d24
keywords:
- MCI_SEEK 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_SEEK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0e34f6fa823092968e74515a885e7a40db9f2d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024785"
---
# <a name="mci_seek-command"></a>MCI \_ 搜尋命令

MCI \_ 搜尋命令會儘快變更內容中的目前位置。 影片和音訊輸出會在搜尋期間停用。 搜尋完成後，裝置就會停止。 CD 音訊、數位影片、MIDI sequencer、VCR、videodisc 和波形-音訊裝置都會辨識此命令。

若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SEEK, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SEEK_PARMS) lpSeek
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

<span id="lpSeek"></span><span id="lpseek"></span><span id="LPSEEK"></span>*lpSeek*
</dt> <dd>

[**MCI \_ 搜尋 \_ PARMS**](mci-seek-parms.md)結構的指標。 具有擴充命令集的 (裝置，可能會以裝置特定結構取代此結構。 ) 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

如果裝置的資料取樣大小大於1個位元組 (例如使用波形音訊身歷聲資料) ，此命令會在指定的位置與範例開始不一致時，移至最接近樣本的開頭。

下列其他旗標適用于所有支援 MCI 搜尋的裝置 \_ ：

<dl> <dt>

<span id="MCI_SEEK_TO_END"></span><span id="mci_seek_to_end"></span>MCI \_ 搜尋 \_ \_ 結束
</dt> <dd>

搜尋至內容的結尾。

</dd> <dt>

<span id="MCI_SEEK_TO_START"></span><span id="mci_seek_to_start"></span>MCI \_ 搜尋 \_ \_ 開始
</dt> <dd>

搜尋內容的開頭。

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ 至
</dt> <dd>

位置會包含在 *lpSeek* 所識別之結構的 **dwTo** 成員中。 指派給位置值的單位，會以 Mci 設定的 \_ \_ 時間格式旗標，以 \_ [mci \_ set](mci-set.md) 命令來指定。 請勿使用此旗標，讓 \_ mci \_ 搜尋 \_ 結束或 mci \_ 搜尋 \_ \_ 開始。

</dd> </dl>

下列其他旗標適用于 **vcr** 裝置類型：

<dl> <dt>

<span id="MCI_VCR_SEEK_AT"></span><span id="mci_vcr_seek_at"></span>MCI \_ VCR \_ 搜尋 \_ 位置
</dt> <dd>

*LpSeek* 所識別之結構的 **dwAt** 成員，包含整個命令開始的時間。

</dd> <dt>

<span id="MCI_VCR_SEEK_MARK"></span><span id="mci_vcr_seek_mark"></span>MCI \_ VCR \_ 搜尋 \_ 標記
</dt> <dd>

*LpSeek* 所識別之結構的 **dwMark** 成員包含要搜尋的編號標記。

</dd> <dt>

<span id="MCI_VCR_SEEK_REVERSE"></span><span id="mci_vcr_seek_reverse"></span>MCI \_ VCR \_ 搜尋 \_ 反向
</dt> <dd>

搜尋方向為反向;這僅適用于 MCI \_ VCR \_ 搜尋 \_ 標記旗標。

</dd> </dl>

若為 VCR 裝置， *lpSeek* 參數會指向 [**MCI \_ VCR \_ 搜尋 \_ PARMS**](mci-vcr-seek-parms.md) 結構。

下列其他旗標適用于 **videodisc** 裝置類型：

<dl> <dt>

<span id="MCI_VD_SEEK_REVERSE"></span><span id="mci_vd_seek_reverse"></span>MCI \_ VD \_ 搜尋 \_ 反向
</dt> <dd>

搜尋方向為反向。

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

 

