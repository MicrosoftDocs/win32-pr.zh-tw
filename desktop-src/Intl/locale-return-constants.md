---
description: 地區設定傳回 \_ \* 常數
ms.assetid: c6aadf84-c597-4cbd-a715-b68325ce5117
title: LOCALE_RETURN * 常數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83d3e5017a6463457b7bc36358e9956365430c3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194548"
---
# <a name="locale_return-constants"></a>地區設定傳回 \_ \* 常數

本主題定義 NLS 所使用的地區設定傳回 \_ \* 常數。



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
<td>LOCALE_RETURN_GENITIVE_NAMES</td>
<td><strong>Windows 7 和更新版本：</strong> 取出月份的所有格名稱，這些名稱是月份名稱與其他專案合併時所使用的名稱。 例如，在「烏克蘭」中， &quot; &quot; 當月份單獨命名時，會將相當於1月的Січень寫入。 不過，當月份名稱用於組合時（例如，在2003年1月5日的日期）中，會使用名稱的所有格形式。 針對烏克蘭範例，所有格月份名稱會顯示為 &quot; 5 січня 2003 &quot; 。 所有格月份名稱的清單會從1月開始，並以分號分隔。 如果沒有13個月，請在清單結尾使用分號。
<blockquote>
[!Note]<br />
所有語言都不會有所有格的月份名稱。
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td>LOCALE_RETURN_NUMBER</td>
<td><strong>Windows Me/98、Windows NT 4.0 和更新版本：</strong> 取出數位。 這個常數會造成 <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa"><strong>GetLocaleInfo</strong></a> 或 <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex"><strong>GetLocaleInfoEx</strong></a> 以數位形式（而不是字串）來取出值。 接收值的緩衝區必須至少為 DWORD 值的長度。 這個常數可以與名稱開頭為 LOCALE_I 的任何其他常數合併 &quot; &quot; 。</td>
</tr>
</tbody>
</table>



 

 

 




