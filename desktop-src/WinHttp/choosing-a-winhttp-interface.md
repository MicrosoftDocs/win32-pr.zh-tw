---
description: 在開始開發 Microsoft Windows HTTP 服務 (WinHTTP) 應用程式之前，您必須先決定要使用 C/c + + API 或 COM 介面。
ms.assetid: 451ad247-962f-4af1-bb21-0aed4ef5f93c
title: 選擇 WinHTTP 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc529e6052b0de2de19a7c15ff1cfad226cee2cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989454"
---
# <a name="choosing-a-winhttp-interface"></a>選擇 WinHTTP 介面

在開始開發 Microsoft Windows HTTP 服務 (WinHTTP) 應用程式之前，您必須先決定要使用 C/c + + API 或 COM 介面。 下表摘要說明每個方法的相關優點和缺點。



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th>C/C + + API</th>
<th>COM 介面</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>優點</td>
<td><ul>
<li>您可以在區塊中處理回應，這會更有效率。</li>
<li>POST 作業也可以在區塊中處理，以加速處理時間。</li>
<li>自動代理支援。</li>
<li>存取 WinHTTP 的完整功能集。</li>
<li>您可以輕鬆地處理二進位資料。</li>
</ul></td>
<td><ul>
<li>建立應用程式很容易，而且需要比 C/c + + API 更少的程式程式碼。</li>
<li>指令碼語言可以使用此介面。</li>
</ul></td>
</tr>
<tr class="even">
<td>缺點</td>
<td><ul>
<li>處理更為複雜。</li>
<li>C/c + + API 需要的步驟多於 COM 介面，才能執行相同的動作。</li>
<li>設定要求需要更多程式碼。</li>
</ul></td>
<td><ul>
<li>COM 介面不提供對 WinHTTP 完整功能集的存取權。</li>
<li>在某些指令碼語言（如 VBScript 和 JScript）中，很難處理二進位資料類型。</li>
<li>COM 介面不支援自動代理。</li>
<li>應用程式必須使用 COM APARTMENT_THREADED 模型。</li>
<li>在開始處理回應之前，必須先接收和緩衝處理整個回應。</li>
</ul></td>
</tr>
</tbody>
</table>



 

 

 



