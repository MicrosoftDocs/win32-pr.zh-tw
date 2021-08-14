---
title: set 命令
description: Set 命令會建立裝置的控制項設定。 CD 音訊、數位影片、MIDI sequencer、VCR、videodisc、影片重迭和波形音訊裝置都會辨識此命令。
ms.assetid: 1ec4d84e-372a-4b6d-b694-f5afb41f90b2
keywords:
- 設定命令 Windows 多媒體
topic_type:
- apiref
api_name:
- set
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75f407a1e360cfbd6407f7ada29192addece7f7a968a2437326dc091fe0d9522
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371010"
---
# <a name="set-command"></a>set 命令

> [!NOTE]
> 無偏差的通訊-Microsoft 支援多樣化且 inclusionary 的環境。  本檔中有 ' 從屬 ' 這個字的參考。 Microsoft 的 [Bias-Free 通訊樣式指南](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) 會將此視為排他性行為單字。  這種用語是用來做為命令內所使用的用語。 為求一致，本檔包含此字。 當您在命令中更改這個字時，我們會將此檔修正為一致。


Set 命令會建立裝置的控制項設定。 CD 音訊、數位影片、MIDI sequencer、VCR、videodisc、影片重迭和波形音訊裝置都會辨識此命令。

若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。

``` syntax
_stprintf_s(
  lpszCommand,
  TEXT("set %s %s %s"),
  lpszDeviceID,
  lpszSetting,
  lpszFlags
);
      
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

MCI 裝置的識別碼。 開啟裝置時，會指派此識別碼或別名。

</dd> <dt>

<span id="lpszSetting"></span><span id="lpszsetting"></span><span id="LPSZSETTING"></span>*lpszSetting*
</dt> <dd>

用來建立控制項設定的旗標。 下表列出可辨識 **set** 命令和每個型別所使用之旗標的裝置類型。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>裝置類型</th>
<th>命令旗標</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>cdaudio</td>
<td><ul>
<li>全音訊</li>
<li>全部音訊</li>
<li>音訊停止</li>
<li>剩餘的音訊</li>
<li>音訊立即關閉</li>
<li>音訊右邊</li>
<li>門已關閉</li>
<li>門開啟</li>
<li>時間格式毫秒</li>
<li>時間格式 msf</li>
<li>時間格式 tmsf</li>
</ul></td>
</tr>
<tr class="even">
<td>digitalvideo</td>
<td><ul>
<li>全音訊</li>
<li>全部音訊</li>
<li>音訊停止</li>
<li>剩餘的音訊</li>
<li>音訊立即關閉</li>
<li>音訊右邊</li>
<li>門已關閉</li>
<li>門開啟</li>
<li>檔案格式 <em>格式</em></li>
<li>確切搜尋</li>
<li>完全搜尋</li>
<li>速度 <em>因素</em></li>
<li>仍為檔案格式 <em>格式</em></li>
<li>時間格式框架</li>
<li>時間格式毫秒</li>
<li>關閉影片</li>
<li>影片開啟</li>
</ul></td>
</tr>
<tr class="odd">
<td>overlay</td>
<td><ul>
<li>全音訊</li>
<li>全部音訊</li>
<li>音訊停止</li>
<li>剩餘的音訊</li>
<li>音訊立即關閉</li>
<li>音訊右邊</li>
<li>門已關閉</li>
<li>門開啟</li>
<li>關閉影片</li>
<li>影片開啟</li>
</ul></td>
</tr>
<tr class="even">
<td>排序器</td>
<td><ul>
<li>全音訊</li>
<li>全部音訊</li>
<li>音訊停止</li>
<li>剩餘的音訊</li>
<li>音訊立即關閉</li>
<li>音訊右邊</li>
<li>門已關閉</li>
<li>門開啟</li>
<li>主要 MIDI</li>
<li>master 無</li>
<li>master SMPTE</li>
<li>位移 <em>時間</em></li>
<li>埠對應程式</li>
<li>埠無</li>
<li>埠 <em>port_number</em></li>
<li>從屬檔案</li>
<li>從屬 MIDI</li>
<li>從屬無</li>
<li>從屬的 SMPTE</li>
<li>節奏 <em>tempo_value</em></li>
<li>時間格式毫秒</li>
<li>時間格式的 SMPTE <em>fps</em></li>
<li>時間格式 SMPTE 30 捨棄</li>
<li>時間格式歌曲指標</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>錄影機</strong></td>
<td><ul>
<li>組合記錄</li>
<li>將記錄組合為關閉</li>
<li>全音訊</li>
<li>全部音訊</li>
<li>音訊停止</li>
<li>剩餘的音訊</li>
<li>音訊立即關閉</li>
<li>音訊右邊</li>
<li>時鐘 <em>時間</em></li>
<li>計數器格式</li>
<li>計數器 <em>值</em></li>
<li>門已關閉</li>
<li>門開啟</li>
<li>索引計數器</li>
<li>索引日期</li>
<li>索引時間</li>
<li>索引時間</li>
<li>codelength <em>持續期間</em></li>
<li>暫停 <em>timeout</em></li>
<li>postroll 持續期間-</li>
<li><em>duration</em></li>
<li>開啟電源</li>
<li>關閉電源</li>
<li>預先進行 <em>持續時間持續時間</em></li>
<li>記錄格式 SP</li>
<li>LP 記錄格式</li>
<li>記錄格式 EP</li>
<li>速度 <em>因素</em></li>
<li>時間格式框架</li>
<li>時間格式 hms</li>
<li>時間格式毫秒</li>
<li>時間格式 msf</li>
<li>時間格式的 SMPTE <em>fps</em></li>
<li>時間格式 SMPTE 30 捨棄</li>
<li>時間格式 tmsf</li>
<li>時間模式計數器</li>
<li>偵測時間模式</li>
<li>時間模式時間碼</li>
<li>追蹤加號</li>
<li>追蹤減號</li>
<li>追蹤重設</li>
</ul></td>
</tr>
<tr class="even">
<td>videodisc</td>
<td><ul>
<li>全音訊</li>
<li>全部音訊</li>
<li>音訊停止</li>
<li>剩餘的音訊</li>
<li>音訊立即關閉</li>
<li>音訊右邊</li>
<li>門已關閉</li>
<li>門開啟</li>
<li>時間格式框架</li>
<li>時間格式 hms</li>
<li>時間格式毫秒</li>
<li>時間格式追蹤</li>
<li>關閉影片</li>
<li>影片開啟</li>
</ul></td>
</tr>
<tr class="odd">
<td>waveaudio</td>
<td><ul>
<li>對齊 <em>整數</em></li>
<li>任何輸入</li>
<li>任何輸出</li>
<li>全音訊</li>
<li>全部音訊</li>
<li>音訊停止</li>
<li>剩餘的音訊</li>
<li>音訊立即關閉</li>
<li>音訊右邊</li>
<li>bitspersample <em>bit_count</em></li>
<li>bytespersec <em>byte_rate</em></li>
<li>通道 <em>channel_count</em></li>
<li>門已關閉</li>
<li>門開啟</li>
<li>格式化標記 pcm</li>
<li>格式化標記 <em>標記</em></li>
<li>輸入 <em>整數</em></li>
<li>輸出 <em>整數</em></li>
<li>samplespersec <em>整數</em></li>
<li>時間格式位元組</li>
<li>時間格式毫秒</li>
<li>時間格式範例</li>
</ul></td>
</tr>
</tbody>
</table>



 

下表列出可在 **lpszSetting** 參數中指定的旗標，以及它們的意義。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>值</th>
<th>意義</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>對齊 <em>整數</em></td>
<td>設定資料區塊相對於傳遞到波形-音訊裝置的開頭的對齊方式。 檔案會以這種格式儲存。</td>
</tr>
<tr class="even">
<td>任何輸入</td>
<td>錄製時，請使用支援目前格式的任何輸入。 這是預設值。</td>
</tr>
<tr class="odd">
<td>任何輸出</td>
<td>在播放時，請使用任何支援目前格式的輸出。 此為預設值。</td>
</tr>
<tr class="even">
<td>組合記錄 <br/> 將記錄組合為關閉 <br/></td>
<td>在組合模式中，所有的追蹤都會依裝置的定義記錄。 大部分的 Vcr 預設為組合模式。</td>
</tr>
<tr class="odd">
<td>全音訊 <br/> 全部音訊 <br/></td>
<td>停用或啟用音訊輸出。 影片重迭裝置、MCISEQ sequencer 和 MCIWAVE 波形-音訊裝置不支援此旗標。</td>
</tr>
<tr class="even">
<td>音訊停止 <br/> 剩餘的音訊 <br/> 音訊立即關閉 <br/> 音訊右邊 <br/></td>
<td>停用或啟用向左或向右音訊頻道的輸出。 影片重迭裝置、MCISEQ sequencer 和 MCIWAVE 波形-音訊裝置不支援此旗標。</td>
</tr>
<tr class="odd">
<td>bitspersample <em>bit_count</em></td>
<td>設定每個 PCM (脈衝程式碼調製) 範例播放或錄製的位數。 檔案會以這種格式儲存。</td>
</tr>
<tr class="even">
<td>bytespersec <em>byte_rate</em></td>
<td>設定每秒播放或記錄的平均位元組數。 檔案會以這種格式儲存。</td>
</tr>
<tr class="odd">
<td>通道 <em>channel_count</em></td>
<td>設定播放和錄製的通道。 檔案會以這種格式儲存。</td>
</tr>
<tr class="even">
<td>時鐘 <em>時間</em></td>
<td>將外部時鐘的時間設定為 <em>時間。</em> 格式會指定為長帶正負號的整數。</td>
</tr>
<tr class="odd">
<td>計數器格式</td>
<td>設定計數器的時間格式，如 status 計數器所傳回<a href="status.md"></a> &quot; &quot; 。 如需適用類型的詳細資訊，請參閱 <strong>設定</strong> &quot; 時間格式 &quot; 命令。</td>
</tr>
<tr class="even">
<td>計數器 <em>值</em></td>
<td>將 VCR 計數器設定為指定的值。 您必須在目前的計數器格式中指定此值。 如需詳細資訊，請參閱 <strong>設定</strong> &quot; 計數器格式 &quot; 命令。</td>
</tr>
<tr class="odd">
<td>門已關閉</td>
<td>在可能的情況下，收回紙匣並關閉門。 若為 Vcr，則會自動載入磁帶。</td>
</tr>
<tr class="even">
<td>門開啟</td>
<td>開啟門並取出紙匣或磁帶（可能的話）。</td>
</tr>
<tr class="odd">
<td>檔案格式 <em>格式</em></td>
<td>指定用於 <a href="save.md">儲存</a> 或 <a href="capture.md">捕捉</a> 命令的檔案格式。 如果省略此參數，則可能會預設為設備磁碟機定義的格式。 如果指定的檔案格式與目前選取的演算法和品質相衝突，則會將它們變更為檔案格式的預設值。 以下是定義的檔案格式：
<ul>
<li>avi：指定 AVI 格式。</li>
<li>avss：指定 AVSS 格式。</li>
<li>dib：指定 DIB 格式。</li>
<li>jfif：指定 JFIF 格式。</li>
<li>jpeg：指定 JPEG 格式。</li>
<li>mpeg：指定 MPEG 格式。</li>
<li>rdib：指定 RLE DIB 格式。</li>
<li>rjpeg：指定 RJPEG 格式。</li>
</ul></td>
</tr>
<tr class="even">
<td>格式化標記 pcm</td>
<td>將格式類型設定為 PCM 以進行播放和錄製。 檔案會以這種格式儲存。</td>
</tr>
<tr class="odd">
<td>格式化標記 <em>標記</em></td>
<td>設定播放和錄製的格式類型。 檔案會以這種格式儲存。</td>
</tr>
<tr class="even">
<td>索引時間碼 <br/> 索引計數器 <br/> 索引日期 <br/> 索引時間 <br/></td>
<td>設定 VCR 的目前顯示畫面。</td>
</tr>
<tr class="odd">
<td>輸入 <em>整數</em></td>
<td>設定用來做為輸入的音訊通道。</td>
</tr>
<tr class="even">
<td>長度 <em>持續時間</em></td>
<td>在 VCR 中設定磁帶的使用者指定長度。 此長度是由 <a href="status.md">status</a> &quot; length 命令所傳回 &quot; ，而且是為了與需要這個命令以傳回有效長度的應用程式相容而提供。</td>
</tr>
<tr class="odd">
<td>主要 midi</td>
<td>將 MIDI sequencer 設定為同步處理來源。 同步處理資料會以 MIDI 格式傳送。 MCISEQ sequencer 不支援此旗標。</td>
</tr>
<tr class="even">
<td>master 無</td>
<td>禁止 MIDI sequencer 傳送同步處理資料。 MCISEQ sequencer 不支援此旗標。</td>
</tr>
<tr class="odd">
<td>master smpte</td>
<td>將 MIDI sequencer 設定為同步處理來源。 同步處理資料會以 SMPTE (社會的運動圖片和電視工程師) 格式傳送。 MCISEQ sequencer 不支援此旗標。</td>
</tr>
<tr class="even">
<td>位移 <em>時間</em></td>
<td>設定 SMPTE 時差 <em>時間</em>。 位移是以 SMPTE 為基礎之序列的開始時間。 <em>時間</em>會表示為<em>hh</em>： <em>mm</em>： <em>ss</em>： <em>ff</em>，其中<em>hh</em>是小時， <em>mm</em>是分鐘， <em>ss</em>是秒，而<em>ff</em>是畫面格。</td>
</tr>
<tr class="odd">
<td>輸出 <em>整數</em></td>
<td>設定用來作為輸出的音訊通道。</td>
</tr>
<tr class="even">
<td>暫停 <em>timeout</em></td>
<td>設定 <a href="pause.md">pause</a> 命令的最長持續時間（以毫秒為單位）。 <em>Timeout</em>值為零表示不會進行任何超時。</td>
</tr>
<tr class="odd">
<td>postroll 持續 <em>期間</em></td>
<td>設定在發出 <a href="stop.md">stop</a> 或 <strong>pause</strong> 命令時，煞車 VCR 傳輸所需的長度（以目前的時間格式）。</td>
</tr>
<tr class="even">
<td>埠對應程式</td>
<td>將 MIDI 對應程式設定為接收 MIDI 訊息的埠。 如果 MIDI 對應程式或其所需的埠正由另一個應用程式使用中，則此命令會失敗。</td>
</tr>
<tr class="odd">
<td>埠無</td>
<td>停用傳送 MIDI 訊息。 此命令也會關閉 MIDI 埠。</td>
</tr>
<tr class="even">
<td>埠 <em>port_number</em></td>
<td>設定接收 MIDI 訊息的 MIDI 埠。 如果您嘗試開啟的埠正由另一個應用程式使用中，則此命令會失敗。</td>
</tr>
<tr class="odd">
<td>開啟電源 <br/> 關閉電源 <br/></td>
<td>將裝置電源設定為開啟或關閉。</td>
</tr>
<tr class="even">
<td>預先進行 <em>持續時間持續時間</em></td>
<td>設定穩定的 VCR 輸出所需的長度（以目前的時間格式）。</td>
</tr>
<tr class="odd">
<td>記錄格式 SP <br/> LP 記錄格式 <br/> 記錄格式 EP <br/></td>
<td>將 VCR 的錄製模式設定為標準 play 的 SP、EP （延長播放）或適用于長時間播放的 LP。 這些值並非 VHS 特定的。 它們會對應到具有其他磁帶格式的三種適當模式。 例如，SP 對應到最快、最高品質的記錄。</td>
</tr>
<tr class="even">
<td>samplespersec <em>整數</em></td>
<td>設定播放和錄製的取樣率。 檔案會以這種格式儲存。</td>
</tr>
<tr class="odd">
<td>確切搜尋<br/> 完全搜尋 <br/></td>
<td>選取兩種搜尋模式的其中一種。 &quot;在完全搜尋的情況 &quot; 下，seek 一律會移至指定的框架。 當 &quot; 完全搜尋時 &quot; ，搜尋會在指定的框架之前移至最接近的主要畫面格。</td>
</tr>
<tr class="even">
<td>從屬檔案</td>
<td>將 MIDI sequencer 設定為使用檔案資料作為同步處理來源。 這是預設值。</td>
</tr>
<tr class="odd">
<td>從屬 midi</td>
<td>將 MIDI sequencer 設定為使用連入的 MIDI 資料作為同步處理來源。 Sequencer 會以 MIDI 格式辨識同步處理資料。 MCISEQ sequencer 不支援此旗標。</td>
</tr>
<tr class="even">
<td>從屬無</td>
<td>將 MIDI sequencer 設定為忽略同步處理</td>
</tr>
<tr class="odd">
<td>從屬的 smpte</td>
<td>將 MIDI sequencer 設定為使用連入的 MIDI 資料作為同步處理來源。 Sequencer 會以 SMPTE 格式辨識同步處理資料。 MCISEQ sequencer 不支援此旗標。</td>
</tr>
<tr class="even">
<td>速度因素</td>
<td>設定從工作區播放影片和音訊的相對速度。 因素是名義畫面播放速率與所需畫面播放速率之間的比率，其中名義畫面播放速率會指定為1000。  (的速率為500的一半是正常的速度、2000是兩倍的一般速度，依此類推。 ) 將速度設定為零，就會盡可能快速地播放影片，而不會卸載畫面格而不需要音訊。</td>
</tr>
<tr class="odd">
<td>仍為檔案格式 <em>格式</em></td>
<td>指定用於 capture 命令的檔案格式。</td>
</tr>
<tr class="even">
<td>節奏 tempo_value</td>
<td>根據目前時間格式設定序列的節奏。 如果是以 PPQN 為基礎的檔案，tempo_value 會以每分鐘的節拍來解讀。 針對以 SMPTE 為基礎的檔案，tempo_value 會轉譯為每秒的畫面格。</td>
</tr>
<tr class="odd">
<td>時間格式位元組</td>
<td>在 PCM 檔案格式中，將時間格式設定為 bytes。 此命令之後的所有位置資訊都指定為位元組。</td>
</tr>
<tr class="even">
<td>時間格式框架</td>
<td>將時間格式設定為框架。 所有使用位置值的命令都將採用框架。 開啟裝置時，框架是預設模式。 使用 CAV 格式的 videodiscs 支援。</td>
</tr>
<tr class="odd">
<td>時間格式 hms</td>
<td>將時間格式設定為小時、分鐘和秒。 所有使用位置值的命令都將採用 HMS。 HMS 是 CLV videodiscs 的預設格式。 將 HMS 值指定為 hh： mm： ss，其中 hh 為 hours，mm 為分鐘，ss 為秒。 如果欄位和下列所有欄位都為零，您可以省略欄位。 例如，3、3:0 和3:0:0 都是表示3小時的有效方式。 <br/></td>
</tr>
<tr class="even">
<td>時間格式毫秒</td>
<td>將時間格式設定為毫秒。 使用位置值的所有命令都將採用毫秒。 您可以將毫秒縮寫為 &quot; 毫秒 &quot; 。 針對 sequencer 裝置，順序檔會將預設格式設定為 PPQN 或 SMPTE。 影片重迭裝置不支援此旗標。<br/></td>
</tr>
<tr class="odd">
<td>時間格式 msf</td>
<td>將時間格式設定為分鐘、秒和框架。 使用位置值的所有命令都會假設 MSF (CD 音訊) 的預設格式。 將 MSF 值指定為 mm： ss： ff，其中 mm 為分鐘，ss 為秒，而 ff 為框架。 如果欄位和下列所有欄位都為零，您可以省略欄位。 例如，3、3:0 和3:0:0 是表示3分鐘的有效方式。<br/> MSF 欄位具有下列最大值：<br/>
<ul>
<li>分鐘99</li>
<li>秒59</li>
<li>畫面格74</li>
</ul></td>
</tr>
<tr class="even">
<td>時間格式範例</td>
<td>將時間格式設定為範例。 在此命令之後，所有位置資訊都指定為範例。</td>
</tr>
<tr class="odd">
<td>時間格式 smpte 24<br/> 時間格式 smpte 25<br/> 時間格式 smpte 30<br/></td>
<td>將時間格式設定為 SMPTE 畫面播放速率。 若為 Vcr，請將時間格式設定為 hh： mm： ss： ff，其中合法的值為00:00:00:00 到23：59：59： xx，而 xx 則小於以旗標中指定的數位24、25或30所指定的每秒畫面格數。 在輸入時，冒號 (： ) 需要分隔元件。 若為00，則可以省略最不重要的單位;例如，02:00 與02:00:00:00 相同。 使用位置值的所有命令都會採用 SMPTE 格式。<br/> 順序檔會將預設格式設定為 PPQN 或 SMPTE。<br/></td>
</tr>
<tr class="even">
<td>時間格式 smpte 30 捨棄</td>
<td>將時間格式設定為 SMPTE 30 捨棄畫面播放速率。 針對 Vcr （與 SMPTE 30 相同），不同之處在于會從格式中卸載特定的時間碼位置，以將每個畫面格的記錄時間碼位置 (為 NTSC 畫面播放速率 29.97 fps) 對應至 30 fps) 的即時 (。 已卸載的時間碼位置如下：每分鐘的兩分鐘（每分鐘），針對記錄內容的每十分鐘的前九個。 例如，在01:04:59:29，下一個時間碼位置會是01:05:00:02，而不是01:05:00:00。 使用位置值的所有命令都會採用 SMPTE 格式。<br/> 順序檔會將預設格式設定為 PPQN 或 SMPTE。<br/></td>
</tr>
<tr class="odd">
<td>時間格式歌曲指標</td>
<td>將時間格式設定為歌曲指標， (第十六個附注) 。 所有使用位置值的命令都將採用歌曲指標單位。 此旗標只適用于一系列的除法類型 PPQN。</td>
</tr>
<tr class="even">
<td>時間格式 tmsf</td>
<td>設定要追蹤、分、秒和框架的時間格式。 所有使用位置值的命令都將採用 TMSF。 將 TMSF 值指定為 tt： mm： ss： ff，其中 tt 為曲目，mm 為分鐘，ss 為秒，而 ff 為框架。 如果欄位和下列所有欄位都為零，您可以省略欄位。 例如，3、3:0、3:0:0 和3:0:0:0 都是快速追蹤3的有效方式。 <br/> TMSF 欄位的最大值如下：<br/>
<ul>
<li>追蹤99</li>
<li>分鐘90</li>
<li>秒59</li>
<li>畫面格74</li>
</ul></td>
</tr>
<tr class="odd">
<td>時間格式追蹤</td>
<td>設定要追蹤的位置格式。 所有使用位置值的命令都將採用追蹤。</td>
</tr>
<tr class="even">
<td>時間模式計數器</td>
<td>設定位置資訊模式以使用 VCR 計數器。</td>
</tr>
<tr class="odd">
<td>偵測時間模式</td>
<td>根據磁帶上的時間碼資訊偵測來設定位置資訊模式。 如果偵測到時間碼資訊，則時間類型會設定為時間 &quot; 碼， &quot; 否則，時間類型會設定為 &quot; counter &quot; 。 &quot;偵測 &quot; 是一種特殊模式。 只要開啟驅動程式、插入新的磁帶，或 &quot; 發出時間模式 &quot; 命令，驅動程式就會檢查磁帶上目前可用的時間模式，並將 &quot; 時間類型設定 &quot; 為時間 &quot; 碼 &quot; 或 &quot; 計數器 &quot; 。 一旦 &quot; 設定時間類型之後 &quot; ，驅動程式就不會變更它，直到上述其中一個條件再次發生為止。<br/></td>
</tr>
<tr class="even">
<td>時間模式時間碼</td>
<td>設定位置資訊模式，以使用 &quot; &quot; 磁帶上的時間碼資訊。</td>
</tr>
<tr class="odd">
<td>追蹤加號 <br/> 追蹤減號 <br/> 追蹤重設 <br/></td>
<td>以精確的遞增方式調整磁帶傳輸的速度。 &quot; &quot; 從 VCR 取得有雜訊的圖片時，請使用追蹤旗標。 &quot;追蹤加號 &quot; 會增加傳送速率。 &quot;追蹤減號可 &quot; 減少傳送速率。 &quot;追蹤重設會 &quot; 將追蹤調整傳回零。</td>
</tr>
<tr class="even">
<td>關閉影片</td>
<td>停用影片輸出。</td>
</tr>
<tr class="odd">
<td>影片開啟</td>
<td>啟用影片輸出。</td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

可以是「等候」、「通知」或兩者。 針對數位影片和 VCR 裝置，也可以指定「測試」。 如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

在儲存資料的檔案建立時，會定義多個波形音訊資料的屬性。 這些屬性會描述如何在檔案中結構化資料，而且在錄製開始之後就無法變更。 下列清單會識別這些屬性：

-   對齊
-   bitspersample
-   bytespersec
-   通道
-   格式標記
-   samplespersec

## <a name="examples"></a>範例

下列命令會將時間格式設定為毫秒，並將波形-音訊格式設定為8位、mono、11 kHz。

``` syntax
set mysound time format ms bitspersample 8 channels 1 samplespersec 11025
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

[捕獲](capture.md)
</dt> <dt>

[pause](pause.md)
</dt> <dt>

[儲存](save.md)
</dt> <dt>

[停止](stop.md)
</dt> </dl>

 

