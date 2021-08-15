---
title: index 命令
description: Index 命令控制 VCR 的螢幕顯示。 VCR 裝置會辨識此命令。
ms.assetid: 16066acf-37aa-4bff-b97e-5eb2420ac3c4
keywords:
- 索引命令 Windows 多媒體
topic_type:
- apiref
api_name:
- index
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9044ce01db5f35354390fd8d09cc085416202f670c8378a2e1a10311b12ab94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690548"
---
# <a name="index-command"></a>index 命令

Index 命令控制 VCR 的螢幕顯示。 VCR 裝置會辨識此命令。

若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("index %s %s %s"), 
  lpszDeviceID, 
  lpszIndex, 
  lpszFlags
); 
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

MCI 裝置的識別碼。 開啟裝置時，會指派此識別碼或別名。

</dd> <dt>

<span id="lpszIndex"></span><span id="lpszindex"></span><span id="LPSZINDEX"></span>*lpszIndex*
</dt> <dd>

下列其中一個旗標。



| 值 | 意義                                                                                                                  |
|-------|--------------------------------------------------------------------------------------------------------------------------|
| 關   | 關閉螢幕顯示。                                                                                         |
| on    | 開啟螢幕顯示。 要顯示的專案是由 [set](set.md) 命令的「index」旗標所指定。 |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

可以是「等候」、「通知」或「測試」。 如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

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
</dt> <dt>

[set](set.md)
</dt> </dl>

 

