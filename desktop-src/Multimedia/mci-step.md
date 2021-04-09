---
title: 'MCI_STEP 命令 (Mmsystem .h) '
description: MCI \_ 步驟命令會將玩家帶到一或多個畫面。 數位影片、VCR 和 CAV 格式的 videodisc 裝置都會辨識此命令。
ms.assetid: 8d976840-fe9d-4393-b9fc-10f847166b1b
keywords:
- MCI_STEP 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_STEP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd81b3ad0e1f10c14d68df12399045149f686a8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093795"
---
# <a name="mci_step-command"></a>MCI \_ 步驟命令

MCI \_ 步驟命令會將玩家帶到一或多個畫面。 數位影片、VCR 和 CAV 格式的 videodisc 裝置都會辨識此命令。

若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_STEP, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpStep
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

<span id="lpStep"></span><span id="lpstep"></span><span id="LPSTEP"></span>*lpStep*
</dt> <dd>

[**MCI \_ 泛型 \_ PARMS**](mci-generic-parms.md)結構的指標。 具有擴充命令集的 (裝置，可能會以裝置特定結構取代此結構。 ) 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

此命令支援在 MCI  \_ GETDEVCAPS \_ 具有 \_ [mci \_ GETDEVCAPS](mci-getdevcaps.md)命令的影片旗標時，傳回 TRUE 的裝置。

下列其他旗標適用于 **digitalvideo** 裝置類型：

<dl> <dt>

<span id="MCI_DGV_STEP_FRAMES"></span><span id="mci_dgv_step_frames"></span>MCI \_ DGV \_ 步驟 \_ 框架
</dt> <dd>

*LpStep* 所識別之結構的 **dwFrames** 成員會指定在顯示另一個影像之前要前進的框架數目。

</dd> <dt>

<span id="MCI_DGV_STEP_REVERSE"></span><span id="mci_dgv_step_reverse"></span>MCI \_ DGV \_ 步驟 \_ 反轉
</dt> <dd>

反向步驟。

</dd> </dl>

針對數位影片裝置， *lpStep* 參數會指向 [**MCI \_ DGV \_ 步驟 \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_step_parms) 結構。

下列其他旗標適用于 **vcr** 裝置類型：

<dl> <dt>

<span id="MCI_VCR_STEP_FRAMES"></span><span id="mci_vcr_step_frames"></span>MCI \_ VCR \_ 步驟 \_ 框架
</dt> <dd>

*LpStep* 所識別之結構的 **dwFrames** 成員會指定在顯示另一個影像之前要前進的框架數目。

</dd> <dt>

<span id="MCI_VCR_STEP_REVERSE"></span><span id="mci_vcr_step_reverse"></span>MCI \_ VCR \_ 步驟 \_ 反轉
</dt> <dd>

反向步驟。

</dd> </dl>

若為 VCR 裝置， *lpStep* 參數會指向 [**MCI \_ VCR \_ 步驟 \_ PARMS**](mci-vcr-step-parms.md) 結構。

下列其他旗標適用于 **videodisc** 裝置類型：

<dl> <dt>

<span id="MCI_VD_STEP_FRAMES"></span><span id="mci_vd_step_frames"></span>MCI \_ VD \_ 步驟 \_ 框架
</dt> <dd>

由 *lpStep* 所識別之結構的 **dwFrames** 成員會指定要逐步執行的框架數目。

</dd> <dt>

<span id="MCI_VD_STEP_REVERSE"></span><span id="mci_vd_step_reverse"></span>MCI \_ VD \_ 步驟 \_ 反轉
</dt> <dd>

反向步驟。

</dd> </dl>

針對 videodisc 裝置， *lpStep* 參數會指向 [**MCI \_ VD \_ 步驟 \_ PARMS**](mci-vd-step-parms.md) 結構。

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

 

