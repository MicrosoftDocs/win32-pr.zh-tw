---
title: 凍結命令
description: 凍結命令會凍結 VCR 的影片輸入或影片輸出，或停用框架緩衝區的影片捕獲。 數位影片、影片重迭和 VCR 裝置都會辨識此命令。
ms.assetid: 49f3ab98-e893-402a-be78-6140af3b81df
keywords:
- 凍結命令 Windows 多媒體
topic_type:
- apiref
api_name:
- freeze
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b63fbb2d888fc1ca315c0b511bcb18224c8168
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024568"
---
# <a name="freeze-command"></a>凍結命令

凍結命令會凍結 VCR 的影片輸入或影片輸出，或停用框架緩衝區的影片捕獲。 數位影片、影片重迭和 VCR 裝置都會辨識此命令。

若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("freeze %s %s %s"), 
  lpszDeviceID, 
  lpszFreezeFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

MCI 裝置的識別碼。 開啟裝置時，會指派此識別碼或別名。

</dd> <dt>

<span id="lpszFreezeFlags"></span><span id="lpszfreezeflags"></span><span id="LPSZFREEZEFLAGS"></span>*lpszFreezeFlags*
</dt> <dd>

識別要凍結之內容的旗標。 下表列出可辨識 **凍結** 命令的裝置類型，以及每種類型所使用的旗標。



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
<td>在 <em>矩形</em></td>
<td>外面</td>
</tr>
<tr class="even">
<td>overlay</td>
<td>在 <em>矩形</em></td>

</tr>
<tr class="odd">
<td>錄影機</td>
<td><ul>
<li>field</li>
<li>框架</li>
</ul></td>
<td><ul>
<li>input</li>
<li>output</li>
</ul></td>
</tr>
</tbody>
</table>



 

下表列出可在 *lpszFreezeFlags* 參數中指定的旗標，以及它們的意義。



| 值          | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 在 *矩形* | 指定即將凍結的區域。 針對影片重迭裝置，此區域將會停用影片的取得。 針對數位影片裝置，除非) 指定「外部」旗標，否則矩形內的圖元將會開啟其鎖定遮罩位 (。 矩形相對於影片緩衝區原點，並指定為 *X1 Y1 X2 Y2*。 座標 *X1 Y1* 指定矩形的左上角，而座標 *X2 Y2* 指定寬度和高度。 |
| field          | 凍結第一個欄位。 如果未指定) 的框架或欄位，預設會假設為 (的欄位。                                                                                                                                                                                                                                                                                                                                                                                               |
| 框架          | 凍結整個框架，同時顯示這兩個欄位。                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| input          | 凍結輸入影像的目前畫面格（不論其是否已暫停或正在執行）。                                                                                                                                                                                                                                                                                                                                                                                                                |
| output         | 從 VCR 凍結目前輸出的畫面格。 如果在發出凍結時現正播放 VCR，則會凍結目前的框架，並暫停 VCR。 如果在發出此命令時，會暫停 VCR，則會凍結目前的框架。 凍結的映射會保留在輸出裝置上，直到發出 [解除凍結](unfreeze.md) 命令為止。 如果未指定 "input" 或 "output"，則會假設為 "output"。                                                                                    |
| 外面        | 表示已凍結使用 "at" 旗標指定區域以外的區域。                                                                                                                                                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

可以是「等候」、「通知」或兩者。 針對數位影片和 VCR 裝置，也可以指定「測試」。 如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

搭配使用 VCR 裝置時，此命令適用于框架抓取卡。

若要使用 "at" 旗標來指定不規則的取得區域，請使用一連串的凍結和 [解除凍結](unfreeze.md) 命令。 某些影片重迭裝置會限制取得區域的複雜度。

只有在具有「可凍結」旗標的 [ [功能](capability.md) ] 命令呼叫傳回 **TRUE** 時，才支援這個命令。

## <a name="examples"></a>範例

下列命令會停用影片緩衝區左上角 100-圖元正方形的影片取得。

``` syntax
freeze vboard at 0 0 100 100
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

[capability](capability.md)
</dt> <dt>

[解凍](unfreeze.md)
</dt> </dl>

 

