---
title: 若要逐行掃描影片
description: 若要逐行掃描影片
ms.assetid: 60e6af09-fde1-4e4a-b54c-4923c0549b6b
keywords:
- Windows Media Format SDK，deinterlaced 影片
- Windows Media Format SDK，反向電視
- Windows Media Format SDK，電影
- Advanced Systems Format (ASF) 、deinterlaced 影片
- ASF (Advanced Systems Format) 、deinterlaced video
- Advanced Systems Format (ASF) ，反向電視
- ASF (Advanced Systems Format) ，反向電視
- Advanced Systems Format (ASF) ，電影
- ASF (Advanced Systems Format) ，電影
- deinterlaced 影片
- 反向電視電影，關於
- 電影、關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 580b8425e5807fefdfa889fcd08deedb4143cf39
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023056"
---
# <a name="to-deinterlace-video"></a>若要逐行掃描影片

影片的某些來源（例如影片捕獲卡片）會傳遞影片資料以進行交錯顯示。 交錯影片的每個畫面格都是由兩個欄位所組成。 頂端欄位包含第一行影片和其後的每一行。 底部的欄位包含第二行的影片和其後的每一行。 其中一個欄位包含所有偶數行，另一個則包含所有奇數的行。 組成框架的欄位代表呈現時間稍微不同，因此在交錯時，它們不會形成靜態影像。

當您想要在電腦監視器上顯示影片時，影片的每個畫面格都應該顯示為一個影像 (此方法會一次顯示一個整個框架的影片，稱為「 *漸進式* 影片」。 ) 如果您以漸進方式顯示交錯的影片，則畫面格可能不會正確，因為這兩個欄位之間的時間差異。 Windows Media 視訊編解碼器和 Windows Media 視訊 Advanced Profile 編解碼器都支援將交錯式內容轉換成漸進式框架的前置處理功能。

若要讓編解碼器將輸入影片進行逐行掃描，請呼叫 [**IWMWriterAdvanced2：： SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) 方法。 要使用的設定為 g \_ wszDeinterlaceMode。 將去交錯模式設定為下列其中一個值。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>值</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WM_DM_NOTINTERLACED</td>
<td>輸入是漸進式的。 當您先前已將去交錯模式設定為另一個值時，請使用此設定來停止去交錯。</td>
</tr>
<tr class="even">
<td>WM_DM_DEINTERLACE_NORMAL</td>
<td>選取此模式以混合交錯框架的偶數和奇數位段， (使用運動補償機制) 。好處：<br/>
<ul>
<li>漸進顯示的交錯構件大幅減少。</li>
<li>Windows Media 視訊編解碼器會產生較高品質的壓縮影片。</li>
</ul></td>
</tr>
<tr class="odd">
<td>WM_DM_DEINTERLACE_HALFSIZE</td>
<td>當輸出解析度為輸入解析度的一半或更少時，請選取此模式。 例如，當輸入影片解析度為 640 x 480 圖元，且輸出視頻解析度為 320 x 240 圖元時，請使用此模式。好處：<br/>
<ul>
<li>漸進顯示的交錯構件大幅減少。</li>
</ul></td>
</tr>
<tr class="even">
<td>WM_DM_DEINTERLACE_HALFSIZEDOUBLERATE</td>
<td>當輸出解析度為輸入解析度的一半或更少時，請選取此模式，而且輸出 <a href="wmformat-glossary.md"><em>畫面播放速率</em></a> 會是高兩倍。 例如，當輸入影片解析度是 640 x 480 圖元（每秒30個交錯的框架/秒），且輸出影片解析度為 320 x 240 圖元（每秒的60畫面格）時，請使用此模式。好處：<br/>
<ul>
<li>這會產生高品質的漸進式框架，因為每個欄位都會轉換成框架，因此不需要 blend 任何資訊。</li>
<li>會捕獲交錯式欄位的完整動作。</li>
</ul></td>
</tr>
<tr class="odd">
<td>WM_DM_DEINTERLACE_INVERSETELECINE</td>
<td>選取此模式可將 telecined 30 個畫面/秒的影片轉換成原始電影的每秒24個畫面格。好處：<br/>
<ul>
<li>壓縮品質大幅改善，因為只需要編碼24個框架/秒，而不是每秒30個畫面格。</li>
<li>由於結果是漸進式的，因此會實現去交錯的相同壓縮和顯示優勢。</li>
</ul></td>
</tr>
<tr class="even">
<td>WM_DM_DEINTERLACE_VERTICALHALFSIZEDOUBLERATE</td>
<td>當垂直輸出解析度是輸入垂直解析度的一半或更少時，請選取此模式，而且輸出 <a href="wmformat-glossary.md"><em>畫面播放速率</em></a> 會是高兩倍。 例如，輸入垂直影片解析度是 640 x 480 圖元，每秒30個交錯的畫面格，輸出垂直影片解析度是 320 x 240 圖元，每秒畫面60。好處：<br/>
<ul>
<li>這會產生高品質的漸進式框架，因為每個欄位都會轉換成框架，因此不需要 blend 任何資訊。</li>
<li>會捕獲交錯式欄位的完整動作。</li>
</ul></td>
</tr>
</tbody>
</table>



 

