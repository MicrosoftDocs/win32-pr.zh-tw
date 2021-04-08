---
title: 支援的編解碼器
description: 支援的編解碼器
ms.assetid: d5907d38-2e26-442e-a0d1-1d7e267b9948
keywords:
- Windows Media Format SDK，支援編解碼器
- Windows Media Format SDK，IWMCodecInfo3 介面
- 編解碼器，支援
- IWMCodecInfo3，關於
- 編解碼器，IWMCodecInfo3 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5ac06ad3d58d066254fa666f96283dca9b8b6ae
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103681431"
---
# <a name="supported-codecs"></a>支援的編解碼器

Windows Media Format SDK 提供下列編解碼器的支援，這些編解碼器會在您安裝 SDK 時包含。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>轉碼器</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows Media 音訊</td>
<td>音訊編解碼器，適用于編碼複雜音訊的一般用途，像是音樂。此編解碼器的最新版本是 Windows Media 音訊9編解碼器和 Windows Media 音訊9.1 編解碼器。<br/></td>
</tr>
<tr class="even">
<td>Windows Media 音訊專業人員</td>
<td>複雜音訊的音訊編解碼器，像是音樂。 支援多重通道和24位編碼。此編解碼器有兩種版本：<br/>
<ul>
<li>Windows Media 音訊9專業版</li>
<li>Windows Media 音訊9.1 專業版</li>
</ul></td>
</tr>
<tr class="odd">
<td>Windows Media 音訊無損</td>
<td>無失真編碼的音訊編解碼器。此編解碼器有兩種版本：<br/>
<ul>
<li>Windows Media 音訊9無損</li>
<li>Windows Media 音訊9.1 無損</li>
</ul></td>
</tr>
<tr class="even">
<td>Windows Media 音訊9語音</td>
<td>針對以高壓縮率編碼人類聲音而優化的音訊編解碼器。 這是最常用於串流的串流編解碼器。 針對混合音樂和語音的內容，此編解碼器可以動態變更用來取得最佳品質的編碼演算法。</td>
</tr>
<tr class="odd">
<td>Windows Media 視訊9</td>
<td>適用于編碼複雜影片（例如電影）的一般使用的影片編解碼器。</td>
</tr>
<tr class="even">
<td>Windows Media 視訊 9 Advanced Profile</td>
<td>影片編解碼器包含先進的編碼功能，包括交錯編碼。</td>
</tr>
<tr class="odd">
<td>Windows Media 視訊9螢幕</td>
<td>針對編碼順序螢幕擷取畫面優化的影片編解碼器。 此編解碼器通常用於軟體訓練或支援，方法是使用電腦應用程式錄製監視器映射。</td>
</tr>
<tr class="even">
<td>Windows Media 視訊映射</td>
<td>將點陣圖影像轉換成壓縮影片的影片編解碼器。此編解碼器有兩種版本：<br/>
<ul>
<li>Windows Media 視訊9映射</li>
<li>Windows Media 視訊9映射 v2</li>
</ul></td>
</tr>
</tbody>
</table>



 

您可以根據所安裝的 Windows Media 格式 SDK 版本，使用不同版本的 Windows Media 音訊和影片編解碼器進行編碼。 當您使用方法來列舉編解碼器和編解碼器格式的 [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) 介面時，只會列舉最新支援的版本。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**選擇編碼方法**](choosing-an-encoding-method.md)
</dt> <dt>

[**編解碼器功能**](codec-features.md)
</dt> </dl>

 

 





