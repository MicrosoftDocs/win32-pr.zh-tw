---
title: 'MCI_MONITOR 命令 (Mmsystem .h) '
description: MCI \_ 監視器命令會指定展示來源。 數位影片裝置辨識此命令。
ms.assetid: b6c476ef-d1a4-477d-a104-dda10be60915
keywords:
- MCI_MONITOR 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_MONITOR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6aa2f36b0e486143dc348d2e150422b2b082ecf7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934684"
---
# <a name="mci_monitor-command"></a>MCI \_ 監視器命令

MCI \_ 監視器命令會指定展示來源。 數位影片裝置辨識此命令。

若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_MONITOR, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_MONITOR_PARMS) lpMonitor
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

<span id="lpMonitor"></span><span id="lpmonitor"></span><span id="LPMONITOR"></span>*lpMonitor*
</dt> <dd>

[**MCI \_ DGV \_ 監視 \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_monitor_parms)結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

下列其他旗標適用于數位視訊裝置：

<dl> <dt>

<span id="MCI_DGV_MONITOR_METHOD"></span><span id="mci_dgv_monitor_method"></span>MCI \_ DGV \_ 監視 \_ 方法
</dt> <dd>

常數，表示監視的方法會包含在 *lpMonitor* 所識別之結構的 **dwMethod** 成員中。

在 \_ \_ \_ **DWSOURCE** 成員中使用 MCI DGV 監視器輸入旗標時，這會選取監視的方法。 一般而言，不同的監視方法對硬體的使用方式有不同的影響。 裝置會選取預設的監視方法。

</dd> <dt>

<span id="MCI_DGV_MONITOR_SOURCE"></span><span id="mci_dgv_monitor_source"></span>MCI \_ DGV \_ 監視 \_ 來源
</dt> <dd>

常數，表示監視器來源包含在 *lpMonitor* 所識別之結構的 **dwSource** 成員中。

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

 

