---
title: 'MCI_FREEZE 命令 (Mmsystem .h) '
description: MCI \_ 凍結命令會凍結顯示器上的動作。 數位影片、影片重迭和 VCR 裝置都會辨識此命令。
ms.assetid: 6f90984a-24dc-4046-8234-986b2125bab4
keywords:
- MCI_FREEZE 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_FREEZE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 705117aef85fe69382657c647240849b515afa07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024790"
---
# <a name="mci_freeze-command"></a>MCI \_ 凍結命令

MCI \_ 凍結命令會凍結顯示器上的動作。 數位影片、影片重迭和 VCR 裝置都會辨識此命令。

若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_FREEZE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpFreeze
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

<span id="lpFreeze"></span><span id="lpfreeze"></span><span id="LPFREEZE"></span>*lpFreeze*
</dt> <dd>

[**MCI \_ 泛型 \_ PARMS**](mci-generic-parms.md)結構的指標。 具有其他參數的 (裝置，可能會以裝置特定結構取代此結構。 ) 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

**Digitalvideo** 裝置類型會使用下列其他旗標：

<dl> <dt>

<span id="MCI_DGV_FREEZE_AT"></span><span id="mci_dgv_freeze_at"></span>MCI \_ DGV \_ 凍結 \_ 于
</dt> <dd>

*LpFreeze* 所識別之結構的 **rc** 成員包含有效的矩形。 矩形會指定框架緩衝區內的區域，以開啟每個圖元的鎖定遮罩位。 在關閉鎖定遮罩位之前，將不會更新指定的圖元。 如果未指定此旗標，矩形就會預設為整個框架緩衝區。 只有當[mci \_ GETDEVCAPS](mci-getdevcaps.md)命令針對 mci  \_ DGV \_ GETDEVCAPS \_ 可鎖定旗標傳回 TRUE 時，才支援此旗標 \_ 。

</dd> <dt>

<span id="MCI_DGV_FREEZE_OUTSIDE"></span><span id="mci_dgv_freeze_outside"></span>MCI \_ DGV \_ 凍結 \_
</dt> <dd>

在旗標上為 MCI DGV 凍結指定的區域以外的區域 \_ \_ \_ 已凍結。

</dd> </dl>

針對數位影片裝置， *lpFreeze* 參數會指向 [**MCI \_ DGV \_ 凍結 \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_rect_parms) 結構。

**Vcr** 裝置類型會使用下列其他旗標：

<dl> <dt>

<span id="MCI_VCR_FREEZE_FIELD"></span><span id="mci_vcr_freeze_field"></span>MCI \_ VCR \_ 凍結 \_ 欄位
</dt> <dd>

只凍結目前框架的一個成員。

</dd> <dt>

<span id="MCI_VCR_FREEZE_FRAME"></span><span id="mci_vcr_freeze_frame"></span>MCI \_ VCR \_ 凍結 \_ 框架
</dt> <dd>

凍結目前框架的兩個欄位。

</dd> <dt>

<span id="MCI_VCR_FREEZE_INPUT"></span><span id="mci_vcr_freeze_input"></span>MCI \_ VCR \_ 凍結 \_ 輸入
</dt> <dd>

凍結螢幕上的目前畫面格 (用於錄製) 。

</dd> <dt>

<span id="MCI_VCR_FREEZE_OUTPUT"></span><span id="mci_vcr_freeze_output"></span>MCI \_ VCR \_ 凍結 \_ 輸出
</dt> <dd>

從 VCR (中，凍結框架捕獲) 所用的目前畫面格。

</dd> </dl>

若為 VCR 裝置， *lpFreeze* 參數會指向 [**MCI \_ 一般 \_ PARMS**](mci-generic-parms.md) 結構。

覆 **迭裝置類型** 會使用下列其他旗標：

<dl> <dt>

<span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI \_ OVLY \_ RECT
</dt> <dd>

*LpFreeze* 所識別之結構的 **rc** 成員包含有效的矩形。 如果未指定此旗標，設備磁碟機將會凍結整個框架。

</dd> </dl>

針對影片重迭裝置， *lpFreeze* 參數會指向 [**MCI \_ OVLY \_ RECT \_ PARMS**](mci-ovly-rect-parms.md) 結構。

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

 

