---
title: 'MCI_OPEN 命令 (Mmsystem .h) '
description: MCI \_ OPEN 命令會初始化裝置或檔案。 所有裝置都會辨識此命令。
ms.assetid: e2ee92b5-b10b-4408-950e-3002fe775b25
keywords:
- MCI_OPEN 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14d8b33e70a2e061b54260aeffc6e69432c469f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843044"
---
# <a name="mci_open-command"></a>MCI \_ 開啟命令

MCI \_ OPEN 命令會初始化裝置或檔案。 所有裝置都會辨識此命令。

若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_OPEN, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_OPEN_PARMS) lpOpen
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

MCI \_ 通知或 mci \_ 等候。 如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。

</dd> <dt>

<span id="lpOpen"></span><span id="lpopen"></span><span id="LPOPEN"></span>*lpOpen*
</dt> <dd>

[**MCI \_ 開啟 \_ PARMS**](mci-open-parms.md)結構的指標。 具有擴充命令集的 (裝置，可能會以裝置特定結構取代此結構。 ) 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

\_ \_ 只要在 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))函式中指定了裝置，就必須使用 MCI 開啟類型旗標。 如果您指定裝置類型常數來開啟裝置， \_ \_ \_ 除了 mci \_ 開啟 \_ 類型之外，您還必須指定 mci 開啟類型識別碼旗標。 如需裝置類型常數的清單，請參閱 [MCI 裝置類型](mci-device-types.md)。

如果在 \_ \_ 一開始開啟裝置或檔案時未指定 mci open 可共用旗標，則所有後續 \_ 的 mci 會開啟裝置或檔案的命令將會失敗。 如果裝置或檔案已經開啟，而且未指定此旗標，即使第一個開啟的命令指定的 MCI 開啟可共用，呼叫也會失敗 \_ \_ 。 針對 MCISEQ 開啟的檔案。WINSPOOL.DRV 和 MCIWAVE。WINSPOOL.DRV 裝置為 nonsharable。

裝置名稱中會忽略大小寫，但不能有開頭或尾端空白。

