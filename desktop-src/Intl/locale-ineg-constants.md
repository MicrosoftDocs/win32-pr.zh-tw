---
description: 本主題定義 NLS 所使用的地區設定 \_ INEG \* 常數。
ms.assetid: 3a1e4a63-31bd-4ff9-a3ca-af357389e179
title: LOCALE_INEG * 常數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b17c61f0ca769206f30b84aa73cc3548ad9b915
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318572"
---
# <a name="locale_ineg-constants"></a>地區設定 \_ INEG \* 常數

本主題定義 NLS 所使用的地區設定 \_ INEG \* 常數。



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
<td>LOCALE_INEGCURR</td>
<td>負貨幣模式。 
<table>
<thead>
<tr class="header">
<th>模式</th>
<th>負貨幣的格式</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0</td>
<td>左括弧、貨幣符號、數位、右括弧;例如， ($1.1) </td>
</tr>
<tr class="even">
<td>1</td>
<td>負號、貨幣符號、數位;例如，-$1。1</td>
</tr>
<tr class="odd">
<td>2</td>
<td>貨幣符號、負號、數位;例如，$-1。1</td>
</tr>
<tr class="even">
<td>3</td>
<td>貨幣符號、數位、負號;例如，$1.1-</td>
</tr>
<tr class="odd">
<td>4</td>
<td>左括弧、數位、貨幣符號、右括弧;例如， ($1.1) </td>
</tr>
<tr class="even">
<td>5</td>
<td>負號、數位、貨幣符號;例如，-$1。1</td>
</tr>
<tr class="odd">
<td>6</td>
<td>數位、負號、貨幣符號;例如，1.1-$</td>
</tr>
<tr class="even">
<td>7</td>
<td>數位、貨幣符號、負號;例如，$1.1-</td>
</tr>
<tr class="odd">
<td>8</td>
<td>負號、數位、空格、貨幣符號 (例如 #5，但貨幣符號前面有一個空格) ;例如，-$1。1</td>
</tr>
<tr class="even">
<td>9</td>
<td>負號、貨幣符號、空間、數位 (例如 #1，但貨幣符號後面有一個空格) ;例如，-$1。1</td>
</tr>
<tr class="odd">
<td>10</td>
<td>數位、空格、貨幣符號、負號 (例如 #7，但貨幣符號前面有一個空格) ;例如，$1.1-</td>
</tr>
<tr class="even">
<td>11</td>
<td>貨幣符號、空格、數位、負號 (例如 #3，但貨幣符號後面有一個空格) ;例如，$1.1-</td>
</tr>
<tr class="odd">
<td>12</td>
<td>貨幣符號、空格、負號、數位 (例如 #2，但貨幣符號後面有一個空格) ;例如，$-1。1</td>
</tr>
<tr class="even">
<td>13</td>
<td>數位、負號、空間、貨幣符號 (例如 #6，但貨幣符號前面有一個空格) ;例如，1.1-$</td>
</tr>
<tr class="odd">
<td>14</td>
<td>左括弧、貨幣符號、空格、數位、右括弧 (例如 #0，但貨幣符號後面有一個空格) ;例如， ($1.1) </td>
</tr>
<tr class="even">
<td>15</td>
<td>左括弧、數位、空格、貨幣符號、右括弧 (例如 #4，但貨幣符號前面有一個空格) ;例如， ($1.1) </td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>LOCALE_INEGNUMBER</td>
<td>負數位模式，也就是負數的格式。 
<table>
<thead>
<tr class="header">
<th>值</th>
<th>格式</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0</td>
<td>左括弧、數位、右括弧;例如， (1.1) </td>
</tr>
<tr class="even">
<td>1</td>
<td>負號、數位;例如，-1。1</td>
</tr>
<tr class="odd">
<td>2</td>
<td>負號、空格、數位;例如，-1。1</td>
</tr>
<tr class="even">
<td>3</td>
<td>數位、負號;例如，1.1-</td>
</tr>
<tr class="odd">
<td>4</td>
<td>數位、空格、負號;例如，1.1-</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>LOCALE_INEGSEPBYSPACE</td>
<td>將負號分隔為貨幣值。 如果貨幣符號是以負金額的空格分隔，則這個值為1，否則為0。</td>
</tr>
<tr class="even">
<td>LOCALE_INEGSIGNPOSN</td>
<td>為貨幣值的負號設定索引格式。 
<table>
<thead>
<tr class="header">
<th>值</th>
<th>意義</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0</td>
<td>以括弧括住數量和貨幣符號。</td>
</tr>
<tr class="even">
<td>1</td>
<td>正負號在數位前面。</td>
</tr>
<tr class="odd">
<td>2</td>
<td>符號會遵循數位。</td>
</tr>
<tr class="even">
<td>3</td>
<td>符號會在貨幣符號之前。</td>
</tr>
<tr class="odd">
<td>4</td>
<td>符號後面接著貨幣符號。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>LOCALE_INEGSYMPRECEDES</td>
<td>貨幣符號的位置（負值貨幣值）。 如果貨幣符號在負值的正上方，則此值為1，如果符號符合該數量，則為0。</td>
</tr>
</tbody>
</table>



 

 

 



