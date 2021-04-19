---
title: IPv6-Aware 和舊版 WPAD helper 函數
description: IPv6-Aware WPAD Helper 函式和舊版 WPAD Helper 函數之間的差異
ms.assetid: ea4b1c0d-ce02-477b-85c8-44e1beef90c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 511b7f04aa0a2abe04b99562c15aeb3a53bdaadf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975214"
---
# <a name="ipv6-aware-and-legacy-wpad-helper-functions"></a>IPv6-Aware 和舊版 WPAD helper 函數

下表說明新的 WPAD helper 函式和舊版 WPAD helper 函數之間的差異。 新的函式會以星號標記。



<table>
<thead>
<tr class="header">
<th>函式</th>
<th>輸入</th>
<th>輸出</th>
<th>變更的原因</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>dnsResolve</td>
<td>主機</td>
<td>IPv4 位址</td>
<td rowspan="2">Ex 函數會傳回 IPv6/IPv4 的清單。 因為 IPv6 或 IPv4 位址可以針對單一介面擁有多個單播位址，所以需要此項。 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>dnsResolveEx*</td>
<td>主機</td>
<td>IPv6/IPv4 地址清單</td>

</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th>函式</th>
<th>輸入</th>
<th>輸出</th>
<th>變更的原因</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>isResolveable</td>
<td>IPv4 主機</td>
<td>TRUE/FALSE</td>
<td rowspan="2">如果主機可以解析成 IPv6 或 IPv4 位址，則 Ex 函數會傳回 TRUE。 如果主機解析成 IPv4 位址，則舊版函式只會傳回 TRUE。 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>isResolveableEx*</td>
<td>IPv6/IPv4 主機</td>
<td>TRUE/FALSE</td>

</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th>函式</th>
<th>輸入</th>
<th>輸出</th>
<th>變更的原因</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>myIPAddress</td>
<td>無</td>
<td>IPv4 位址</td>
<td rowspan="2">Ex 函數會傳回 IPv6/IPv4 的清單。 需要的原因是 IPv6 或 IPv4 位址可以有單一介面 $ {REMOVE} $ 的多重單播位址<br />
</td>
</tr>
<tr class="even">
<td>myIPAddressEx*</td>
<td>無</td>
<td>IPv6/IPv4 地址清單</td>

</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th>函式</th>
<th>輸入</th>
<th>輸出</th>
<th>變更的原因</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>isInNet</td>
<td>主機、點分隔 IP 位址模式、IP 位址遮罩</td>
<td>TRUE/FALSE</td>
<td rowspan="2">提供 IP 版本中立的方式，以找出 IP 位址是否在指定的子網中。 此外，IPv4 中的遮罩標記法已淘汰。 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>isInNetEx*</td>
<td>IP 位址 IP 首碼</td>
<td>TRUE/FALSE</td>

</tr>
</tbody>
</table>



 



| 函式           | 輸入                       | 輸出                             | 變更的原因                                                                                                                           |
|---------------------|-----------------------------|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| sortIPAddressList\* | IPv6/IPv4 地址清單 | IPv6/IPv4 位址的排序清單 | 沒有對應的舊版函式，因為舊版函式只會傳回單一的 IPv4 位址，因此不需要排序。 |



 



| 函式          | 輸入 | 輸出                     | 變更的原因                                                                                                                                                                                                           |
|--------------------|-------|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| getClientVersion\* | 無  | WPAD 引擎版本號碼 | 此函數目前會傳回1.0 版。 我們新增了此函式，可讓 IT 系統管理員更新其 WPAD 以使用不同版本的 WPAD 引擎，而不會導致其存在的部署中斷。 |



 

> [!Note]  
> 這種功能需要 Windows Internet Explorer 7 或更新版本。

 

 

 