若要透過登錄) 中的專案來使用自動類型選取 (，請將檔案名和副檔名指派給 *lpOpen* 所識別之結構的 **lpstrElementName** 成員、將 **lpstrDeviceType** 成員設為 **Null**，並設定 MCI \_ OPEN \_ 元素旗標。

下列其他旗標適用于所有支援開啟 MCI 的裝置 \_ ：

<dl> <dt>

<span id="MCI_OPEN_ALIAS"></span><span id="mci_open_alias"></span>MCI \_ 開啟 \_ 別名
</dt> <dd>

別名會包含在 *lpOpen* 所識別之結構的 **lpstrAlias** 成員中。

</dd> <dt>

<span id="MCI_OPEN_SHAREABLE"></span><span id="mci_open_shareable"></span>\_開啟 \_ 共用的 MCI
</dt> <dd>

裝置或檔案應開啟為可共用。

</dd> <dt>

<span id="MCI_OPEN_TYPE"></span><span id="mci_open_type"></span>MCI \_ 開啟 \_ 類型
</dt> <dd>

裝置類型名稱或常數會包含在由 *lpOpen* 所識別之結構的 **lpstrDeviceType** 成員中。

</dd> <dt>

<span id="MCI_OPEN_TYPE_ID"></span><span id="mci_open_type_id"></span>MCI \_ 開啟 \_ 類型 \_ 識別碼
</dt> <dd>

由 *lpOpen* 所識別之結構的 **lpstrDeviceType** 成員的低序位文字包含標準的 MCI 裝置類型識別碼，而高序位字則選擇性地包含裝置的序數索引。 使用此旗標搭配 MCI \_ 開啟 \_ 類型旗標。

</dd> </dl>

下列其他旗標適用于複合裝置：

<dl> <dt>

<span id="MCI_OPEN_ELEMENT"></span><span id="mci_open_element"></span>MCI \_ OPEN \_ 元素
</dt> <dd>

檔案名會包含在 *lpOpen* 所識別之結構的 **lpstrElementName** 成員中。

</dd> <dt>

<span id="MCI_OPEN_ELEMENT_ID"></span><span id="mci_open_element_id"></span>MCI \_ 開啟 \_ 元素 \_ 識別碼
</dt> <dd>

*LpOpen* 所識別之結構的 **lpstrElementName** 成員會被解釋為 **DWORD** 值，而且具有裝置內部的意義。 使用此旗標搭配 MCI \_ OPEN \_ 元素旗標。

</dd> </dl>

下列其他旗標適用于 **digitalvideo** 裝置類型：

<dl> <dt>

<span id="MCI_DGV_OPEN_NOSTATIC"></span><span id="mci_dgv_open_nostatic"></span>MCI \_ DGV \_ OPEN \_ NOSTATIC
</dt> <dd>

裝置應該減少在調色板中的靜態 (系統) 色彩數目。 這會增加可用於轉譯影片資料流程的色彩數目。 此旗標只適用于與 Windows 共用調色板的裝置。

</dd> <dt>

<span id="MCI_DGV_OPEN_PARENT"></span><span id="mci_dgv_open_parent"></span>MCI \_ DGV \_ 開啟 \_ 父系
</dt> <dd>

父視窗控制碼是在 *lpOpen* 所識別之結構的 **hWndParent** 成員中指定。

</dd> <dt>

<span id="MCI_DGV_OPEN_WS"></span><span id="mci_dgv_open_ws"></span>MCI \_ DGV \_ 開啟 \_ WS
</dt> <dd>

視窗樣式是在 *lpOpen* 所識別之結構的 **dwStyle** 成員中指定。

</dd> <dt>

<span id="MCI_DGV_OPEN_16BIT"></span><span id="mci_dgv_open_16bit"></span>MCI \_ DGV \_ OPEN \_ 16BIT
</dt> <dd>

指出16位 MCI 裝置支援的喜好設定。

</dd> <dt>

<span id="MCI_DGV_OPEN_32BIT"></span><span id="mci_dgv_open_32bit"></span>MCI \_ DGV \_ 開啟 \_ 32 位
</dt> <dd>

指出32位 MCI 裝置支援的喜好設定。

</dd> </dl>

針對數位影片裝置， *lpOpen* 參數會指向 [**MCI \_ DGV \_ OPEN \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_open_parmsa) 結構。

下列其他旗標會搭配覆迭 **裝置類型** 使用：

<dl> <dt>

<span id="MCI_OVLY_OPEN_PARENT"></span><span id="mci_ovly_open_parent"></span>MCI \_ OVLY \_ 開啟 \_ 父系
</dt> <dd>

父視窗控制碼是在 *lpOpen* 所識別之結構的 **hWndParent** 成員中指定。

</dd> <dt>

<span id="MCI_OVLY_OPEN_WS"></span><span id="mci_ovly_open_ws"></span>MCI \_ OVLY \_ 開啟 \_ WS
</dt> <dd>

視窗樣式是在 *lpOpen* 所識別之結構的 **dwStyle** 成員中指定。 **DwStyle** 值會指定驅動程式將建立之視窗的樣式，並在應用程式未提供時加以顯示。 Style 參數會採用定義視窗樣式的整數。 這些常數與標準視窗樣式相同 (例如 WS \_ CHILD、ws \_ OVERLAPPEDWINDOW 或 ws \_ POPUP) 。

</dd> </dl>

針對影片重迭裝置， *lpOpen* 參數會指向 [**MCI \_ OVLY \_ OPEN \_ PARMS**](mci-ovly-open-parms.md) 結構。

下列其他旗標適用于 **waveaudio** 裝置類型：

<dl> <dt>

<span id="MCI_WAVE_OPEN_BUFFER"></span><span id="mci_wave_open_buffer"></span>MCI \_ WAVE \_ 開啟 \_ 緩衝區
</dt> <dd>

緩衝區長度是在 *lpOpen* 所識別之結構的 **dwBufferSeconds** 成員中指定。

</dd> </dl>

針對波形音訊裝置， *lpOpen* 參數會指向 [**MCI \_ WAVE \_ 開啟 \_ PARMS**](mci-wave-open-parms.md) 結構。 MCIWAVE 驅動程式需要非同步波形音訊裝置。

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

 

