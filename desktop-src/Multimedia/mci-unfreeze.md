---
title: 'MCI_UNFREEZE 命令 (Mmsystem .h) '
description: MCI \_ 解除凍結命令會將動作還原至視訊緩衝區的區域，並透過 MCI \_ 凍結命令加以凍結。 數位影片、VCR 和影片重迭裝置會辨識此命令。
ms.assetid: 79ff1be5-6e30-4ef4-ab81-fc5643e3a72d
keywords:
- MCI_UNFREEZE 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_UNFREEZE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8736e27998330f9337bb21569e145a4395e90020
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105912"
---
# <a name="mci_unfreeze-command"></a>MCI \_ 解除凍結命令

MCI \_ 解除凍結命令會將動作還原至視訊緩衝區的區域，並透過 [MCI \_ 凍結](mci-freeze.md) 命令加以凍結。 數位影片、VCR 和影片重迭裝置會辨識此命令。

若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_UNFREEZE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpUnfreeze
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

<span id="lpUnfreeze"></span><span id="lpunfreeze"></span><span id="LPUNFREEZE"></span>*lpUnfreeze*
</dt> <dd>

[**MCI \_ 泛型 \_ PARMS**](mci-generic-parms.md)結構的指標。 具有擴充命令集的 (裝置，可能會以裝置特定結構取代此結構。 ) 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

下列其他旗標適用于 **digitalvideo** 裝置類型：

MCI \_ DGV \_ RECT

*LpUnfreeze* 所識別之結構的 **rc** 成員包含有效的顯示矩形。 矩形會指定框架緩衝區內的區域，其圖元應關閉其鎖定遮罩位。 系統會依照 [MCI \_ PUT](mci-put.md) 命令的說明指定矩形區域。 如果省略，矩形就會預設為整個框架緩衝區。 藉由使用一系列的凍結並解除凍結具有不同矩形的命令，即可描述鎖定遮罩位的任意模式。

針對數位影片裝置， *lpUnfreeze* 參數會指向 **MCI DGV，以 \_ \_ 解除凍結 \_ PARMS** 結構。 如需詳細資訊，請參閱 [**MCI \_ DGV \_ RECT \_ PARMS**](/windows/win32/api/digitalv/ns-digitalv-mci_dgv_rect_parms) 結構的批註。

下列其他旗標適用于 **vcr** 裝置類型：

<dl> <dt>

<span id="MCI_VCR_UNFREEZE_INPUT"></span><span id="mci_vcr_unfreeze_input"></span>MCI \_ VCR \_ 解除凍結 \_ 輸入
</dt> <dd>

解除凍結輸入。

</dd> <dt>

<span id="MCI_VCR_UNFREEZE_OUTPUT"></span><span id="mci_vcr_unfreeze_output"></span>MCI \_ VCR \_ 解除凍結 \_ 輸出
</dt> <dd>

解除凍結輸出。

</dd> </dl>

下列其他旗標會搭配覆迭 **裝置類型** 使用：

<dl> <dt>

<span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI \_ OVLY \_ RECT
</dt> <dd>

*LpUnfreeze* 所識別之結構的 **rc** 成員包含有效的顯示矩形。 這是必要參數。

</dd> </dl>

針對影片重迭裝置， *lpUnfreeze* 參數會指向 [**MCI \_ OVLY \_ RECT \_ PARMS**](mci-ovly-rect-parms.md) 結構。

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

 

