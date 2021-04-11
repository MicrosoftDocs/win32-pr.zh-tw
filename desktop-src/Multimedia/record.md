---
title: 記錄命令
description: 記錄命令會開始記錄資料。 VCR 和波形-音訊裝置會辨識此命令。 雖然數位視訊裝置和 MIDI sequencers 也會辨識此命令，但 MCIAVI 和 MCISEQ 驅動程式並不會執行此命令。
ms.assetid: a0838153-5ac2-437f-ae1e-0c4f950fcac5
keywords:
- 錄製命令 Windows 多媒體
topic_type:
- apiref
api_name:
- record
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39d3659d4577517726260f948563cd31ecc07bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843120"
---
# <a name="record-command"></a>記錄命令

記錄命令會開始記錄資料。 VCR 和波形-音訊裝置會辨識此命令。 雖然數位視訊裝置和 MIDI sequencers 也會辨識此命令，但 MCIAVI 和 MCISEQ 驅動程式並不會執行此命令。

若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("record %s %s %s"), 
  lpszDeviceID, 
  lpszRecordFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

MCI 裝置的識別碼。 開啟裝置時，會指派此識別碼或別名。

</dd> <dt>

<span id="lpszRecordFlags"></span><span id="lpszrecordflags"></span><span id="LPSZRECORDFLAGS"></span>*lpszRecordFlags*
</dt> <dd>

記錄資料的旗標。 下表列出可辨識 **記錄** 命令的裝置類型，以及每種類型使用的旗標。



| 值        | 意義                                                | 意義                                             |
|--------------|--------------------------------------------------------|-----------------------------------------------------|
| digitalvideo | 從 *位置* 保留的 *矩形* 音訊串流 *串流* | 插入覆寫以 *定位* 影片串流 *串流* |
| 排序器    | 從 *位置* 插入                                  | 覆寫至 *位置*                             |
| 錄影機          | 從 *位置* 初始化的 *時間*                     | 將覆寫插入至 *位置*                      |
| waveaudio    | 從 *位置* 插入                                  | 覆寫至 *位置*                             |



 

下表列出可在 **lpszRecordFlags** 參數中指定的旗標，以及它們的意義。



| 值                 | 意義                                                                                                                                                                                                                                                                                                          |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 在 *矩形*        | 指定外部輸入的矩形區域，做為壓縮和儲存的圖元來源。 如果未指定，矩形會預設為 [put](put.md) "video" 所指定的矩形。 當不同于「影片」矩形的設定時，所顯示的影像並不是所錄製的影像。 |
| *準時*             | 指出裝置應該開始執行此命令的時間，如果裝置已 cued，則在 cued 命令開始時。 如需詳細資訊，請參閱 [提示](cue.md) 命令。                                                                                                                             |
| 音訊串流 *串流* | 指定用於錄製的音訊資料流程。 如果未指定此旗標，而且檔案格式未定義預設值，則會將它記錄到實際優先的資料流程中。                                                                                                                             |
| 從 *位置*       | 指定錄製的開始位置。 如果未指定 "from" 旗標，則裝置會在目前的位置開始錄製。                                                                                                                                                                       |
| hold                  | 錄製完成時凍結影像，而不是顯示即時影片。 錄製停止時，會執行自動 [監視](monitor.md) "file" 命令。 若要返回即時影片，請發出 **監視器** "input" 命令。                                                                              |
| initialize            | 將磁帶 (媒體) ，其牽涉到錄製時間碼 (如果可能) 空白的影片和音訊。 如果必須初始化整個磁帶，此命令可能需要數小時的時間。                                                                                                                            |
| insert                | 指定將新的資料加入至檔案中的目前位置。                                                                                                                                                                                                                                            |
| overwrite             | 指定新的資料將會取代檔案中的資料。                                                                                                                                                                                                                                                           |
| *定位*         | 指定錄製的結束位置。 如果未指定「到」旗標，則會記錄裝置，直到收到「 [停止](stop.md) 」或「 [暫停](pause.md) 」命令為止。                                                                                                                                        |
| 影片串流 *串流* | 指定用於錄製的影片資料流程。 如果未指定此值，且檔案格式未定義預設值，則會將它記錄到實際優先的資料流程中。                                                                                                                             |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

可以是「等候」、「通知」或兩者。 針對數位影片和 VCR 裝置，也可以指定「測試」。 如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

發出 [停止](stop.md) 或 [暫停](pause.md) 命令時，會停止錄製。 針對 MCIWAVE 驅動程式，如果檔案已關閉而不儲存，則會捨棄檔案之後記錄的所有資料。

發出使用位置值的任何命令之前，您應該使用 [set](set.md) 命令來設定所需的時間格式。 要記錄的追蹤是由 [settimecode](settimecode.md) "record" 指定、設定 "組合記錄"、 [setvideo](setvideo.md) "record" 和 [setaudio](setaudio.md) "record" 命令。

## <a name="examples"></a>範例

下列命令會在目前的位置開始錄製。

``` syntax
record mysound
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

[監控](monitor.md)
</dt> <dt>

[pause](pause.md)
</dt> <dt>

[把](put.md)
</dt> <dt>

[set](set.md)
</dt> <dt>

[setaudio](setaudio.md)
</dt> <dt>

[settimecode](settimecode.md)
</dt> <dt>

[setvideo](setvideo.md)
</dt> <dt>

[停止](stop.md)
</dt> </dl>

 

