---
title: 監視命令
description: Monitor 命令會指定展示來源。  (預設的展示來源為工作區。 ) 切換展示來源會切換來源中的所有音訊和影片串流。 數位影片裝置辨識此命令。
ms.assetid: 5cacbe88-b94e-4101-badf-2bb4796b19cf
keywords:
- 監視命令 Windows 多媒體
topic_type:
- apiref
api_name:
- monitor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ccbe1d8919c232ab88d04081dad242944868893
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685889"
---
# <a name="monitor-command"></a>監視命令

Monitor 命令會指定展示來源。  (預設的展示來源為工作區。 ) 切換展示來源會切換來源中的所有音訊和影片串流。 數位影片裝置辨識此命令。

若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("monitor %s %s %s"), 
  lpszDeviceID, 
  lpszMonitor, 
  lpszFlags
); 
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

MCI 裝置的識別碼。 開啟裝置時，會指派此識別碼或別名。

</dd> <dt>

<span id="lpszMonitor"></span><span id="lpszmonitor"></span><span id="LPSZMONITOR"></span>*lpszMonitor*
</dt> <dd>

下列一或多個旗標。



| 值           | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| file            | 指定工作區是展示來源。 這是預設來源。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| input           | 指定外部輸入是展示來源。 如果 [播放](play.md) 命令正在進行，它會先暫停。 如果 [setvideo](setvideo.md) 是 "on"，此旗標會顯示預設的隱藏視窗。 裝置可能會限制其他裝置實例可在監視輸入時進行的動作。                                                                                                                                                                                                                                                                                                                                                                    |
| 方法 *方法* | 與 **監視** 「輸入」搭配使用時，此旗標會選取監視的方法。 *方法* 可以是 "pre"、"post" 或 "direct"。 直接監視要求裝置在監視期間設定為最佳顯示品質。 直接監視方法可能與運動影片錄製不相容。前置和後置監視允許播放影片錄影。 預先監視會顯示壓縮前的外部輸入，而後續監視會在壓縮之後顯示外部輸入。 一般而言，不同的監視方法會有不同的硬體含意。 裝置會選取預設的監視方法。<br/> |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

可以是「等候」、「通知」、「測試」或它們的組合。 如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

展示來源會在 [play](play.md)、 [step](step.md)、 [pause](pause.md)、 [提示](cue.md) "output" 或 [seek](seek.md) 命令之後，自動切換至工作區。 [ [記錄](record.md) ] 命令不會自動切換展示來源，可讓您的應用程式在錄製時不會顯示影片的選項。

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

[提示](cue.md)
</dt> <dt>

[pause](pause.md)
</dt> <dt>

[玩](play.md)
</dt> <dt>

[記錄](record.md)
</dt> <dt>

[尋求](seek.md)
</dt> <dt>

[步](step.md)
</dt> </dl>

 

