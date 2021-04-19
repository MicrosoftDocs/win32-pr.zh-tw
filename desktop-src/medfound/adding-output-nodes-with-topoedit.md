---
description: 使用 TopoEdit 新增輸出節點
ms.assetid: 23d60fc7-547b-4ef5-b334-5f1b38e58e92
title: 使用 TopoEdit 新增輸出節點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a84dc30631332e8138b35e4bbc0ccde75ec9b0cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970411"
---
# <a name="adding-output-nodes-with-topoedit"></a>使用 TopoEdit 新增輸出節點

在拓撲中，輸出節點代表從轉換節點接收媒體資料並呈現播放的媒體接收。 輸出節點的類型取決於來源節點的媒體類型。

下表顯示將輸出節點加入拓撲的功能表/工具列命令。



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>來源媒體類型</th>
<th>功能表/工具列命令</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>音訊資料流</td>
<td>在 [ <strong>拓撲</strong> ] 功能表上，按一下 [ <strong>新增 SAR</strong>]。</td>
<td>建立串流音訊轉譯器的輸出節點， (SAR) 透過音訊裝置（例如音效卡）播放音訊串流。</td>
</tr>
<tr class="even">
<td>影片串流</td>
<td>在 [ <strong>拓撲</strong> ] 功能表上，按一下 [ <strong>新增 EVR</strong>]。</td>
<td>建立增強型影片轉譯器的輸出節點 (EVR) ，以顯示影片串流的畫面格。</td>
</tr>
<tr class="odd">
<td>自訂媒體接收</td>
<td><ol>
<li>在 [ <strong>拓撲</strong> ] 功能表上，按一下 [ <strong>新增自訂接收</strong>]。<br/> [ <strong>輸入自訂 GUID</strong> ] 對話方塊隨即開啟。<br/></li>
<li><p>在 [ <strong>GUID：</strong> ] 欄位中，輸入您要新增至拓撲的自訂接收的 GUID。<br/></p>
<blockquote>
[!Note]<br />
TopoEdit 預期格式應為 &quot; {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} 的 GUID &quot; 。 否則，它無法新增節點，並顯示不正確 &quot; GUID &quot; 錯誤訊息。
</blockquote>
<p><br/></p></li>
<li>按一下 [確定]  。<br/></li>
</ol></td>
<td>為自訂媒體來源的資料流程接收建立輸出節點。<br/> 自訂接收必須支援 <strong>CoCreateInstance</strong> ，才能以 CLSID 指定接收。<br/></td>
</tr>
</tbody>
</table>



 

TopoEdit 會建立指定的輸出節點。 [ **拓撲] 窗格** 會將輸出節點顯示為顯示資料流程接收名稱的綠色方塊。

如需使用媒體基礎 Api 以程式設計方式加入輸出節點的詳細資訊，請參閱 [建立輸出節點](creating-output-nodes.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 TopoEdit 建立拓撲](building-topologies-by-using-topoedit.md)
</dt> <dt>

[串流音訊轉譯器](streaming-audio-renderer.md)
</dt> <dt>

[增強的影片轉譯器](enhanced-video-renderer.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 




