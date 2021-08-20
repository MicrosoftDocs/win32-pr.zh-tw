---
title: mark 命令
description: Mark 命令控制錄影帶上的標記錄製和清除。 VCR 裝置會辨識此命令。
ms.assetid: d5f7a546-dc46-459c-b5dc-0651bca842cb
keywords:
- 將命令標示 Windows 多媒體
topic_type:
- apiref
api_name:
- mark
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f59f56a6d542120d088d764d1b301329a7f0b167f25952587a9e743878643e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138749"
---
# <a name="mark-command"></a>mark 命令

Mark 命令控制錄影帶上的標記錄製和清除。 VCR 裝置會辨識此命令。

若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("mark %s %s %s"), 
  lpszDeviceID, 
  lpszMark, 
  lpszFlags
); 
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

MCI 裝置的識別碼。 開啟裝置時，會指派此識別碼或別名。

</dd> <dt>

<span id="lpszMark"></span><span id="lpszmark"></span><span id="LPSZMARK"></span>*lpszMark*
</dt> <dd>

下列其中一個旗標。



| 值 | 意義                                                                                                                                |
|-------|----------------------------------------------------------------------------------------------------------------------------------------|
| erase | 清除目前位置的標記（如果有的話）。 若要清除標記，請先搜尋標記，然後發出 mark "erase" 命令。 |
| 寫入 | 在目前位置寫入標記。 VCR 可能必須處於「播放」或「錄製」模式，此命令才會成功。                    |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

可以是「等候」、「通知」或「測試」。 如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

標記是寫入內容的特殊信號，可由 VCR 在高速搜尋期間偵測到。 標記是 VCR 特定的。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[MCI 命令字串](mci-command-strings.md)
</dt> </dl>

 

