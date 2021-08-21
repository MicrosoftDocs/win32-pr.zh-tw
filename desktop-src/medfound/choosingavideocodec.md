---
description: 選擇影片編解碼器
ms.assetid: 3a4b925a-4fb4-4189-a571-8083454fed0e
title: '選擇影片編解碼器 (Microsoft 媒體基礎) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b560666ddeebb88fc3bb720cbc9f1be26308e7ecd8a4ad872fbb1f0991826fe2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035366"
---
# <a name="choosing-a-video-codec-microsoft-media-foundation"></a>選擇影片編解碼器 (Microsoft 媒體基礎) 

Windows Media 視訊9編碼器支援三種編碼輸出類別：主要設定檔、Advanced profile 和 Image。 主要設定檔類別提供複雜影片內容的一般影片壓縮，例如電影或音樂影片。 主要設定檔的功能提供各式各樣的編碼設定。 您可以使用主要設定檔以非常低的位元速率來建立可在掌上型裝置上傳遞的影片，或在色譜的另一端使用它來建立數位影院的高定義影片。

主要設定檔中編碼演算法的重點在於動態影片內容，但也適用于其他影片內容。 主要設定檔應該是影片內容的預設類別。 若要符合特定需求，您可以使用 Advanced Profile 類別、影像類別或個別的編碼器，稱為 Windows Media 視訊9螢幕編碼器。 下表列出四個選項。



<table>
<thead>
<tr class="header">
<th>目的</th>
<th>轉碼器</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>一般用途的影片編碼</td>
<td><a href="windowsmediavideo9encoder.md">WindowsMedia Video 9 編碼器</a><dl> 主要設定檔<br />
</dl></td>
</tr>
<tr class="even">
<td>編碼符合 VC 1 Advanced Profile SMPTE 標準的高定義影片或影片</td>
<td><a href="windowsmediavideo9encoder.md">WindowsMedia Video 9 編碼器</a><dl> Advanced Profile<br />
</dl></td>
</tr>
<tr class="odd">
<td>將點陣圖影像轉換成動態影片</td>
<td><a href="windowsmediavideo9encoder.md">WindowsMedia Video 9 編碼器</a><dl> 映像<br />
</dl></td>
</tr>
<tr class="even">
<td>編碼電腦-應用程式影片 (螢幕擷取畫面) 或其他高度靜態的影片</td>
<td><a href="windowsmediavideo9screenencoder.md"><strong>WindowsMedia Video 9 螢幕編碼器</strong></a></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用影片](workingwithvideo.md)
</dt> </dl>

 

 



