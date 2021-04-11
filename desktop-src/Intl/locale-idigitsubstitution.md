---
description: 地區設定 \_ IDIGITSUBSTITUTION
ms.assetid: f3f7d7ac-8f1e-4bfa-84f0-dfe8cff568c3
title: LOCALE_IDIGITSUBSTITUTION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c063ed5b937c3e4c4ae06e40631b9795f6a73ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112001"
---
# <a name="locale_idigitsubstitution"></a>地區設定 \_ IDIGITSUBSTITUTION

**Windows 2000：** 數位的形狀。 例如，阿拉伯文、泰文和印度數位具有與歐洲數位不同的傳統圖形。 如果地區設定 [ \_ SNATIVEDIGITS](locale-snative-constants.md) 指定為 ASCII 0-9 以外的值，此值會指定是否應將喜好設定提供給其他數位，以供顯示之用。 例如，如果選擇的值為2，則一律會使用地區設定 SNATIVEDIGITS 所指定的位數 \_ 。 如果選擇1，一律會使用 ASCII 0-9 位數。 如果選擇0，則會在某些情況下使用 ASCII，並在其他情況下使用地區設定 SNATIVEDIGITS 所指定的位數 \_ （視內容而定）。



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
<td>0</td>
<td>以內容為基礎的替代。 會根據相同輸出中先前的文字來顯示數位。 歐洲數位遵循拉丁腳本、Arabic-Indic 位數遵循阿拉伯文文字，而其他國家/地區則遵循其他腳本中所撰寫的文字。 如果沒有上述文字，地區設定和顯示的讀取順序會決定數位替代，如下表所示。
<table>
<thead>
<tr class="header">
<th>Locale</th>
<th>讀取順序</th>
<th>使用的數位</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>阿拉伯文</td>
<td>由右至左</td>
<td>阿拉伯文印度語系</td>
</tr>
<tr class="even">
<td>泰文</td>
<td>從左至右</td>
<td>泰文數位</td>
</tr>
<tr class="odd">
<td>All others</td>
<td>任意</td>
<td>未使用任何替代</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>1</td>
<td>未使用任何替代。 完整的 Unicode 相容性。</td>
</tr>
<tr class="odd">
<td>2</td>
<td>原生位數的替代。 國家（地區）圖形會根據 LOCALE_SNATIVEDIGITS 來顯示。</td>
</tr>
</tbody>
</table>



 

 

 



