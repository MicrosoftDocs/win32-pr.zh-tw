---
title: step 命令
description: 步驟命令會逐步執行一或多個畫面的向前或反向播放。 預設動作是向前前進一個畫面格。 數位影片、VCR 和 CAV 格式的 videodisc 裝置都會辨識此命令。
ms.assetid: 6017ace5-cde9-42a0-bb2f-f85d7847adc5
keywords:
- Windows 多媒體的步驟命令
topic_type:
- apiref
api_name:
- step
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b804ac64c2641ba1eb43ba7019ae2668c04a7d8b07fbfd20ab7b8cb570d8fab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118370828"
---
# <a name="step-command"></a>step 命令

步驟命令會逐步執行一或多個畫面的向前或反向播放。 預設動作是向前前進一個畫面格。 數位影片、VCR 和 CAV 格式的 videodisc 裝置都會辨識此命令。

若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("step %s %s %s"), 
  lpszDeviceID, 
  lpszStepFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

MCI 裝置的識別碼。 開啟裝置時，會指派此識別碼或別名。

</dd> <dt>

<span id="lpszStepFlags"></span><span id="lpszstepflags"></span><span id="LPSZSTEPFLAGS"></span>*lpszStepFlags*
</dt> <dd>

下列其中一個或兩個旗標。



| 值       | 意義                                                                                                                  |
|-------------|--------------------------------------------------------------------------------------------------------------------------|
| 依 *畫面* 格 | 指出要逐步執行的框架數目。 如果您指定了負值的 *框架* 值，就不能指定「反轉」旗標。 |
| reverse     | 反向步驟畫面格。                                                                                              |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

可以是「等候」、「通知」或兩者。 針對數位影片和 VCR 裝置，也可以指定「測試」。 如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。

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
</dt> </dl>

 

