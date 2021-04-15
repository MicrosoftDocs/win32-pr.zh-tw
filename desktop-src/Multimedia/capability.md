---
title: 功能命令
description: 功能命令會要求裝置特定功能的相關資訊。 所有 MCI 裝置都會辨識此命令。
ms.assetid: 1b470473-0de6-41ba-9f6e-41f0b13ceaeb
keywords:
- 功能命令 Windows 多媒體
topic_type:
- apiref
api_name:
- capability
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a6ac87b98fb8d748a5baf2665cc5a63230b6a98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464636"
---
# <a name="capability-command"></a>功能命令

功能命令會要求裝置特定功能的相關資訊。 所有 MCI 裝置都會辨識此命令。

若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("capability %s %s %s"), 
  lpszDeviceID, 
  lpszRequest, 
  lpszFlags
); 
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

MCI 裝置的識別碼。 開啟裝置時，會指派此識別碼或別名。

</dd> <dt>

<span id="lpszRequest"></span><span id="lpszrequest"></span><span id="LPSZREQUEST"></span>*lpszRequest*
</dt> <dd>

識別裝置功能的旗標。 下表列出可辨識 **功能** 命令的裝置類型，以及每種類型使用的旗標：



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>值</th>
<th>類型</th>
<th>類型</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>cdaudio</td>
<td><ul>
<li>可以退出</li>
<li>可以播放</li>
<li>可以記錄</li>
<li>可以儲存</li>
<li>複合裝置</li>
</ul></td>
<td><ul>
<li>裝置類型</li>
<li>有音訊</li>
<li>有影片</li>
<li>使用檔案</li>
</ul></td>
</tr>
<tr class="even">
<td>digitalvideo</td>
<td><ul>
<li>可以退出</li>
<li>可以凍結</li>
<li>可以鎖定</li>
<li>可以播放</li>
<li>可以記錄</li>
<li>可以反轉</li>
<li>可以儲存</li>
<li>可以延展</li>
<li>可延展輸入</li>
<li>可以測試</li>
</ul></td>
<td><ul>
<li>複合裝置</li>
<li>裝置類型</li>
<li>有音訊</li>
<li>仍有</li>
<li>有影片</li>
<li>最大播放率</li>
<li>最小播放率</li>
<li>使用檔案</li>
<li>使用調色板</li>
<li>windows</li>
</ul></td>
</tr>
<tr class="odd">
<td>overlay</td>
<td><ul>
<li>可以退出</li>
<li>可以凍結</li>
<li>可以播放</li>
<li>可以記錄</li>
<li>可以儲存</li>
<li>可以延展</li>
</ul></td>
<td><ul>
<li>複合裝置</li>
<li>裝置類型</li>
<li>有音訊</li>
<li>有影片</li>
<li>使用檔案</li>
<li>windows</li>
</ul></td>
</tr>
<tr class="even">
<td>排序器</td>
<td><ul>
<li>可以退出</li>
<li>可以播放</li>
<li>可以記錄</li>
<li>可以儲存</li>
<li>複合裝置</li>
</ul></td>
<td><ul>
<li>裝置類型</li>
<li>有音訊</li>
<li>有影片</li>
<li>使用檔案</li>
</ul></td>
</tr>
<tr class="odd">
<td>錄影機</td>
<td><ul>
<li>可以偵測長度</li>
<li>可以退出</li>
<li>可以凍結</li>
<li>可以監視來源</li>
<li>可以播放</li>
<li>可以預先進行</li>
<li>可以預覽</li>
<li>可以記錄</li>
<li>可以反轉</li>
<li>可以儲存</li>
<li>可以測試</li>
</ul></td>
<td><ul>
<li>頻率遞增率</li>
<li>複合裝置</li>
<li>裝置類型</li>
<li>有音訊</li>
<li>具有時鐘</li>
<li>有時間碼</li>
<li>有影片</li>
<li>標記數目</li>
<li>搜尋精確度</li>
<li>使用檔案</li>
</ul></td>
</tr>
<tr class="even">
<td>videodisc</td>
<td><ul>
<li>可以退出</li>
<li>可以播放</li>
<li>可以記錄</li>
<li>可以反轉</li>
<li>可以儲存</li>
<li>CAV</li>
<li>CLV</li>
<li>複合裝置</li>
</ul></td>
<td><ul>
<li>裝置類型</li>
<li>快速播放速率</li>
<li>有音訊</li>
<li>有影片</li>
<li>正常播放率</li>
<li>緩慢的播放率</li>
<li>使用檔案</li>
</ul></td>
</tr>
<tr class="odd">
<td>waveaudio</td>
<td><ul>
<li>可以退出</li>
<li>可以播放</li>
<li>可以記錄</li>
<li>可以儲存</li>
<li>複合裝置</li>
<li>裝置類型</li>
</ul></td>
<td><ul>
<li>有音訊</li>
<li>有影片</li>
<li>輸入</li>
<li>輸出</li>
<li>使用檔案</li>
</ul></td>
</tr>
</tbody>
</table>



 

