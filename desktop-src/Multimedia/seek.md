---
title: 搜尋命令
description: 搜尋命令會移至指定的位置，並停止。 CD 音訊、數位影片、MIDI sequencer、VCR、videodisc 和波形-音訊裝置都會辨識此命令。
ms.assetid: e9e8ca14-d181-4f29-b4d3-c7f5b0301164
keywords:
- 搜尋命令 Windows 多媒體
topic_type:
- apiref
api_name:
- seek
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d40f3467d328e161245e77217b4ce6edfa9665ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383925"
---
# <a name="seek-command"></a>搜尋命令

搜尋命令會移至指定的位置，並停止。 CD 音訊、數位影片、MIDI sequencer、VCR、videodisc 和波形-音訊裝置都會辨識此命令。

若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("seek %s %s %s"), 
  lpszDeviceID, 
  lpszSeekFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

MCI 裝置的識別碼。 開啟裝置時，會指派此識別碼或別名。

</dd> <dt>

<span id="lpszSeekFlags"></span><span id="lpszseekflags"></span><span id="LPSZSEEKFLAGS"></span>*lpszSeekFlags*
</dt> <dd>

移至指定位置的旗標。 下表列出可辨識 **搜尋** 命令的裝置類型，以及每種類型所使用的旗標。



| 值        | 意義                          | 意義                      |
|--------------|----------------------------------|------------------------------|
| cdaudio      | 結束至 *位置*             | 開始                     |
| digitalvideo | 結束至 *位置*             | 開始                     |
| 排序器    | 結束至 *位置*             | 開始                     |
| 錄影機          | 以 *時間* 標記 *的 \_ 順序反轉* | 結束 *位置* 以開始 |
| videodisc    | 反向至結尾                   | 開始 *位置*        |
| waveaudio    | 結束至 *位置*             | 開始                     |



 

下表列出可在 **lpszSeekFlags** 參數中指定的旗標，以及它們的意義。



| 值            | 意義                                                                                                                                                                                                          |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *準時*        | 指出裝置應該開始執行此命令的時間，如果裝置已 cued，則在 cued 命令開始時。 如需詳細資訊，請參閱 [提示](cue.md) 命令。                             |
| 標記 *\_ 編號* | 搜尋 *標記 \_ num* 所指出的相對標記，這必須是正整數值。 標記是使用 [mark](mark.md) 命令寫入至 VCR 磁帶的信號，用於高速搜尋。 |
| reverse          | 指出 Vcr 和 CAV videodiscs 上的搜尋方向是向後。 如果指定了 "to" 旗標，則此旗標無效。 若為 Vcr，此旗標必須與「標記」旗標搭配使用。                             |
| 結束           | 搜尋內容的結尾。                                                                                                                                                                                 |
| *定位*    | 指定要停止搜尋的位置。 針對 **cdaudio** 裝置，如果指定的位置大於光碟的長度，則 MCI 會傳回超出範圍的錯誤。                                            |
| 開始         | 搜尋內容的開頭。                                                                                                                                                                               |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

可以是「等候」、「通知」或兩者。 針對數位影片和 VCR 裝置，也可以指定「測試」。 如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

發出使用位置值的任何命令之前，您應該使用 [set](set.md) 命令來設定所需的時間格式。

數位影片裝置支援兩種搜尋模式，您可以使用 [set](set.md) 命令加以變更。 「完全搜尋」模式會使 seek 命令移至指定的框架。 「完全搜尋」模式會導致搜尋命令在指定的框架之前移至最接近的主要畫面格。

如果在發出搜尋命令時播放 CD 音訊裝置，則會停止播放。 當搜尋命令以 videodisc 裝置發出時，裝置會使用向前快轉或快速反轉來搜尋影片和音訊。

使用波形音訊裝置發出搜尋命令時，行為取決於樣本大小。 如果樣本大小為16位或更大，則當指定的位置與範例開始不一致時，搜尋會移至最接近的樣本的開頭。

## <a name="examples"></a>範例

下列命令會搜尋與 "mysound" 裝置相關聯之媒體檔案的開頭。

``` syntax
seek mysound to start
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

[提示](cue.md)
</dt> <dt>

[標記](mark.md)
</dt> <dt>

[set](set.md)
</dt> </dl>

 

