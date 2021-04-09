---
title: delete 命令
description: Delete 命令會刪除檔案中的資料區段。 數位-視頻和波形-音訊裝置辨識此命令。
ms.assetid: 9cf084f6-d64e-4487-9407-b68502b7cec9
keywords:
- 刪除命令 Windows 多媒體
topic_type:
- apiref
api_name:
- delete
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e356d4972384e676f2e521bd2ca102bb21d7ef2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844231"
---
# <a name="delete-command"></a>delete 命令

Delete 命令會刪除檔案中的資料區段。 數位-視頻和波形-音訊裝置辨識此命令。

若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("delete %s %s %s"), 
  lpszDeviceID, 
  lpszPosition, 
  lpszFlags
); 
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

MCI 裝置的識別碼。 開啟裝置時，會指派此識別碼或別名。

</dd> <dt>

<span id="lpszPosition"></span><span id="lpszposition"></span><span id="LPSZPOSITION"></span>*lpszPosition*
</dt> <dd>

識別要刪除之資料區段的旗標。 下表列出可辨識 **刪除** 命令的裝置類型，以及每種類型所使用的旗標。



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>值</th>
<th>意義</th>
<th>意義</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>digitalvideo</td>
<td><ul>
<li>在 <em>矩形</em></li>
<li>音訊串流 <em>串流</em></li>
<li>從 <em>位置</em></li>
</ul></td>
<td><ul>
<li><em>定位</em></li>
<li>影片串流 <em>串流</em></li>
</ul></td>
</tr>
<tr class="even">
<td>waveaudio</td>
<td>從 <em>位置</em></td>
<td><em>定位</em></td>
</tr>
</tbody>
</table>



 

下表列出可在 *lpszPosition* 參數中指定的旗標，以及它們的意義。



| 值                 | 意義                                                                                                                                                                                                                                      |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 在 *矩形*        | 指定刪除每個框架的部分。 如果省略，則會預設為整個框架。 指定此專案時，不會刪除畫面格。 而是矩形內的區域會變成黑色。                                          |
| 音訊串流 *串流* | 指定工作區中受命令影響的音訊串流。 如果您使用此旗標，而且也想要刪除影片，您也必須使用「影片串流」旗標。  (如果未指定任何旗標，則會刪除所有音訊和影片串流。 )  |
| 從 *位置*       | 指定開始刪除的位置。 如果省略此旗標，則會從目前的位置開始刪除。                                                                                                                       |
| *定位*         | 指定刪除結束的位置。 如果省略此旗標，則刪除作業會繼續至內容或工作區的結尾。                                                                                                       |
| 影片串流 *串流* | 在工作區中指定受命令影響的影片串流。 如果您使用此旗標，而且也想要刪除音訊，您也必須使用「音訊串流」旗標。  (如果未指定任何旗標，則會刪除所有音訊和影片串流。 )      |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

可以是「等候」、「通知」或兩者。 針對數位影片和 VCR 裝置，也可以指定「測試」。 如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

發出使用位置值的任何命令之前，您應該使用 [set](set.md) 命令來設定所需的時間格式。

## <a name="examples"></a>範例

下列命令會從1毫秒到900毫秒來刪除波形音訊資料 (假設時間格式設定為毫秒) 。

``` syntax
delete mysound from 1 to 900
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

[set](set.md)
</dt> </dl>

 

