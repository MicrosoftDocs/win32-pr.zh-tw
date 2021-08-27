---
title: status 命令
description: Status 命令會要求來自裝置的狀態資訊。 所有裝置都會辨識此命令。
ms.assetid: 39961bd7-866d-450d-9fbf-347a8f508481
keywords:
- 狀態命令 Windows 多媒體
topic_type:
- apiref
api_name:
- status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd209ed04e51671ce7d9c8a7ae88a79073836c2e
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626113"
---
# <a name="status-command"></a>status 命令

> [!NOTE]
> 無偏差的通訊-Microsoft 支援多樣化且 inclusionary 的環境。  本檔中有 ' 從屬 ' 這個字的參考。 Microsoft 的 [Bias-Free 通訊樣式指南](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) 會將此視為排他性行為單字。  這種用語是用來做為命令內所使用的用語。 為求一致，本檔包含此字。 當您在命令中更改這個字時，我們會將此檔修正為一致。

Status 命令會要求來自裝置的狀態資訊。 所有裝置都會辨識此命令。

若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。

``` syntax
_stprintf_s(
  lpszCommand,
  TEXT("status %s %s %s"),
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

要求狀態資訊的旗標。 下表列出可辨識 **status** 命令的裝置類型，以及每種類型所使用的旗標。



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>裝置類型</th>
<th>要求旗標</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>cdaudio</td>
<td><ul>
<li>cdaudio 類型追蹤 <em>編號</em></li>
<li>目前的曲目</li>
<li>長度</li>
<li>長度追蹤 <em>號碼</em></li>
<li>媒體存在</li>
<li>mode</li>
<li>曲目數</li>
<li>position</li>
<li>位置曲目 <em>編號</em></li>
<li>準備</li>
<li>開始位置</li>
<li>時間格式</li>
</ul></td>
</tr>
<tr class="even">
<td>digitalvideo</td>
<td><ul>
<li>音訊</li>
<li>音訊對齊</li>
<li>音訊 bitspersample</li>
<li>音訊中斷</li>
<li>音訊 bytespersec</li>
<li>音訊輸入</li>
<li>音訊記錄</li>
<li>音訊來源</li>
<li>音訊 samplespersec</li>
<li>音訊串流</li>
<li>低音</li>
<li>bitsperpel</li>
<li>亮度</li>
<li>color</li>
<li>對比</li>
<li>目前的曲目</li>
<li>磁碟空間磁片 <em>磁碟機</em></li>
<li>檔案完成</li>
<li>檔案格式</li>
<li>檔案模式</li>
<li>forward</li>
<li>略過框架</li>
<li>gamma</li>
<li>input</li>
<li>左方磁片區</li>
<li>長度</li>
<li>長度追蹤 <em>號碼</em></li>
<li>媒體存在</li>
<li>mode</li>
<li>monitor</li>
<li>監視方法</li>
<li>名義</li>
<li>名義畫面播放速率</li>
<li>名義記錄畫面播放速率</li>
<li>曲目數</li>
<li>output</li>
<li>調色板控制碼</li>
<li>暫停模式</li>
<li>播放速度</li>
<li>position</li>
<li>位置曲目 <em>編號</em></li>
<li>準備</li>
<li>記錄畫面播放速率</li>
<li>參考 <em>框架</em></li>
<li>保留大小</li>
<li>右磁片區</li>
<li>確切搜尋</li>
<li>清晰度</li>
<li>smpte</li>
<li>速度</li>
<li>開始位置</li>
<li>仍為檔案格式</li>
<li>時間格式</li>
<li>色調</li>
<li>高音</li>
<li>未儲存</li>
<li>影片</li>
<li>影片索引鍵索引</li>
<li>影片按鍵色彩</li>
<li>影片記錄</li>
<li>影片來源</li>
<li>影片來源編號</li>
<li>影片串流</li>
<li>磁碟區</li>
<li>視窗控制碼</li>
<li>視窗可見</li>
<li>視窗最小化</li>
<li>視窗最大化</li>
</ul></td>
</tr>
<tr class="odd">
<td>overlay</td>
<td><ul>
<li>媒體存在</li>
<li>mode</li>
<li>曲目數</li>
<li>準備</li>
<li>Stretch - 自動縮放</li>
<li>視窗控制碼</li>
</ul></td>
</tr>
<tr class="even">
<td>排序器</td>
<td><ul>
<li>目前的曲目</li>
<li>除法類型</li>
<li>長度</li>
<li>長度追蹤 <em>號碼</em> 主機</li>
<li>媒體存在</li>
<li>mode</li>
<li>曲目數</li>
<li>Offset</li>
<li>連接埠</li>
<li>position</li>
<li>位置曲目 <em>編號</em></li>
<li>準備</li>
<li>奴隸</li>
<li>開始位置</li>
<li>節奏</li>
<li>時間格式</li>
</ul></td>
</tr>
<tr class="odd">
<td>錄影機</td>
<td><ul>
<li>組合記錄</li>
<li>音訊監視器</li>
<li>音訊監視器編號</li>
<li>音訊記錄</li>
<li>音訊記錄播放軌 <em>編號</em></li>
<li>音訊來源</li>
<li>音訊來源編號</li>
<li>通道</li>
<li>通道調諧器 <em>號碼</em></li>
<li>時鐘</li>
<li>時鐘識別碼</li>
<li>counter</li>
<li>計數器格式</li>
<li>計數器解析</li>
<li>目前的曲目</li>
<li>畫面播放速率</li>
<li>索引</li>
<li>索引開啟</li>
<li>長度</li>
<li>長度追蹤 <em>號碼</em></li>
<li>媒體存在</li>
<li>媒體類型</li>
<li>mode</li>
<li>音訊曲目數目</li>
<li>曲目數</li>
<li>影片曲目數</li>
<li>暫停 <em>timeout</em></li>
<li>播放格式</li>
<li>position</li>
<li>開始位置</li>
<li>位置曲目 <em>編號</em></li>
<li>postroll <em>持續期間</em></li>
<li>開啟電源</li>
<li>預先的 <em>持續時間</em></li>
<li>準備</li>
<li>記錄格式</li>
<li>速度</li>
<li>時間格式</li>
<li>時間模式</li>
<li>時間類型</li>
<li>出現的時間碼</li>
<li>時間碼記錄</li>
<li>時間碼類型</li>
<li>調諧器數目</li>
<li>影片監視器</li>
<li>影片監視器編號</li>
<li>影片記錄</li>
<li>影片記錄播放軌 <em>編號</em></li>
<li>影片來源</li>
<li>影片來源編號</li>
<li>寫入受保護</li>
</ul></td>
</tr>
<tr class="even">
<td>videodisc</td>
<td><ul>
<li>目前的曲目</li>
<li>磁片大小</li>
<li>forward</li>
<li>長度</li>
<li>長度追蹤 <em>號碼</em></li>
<li>媒體存在</li>
<li>媒體類型</li>
<li>mode</li>
<li>曲目數</li>
<li>position</li>
<li>位置曲目 <em>編號</em></li>
<li>準備</li>
<li>一邊</li>
<li>速度</li>
<li>開始位置</li>
<li>時間格式</li>
</ul></td>
</tr>
<tr class="odd">
<td>waveaudio</td>
<td><ul>
<li>對齊</li>
<li>bitspersample</li>
<li>bytespersec</li>
<li>通道</li>
<li>目前的曲目</li>
<li>格式標記</li>
<li>input</li>
<li>長度</li>
<li>長度追蹤 <em>號碼</em></li>
<li>等級</li>
<li>媒體存在</li>
<li>mode</li>
<li>曲目數</li>
<li>output</li>
<li>position</li>
<li>位置曲目 <em>編號</em></li>
<li>準備</li>
<li>samplespersec</li>
<li>開始位置</li>
<li>時間格式</li>
</ul></td>
</tr>
</tbody>
</table>



 

下表列出可在 **lpszRequest** 參數中指定的旗標，以及它們的意義。



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>值</th>
<th>意義</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>對齊</td>
<td>傳回資料的區塊對齊（以位元組為單位）。</td>
</tr>
<tr class="even">
<td>組合記錄</td>
<td>如果裝置設定為組合模式記錄，則傳回 <strong>TRUE</strong> 。</td>
</tr>
<tr class="odd">
<td>音訊</td>
<td>&quot; &quot; &quot; &quot; 根據最新的<a href="setaudio.md">setaudio</a> &quot; on &quot; 或 &quot; off &quot; 命令傳回 on 或 off。 &quot; &quot; 如果已啟用其中一或兩個喇叭，則會傳回，否則會傳回 &quot; &quot; 。</td>
</tr>
<tr class="even">
<td>音訊對齊</td>
<td>傳回資料區塊相對於輸入波形-音訊資料開頭的對齊方式。</td>
</tr>
<tr class="odd">
<td>音訊 bitspersample</td>
<td>傳回裝置用來錄製的每個樣本位數。 此旗標只適用于支援 &quot; pcm 演算法的裝置 &quot; 。</td>
</tr>
<tr class="even">
<td>音訊中斷</td>
<td>傳回最後一個 AVI 序列的音訊部分中斷的次數。 當系統嘗試將音訊資料寫入設備磁碟機，併發現該驅動程式已經播放了所有可用的資料時，系統就會計算出一份音訊中斷的次數。 只有 MCIAVI 數位視訊驅動程式能辨識此旗標。 它僅適用于效能評估;傳回值難以解讀。</td>
</tr>
<tr class="odd">
<td>音訊 bytespersec</td>
<td>傳回用於錄製的平均每秒位元組數。</td>
</tr>
<tr class="even">
<td>音訊輸入</td>
<td>傳回類比輸入音訊信號的近似即時音訊層級。 大於1000的值表示裁剪扭曲。 某些裝置只能在錄製音訊時傳回此值。 值沒有相關聯的 <a href="set.md">set</a> 或 <a href="setaudio.md">setaudio</a> 命令。</td>
</tr>
<tr class="odd">
<td>音訊監視器</td>
<td>傳回 &quot; 輸出 &quot; ，或其中一個有效的來源輸入類型。 如需詳細資訊，請參閱 <strong>setaudio</strong> &quot; 監視器 &quot; 命令。</td>
</tr>
<tr class="even">
<td>音訊監視器編號</td>
<td>傳回 <strong>狀態</strong>音訊監視器所指定之類型的監視影片編號 &quot; &quot; 。 如需詳細資訊，請參閱 <a href="setaudio.md">setaudio</a> 命令。</td>
</tr>
<tr class="odd">
<td>音訊記錄</td>
<td>傳回 &quot; &quot; 或 &quot; 關閉 &quot; ，反映 <strong>setaudio</strong>記錄所設定的狀態 &quot; &quot; 。</td>
</tr>
<tr class="even">
<td>音訊記錄播放軌 <em>編號</em></td>
<td>如果 VCR 設定為錄製音訊，則傳回 <strong>TRUE</strong> 。 如果未指定任何追蹤編號，則會假設為預設值1。</td>
</tr>
<tr class="odd">
<td>音訊 samplespersec</td>
<td>傳回每秒記錄的樣本數。</td>
</tr>
<tr class="even">
<td>音訊來源</td>
<td>傳回目前的音訊數位板來源： &quot; 左方 &quot; 、 &quot; 右邊 &quot; 、 &quot; 平均 &quot; 或 &quot; 身歷聲 &quot; 。</td>
</tr>
<tr class="odd">
<td>音訊來源編號</td>
<td>傳回 <strong>狀態</strong>音訊來源所傳回之類型的音訊來源編號 &quot; &quot; 。 如需詳細資訊，請參閱 <a href="setaudio.md">setaudio</a> 命令。</td>
</tr>
<tr class="even">
<td>音訊串流</td>
<td>傳回目前的音訊資料流程數目。</td>
</tr>
<tr class="odd">
<td>低音</td>
<td>傳回目前的音訊低音等級。</td>
</tr>
<tr class="even">
<td>bitsperpel</td>
<td>傳回儲存已捕捉或已記錄資料之每個圖元的位元組數目。</td>
</tr>
<tr class="odd">
<td>bitspersample</td>
<td>傳回每個樣本的位數。</td>
</tr>
<tr class="even">
<td>亮度</td>
<td>傳回目前的視頻亮度層級。</td>
</tr>
<tr class="odd">
<td>bytespersec</td>
<td>傳回每秒播放或記錄的平均位元組數。</td>
</tr>
<tr class="even">
<td>cdaudio 類型追蹤 <em>編號</em></td>
<td>傳回指定之追蹤編號的型別。 這可以是 &quot; 音訊 &quot; 或 &quot; 其他。&quot;</td>
</tr>
<tr class="odd">
<td>通道</td>
<td>傳回檔諧器上通道集的整數值。</td>
</tr>
<tr class="even">
<td>通道調諧器 <em>號碼</em></td>
<td>如果 &quot; 指定了調諧器 &quot; <em>號碼</em>，則會傳回邏輯調諧器上目前選取的<em></em>通道。 請注意，您可以有數個邏輯調諧器。</td>
</tr>
<tr class="odd">
<td>通道</td>
<td>傳回為 mono 設定的通道數目 (1，) 為身歷聲的2。</td>
</tr>
<tr class="even">
<td>時鐘</td>
<td>傳回外部時間。 時間必須是以不帶正負號的長整數表示總增量。 如需詳細資訊，請參閱 <a href="capability.md">功能</a> &quot; 頻率遞增速率 &quot; 命令。</td>
</tr>
<tr class="odd">
<td>時鐘識別碼</td>
<td>傳回識別時鐘的唯一整數。</td>
</tr>
<tr class="even">
<td>color</td>
<td>傳回目前的色彩層級。</td>
</tr>
<tr class="odd">
<td>對比</td>
<td>傳回目前的對比層級。</td>
</tr>
<tr class="even">
<td>counter</td>
<td>傳回目前計數器格式的計數器位置。</td>
</tr>
<tr class="odd">
<td>計數器格式</td>
<td>傳回目前的計數器格式。 如需詳細資訊，請參閱 <a href="set.md">設定</a> &quot; 計數器格式 &quot; 命令。</td>
</tr>
<tr class="even">
<td>計數器解析</td>
<td>傳回 &quot; &quot; 表示計數器解析度的框架或 &quot; 秒數 &quot; 。 這與精確度不同。</td>
</tr>
<tr class="odd">
<td>目前的曲目</td>
<td>傳回目前的曲目。MCISEQ sequencer 會傳回1。</td>
</tr>
<tr class="even">
<td>磁片大小</td>
<td>傳回8或12，表示載入的光碟大小（以英寸為單位）。</td>
</tr>
<tr class="odd">
<td>磁碟空間磁片 <em>磁碟機</em></td>
<td>傳回指定磁片磁碟機的 <a href="reserve.md">reserve</a> 命令可取得的大約磁碟空間（以目前的時間格式表示） <em>。</em> <em>磁片磁碟機</em>通常會指定為單一字母或單一字母，後面接著冒號 (： ) 。 不過，某些裝置可能會使用路徑。</td>
</tr>
<tr class="even">
<td>除法類型</td>
<td>傳回下列其中一個檔案除法類型：
<ul>
<li>PPQN</li>
<li>SMPTE 24 框架</li>
<li>SMPTE 25 框架</li>
<li>SMPTE 30 捨棄框架</li>
<li>SMPTE 30 框架</li>
</ul>
<br/> 您可以使用這項資訊來判斷 MIDI 檔案的格式，以及節奏和位置資訊的意義。<br/></td>
</tr>
<tr class="odd">
<td>檔案完成</td>
<td>傳回 <a href="load.md">負載</a>、 <a href="save.md">儲存</a>、 <a href="capture.md">捕捉</a>、 <a href="cut.md">剪</a>下、 <a href="copy.md">複製</a>、 <a href="delete.md">刪除</a>、 <a href="paste.md">貼</a>上或 <a href="undo.md">復原</a> 作業進度的估計百分比。  (的應用程式可以使用它來提供進度的視覺指標。 ) </td>
</tr>
<tr class="even">
<td>檔案格式</td>
<td>傳回 <a href="record.md">記錄</a> 或 <strong>儲存</strong> 命令的目前檔案格式。</td>
</tr>
<tr class="odd">
<td>檔案模式</td>
<td>傳回 &quot; 載入 &quot; 、 &quot; 儲存 &quot; 、 &quot; 編輯 &quot; 或 &quot; 閒置 &quot; 。 在 <a href="load.md"><strong>載入</strong></a> 作業期間，它會傳回 &quot; 載入 &quot; 。 在 <a href="https://www.bing.com/search?q=<strong>save</strong>"><strong>儲存</strong></a> 和 <a href="capture.md"><strong>捕獲</strong></a> 作業期間，它會傳回 &quot; 儲存 &quot; 。 在 <a href="cut.md"><strong>剪</strong></a>下、 <a href="copy.md"><strong>複製</strong></a>、 <a href="delete.md"><strong>刪除</strong></a>、 <a href="paste.md"><strong>貼</strong></a>上或 <a href="undo.md"><strong>復原</strong></a> 作業期間，它會傳回 &quot; 編輯 &quot; 。</td>
</tr>
<tr class="even">
<td>格式標記</td>
<td>傳回格式標記。</td>
</tr>
<tr class="odd">
<td>forward</td>
<td>如果播放方向為向前或裝置未播放，則傳回 <strong>TRUE</strong> 。</td>
</tr>
<tr class="even">
<td>畫面播放速率</td>
<td>傳回裝置預設會使用的每秒畫面格數數目。 NTSC 裝置會傳回30、PAL 25 等等。</td>
</tr>
<tr class="odd">
<td>略過框架</td>
<td>傳回播放最後一個 AVI 序列時未繪製的框架數目。 只有 MCIAVI 數位視訊驅動程式能辨識此旗標。 它僅適用于效能評估;傳回值難以解讀。</td>
</tr>
<tr class="even">
<td>gamma</td>
<td>傳回將 <a href="setvideo.md"><strong>setvideo</strong></a> &quot; gamma 設定為 &quot; <em>value</em>的值。</td>
</tr>
<tr class="odd">
<td>索引</td>
<td>傳回目前的索引顯示。 如需詳細資訊，請參閱 <a href="set.md"><strong>set</strong></a> &quot; index &quot; 命令。</td>
</tr>
<tr class="even">
<td>索引開啟</td>
<td>如果索引為 on，則傳回 <strong>TRUE</strong> 。</td>
</tr>
<tr class="odd">
<td>input</td>
<td>傳回輸入集。 如果未設定，則傳回的錯誤表示可以使用任何裝置。 針對數位視訊裝置，修改 &quot; 低音 &quot; 、 &quot; 高音 &quot; 、 &quot; 音量 &quot; 、 &quot; 亮度 &quot; 、 &quot; 色彩 &quot; 、 &quot; 對比 &quot; 、 &quot; gamma &quot; 、 &quot; 清晰度 &quot; 或 &quot; 色調旗標， &quot; 使其僅適用于輸入。 這是監視輸入時的預設值。</td>
</tr>
<tr class="even">
<td>左方磁片區</td>
<td>傳回左方音訊頻道的磁片區集合。</td>
</tr>
<tr class="odd">
<td>長度</td>
<td>以目前的時間格式傳回媒體的總長度。 若為 PPQN 檔案，則會以首歌指標單位傳回長度。 對於 SMPTE 檔案，它會傳回為 <em>hh： mm： ss： ff</em>，其中 <em>hh</em> 是小時， <em>mm</em> 是分鐘， <em>ss</em> 是秒，而 <em>ff</em> 是畫面格。 若為 VCR 裝置，長度為2小時 (除非已使用 <a href="https://www.bing.com/search?q=<strong>set</strong>"><strong>set</strong></a> 命令) 明確變更長度。</td>
</tr>
<tr class="even">
<td>長度追蹤 <em>號碼</em></td>
<td>傳回以 <em>數位</em>指定的曲目長度（以時間或框架為限）。若為 PPQN 檔案，則會以首歌指標單位傳回長度。 對於 SMPTE 檔案，它會傳回為 <em>hh： mm： ss： ff</em>，其中 <em>hh</em> 是小時， <em>mm</em> 是分鐘， <em>ss</em> 是秒，而 <em>ff</em> 是畫面格。<br/></td>
</tr>
<tr class="odd">
<td>等級</td>
<td>傳回目前的 PCM 音訊範例值。</td>
</tr>
<tr class="even">
<td>master</td>
<td>&quot; &quot; &quot; &quot; &quot; &quot; 根據同步處理集的類型，傳回 midi、無或 smpte。</td>
</tr>
<tr class="odd">
<td>媒體存在</td>
<td>如果媒體插入裝置中，則傳回 <strong>TRUE</strong> ，否則傳回 <strong>FALSE</strong> 。 Sequencer、影片重迭、數位影片和波形音訊裝置都會傳回 <strong>TRUE</strong>。</td>
</tr>
<tr class="even">
<td>媒體類型</td>
<td>傳回媒體的類型。 若為 VCR，此為 &quot; 8：8、 &quot; &quot; vhs &quot; 、 &quot; svhs &quot; 、 &quot; Beta &quot; 、 &quot; Hi8 &quot; 、 &quot; edBeta &quot; 或 &quot; 其他 &quot; 。 針對 videodiscs，這是 &quot; CAV &quot; 、 &quot; CLV &quot; 或 &quot; 其他 &quot; ，視 videodisc 類型而定。</td>
</tr>
<tr class="odd">
<td>mode</td>
<td>傳回裝置的目前模式。 所有裝置都可以傳回 &quot; 未就緒 &quot; 、 &quot; &quot; 已暫停、 &quot; 播放 &quot; 和 &quot; 停止的 &quot; 值。 某些裝置可以傳回額外的 &quot; 開啟 &quot; 、 &quot; 暫停 &quot; 、 &quot; 錄製 &quot; 和 &quot; 搜尋 &quot; 值。</td>
</tr>
<tr class="even">
<td>monitor</td>
<td>傳回 &quot; 檔案 &quot; 或 &quot; 輸入 &quot; 。 傳回的值表示目前的展示來源。</td>
</tr>
<tr class="odd">
<td>監視方法</td>
<td>傳回 &quot; 前置 &quot; 、 &quot; 貼文 &quot; 或 &quot; 直接 &quot; 。 傳回的值表示用於輸入監視的方法。</td>
</tr>
<tr class="even">
<td>名義</td>
<td>專案會修改 &quot; 低音 &quot; 、 &quot; 亮度 &quot; 、 &quot; 色彩 &quot; 、 &quot; 對比 &quot; 、 &quot; gamma &quot; 、清晰度、 &quot; &quot; &quot; 色調 &quot; 、 &quot; 高音 &quot; 和 &quot; 音量 &quot; 旗標，以傳回名義值，而不是目前的設定。</td>
</tr>
<tr class="odd">
<td>名義畫面播放速率</td>
<td>傳回與檔案相關聯的名義畫面播放速率。 單位為每秒畫面數乘以1000。</td>
</tr>
<tr class="even">
<td>名義記錄畫面播放速率</td>
<td>傳回與輸入視訊訊號相關聯的名義畫面播放速率。 單位為每秒畫面數乘以1000。</td>
</tr>
<tr class="odd">
<td>音訊曲目數目</td>
<td>傳回媒體上的音訊曲目數目。</td>
</tr>
<tr class="even">
<td>曲目數</td>
<td>傳回媒體上的曲目數目。 MCISEQ 和 MCIWAVE 裝置會傳回1，就像大部分的 VCR 裝置一樣。 MCIPIONR 裝置不支援此旗標。</td>
</tr>
<tr class="odd">
<td>影片曲目數</td>
<td>傳回媒體上的影片曲目數目。</td>
</tr>
<tr class="even">
<td>Offset</td>
<td>傳回以 SMPTE 為基礎之檔案的位移。 位移是以 SMPTE 為基礎之序列的開始時間。 時間會以 <em>hh： mm： ss： ff</em>傳回，其中 <em>hh</em> 是小時， <em>mm</em> 是分鐘， <em>ss</em> 是秒，而 <em>ff</em> 是畫面格。</td>
</tr>
<tr class="odd">
<td>output</td>
<td>傳回目前設定的輸出。 如果未設定任何輸出，則傳回的錯誤表示可以使用任何裝置。 針對數位視訊裝置，修改 &quot; 低音 &quot; 、 &quot; 高音 &quot; 、 &quot; 音量 &quot; 、 &quot; 亮度 &quot; 、 &quot; 色彩 &quot; 、 &quot; 對比 &quot; 、 &quot; gamma &quot; 、 &quot; 清晰度 &quot; 或 &quot; 色調旗標， &quot; 使其僅適用于輸出。 這是監視檔案時的預設值。</td>
</tr>
<tr class="even">
<td>暫停模式</td>
<td>&quot; &quot; 如果裝置在錄製時暫停，則會傳回錄製。 &quot; &quot; 如果裝置在播放時暫停，則會傳回播放。 如果裝置未暫停，則會傳回 &quot; 目前模式中不適用的錯誤動作 &quot; 。</td>
</tr>
<tr class="odd">
<td>暫停 timeout</td>
<td>傳回 <a href="pause.md"><strong>pause</strong></a> 命令的最長持續時間（以毫秒為單位）。</td>
</tr>
<tr class="even">
<td>播放格式</td>
<td>傳回程序代碼，指出磁帶將播放的格式（如果可偵測）： &quot; lp &quot; 、 &quot; ep &quot; 、 &quot; sp &quot; 或 &quot; 其他 &quot; 。 如需詳細資訊，請參閱 &quot; 記錄格式 &quot; 旗標。</td>
</tr>
<tr class="odd">
<td>播放速度</td>
<td>傳回值，這個值表示上一個 AVI 序列的實際播放時間與目標播放時間相符的程度。 值1000表示目標時間和實際時間相同。 例如，值為2000時，會指出 AVI 序列所花的時間比應該有兩倍的時間。 只有 MCIAVI 數位視訊驅動程式能辨識此旗標。 它僅適用于效能評估;傳回值難以解讀。</td>
</tr>
<tr class="even">
<td>連接埠</td>
<td>傳回指派給順序的 MIDI 埠號碼。</td>
</tr>
<tr class="odd">
<td>position</td>
<td>傳回目前的位置。若為 PPQN 檔案，則會以首歌指標單位傳回位置。 對於 SMPTE 檔案，它會傳回為 <em>hh： mm： ss： ff</em>，其中 <em>hh</em> 是小時， <em>mm</em> 是分鐘，ss 是秒，而 <em>ff</em> 是畫面格。<br/></td>
</tr>
<tr class="even">
<td>開始位置</td>
<td>傳回可用媒體開始的位置。</td>
</tr>
<tr class="odd">
<td>位置曲目 <em>編號</em></td>
<td>傳回由 <em>數位</em>指定的曲目開始位置。 若為 PPQN 檔案，則會以首歌指標單位傳回時間格式。 對於 SMPTE 檔案，它會傳回為 <em>hh： mm： ss： ff</em>，其中 <em>hh</em> 是小時， <em>mm</em> 是分鐘， <em>ss</em> 是秒，而 <em>ff</em> 是畫面格。 MCISEQ sequencer 會傳回零。 MCIPIONR 裝置不支援此旗標。 MCIWAVE 裝置會傳回零。</td>
</tr>
<tr class="even">
<td>postroll 持續期間</td>
<td>傳回在發出 <a href="stop.md"><strong>stop</strong></a> 或 <a href="pause.md"><strong>pause</strong></a> 命令時，煞車 VCR 傳輸所需的磁帶長度（以目前的時間格式）。</td>
</tr>
<tr class="odd">
<td>開啟電源</td>
<td>如果 VCR 的電源開啟，則傳回 <strong>TRUE</strong> 。</td>
</tr>
<tr class="even">
<td>預先的持續時間</td>
<td>以目前時間格式傳回磁帶的長度（以目前時間格式為限），以穩定 VCR 輸出。</td>
</tr>
<tr class="odd">
<td>準備</td>
<td>如果裝置已準備好接受另一個命令，則會傳回 <strong>TRUE</strong> 。</td>
</tr>
<tr class="even">
<td>記錄格式</td>
<td>傳回程序代碼，指出將在其中記錄磁帶的格式。 目前的傳回型別為 &quot; lp &quot; 、 &quot; ep &quot; 、 &quot; sp &quot; 或 &quot; 其他類型 &quot; 。 這些格式不是 VHS 特有的，而且可以套用至任何具有多個可選取記錄格式的 VCR。 &quot;Sp &quot; 類型是最快、最高品質的錄製格式，並且在單一格式的 vcr 上當做預設值使用。</td>
</tr>
<tr class="odd">
<td>記錄畫面播放速率</td>
<td>傳回畫面播放速率（以每秒畫面數乘以1000），用於壓縮。</td>
</tr>
<tr class="even">
<td>參考 <em>框架</em></td>
<td>傳回指定 <em>框架</em>之前最接近之主要畫面格影像的框架編號。</td>
</tr>
<tr class="odd">
<td>保留大小</td>
<td>傳回保留工作區的大小（以目前的時間格式）。 大小對應于從完整工作區播放壓縮資料所需的大約時間。 如果沒有保留的磁碟空間，則會傳回零。 此旗標會傳回大約的大小，因為壓縮資料的精確磁碟空間無法在資料壓縮後才進行預測。</td>
</tr>
<tr class="even">
<td>右磁片區</td>
<td>傳回右邊音訊頻道的磁片區集。</td>
</tr>
<tr class="odd">
<td>samplespersec</td>
<td>傳回每秒播放或錄製的樣本數。</td>
</tr>
<tr class="even">
<td>確切搜尋</td>
<td>傳回 &quot; &quot; 或 &quot; 關閉 &quot; ，指出是否 &quot; 已設定搜尋確切旗標 &quot; 。</td>
</tr>
<tr class="odd">
<td>清晰度</td>
<td>傳回裝置目前的清晰度層級。</td>
</tr>
<tr class="even">
<td>一邊</td>
<td>傳回1或2，表示載入 videodisc 的哪一端。</td>
</tr>
<tr class="odd">
<td>奴隸</td>
<td>&quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; 根據同步處理集的類型，傳回 file、midi、none 或 smpte。</td>
</tr>
<tr class="even">
<td>smpte</td>
<td>傳回與工作區中目前位置相關聯的 SMPTE 時間碼。 這是格式為 <em>dd</em>： dd： dd 的字串，其中每個 <em>d</em> 代表0到9的數位。 如果工作區資料不包含時間碼資料，則此旗標會傳回00:00:00:00。</td>
</tr>
<tr class="odd">
<td>速度</td>
<td>以 [ <a href="https://www.bing.com/search?q=<strong>set</strong>"><strong>設定</strong></a> &quot; 速度] 命令) 所使用的相同格式，傳回裝置的目前速度（以每秒的畫面格為單位） (或相同的格式 &quot; 。 MCIPIONR videodisc player 不支援此旗標。</td>
</tr>
<tr class="even">
<td>開始位置</td>
<td>傳回媒體的開始位置。</td>
</tr>
<tr class="odd">
<td>仍為檔案格式</td>
<td>傳回 <a href="capture.md"><strong>capture</strong></a> 命令的目前檔案格式。</td>
</tr>
<tr class="even">
<td>Stretch - 自動縮放</td>
<td>如果已啟用延展， <strong>則傳回 TRUE</strong> 。</td>
</tr>
<tr class="odd">
<td>節奏</td>
<td>傳回目前時間格式之 MIDI 序列的目前節奏。 針對具有 PPQN 格式的檔案，節奏是每分鐘的節拍。 針對具有 SMPTE 格式的檔案，節奏是以每秒的畫面格為單位。</td>
</tr>
<tr class="even">
<td>時間格式</td>
<td>傳回目前的時間格式。 如需詳細資訊，請參閱 <a href="set.md"><strong>set</strong></a> 命令中的時間格式。</td>
</tr>
<tr class="odd">
<td>時間模式</td>
<td>傳回目前的位置時間模式。 它可以是 &quot; 偵測 &quot; 、時間 &quot; 碼 &quot; 或 &quot; 計數器 &quot; 。</td>
</tr>
<tr class="even">
<td>時間類型</td>
<td>傳回使用中的目前位置時間：時間 &quot; 碼 &quot; 或 &quot; 計數器 &quot; 。</td>
</tr>
<tr class="odd">
<td>出現的時間碼</td>
<td>如果已在磁帶的目前位置記錄時間碼， <strong>則傳回 TRUE</strong> 。 時間碼必須從目前的位置前進。 可能必須播放 VCR 才能檢查這種情況。</td>
</tr>
<tr class="even">
<td>時間碼記錄</td>
<td>如果 VCR 設定為記錄時間碼，則傳回 <strong>TRUE</strong> 。</td>
</tr>
<tr class="odd">
<td>時間碼類型</td>
<td>傳回 &quot; smpte &quot; 、 &quot; smpte drop &quot; 、 &quot; other &quot; 或 &quot; none &quot; 。 請注意，每秒畫面格數可以從 [狀態 &quot; 畫面播放速率] &quot; 命令取得，而 [ <a href="capability.md"><strong>功能</strong></a> &quot; 搜尋精確度] 命令可以傳回裝置的精確度 &quot; 。</td>
</tr>
<tr class="even">
<td>色調</td>
<td>傳回目前的影片色調層級。</td>
</tr>
<tr class="odd">
<td>高音</td>
<td>傳回目前的音訊高音層級。</td>
</tr>
<tr class="even">
<td>調諧器數目</td>
<td>傳回目前的邏輯調諧器數目。</td>
</tr>
<tr class="odd">
<td>未儲存</td>
<td>如果工作區中有記錄的資料可能因為<a href="close.md"><strong>close</strong></a>、 <a href="load.md"><strong>load</strong></a>、 <a href="record.md"><strong>record</strong></a>、 <a href="reserve.md"><strong>reserve</strong></a>、<a href="cut.md"><strong>剪</strong></a>下、<a href="delete.md"><strong>刪除</strong></a>或<a href="paste.md"><strong>貼</strong></a>上命令而遺失，則傳回<strong>TRUE</strong> 。 否則傳回 <strong>FALSE</strong> 。</td>
</tr>
<tr class="even">
<td>影片</td>
<td>傳回 &quot; &quot; 或 &quot; 關閉 &quot; ，反映 <a href="setvideo.md"><strong>setvideo</strong></a> 命令所設定的狀態。</td>
</tr>
<tr class="odd">
<td>影片按鍵色彩</td>
<td>傳回索引鍵色彩的值。</td>
</tr>
<tr class="even">
<td>影片索引鍵索引</td>
<td>傳回索引鍵索引的值。</td>
</tr>
<tr class="odd">
<td>影片監視器</td>
<td>傳回 &quot; 輸出 &quot; 或其中一個有效的來源輸入類型。 如需詳細資訊，請參閱 <a href="setvideo.md"><strong>setvideo</strong></a> &quot; 監視器 &quot; 命令。</td>
</tr>
<tr class="even">
<td>影片監視器編號</td>
<td>傳回狀態影片監視器所傳回之類型的受監視影片編號 &quot; &quot; 。 如需詳細資訊，請參閱 <a href="setvideo.md">setvideo</a> 命令。</td>
</tr>
<tr class="odd">
<td>影片記錄</td>
<td>傳回 &quot; &quot; 或 &quot; 關閉 &quot; ，反映 <a href="setvideo.md"><strong>setvideo</strong></a>記錄所設定的目前狀態 &quot; &quot; 。</td>
</tr>
<tr class="even">
<td>影片記錄播放軌 <em>編號</em></td>
<td>如果 VCR 設定為錄製影片，則傳回 <strong>TRUE</strong> 。 如果未指定任何追蹤編號，則會假設為預設值1。</td>
</tr>
<tr class="odd">
<td>影片來源</td>
<td>傳回影片來源類型。 如需詳細資訊，請參閱 <a href="setvideo.md"><strong>setvideo</strong></a> 命令。</td>
</tr>
<tr class="even">
<td>影片來源編號</td>
<td>傳回數位，此數位對應于所使用之類型的影片來源。 例如，如果使用第二個 NTSC video 來源輸入，則會傳回2。</td>
</tr>
<tr class="odd">
<td>影片串流</td>
<td>傳回目前的視頻串流號碼。</td>
</tr>
<tr class="even">
<td>磁碟區</td>
<td>將平均音量傳回到左邊和右邊的喇叭。 如果裝置尚未播放或尚未設定磁片區，則會傳回錯誤。</td>
</tr>
<tr class="odd">
<td>視窗控制碼</td>
<td>傳回傳回值低序位字組中視窗控制碼的 ASCII 十進位值。</td>
</tr>
<tr class="even">
<td>視窗最大化</td>
<td>如果視窗最大化，則傳回 <strong>TRUE</strong> 。</td>
</tr>
<tr class="odd">
<td>視窗最小化</td>
<td>如果視窗最小化，則傳回 <strong>TRUE</strong> 。</td>
</tr>
<tr class="even">
<td>視窗可見</td>
<td>如果視窗不是隱藏的，則傳回 <strong>TRUE</strong> 。</td>
</tr>
<tr class="odd">
<td>寫入受保護</td>
<td>如果裝置 (偵測到寫入保護是在) 上，則會傳回 <strong>TRUE</strong> 。 如果可以錄製，或無法判斷它是否可以記錄 (而不實際寫入) ，驅動程式會傳回 <strong>FALSE</strong>。</td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

可以是「等候」、「通知」或兩者。 針對數位影片和 VCR 裝置，也可以指定「測試」。 如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 [**mciSendString**](/previous-versions//dd757161(v=vs.85))的 *lpszReturnString* 參數中的資訊。 此資訊取決於要求類型。

## <a name="remarks"></a>備註

發出使用位置值的任何命令之前，您應該使用 [set](set.md) 命令來設定所需的時間格式。

## <a name="examples"></a>範例

下列命令會傳回 "mysound" 裝置的目前模式。

``` syntax
status mysound mode
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

[capability](capability.md)
</dt> <dt>

[捕獲](capture.md)
</dt> <dt>

[close](close.md)
</dt> <dt>

[削減](cut.md)
</dt> <dt>

[delete](delete.md)
</dt> <dt>

[載入](load.md)
</dt> <dt>

[pause](pause.md)
</dt> <dt>

[粘貼](paste.md)
</dt> <dt>

[記錄](record.md)
</dt> <dt>

[儲備](reserve.md)
</dt> <dt>

[儲存](save.md)
</dt> <dt>

[set](set.md)
</dt> <dt>

[setaudio](setaudio.md)
</dt> <dt>

[setvideo](setvideo.md)
</dt> <dt>

[停止](stop.md)
</dt> <dt>

[復原](undo.md)
</dt> </dl>

 

