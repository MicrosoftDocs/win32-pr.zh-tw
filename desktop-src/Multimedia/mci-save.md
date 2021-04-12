---
title: 'MCI_SAVE 命令 (Mmsystem .h) '
description: MCI \_ SAVE 命令會儲存目前的檔案。
ms.assetid: 286e6f31-cb93-443b-8191-8c363b366eae
keywords:
- MCI_SAVE 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_SAVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a241c0379731e870940cd676c33ae192efc5d297
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464625"
---
# <a name="mci_save-command"></a>MCI \_ 儲存命令

MCI \_ SAVE 命令會儲存目前的檔案。 修改檔案的裝置在收到儲存訊息之前，不應終結原始複本。 影片-重迭和波形-音訊裝置會辨識此命令。 雖然數位視訊裝置和 MIDI sequencers 也會辨識此命令，但 MCIAVI 和 MCISEQ 驅動程式並不會執行此命令。

若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SAVE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SAVE_PARMS ) lpSave
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

<span id="lpSave"></span><span id="lpsave"></span><span id="LPSAVE"></span>*lpSave*
</dt> <dd>

[**MCI \_ 儲存 \_ PARMS**](mci-save-parms.md)結構的指標。 具有其他參數的 (裝置，可能會以裝置特定結構取代此結構。 ) 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

當您使用 MCI  GETDEVCAPS 可以[ \_ ](mci-getdevcaps.md) \_ \_ \_ 儲存旗標來呼叫 mci GETDEVCAPS 命令時，會傳回 TRUE 的裝置支援此命令。

下列其他旗標適用于所有支援 [MCI \_ 儲存](/windows)的裝置：

<dl> <dt>

<span id="MCI_SAVE_FILE"></span><span id="mci_save_file"></span>MCI \_ 儲存檔案 \_
</dt> <dd>

*LpSave* 所識別之結構的 **lpfilename** 成員包含包含目的地檔案名之緩衝區的位址。

</dd> </dl>

下列其他旗標適用于 **digitalvideo** 裝置類型：

<dl> <dt>

<span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI \_ DGV \_ RECT
</dt> <dd>

*LpSave* 所識別之結構的 **rc** 成員包含有效的矩形。 矩形會指定將儲存到指定檔案的框架緩衝區區域。 第一對座標指定矩形的左上角;第二個配對指定寬度和高度。 數位視訊裝置必須使用 [MCI \_ capture](mci-capture.md) 命令來捕獲框架緩衝區的內容。  (的影片重迭裝置也應使用 MCI \_ CAPTURE。 ) 此旗標是為了與現有的 MCI 影片重迭命令集相容。

</dd> <dt>

<span id="MCI_DGV_SAVE_ABORT"></span><span id="mci_dgv_save_abort"></span>MCI \_ DGV \_ 儲存 \_ 中止
</dt> <dd>

停止進行中的儲存作業。 這必須是唯一的旗標。

</dd> <dt>

<span id="MCI_DGV_SAVE_KEEPRESERVE"></span><span id="mci_dgv_save_keepreserve"></span>MCI \_ DGV \_ 儲存 \_ KEEPRESERVE
</dt> <dd>

未解除配置原始 [MCI \_ 保留](mci-reserve.md) 命令剩餘的未使用磁碟空間。

</dd> </dl>

針對數位影片裝置， *lpSave* 參數會指向 [**MCI \_ DGV \_ 儲存 \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_save_parmsa) 結構。

下列其他旗標會搭配覆迭 **裝置類型** 使用：

<dl> <dt>

<span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI \_ OVLY \_ RECT
</dt> <dd>

*LpSave* 所識別之結構的 **rc** 成員包含有效的顯示矩形，指出要儲存的影片緩衝區區域。

</dd> </dl>

針對影片重迭裝置， *lpSave* 參數會指向 [**MCI \_ OVLY \_ 儲存 \_ PARMS**](/previous-versions//dd743447(v=vs.85)) 結構。

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

 

