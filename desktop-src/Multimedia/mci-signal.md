---
title: 'MCI_SIGNAL 命令 (Mmsystem .h) '
description: MCI \_ 信號命令會在工作區中設定指定的位置。 數位影片裝置辨識此命令。 MCIAVI 一次只支援一個作用中的信號。
ms.assetid: 32ca21a0-e2df-47f1-8e13-67c9d8f149db
keywords:
- MCI_SIGNAL 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_SIGNAL
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 711238d73ee40f5809f15a2d6df93183fb17bf67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384477"
---
# <a name="mci_signal-command"></a>MCI \_ 信號命令

MCI \_ 信號命令會在工作區中設定指定的位置。 數位影片裝置辨識此命令。 MCIAVI 一次只支援一個作用中的信號。

若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SIGNAL, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_SIGNAL_PARMS) lpSignal
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

<span id="lpSignal"></span><span id="lpsignal"></span><span id="LPSIGNAL"></span>*lpSignal*
</dt> <dd>

[**MCI \_ DGV \_ 信號 \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms)結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

在 [**MCI \_ DGV \_ 信號 \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms)結構的 **dwCallback** 成員中指定其控制碼的視窗，會收到 MM \_ MCISIGNAL 訊息。

下列旗標適用于數位視訊裝置：

<dl> <dt>

<span id="MCI_DGV_SIGNAL_AT"></span><span id="mci_dgv_signal_at"></span>MCI \_ DGV \_ 發出信號 \_
</dt> <dd>

信號位置會包含在由 *lpSignal* 所識別之結構的 **dwPosition** 成員中。

</dd> <dt>

<span id="MCI_DGV_SIGNAL_CANCEL"></span><span id="mci_dgv_signal_cancel"></span>MCI \_ DGV \_ 信號 \_ 取消
</dt> <dd>

移除與 MCI \_ DGV 信號 USERVAL 關聯之值所指定的信號位置 \_ \_ 。

</dd> <dt>

<span id="MCI_DGV_SIGNAL_EVERY"></span><span id="mci_dgv_signal_every"></span>MCI \_ DGV \_ \_ 每個信號
</dt> <dd>

信號期間值會包含在由 *lpSignal* 所識別之結構的 **dwPeriod** 成員中。

</dd> <dt>

<span id="MCI_DGV_SIGNAL_POSITION"></span><span id="mci_dgv_signal_position"></span>MCI \_ DGV \_ 信號 \_ 位置
</dt> <dd>

裝置會傳送位置值與 Windows 訊息，而不是使用者指定的值。

</dd> <dt>

<span id="MCI_DGV_SIGNAL_USERVAL"></span><span id="mci_dgv_signal_userval"></span>MCI \_ DGV \_ 信號 \_ USERVAL
</dt> <dd>

資料值會包含在 *lpSignal* 所識別之結構的 **dwUserParm** 成員中。 與此要求相關聯的資料值會與 Windows 訊息一起回報。

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

 

