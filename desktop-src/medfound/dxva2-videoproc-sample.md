---
description: 說明如何使用 DXVA 影片處理。
ms.assetid: 1465bd41-94f9-4e19-8236-00e7a2d6f54a
title: DXVA2_VideoProc 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8497a241baf07b76148a5bc2e7ddb4dd5e878e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317975"
---
# <a name="dxva2_videoproc-sample"></a>DXVA2 \_ VideoProc 範例

說明如何使用 [DXVA 影片處理](dxva-video-processing.md)。

此範例會以程式設計方式產生具有主要資料流程和子資料流程的影片。 主要資料流程會顯示 SMPTE 色軸，而子資料流程是半透明的矩形。 接著會使用 DXVA 視頻處理器來處理並顯示影片。 使用者可以變更平面 Alpha 值、來源和目的地矩形、色彩調整和色彩空間。

![dxva2 videoproc 範例的螢幕擷取畫面 \-](images/dxva2-videoproc.png)

## <a name="apis-demonstrated"></a>示範的 Api

這個範例會示範下列 DXVA 介面：

-   [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice)
-   [**IDirectXVideoProcessor**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor)

## <a name="usage"></a>使用方式

DXVA2 \_ VideoProc 範例會建立 Windows 應用程式。

命令列選項：



| 選項 | Description                                                                          |
|--------|--------------------------------------------------------------------------------------|
| -hh    | 強制應用程式使用硬體 Direct3D 裝置和硬體 DXVA 裝置。 |
| -hs    | 強制應用程式使用硬體 Direct3D 裝置和軟體 DXVA 裝置。 |
| -ss    | 強制應用程式使用軟體 Direct3D 裝置和軟體 DXVA 裝置。 |



 

鍵盤命令：



| Key       | 描述                                             |
|-----------|---------------------------------------------------------|
| ALT+ENTER | 切換視窗模式和全螢幕模式。      |
| F1 – F8     | 輸入下表所示的其中一個模式。    |
| END       | 啟用或停用已卸載框架的偵錯工具記錄。 |
| HOME      | 將參數重設為其初始值。                 |



 

每個函式按鍵 F1 到 F8 都會切換至模式，以使用方向鍵來調整特定轉譯參數。 此外，子流的色彩也會變更。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Key</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>F1</td>
<td>調整 Alpha 值。<br/>
<ul>
<li>向上：增加兩個數據流的平面 Alpha。</li>
<li>向下：減少這兩個數據流的平面 Alpha。</li>
<li>RIGHT：增加子流的圖元 Alpha。</li>
<li>左方：減少子流的圖元 Alpha。</li>
</ul>
子流色彩：白色<br/></td>
</tr>
<tr class="even">
<td>F2</td>
<td>調整主要資料流程的來源區域 (縮放) 。<br/>
<ul>
<li>向上：提高) 的垂直 (放大。</li>
<li>下：減少垂直 (縮小) 。</li>
<li>RIGHT：水準增加 (放大) 。</li>
<li>左方：減少水準 (放大) 。</li>
</ul>
子流色彩：紅色<br/></td>
</tr>
<tr class="odd">
<td>F3</td>
<td>移動主要資料流程的來源區域。<br/>
<ul>
<li>向上：向上移動。</li>
<li>向下：下移。</li>
<li>RIGHT：右移。</li>
<li>左方：左移。</li>
</ul>
子流色彩：黃色<br/></td>
</tr>
<tr class="even">
<td>F4</td>
<td>調整主要資料流程的目的地區域。<br/>
<ul>
<li>向上：垂直增加。</li>
<li>向下：垂直減少。</li>
<li>RIGHT：水準增加。</li>
<li>左方：水準減少。</li>
</ul>
子流色彩：綠色<br/></td>
</tr>
<tr class="odd">
<td>F5</td>
<td>移動主要資料流程的目的地區域。<br/>
<ul>
<li>向上：向上移動。</li>
<li>向下：下移。</li>
<li>RIGHT：右移。</li>
<li>左方：左移。</li>
</ul>
子流色彩：青色<br/></td>
</tr>
<tr class="even">
<td>F6</td>
<td>變更背景色彩或色彩空間。<br/>
<ul>
<li>向上、向下：迴圈顯示色彩空間。</li>
<li>靠右、靠左：迴圈顯示背景色彩。</li>
</ul>
子流色彩：藍色<br/></td>
</tr>
<tr class="odd">
<td>F7</td>
<td>調整亮度和對比。<br/>
<ul>
<li>向上：提高亮度。</li>
<li>減少：降低亮度。</li>
<li>RIGHT：提高對比。</li>
<li>左方：減少對比。</li>
</ul>
子流色彩：洋紅<br/></td>
</tr>
<tr class="even">
<td>F8</td>
<td>調整色調和飽和度。<br/>
<ul>
<li>向上：提高色調。</li>
<li>DOWN：減少色調。</li>
<li>RIGHT：提高飽和度。</li>
<li>左方：減少飽和度。</li>
</ul>
子流色彩：黑色<br/></td>
</tr>
</tbody>
</table>



 

在每個模式中，按 HOME 鍵會將該模式的參數重設為其初始值。

## <a name="requirements"></a>規格需求



| 產品                                                        | 版本   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>下載範例

此範例可在 [Windows 傳統範例 github 存放庫](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/evrpresenter)中取得。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectX Video 加速2。0](directx-video-acceleration-2-0.md)
</dt> <dt>

[DXVA 影片處理](dxva-video-processing.md)
</dt> <dt>

[媒體基礎 SDK 範例](media-foundation-sdk-samples.md)
</dt> </dl>

 

 




