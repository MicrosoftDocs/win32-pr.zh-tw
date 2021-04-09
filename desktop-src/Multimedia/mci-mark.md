---
title: 'MCI_MARK 命令 (Mmsystem .h) '
description: MCI \_ MARK 命令會記錄或清除可與 MCI \_ 搜尋命令搭配使用以進行高速搜尋的標記。 VCR 裝置會辨識此命令。
ms.assetid: 69b17e5b-99a1-4fb9-bc0e-30e772c1f11f
keywords:
- MCI_MARK 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_MARK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ddc80decb4559659efb29132f17f18459c334fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024787"
---
# <a name="mci_mark-command"></a>MCI \_ MARK 命令

MCI \_ MARK 命令會記錄或清除可與 [MCI \_ 搜尋](mci-seek.md) 命令搭配使用以進行高速搜尋的標記。 VCR 裝置會辨識此命令。

若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_MARK, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpMark
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

<span id="lpMark"></span><span id="lpmark"></span><span id="LPMARK"></span>*lpMark*
</dt> <dd>

[**MCI \_ 泛型 \_ PARMS**](mci-generic-parms.md)結構的指標。 具有擴充命令集的 (裝置，可能會以裝置特定結構取代此結構。 ) 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

下列其他旗標適用于 VCR 裝置：

<dl> <dt>

<span id="MCI_VCR_MARK_ERASE"></span><span id="mci_vcr_mark_erase"></span>MCI \_ VCR \_ 標示 \_ 清除
</dt> <dd>

清除目前位置的標記（如果有的話）。

</dd> <dt>

<span id="MCI_VCR_MARK_WRITE"></span><span id="mci_vcr_mark_write"></span>MCI \_ VCR \_ 標示 \_ 寫入
</dt> <dd>

在目前位置寫入標記。

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

 

