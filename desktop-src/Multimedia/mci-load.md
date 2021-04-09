---
title: 'MCI_LOAD 命令 (Mmsystem .h) '
description: MCI \_ LOAD 命令會載入檔案。 數位影片和影片重迭裝置會辨識此命令。
ms.assetid: 0f48afa0-e845-4de5-8433-15bbf4eae683
keywords:
- MCI_LOAD 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_LOAD
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb00ebe9dc9107c4673fc323fcb7719a89beffd4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933901"
---
# <a name="mci_load-command"></a>MCI \_ LOAD 命令

MCI \_ LOAD 命令會載入檔案。 數位影片和影片重迭裝置會辨識此命令。

若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_LOAD, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_LOAD_PARMS) lpLoad
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

<span id="lpLoad"></span><span id="lpload"></span><span id="LPLOAD"></span>*lpLoad*
</dt> <dd>

[**MCI \_ LOAD \_ PARMS**](mci-load-parms.md)結構的指標。 具有其他參數的 (裝置，可能會以裝置特定的結構取代此結構。 針對數位影片裝置， **lpLoad** 參數會指向 [**MCI \_ DGV \_ LOAD \_ PARMS**](/previous-versions//dd743391(v=vs.85)) 結構。 ) 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

下列其他旗標適用于所有支援 MCI 負載的裝置 \_ ：

<dl> <dt>

<span id="MCI_LOAD_FILE"></span><span id="mci_load_file"></span>MCI \_ 載入 \_ 檔
</dt> <dd>

*LpLoad* 所識別之結構的 **lpfilename** 成員包含包含檔案名之緩衝區的位址。

</dd> </dl>

下列其他旗標會搭配覆迭 **裝置類型** 使用：

<dl> <dt>

<span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI \_ OVLY \_ RECT
</dt> <dd>

*LpLoad* 所識別之結構的 **rc** 成員包含有效的顯示矩形，可識別要更新的影片緩衝區區域。

</dd> </dl>

針對影片重迭裝置， *lpLoad* 參數會指向 [**MCI \_ OVLY \_ LOAD \_ PARMS**](mci-ovly-load-parms.md) 結構。

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

 

