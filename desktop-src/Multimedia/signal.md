---
title: 信號命令
description: 信號命令會將 MCISIGNAL 訊息傳送給應用程式，以識別工作區中的指定位置 \_ 。 數位影片裝置辨識此命令。 MCIAVI 一次只支援一個作用中的信號。
ms.assetid: 3d10eac0-fd1a-41ee-98fa-2518642c7339
keywords:
- 發出命令 Windows 多媒體
topic_type:
- apiref
api_name:
- signal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fd96b8970ebbb6502306c6d2d5fd8c49f172cad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106979682"
---
# <a name="signal-command"></a>信號命令

信號命令會將 [ \_ MCISIGNAL](mm-mcisignal.md) 訊息傳送給應用程式，以識別工作區中的指定位置。 數位影片裝置辨識此命令。 MCIAVI 一次只支援一個作用中的信號。

若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("signal %s %s %s"), 
  lpszDeviceID, 
  lpszSignalFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

MCI 裝置的識別碼。 開啟裝置時，會指派此識別碼或別名。

</dd> <dt>

<span id="lpszSignalFlags"></span><span id="lpszsignalflags"></span><span id="LPSZSIGNALFLAGS"></span>*lpszSignalFlags*
</dt> <dd>

下列其中一個旗標。



| 值            | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 在位置      | 指定要叫用信號的框架。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| cancel           | 移除工作區中的信號。 您可以使用 "uservalue" 旗標來指定個別信號。 如果未使用 "cancel" 來指定 "uservalue" 旗標，則裝置會取消所有信號。 「取消」旗標與「at」、「每個」和「傳回位置」旗標不相容。                                                                                                                                                                                                                                                                                          |
| 每個 *間隔* | 指定信號的期間。 *間隔* 值是以目前時間格式指定。如果搭配 "at"*位置* 使用，則會在工作區中放置信號，並在 *位置* 放置一個信號標記。<br/> 如果沒有 "at" 旗標，則會在工作區中放置信號，並在目前位置有一個信號。<br/> 如果省略此旗標，則只會標示 "at" 旗標所指定的位置。<br/> 如果 *間隔* 值小於裝置所支援的最小頻率，則會使用其最小值。<br/> |
| 傳回位置  | 指出裝置應該傳送位置值，而不是傳送信號訊息中的 "uservalue" 識別碼。 "Uservalue" 識別碼仍然可以用來取消或重新定義信號標記。                                                                                                                                                                                                                                                                                                                                                                      |
| uservalue *識別碼*   | 指定使用信號訊息回報的識別碼。 此識別碼會作為可與其他 **信號** 命令搭配使用以參考此 **信號** 設定的識別碼。 如果省略，預設值為零。                                                                                                                                                                                                                                                                                                                                     |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

可以是「等候」、「通知」、「測試」或它們的組合。 如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

用於命令完成訊息通知的視窗控制碼也會用來發出信號。

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

[MM \_ MCISIGNAL](mm-mcisignal.md)
</dt> </dl>

 

