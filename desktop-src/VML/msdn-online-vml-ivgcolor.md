---
title: VML IVgColor
description: VML IVgColor
ms.assetid: 6121c5bf-1969-4402-9f45-8891a1538fea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97093d9e9315db1389c71db7e8e21fdbf640353c95c5cf11f607c708e1679166
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118599513"
---
# <a name="vml-ivgcolor"></a>VML IVgColor

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

指定色彩。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>屬性</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>String</td>
<td>字串。 色彩的文字標記法。 以下是支援的命名色彩類型：
<ul>
<li>黑色 (#000000) </li>
<li>銀級 (#C0C0C0) </li>
<li>灰色 (#808080) </li>
<li>白色 (#FFFFFF) </li>
<li> (#800000) 的暗紫紅色</li>
<li>紅色 (#FF0000) </li>
<li>紫色 (#800080) </li>
<li>Fuchsia (#FF00FF) </li>
<li>綠色 (#008000) </li>
<li> (#00FF00) 的橙色</li>
<li>) 的橄欖綠 (#808000</li>
<li>黃色 (#FFFF00) </li>
<li>Navy (#000080) </li>
<li>藍色 (#0000FF) </li>
<li>青色 (#008080) </li>
<li>綠色 (#00FFFF) </li>
</ul></td>
</tr>
<tr class="even">
<td>類型</td>
<td>VgColorType. 色彩的類型。 下列其中一種類型：
<ul>
<li>Mixed</li>
<li>RGB</li>
<li>配置</li>
<li>已命名</li>
</ul></td>
</tr>
<tr class="odd">
<td>RGB</td>
<td>VgRGBType. RGB 值 (色彩的 <strong>長</strong>) 。 只有當類型為 RGB 時才有效 &quot; <strong></strong> &quot; 。</td>
</tr>
<tr class="even">
<td>R</td>
<td><strong>Integer</strong> (整數)。 色彩的紅色元件。 的範圍可以介於0到255之間。</td>
</tr>
<tr class="odd">
<td>G</td>
<td><strong>Integer</strong> (整數)。 色彩的綠色元件。 的範圍可以介於0到255之間。</td>
</tr>
<tr class="even">
<td>B</td>
<td><strong>Integer</strong> (整數)。 色彩的藍色元件。 的範圍可以介於0到255之間。</td>
</tr>
</tbody>
</table>



 

 

 