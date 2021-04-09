---
title: pause 命令
description: Pause 命令會暫停播放或錄製。
ms.assetid: 8fa1a40d-fdb1-4c9f-a8db-9dd6a0d83b87
keywords:
- 暫停命令 Windows 多媒體
topic_type:
- apiref
api_name:
- pause
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25957defa4db514ce84f2e013dcc3751e21779b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844395"
---
# <a name="pause-command"></a>pause 命令

Pause 命令會暫停播放或錄製。 大部分的驅動程式都會保留目前的位置，最後會在此位置繼續播放或錄製。 CD 音訊、數位影片、MIDI sequencer、VCR、videodisc 和波形-音訊裝置都會辨識此命令。

若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("pause %s %s"), 
  lpszDeviceID, 
  lpszFlags
); 
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

MCI 裝置的識別碼。 開啟裝置時，會指派此識別碼或別名。

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

可以是「等候」、「通知」或兩者。 針對數位影片和 VCR 裝置，也可以指定「測試」。 如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

使用 MCICDA、MCISEQ 和 MCIPIONR 驅動程式時，pause 命令的運作方式與 [stop](stop.md) 命令相同。

## <a name="examples"></a>範例

下列命令會暫停 "mysound" 裝置。

``` syntax
pause mysound
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[MCI 命令字串](mci-command-strings.md)
</dt> <dt>

[停止](stop.md)
</dt> </dl>

 

