---
description: Network DDE 提供可讓您刪除共用、取得或設定共用資訊，或列舉共用的函式。
ms.assetid: d7924e93-75e4-4f94-b159-02408535170d
title: 管理 DDE 共用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fcc8c7d2eb3983aaabd054b9b729daea176bb10
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/05/2021
ms.locfileid: "104321356"
---
# <a name="managing-dde-shares"></a>管理 DDE 共用

\[不再支援網路 DDE。 Windows Vista 上有 Nddeapi.dll，但是所有的函式呼叫都會傳回 NDDE \_ 未 \_ 執行。\]

Network DDE 提供可讓您刪除共用、取得或設定共用資訊，或列舉共用的函式。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Task</th>
<th>程序</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>刪除 DDE 共用</td>
<td>使用 <a href="nddesharedel.md"><strong>NDdeShareDel</strong></a> 函數。</td>
</tr>
<tr class="even">
<td>取得 DDE 共用資訊</td>
<td>使用 <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a> 函數。</td>
</tr>
<tr class="odd">
<td>設定 DDE 共用資訊</td>
<td>使用 <a href="nddesharesetinfo.md"><strong>NDdeShareSetInfo</strong></a> 函數。</td>
</tr>
<tr class="even">
<td>列舉 DDE 共用</td>
<td>使用 <a href="nddeshareenum.md"><strong>NDdeShareEnum</strong></a> 函數。 您也可以使用 <a href="nddetrustedshareenum.md"><strong>NDdeTrustedShareEnum</strong></a> 函數來列舉受信任的 DDE 共用。<br/></td>
</tr>
<tr class="odd">
<td>列舉已連線的使用者</td>
<td>使用 <a href="/windows/desktop/api/lmshare/nf-lmshare-netsessionenum"><strong>NetSessionEnum</strong></a> 函數。</td>
</tr>
<tr class="even">
<td>變更 DDE 共用名稱</td>
<td>刪除舊的共用並建立新的共用。
<ol>
<li>使用 <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a>取出共用資訊。</li>
<li>使用 <a href="nddesharedel.md"><strong>NDdeShareDel</strong></a>移除共用。</li>
<li>變更<a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a>所傳回之<a href="nddeshareinfo-str.md"><strong>NDDESHAREINFO</strong></a>結構的<strong>lpszShareName</strong>成員。</li>
<li>將修改過的 <a href="nddeshareinfo-str.md"><strong>NDDESHAREINFO</strong></a> 結構傳遞至 <a href="nddeshareadd.md"><strong>NDdeShareAdd</strong></a>。</li>
</ol></td>
</tr>
</tbody>
</table>



 

 

