---
title: 'MCI_RESTORE 命令 (Mmsystem .h) '
description: MCI \_ RESTORE 命令會將點陣圖從檔案複製到框架緩衝區。 數位影片裝置辨識此命令。 此命令會執行 MCI CAPTURE 命令的相反動作 \_ 。
ms.assetid: ed309cc6-72a3-4abb-aef2-40a55381d8b6
keywords:
- MCI_RESTORE 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_RESTORE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b0c82db597a0e347f382c7cda55ce507f4e6dcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686235"
---
# <a name="mci_restore-command"></a>MCI \_ 還原命令

MCI \_ RESTORE 命令會將點陣圖從檔案複製到框架緩衝區。 數位影片裝置辨識此命令。 此命令會執行 [MCI \_ CAPTURE](mci-capture.md) 命令的相反動作。

若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_RESTORE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_RESTORE_PARMS) lpRestore
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

<span id="lpRestore"></span><span id="lprestore"></span><span id="LPRESTORE"></span>*lpRestore*
</dt> <dd>

[**MCI \_ DGV \_ RESTORE \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_restore_parmsa)結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

此執行可辨識各種不同的影像格式，但一律接受 Windows 裝置獨立點陣圖 (DIB) 。

下列其他旗標適用于數位視訊裝置：

<dl> <dt>

<span id="MCI_DGV_RESTORE_FROM"></span><span id="mci_dgv_restore_from"></span>MCI \_ DGV \_ 還原 \_ 來源
</dt> <dd>

*LpRestore* 所識別之結構的 **lpstrFileName** 成員包含包含來原始檔案名的緩衝區位址。 需要檔案名。

</dd> <dt>

<span id="MCI_DGV_RESTORE_AT"></span><span id="mci_dgv_restore_at"></span>MCI \_ DGV \_ RESTORE \_ AT
</dt> <dd>

*LpRestore* 所識別之結構的 **rc** 成員包含有效的矩形。 矩形會指定框架緩衝區相對於其來源的區域。 第一對座標指定矩形的左上角;第二個配對指定寬度和高度。 如果未指定此旗標，則會將影像複製到框架緩衝區的左上角。

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

 

