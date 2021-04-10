---
title: 'MCI_PUT 命令 (Mmsystem .h) '
description: MCI \_ PUT 命令會設定來源、目的地和框架矩形。 數位影片和影片重迭裝置會辨識此命令。
ms.assetid: 9d81682b-6546-4e6d-a6df-e2de8c013b66
keywords:
- MCI_PUT 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_PUT
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8fa4af30aa2b3aa6f7cdd50f453bc8edca83334
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106536"
---
# <a name="mci_put-command"></a>MCI \_ PUT 命令

MCI \_ PUT 命令會設定來源、目的地和框架矩形。 數位影片和影片重迭裝置會辨識此命令。

若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_PUT, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpDest
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

<span id="lpDest"></span><span id="lpdest"></span><span id="LPDEST"></span>*lpDest*
</dt> <dd>

[**MCI \_ 泛型 \_ PARMS**](mci-generic-parms.md)結構的指標。 具有擴充命令集的 (裝置，可能會以裝置特定結構取代此結構。 ) 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

下列其他旗標適用于 **digitalvideo** 裝置類型：

<dl> <dt>

<span id="MCI_DGV_PUT_CLIENT"></span><span id="mci_dgv_put_client"></span>MCI \_ DGV \_ PUT \_ 用戶端
</dt> <dd>

針對 MCI DGV RECT 定義的矩形會 \_ \_ 套用至用戶端視窗的位置。 指定的矩形是相對於顯示視窗的父視窗。 您 \_ \_ \_ 必須使用此旗標同時設定 MCI DGV PUT 視窗。

</dd> <dt>

<span id="MCI_DGV_PUT_DESTINATION"></span><span id="mci_dgv_put_destination"></span>MCI \_ DGV \_ PUT \_ DESTINATION
</dt> <dd>

針對 MCI DGV RECT 定義的矩形會 \_ \_ 指定目的地矩形。 目的地矩形會指定與此設備磁碟機實例相關聯的用戶端視窗部分，以顯示影像或影片。

</dd> <dt>

<span id="MCI_DGV_PUT_FRAME"></span><span id="mci_dgv_put_frame"></span>MCI \_ DGV \_ PUT \_ FRAME
</dt> <dd>

針對 MCI DGV RECT 定義的矩形會 \_ \_ 套用至框架矩形。 框架矩形會指定框架緩衝區的部分，作為從影片矩形取得之影片影像的目的地。 影片應該調整以符合框架緩衝區矩形。

矩形是在框架緩衝區座標中指定。 預設的矩形是完整的框架緩衝區。 指定此矩形可讓裝置在 digitizes 資料時調整影像。 無法調整映射的裝置會使用 MCIERR 不支援的功能來拒絕此命令 \_ \_ 。 您可以使用 MCI \_ GETDEVCAPS \_ 來 \_ 延展旗標與 [mci \_ GETDEVCAPS](mci-getdevcaps.md) 命令，以判斷裝置是否調整映射。 如果裝置無法調整影像，則會傳回 **FALSE** 。

</dd> <dt>

<span id="MCI_DGV_PUT_SOURCE"></span><span id="mci_dgv_put_source"></span>MCI \_ DGV \_ PUT \_ 來源
</dt> <dd>

針對 MCI DGV RECT 定義的矩形會 \_ \_ 指定來源矩形。 來源矩形會指定要調整的框架緩衝區部分，以符合目的矩形。

</dd> <dt>

<span id="MCI_DGV_PUT_VIDEO"></span><span id="mci_dgv_put_video"></span>MCI \_ DGV \_ PUT \_ 影片
</dt> <dd>

針對 MCI DGV RECT 定義的矩形會 \_ \_ 套用至影片矩形。 影片矩形會指定目前展示來源的哪個部分儲存在框架緩衝區中。 矩形是使用展示來源的自然座標來指定。 它允許在框架緩衝區中儲存影像和影片之前所發生的裁剪規格。 預設矩形是完整的主動式掃描區域或完整解壓縮的影像和影片。

</dd> <dt>

<span id="MCI_DGV_PUT_WINDOW"></span><span id="mci_dgv_put_window"></span>MCI \_ DGV \_ PUT \_ 視窗
</dt> <dd>

針對 MCI DGV RECT 定義的矩形會 \_ \_ 套用至顯示視窗。 這個矩形相對於顯示視窗的父視窗， (通常是桌面) 。 如果未指定視窗，則會預設為初始視窗大小和位置。

</dd> <dt>

<span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI \_ DGV \_ RECT
</dt> <dd>

*LpDest* 所識別之結構的 **rc** 成員包含有效的矩形。

</dd> </dl>

針對數位影片裝置， *lpDest* 會指向 [**MCI \_ DGV \_ PUT \_ PARMS**](/previous-versions//dd743397(v=vs.85)) 結構。

下列其他旗標會搭配覆迭 **裝置類型** 使用：

<dl> <dt>

<span id="MCI_OVLY_PUT_DESTINATION"></span><span id="mci_ovly_put_destination"></span>MCI \_ OVLY \_ PUT \_ DESTINATION
</dt> <dd>

針對 MCI OVLY RECT 定義的矩形會 \_ \_ 指定用來顯示影像的用戶端視窗區域。 矩形包含相對於視窗原點之影像的位移和可見範圍。 如果框架正在延展，則來源會延伸至目的地矩形。

</dd> <dt>

<span id="MCI_OVLY_PUT_FRAME"></span><span id="mci_ovly_put_frame"></span>MCI \_ OVLY \_ PUT \_ FRAME
</dt> <dd>

針對 MCI OVLY RECT 定義的矩形 \_ \_ 會指定用來接收影片影像的影片緩衝區區域。 矩形包含相對於影片緩衝區原點的緩衝區區域位移與範圍。

</dd> <dt>

<span id="MCI_OVLY_PUT_SOURCE"></span><span id="mci_ovly_put_source"></span>MCI \_ OVLY \_ PUT \_ 來源
</dt> <dd>

針對 MCI OVLY RECT 定義的矩形會 \_ \_ 指定用來做為數位影像來源的影片緩衝區區域。 矩形包含相對於影片緩衝區之剪輯矩形的位移和範圍（相對於其來源）。

</dd> <dt>

<span id="MCI_OVLY_PUT_VIDEO"></span><span id="mci_ovly_put_video"></span>MCI \_ OVLY \_ PUT \_ 影片
</dt> <dd>

針對 MCI OVLY RECT 定義的矩形會 \_ \_ 指定影片緩衝區的影片來源捕捉區域。 矩形包含影片來源（相對於其原點）之裁剪矩形的位移與範圍。

</dd> <dt>

<span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI \_ OVLY \_ RECT
</dt> <dd>

*LpDest* 所識別之結構的 **rc** 成員包含有效的顯示矩形。 如果未指定此旗標，則預設矩形會符合要裁剪的影片緩衝區或視窗的座標。

</dd> </dl>

針對影片重迭裝置， *lpDest* 會指向 [**MCI \_ OVLY \_ RECT \_ PARMS**](mci-ovly-rect-parms.md) 結構。

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

 

