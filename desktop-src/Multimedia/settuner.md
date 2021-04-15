---
title: settuner 命令
description: Settuner 命令會變更目前的調諧器或目前調諧器的通道設定。 VCR 裝置會辨識此命令。
ms.assetid: 76d05210-3c2a-4d00-b3eb-c912c1deabf7
keywords:
- settuner 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- settuner
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51150043a68f3cd34525eb74a64237fc4dc150e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467076"
---
# <a name="settuner-command"></a>settuner 命令

Settuner 命令會變更目前的調諧器或目前調諧器的通道設定。 VCR 裝置會辨識此命令。

若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("settuner %s %s %s"), 
  lpszDeviceID, 
  lpszTuner, 
  lpszFlags
); 
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

MCI 裝置的識別碼。 開啟裝置時，會指派此識別碼或別名。

</dd> <dt>

<span id="lpszTuner"></span><span id="lpsztuner"></span><span id="LPSZTUNER"></span>*lpszTuner*
</dt> <dd>

下列其中一個旗標。



| 值                            | 意義                                                                                                                                                                                                                                                                                                     |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 通道 *通道*                | 將調諧器設定為 *頻道*。 根據 VCR，您可能無法在錄製時變更通道。 大於最大通道的通道會將調諧器設定為最大頻道。                                                                                                                    |
| 頻道搜尋 upchannel 向下搜尋 | 使用有效的信號搜尋下一個通道。 「搜尋」會在其搜尋中遞增頻道號碼。 「向下搜尋」會在其搜尋中遞減頻道號碼。 當超過最大頻道數目時，調諧器會換行至頻道1。 同樣地，當向下搜尋時，調諧器會換行到最大頻道。 |
| 頻道 upchannel 向下           | 將調諧器頻道遞增或遞減。 根據 VCR，您可能無法在錄製時變更通道。 當超過最大頻道數目時，調諧器會換行至頻道1。 同樣地，當向下搜尋時，調諧器會換行到最大頻道。                              |
| 編號                  | 指定要受 settuner 命令影響的調諧器。 如果未指定 *數位* ，則會假設為預設值1。                                                                                                                                                                                    |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

可以是「等候」、「通知」、「測試」或它們的組合。 如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。

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

[Mci](mci.md)
</dt> <dt>

[MCI 命令字串](mci-command-strings.md)
</dt> </dl>

 