下表列出可在 *lpszRequest* 參數中指定的旗標，以及它們的意義：



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Flags</th>
<th>意義</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>可以偵測長度</td>
<td>如果裝置可以偵測出媒體的長度，則傳回 <strong>TRUE</strong> 。</td>
</tr>
<tr class="even">
<td>可以退出</td>
<td>如果裝置可以退出媒體，則傳回 <strong>TRUE</strong> 。</td>
</tr>
<tr class="odd">
<td>可以凍結</td>
<td>如果裝置可以凍結框架緩衝區中的資料，則傳回 <strong>TRUE</strong> 。</td>
</tr>
<tr class="even">
<td>可以鎖定</td>
<td>如果裝置可以鎖定資料，則傳回 <strong>TRUE</strong> 。</td>
</tr>
<tr class="odd">
<td>可以監視來源</td>
<td>如果裝置可將輸入 (來源) 傳遞至受監視的輸出，而不是目前的輸入選取範圍，則傳回 <strong>TRUE</strong> 。</td>
</tr>
<tr class="even">
<td>可以播放</td>
<td>如果裝置可以播放，則傳回 <strong>TRUE</strong> 。</td>
</tr>
<tr class="odd">
<td>可以預先進行</td>
<td>如果<strong></strong>裝置支援 &quot; &quot; 使用<a href="cue.md">提示</a>命令的預先處理旗標，則傳回 TRUE。</td>
</tr>
<tr class="even">
<td>可以預覽</td>
<td>如果裝置支援預覽，則傳回 <strong>TRUE</strong> 。</td>
</tr>
<tr class="odd">
<td>可以記錄</td>
<td>如果裝置支援錄製，則傳回 <strong>TRUE</strong> 。</td>
</tr>
<tr class="even">
<td>可以反轉</td>
<td>如果裝置可以反向播放，則傳回 <strong>TRUE</strong> 。</td>
</tr>
<tr class="odd">
<td>可以儲存</td>
<td>如果裝置可以儲存資料，則傳回 <strong>TRUE</strong> 。</td>
</tr>
<tr class="even">
<td>可以延展</td>
<td>如果裝置可以延展框架以填滿指定的顯示矩形，則傳回 <strong>TRUE</strong> 。</td>
</tr>
<tr class="odd">
<td>可延展輸入</td>
<td>如果裝置可以在將影像數位化至框架緩衝區的過程中調整影像的大小，則會傳回 <strong>TRUE</strong> 。</td>
</tr>
<tr class="even">
<td>可以測試</td>
<td>如果裝置辨識 test 關鍵字，則傳回 <strong>TRUE</strong> 。</td>
</tr>
<tr class="odd">
<td>cav</td>
<td>此旗標與其他專案結合時，會指定傳回信息適用于 CAV 格式 videodiscs。 如果未插入任何 videodisc，則這是預設值。</td>
</tr>
<tr class="even">
<td>頻率遞增率</td>
<td>傳回外部時鐘每秒支援的分割數目。 如果外部時鐘為毫秒時鐘，則傳回值為1000。 如果傳回值為0，則不支援時鐘。</td>
</tr>
<tr class="odd">
<td>clv</td>
<td>此旗標與其他專案結合時，會指定傳回信息適用于 CLV 格式 videodiscs。</td>
</tr>
<tr class="even">
<td>複合裝置</td>
<td>如果裝置支援 (檔案名) 的元素名稱，則傳回 <strong>TRUE</strong> 。</td>
</tr>
<tr class="odd">
<td>裝置類型</td>
<td>傳回裝置類型名稱，此名稱可以是下列其中一項：
<ul>
<li>cdaudio</li>
<li>Dat</li>
<li>digitalvideo</li>
<li>其他</li>
<li>overlay</li>
<li>掃描器</li>
<li>排序器</li>
<li>錄影機</li>
<li>videodisc</li>
<li>waveaudio</li>
</ul></td>
</tr>
<tr class="even">
<td>快速播放速率</td>
<td>傳回每秒畫面格的快速播放速率，如果裝置無法快速播放，則為零。</td>
</tr>
<tr class="odd">
<td>有音訊</td>
<td>如果裝置支援音訊播放，則傳回 <strong>TRUE</strong> 。</td>
</tr>
<tr class="even">
<td>具有時鐘</td>
<td>如果裝置具有時鐘，則傳回 <strong>TRUE</strong> 。</td>
</tr>
<tr class="odd">
<td>仍有</td>
<td>如果裝置以比動畫影片檔案更有效率的方式來處理具有單一影像的檔案，則會傳回 <strong>TRUE</strong> 。</td>
</tr>
<tr class="even">
<td>有時間碼</td>
<td>如果裝置能夠支援時間碼或不明，則傳回 <strong>TRUE</strong> 。</td>
</tr>
<tr class="odd">
<td>有影片</td>
<td>如果裝置支援影片，則傳回 <strong>TRUE</strong> 。</td>
</tr>
<tr class="even">
<td>輸入</td>
<td>傳回輸入裝置的總數。</td>
</tr>
<tr class="odd">
<td>最大播放率</td>
<td>傳回裝置的最大播放速率（以每秒畫面數為單位）。</td>
</tr>
<tr class="even">
<td>最小播放率</td>
<td>傳回裝置的最小播放速率（以每秒畫面數為單位）。</td>
</tr>
<tr class="odd">
<td>正常播放率</td>
<td>傳回裝置的正常播放速率（以每秒畫面格為單位）。</td>
</tr>
<tr class="even">
<td>標記數目</td>
<td>傳回可使用的標記數目上限;零表示不支援標記。</td>
</tr>
<tr class="odd">
<td>輸出</td>
<td>傳回輸出裝置的總數。</td>
</tr>
<tr class="even">
<td>搜尋精確度</td>
<td>傳回框架中搜尋的預期精確度;0表示裝置為框架正確，1表示裝置預期會在指定搜尋位置的某個畫面中，依此類推。</td>
</tr>
<tr class="odd">
<td>緩慢的播放率</td>
<td>傳回每秒畫面格的慢速播放速率，如果裝置無法慢慢播放則傳回零。</td>
</tr>
<tr class="even">
<td>使用檔案</td>
<td>如果複合裝置使用的資料存放區是檔案，則傳回 <strong>TRUE</strong> 。</td>
</tr>
<tr class="odd">
<td>使用調色板</td>
<td>如果裝置使用調色板，則傳回 <strong>TRUE</strong> 。</td>
</tr>
<tr class="even">
<td>windows</td>
<td>傳回裝置可支援的同時顯示視窗數目。</td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

可以是「等候」、「通知」或兩者。 針對數位影片和 VCR 裝置，也可以指定「測試」。 如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函數的 *lpszReturnString* 參數中的資訊。 此資訊取決於要求類型。

## <a name="examples"></a>範例

下列命令會傳回 "mysound" 裝置的裝置類型。

``` syntax
capability mysound device type
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
</dt> </dl>

 