針對混合內容，請在傳遞新類型的範例之前，視需要設定去交錯模式。 例如，若要以漸進式輸入開始編碼，您不需要設定任何去交錯模式。 如果某些範例接著需要一般去交錯，您必須將去交錯模式設定為 WM \_ DM 可進行 \_ 一般的交錯 \_ 。 若要處理其他漸進式範例，您必須將去交錯模式設定為 WM \_ DM \_ NOTINTERLACED。

## <a name="inverse-telecine-settings"></a>反向電影設定

如需反向電視電影的說明，請參閱 [使用反向電視電影](to-use-inverse-telecine.md)。

如果您將去交錯模式設定為 WM \_ DM \_ 交錯 \_ INVERSETELECINE，您可以藉由呼叫 [**IWMWriterAdvanced2：： SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting)，指定第一個輸入框架的電影模式。 要使用的設定為 g \_ wszInitialPatternForInverseTelecine。 將初始模式設定為下列其中一個值。



| 值                                              | 描述                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WM \_ DM \_ IT \_ 停用 \_ 一致 \_ 模式                | 指定輸入媒體已通過電視程式，但框架已不再處於可預測的模式。 這通常表示媒體是在電影處理之後編輯。 當您使用此設定時，編解碼器會嘗試自行重建原始框架。 |
| \_以 WM \_ 的 \_ 方式將第一個剪輯中的第一個 \_ 框架顯示 \_ \_ \_ 為 \_ AA \_ TOP    | 指定 AA 框架的頂端欄位是第一個範例。                                                                                                                                                                                                                                             |
| \_ \_ \_ 在剪輯中的第一幀第一個 \_ 框架 \_ \_ \_ 是 \_ BB \_ TOP    | 指定 BB 框架的頂端欄位是第一個範例。                                                                                                                                                                                                                                             |
| \_ \_ \_ 在剪輯中的第一幀 IT 第一個 \_ 框架 \_ \_ \_ 是 \_ BC \_ TOP    | 指定 BC 框架的頂端欄位是第一個範例。                                                                                                                                                                                                                                             |
| \_以 WM \_ 的 \_ 方式將第一個剪輯中的第一個 \_ 框架 \_ \_ 放在 \_ \_ \_ 最上層    | 指定 CD 框架的頂端欄位是第一個範例。                                                                                                                                                                                                                                             |
| \_以 WM \_ 的 \_ \_ 方式將剪輯第一個框架中的第一個框架 \_ \_ \_ 作為 \_ DD \_ TOP    | 指定 DD 框架的頂端欄位是第一個範例。                                                                                                                                                                                                                                             |
| WM \_ DM \_ IT \_ 第一個 \_ 框架 \_ 在 \_ 剪輯中 \_ 是 \_ AA \_ 底部 | 指定 AA 框架的底部欄位是第一個範例。                                                                                                                                                                                                                                          |
| \_ \_ \_ \_ 在剪輯中，WM 的第一個框架 \_ \_ \_ 是 \_ BB \_ 底端 | 指定 BB 框架的底端欄位是第一個範例。                                                                                                                                                                                                                                          |
| \_以 WM \_ \_ \_ 為範圍的第一個剪輯第一個框架 \_ \_ \_ 是 \_ BC \_ 底部 | 指定 BC 框架的底部欄位是第一個範例。                                                                                                                                                                                                                                          |
| \_以 WM \_ 的 \_ \_ 方式將剪輯第一個框架的第一個框架 \_ \_ 放在 \_ \_ 光碟上 \_ | 指定 CD 框架的底部欄位是第一個範例。                                                                                                                                                                                                                                          |
| \_以 WM \_ 的 \_ \_ 方式將剪輯第一個框架中的第一個框架 \_ \_ \_ 作為 \_ DD \_ 底部 | 指定 DD 框架的下半部欄位是第一個範例。                                                                                                                                                                                                                                          |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Advanced 主題**](advanced-topics.md)
</dt> </dl>

 

 





