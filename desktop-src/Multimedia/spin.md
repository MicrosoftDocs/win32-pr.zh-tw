---
title: 微調命令
description: 微調命令會開始旋轉光碟或停止光碟的旋轉。 Videodisc 裝置會辨識此命令。
ms.assetid: 1fdf4d09-fafd-4245-ad92-397114d0f473
keywords:
- 微調命令 Windows 多媒體
topic_type:
- apiref
api_name:
- spin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4b643d1f641f7f7faf2711bc2fa8ec43efe7ca1e60a2fb178191870c5ce2354
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118136450"
---
# <a name="spin-command"></a>微調命令

微調命令會開始旋轉光碟或停止光碟的旋轉。 Videodisc 裝置會辨識此命令。

若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("spin %s %s %s"), 
  lpszDeviceID, 
  lpszUpDown, 
  lpszFlags
); 
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

MCI 裝置的識別碼。 開啟裝置時，會指派此識別碼或別名。

</dd> <dt>

<span id="lpszUpDown"></span><span id="lpszupdown"></span><span id="LPSZUPDOWN"></span>*lpszUpDown*
</dt> <dd>

下列其中一個旗標。



| 值 | 意義                       |
|-------|-------------------------------|
| 機  | 停止光碟的旋轉。 |
| 啟動    | 開始旋轉光碟。     |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

可以是「等候」、「通知」或兩者。 如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="examples"></a>範例

下列命令會開始旋轉 videodisc 裝置。

``` syntax
spin videodisc up
```

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

 

