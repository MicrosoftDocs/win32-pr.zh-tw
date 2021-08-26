---
title: play 命令
description: Play 命令會開始播放裝置。 CD 音訊、數位影片、MIDI sequencer、videodisc、VCR 和波形音訊裝置都會辨識此命令。
ms.assetid: 3ee707d6-6af4-494d-a887-d91ea5666ac4
keywords:
- 播放命令 Windows 多媒體
topic_type:
- apiref
api_name:
- play
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2da0df530f1c7a0166dcbb7c852fe491127a9e187d1cb6cb953ec46b2533ac00
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038048"
---
# <a name="play-command"></a>play 命令

Play 命令會開始播放裝置。 CD 音訊、數位影片、MIDI sequencer、videodisc、VCR 和波形音訊裝置都會辨識此命令。

若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("play %s %s %s"), 
  lpszDeviceID, 
  lpszPlayFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

MCI 裝置的識別碼。 開啟裝置時，會指派此識別碼或別名。

</dd> <dt>

<span id="lpszPlayFlags"></span><span id="lpszplayflags"></span><span id="LPSZPLAYFLAGS"></span>*lpszPlayFlags*
</dt> <dd>

播放裝置的旗標。 下表列出可辨識 **播放** 命令的裝置類型，以及每種類型所使用的旗標。



| 值        | 意義                          | 意義                           |
|--------------|----------------------------------|-----------------------------------|
| cdaudio      | 從 *位置*                  | *定位*                     |
| digitalvideo | 從 *位置* 全螢幕重複 | 反向至 *定位* 視窗       |
| 排序器    | 從 *位置*                  | *定位*                     |
| 錄影機          | 從 *位置* 反向的 *時間*  | 掃描至 *位置*                |
| videodisc    | 從 *位置* 反向掃描快速 | 緩慢 *的速度**整數* |
| waveaudio    | 從 *位置*                  | *定位*                     |



 

下表列出可在 **lpszPlayFlags** 參數中指定的旗標，以及它們的意義。



| 值           | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *準時*       | 指出裝置應該開始執行此命令的時間，如果裝置已 cued，則在 cued 命令開始時。 如需詳細資訊，請參閱 [提示](cue.md) 命令。                                                                                                                                                                                                                                                                 |
| 快速            | 指出裝置的播放速度比平常更快。 若要判斷 videodisc 播放程式的確切速度，請使用 [status](status.md) 命令的「速度」旗標。 若要更精確地指定速度，請使用此命令的「速度」旗標。                                                                                                                                                                                                   |
| 從 *位置* | 指定播放的開始位置。 如果未指定 "from" 旗標，則會從目前的位置開始播放。 針對 **cdaudio** 裝置，如果 "from" 位置大於光碟的結束位置，或「從」位置大於「到」位置，則驅動程式會傳回錯誤。 針對 **videodisc** 裝置，預設位置會是 CAV 光碟的框架，而以小時、分鐘和秒為單位的 CLV 光碟。 |
| 全螢幕      | 指定應該使用全螢幕顯示。 只有在播放壓縮檔案時，才使用此旗標。  (未壓縮檔案將無法播放全螢幕。 )                                                                                                                                                                                                                                                                                                   |
| 重複          | 指定當到達內容的結尾時，播放應該重新開機。                                                                                                                                                                                                                                                                                                                                                                       |
| reverse         | 指定播放方向反向。 您無法使用「反轉」旗標來指定結束位置。 若為 videodiscs，"scan" 只適用于 CAV 格式。                                                                                                                                                                                                                                                                                     |
| 掃描            | 盡可能快速地播放，而不停用影片 (雖然音訊可能會停用) 。 若為 videodiscs，"scan" 只適用于 CAV 格式。                                                                                                                                                                                                                                                                                                             |
| slow            | 的播放速度很慢。 若要判斷 videodisc 播放程式的確切速度，請使用 [status](status.md) 命令的「速度」旗標。 若要更精確地指定速度，請使用此命令的「速度」旗標。 針對 videodiscs，「慢」只適用于 CAV 格式。                                                                                                                                                                                            |
| 速度 *整數* | 以指定的速度（以每秒的畫面格）來播放 videodisc。 此旗標只適用于 CAV 光碟。                                                                                                                                                                                                                                                                                                                                                 |
| *定位*   | 指定播放的結束位置。 如果未指定 "to" 旗標，則會在內容結尾停止播放。 針對 **cdaudio** 裝置，如果「到」位置大於光碟的結束位置，驅動程式會傳回錯誤。 針對 **videodisc** 裝置，預設位置會是 CAV 光碟的框架，而以小時、分鐘和秒為單位的 CLV 光碟。                                                                  |
| 時間範圍          | 指定播放應使用與裝置實例相關聯的視窗。 這是預設值。                                                                                                                                                                                                                                                                                                                                       |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

可以是「等候」、「通知」或兩者。 針對數位影片和 VCR 裝置，也可以指定「測試」。 如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

發出使用位置值的命令之前，您應該使用 [set](set.md) 命令來設定所需的時間格式。 此命令會以設定的 "speed" 命令開始，以目前的速度開始播放。 如果指定「反轉」旗標，或將 "to" 旗標指定為小於 "from" 旗標的值，則方向會反轉。 如果未指定 "from" 旗標，則會從目前的位置開始播放。 「到」和「反轉」旗標不能一起使用。

## <a name="examples"></a>範例

下列命令會從位置1000到位置2000播放 "mysound" 裝置，並在播放完成時傳送通知訊息。

``` syntax
play mysound from 1000 to 2000 notify
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
</dt> <dt>

[提示](cue.md)
</dt> <dt>

[set](set.md)
</dt> </dl>

 

