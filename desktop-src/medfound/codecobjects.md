---
description: 編解碼器物件
ms.assetid: c944e5df-c375-4bad-92dc-bb3d8c09b1b3
title: 編解碼器物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3a4f140c81f162aaee2ffc416ed1de96dfcb470
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689352"
---
# <a name="codec-objects"></a>編解碼器物件

本節說明 Microsoft 媒體基礎中支援的編碼器和解碼器。 此章節包含下列主題。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>主題</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="aac-decoder.md"><strong>AAC 解碼器</strong></a></td>
<td>音訊解碼器，可將下列高階音訊編碼編碼 (AAC) 和高效率 AAC (AAC) 設定檔：
<ul>
<li>MPEG-2 AAC 低複雜度 (LC) 設定檔 (多重通道) 。</li>
<li>MPEG-2 AAC v1 (多重通道) 搭配 AAC-LC 核心。</li>
<li>使用 AAC-LC 核心的 MPEG-2 AAC v2 (身歷聲) 。</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="aac-encoder.md"><strong>AAC 編碼器</strong></a></td>
<td>編碼 Advanced Audio 編碼 (AAC) 低複雜度 (LC) 設定檔的音訊編碼器。</td>
</tr>
<tr class="odd">
<td><a href="dv-video-decoder.md"><strong>DV 影片解碼</strong></a></td>
<td>解碼 DV 影片的視頻解碼器。</td>
</tr>
<tr class="even">
<td><a href="h-264-video-decoder.md"><strong>H.264 Video 解碼</strong></a></td>
<td>解碼 h.264 video 的視頻解碼器。 它支援解碼基準、主要和高設定檔，最多可達層級5.1。</td>
</tr>
<tr class="odd">
<td><a href="h-264-video-encoder.md"><strong>H.264 影片編碼器</strong></a></td>
<td>編碼 h.264 影片的視頻編碼器。 它支援下列 h.264 設定檔：
<ul>
<li>基準設定檔</li>
<li>主要設定檔</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="h-264-video-decoder.md"><strong>H. 265/HEVC 影片解碼器</strong></a></td>
<td>支援以附錄 B 格式解碼 H. 265/HEVC 內容的視頻解碼器，可用於播放數量和 .m2ts 檔案。 它支援下列 h.264 設定檔：
<ul>
<li>主要設定檔</li>
<li>主要10設定檔</li>
<li>主要還是圖片</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="h-264-video-encoder.md"><strong>H. 265/HEVC 影片編碼器</strong></a></td>
<td>編碼 H 265/HEVC 格式的影片編碼器。 它支援下列 .H 設定檔：
<ul>
<li>主要設定檔</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="mpeg4part2videodecoder.md"><strong>MPEG4 第2部分影片解碼</strong></a></td>
<td>MPEG-2 第2部分影片解碼器。</td>
</tr>
<tr class="odd">
<td><a href="windowsmediaaudiodecoder.md"><strong>Windows Media 音訊的解碼器</strong></a></td>
<td>解碼 Windows Media 音訊編碼器所編碼之資料流程的解碼器。</td>
</tr>
<tr class="even">
<td><a href="windowsmediaaudioencoder.md">Windows Media 音訊編碼器</a></td>
<td>支援三種編碼輸出類別的音訊編碼器：
<ul>
<li>標準</li>
<li>Professional</li>
<li>Lossless</li>
</ul>
標準類別適用于一般用途的音訊編碼。 Professional 類別目錄適用于編碼多重通道或高定義音訊。 無失真類別是用來壓縮音訊，而不會遺失任何原始資料。</td>
</tr>
<tr class="odd">
<td><a href="windowsmediaaudiovoicedecoder.md"><strong>Windows Media 音訊語音解碼器</strong></a></td>
<td>解碼 Windows Media 音訊聲音編碼程式所編碼之資料流程的解碼器。</td>
</tr>
<tr class="even">
<td><a href="windowsmediaaudiovoiceencoder.md">Windows Media 音訊語音編碼器</a></td>
<td>編碼音訊的編碼器，其中包含大部分的語音。</td>
</tr>
<tr class="odd">
<td><a href="windows-media-mp3-decoder.md"><strong>Windows Media MP3 解碼</strong></a></td>
<td>解碼下列音訊格式的音訊解碼器。
<ul>
<li>ISO/IEC 11172-3 (MPEG 1 音訊) 第3層</li>
<li>ISO/IEC 13818-3 (MPEG-2 音訊) 第3層，低取樣頻率延伸</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="windowsmediampeg4decoder.md"><strong>Windows Media MPEG4 V1/V2 解碼器</strong></a></td>
<td>可執行 MPEG 4 V1/V2 影片解碼的解碼器。</td>
</tr>
<tr class="odd">
<td><a href="windows-media-video-7-and-8-encoders.md"><strong>Windows Media 視訊7/8 編碼器</strong></a></td>
<td>可執行舊版 Windows Media 視訊編碼器的影片編碼器。</td>
</tr>
<tr class="even">
<td><a href="windowsmediavideo9decoder.md">Windows Media 視訊9解碼器</a></td>
<td>可解碼 Windows Media 視訊9編碼器編碼之資料流程的視頻編碼器。</td>
</tr>
<tr class="odd">
<td><a href="windowsmediavideo9encoder.md">Windows Media 視訊9編碼器</a></td>
<td>支援三種 endoded 輸出類別的影片編碼器：
<ul>
<li>Windows Media 視訊9</li>
<li>Windows Media 視訊 9 Advanced Profile</li>
<li>Windows Media 視訊9.1 影像</li>
</ul>
Windows Media 視訊9類別適用于一般用途的影片編碼。 「高階設定檔」類別適用于編碼符合 VC 1 Advanced Profile SMPTE 標準的高定義影片或影片。 影像類別目錄是用來將點陣圖影像轉換成動態影片。</td>
</tr>
<tr class="even">
<td><a href="windowsmediavideo9screendecoder.md"><strong>Windows Media 視訊9螢幕解碼</strong></a></td>
<td>解碼 Windows Media 視訊9螢幕編碼器所編碼之資料流程的解碼器。</td>
</tr>
<tr class="odd">
<td><a href="windowsmediavideo9screenencoder.md"><strong>Windows Media 視訊9螢幕編碼器</strong></a></td>
<td>編碼電腦的編碼程式影片 (螢幕擷取畫面) 或其他高度靜態的影片。</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎程式設計參考](media-foundation-programming-reference.md)
</dt> <dt>

[媒體基礎中支援的媒體格式](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 



