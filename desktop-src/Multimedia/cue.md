---
title: 提示命令
description: 提示命令可準備播放或錄製。 數位-影片、VCR 和波形-音訊裝置會辨識此命令。
ms.assetid: 94fa0d0c-d5c9-4ef1-bb7d-22dfb09a7689
keywords:
- 提示命令 Windows 多媒體
topic_type:
- apiref
api_name:
- cue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dd71f06a71c8aff4752fc31d750a3612564eb8a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844411"
---
# <a name="cue-command"></a>提示命令

提示命令可準備播放或錄製。 數位-影片、VCR 和波形-音訊裝置會辨識此命令。

若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("cue %s %s %s"), 
  lpszDeviceID, 
  lpszInOutTo, 
  lpszFlags
); 
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

MCI 裝置的識別碼。 開啟裝置時，會指派此識別碼或別名。

</dd> <dt>

<span id="lpszInOutTo"></span><span id="lpszinoutto"></span><span id="LPSZINOUTTO"></span>*lpszInOutTo*
</dt> <dd>

準備裝置以進行播放或錄製的旗標。 下表列出可辨識 **提示** 命令的裝置類型，以及每種類型所使用的旗標。



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>值</th>
<th>提示</th>
<th>提示</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>digitalvideo</td>
<td><ul>
<li>input</li>
<li>noshow</li>
</ul></td>
<td><ul>
<li>output</li>
<li><em>定位</em></li>
</ul></td>
</tr>
<tr class="even">
<td>錄影機</td>
<td><ul>
<li>從 <em>位置</em></li>
<li>input</li>
<li>output</li>
</ul></td>
<td><ul>
<li>預</li>
<li>reverse</li>
<li><em>定位</em></li>
</ul></td>
</tr>
<tr class="odd">
<td>waveaudio</td>
<td>input</td>
<td>output</td>
</tr>
</tbody>
</table>



 

下表列出可在 *lpszInOutTo* 參數中指定的旗標，以及它們的意義。



| 值           | 意義                                                                                                                                                                                                                                                                                                        |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 從 *位置* | 表示要從何處開始。                                                                                                                                                                                                                                                                                      |
| input           | 準備錄製。 若為數位視訊裝置，如果目前的簡報來源已經是外部輸入，就可以省略此旗標。                                                                                                                                                                  |
| noshow          | 準備播放框架而不顯示。 當指定這個旗標時，即使對應的框架不是目前的位置，顯示器仍會繼續在框架緩衝區中顯示影像。 沒有此旗標且沒有 "to" 旗標的後續提示命令會顯示目前的畫面格。 |
| output          | 準備進行播放。 如果未指定「輸入」和「輸出」，則預設設定為「輸出」。                                                                                                                                                                                                           |
| 預         | 從 *點* 移動向前算起的距離。 點對點是目前的位置，或是由 "from" 旗標所指定的位置。                                                                                                                                                                            |
| reverse         | 表示播放方向是反向 (回溯) 。                                                                                                                                                                                                                                                             |
| *定位*   | 將工作區移至指定的位置。 若為 VCR 裝置，此旗標會指出停止的位置。                                                                                                                                                                                                             |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

可以是「等候」、「通知」或兩者。 針對數位影片和 VCR 裝置，也可以指定「測試」。 如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

雖然並非必要，但在某些裝置上播放或錄製之前發出提示命令可能會降低裝置啟動動作之前的延遲。

如果播放或錄製正在進行中，或裝置已暫停，此命令將會失敗。

當使用提示 "output" ) 提示播放 (時，發出使用 "from"、"to" 或 "reverse" 旗標的 [play](play.md) 命令會取消提示命令。

使用提示 "input" ) 提示錄製 (時，發出具有 "from"、"to" 或 "initialize" 旗標的 [記錄](record.md) 命令會取消提示命令。

## <a name="examples"></a>範例

下列命令會準備 "mysound" 裝置以進行錄製。

``` syntax
cue mysound input
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

[玩](play.md)
</dt> <dt>

[記錄](record.md)
</dt> </dl>

 

