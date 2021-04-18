---
description: 許多 factoids 描述所有語言辨識器通用的輸入，且不需要針對不同的語言使用不同的格式。 下表列出所有語言之間的通用 factoids。
ms.assetid: dae4a28d-0332-4bb2-b040-13a959c7945e
title: 跨語言的通用 Factoids
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1faefbb9991562535f711f867c45bd614c595941
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971235"
---
# <a name="factoids-common-across-languages"></a>跨語言的通用 Factoids

許多 factoids 描述所有語言辨識器通用的輸入，且不需要針對不同的語言使用不同的格式。 下表列出所有語言之間的通用 factoids。



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>標記</th>
<th>定義</th>
<th>範例</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>數位</strong></td>
<td>設定單一數位的偏差。 辨識器在設定此模擬項時，會偏向只傳回單一位數。<br/></td>
<td>0-9<br/></td>
</tr>
<tr class="even">
<td><strong>電子郵件</strong></td>
<td>設定電子郵件地址的偏差。<br/></td>
<td>someone@example.com<br/></td>
</tr>
<tr class="odd">
<td><strong>Web</strong></td>
<td>設定各種 URL 格式的偏差。<br/>
<blockquote>
[!Note]<br />
辨識器的預設設定包括 <strong>Web</strong> 模擬程式。 因此，您可能不會注意到 <strong>Web</strong> 模擬程式和預設設定之間有很大的差異。 不過， <strong>網路</strong> 模擬可協助消除 URL 中的單字之間的空格。
</blockquote>
<br/></td>
<td>HTTP： \\ microsoft.net<br/> https://microsoft.us/<br/> HTTPs： \\ www.microsoft.au \<br/> https://microsoft.com<br/> www.microsoft_world .com<br/> www.microsoft.us \<br/> HTTP： \\www.microsoft.com\myfile.htm<br/> HTTP： \\www.microsoft.com\myfile.html<br/> HTTP： \\ www. com\myfile.asp<br/> HTTP： \\ www.microsoft.uk<br/> HTTP： \\ www.microsoft.info<br/> www.microsoft.biz<br/></td>
</tr>
<tr class="even">
<td><strong>預設值</strong></td>
<td>將辨識器傳回到其預設設定。<br/></td>
<td>西方語言的 factoids 預設設定包括系統字典、使用者字典、各種標點符號，以及 <strong>Web</strong> 和 <strong>數位</strong> factoids。<br/> 東亞語言的 factoids 預設設定包含辨識器支援的所有字元。<br/></td>
</tr>
<tr class="odd">
<td><strong>None</strong></td>
<td>停用所有 factoids、字典和語言模型。<br/></td>
<td>只有當您不希望辨識器使用任何文法規則或字典（包括系統字典）時，才應該使用此模擬。 這項模擬適用于輸入隨機字串，例如產品代碼。 請勿搭配此模擬使用強制旗標。<br/></td>
</tr>
</tbody>
</table>



 

 

 




