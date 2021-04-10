---
description: 此頁面描述以各種通訊端選項設定狀態為基礎的多播通訊端選項行為。
ms.assetid: a411e831-7b28-4ab5-a09a-650db99a7cd5
title: 多播通訊端選項行為
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fd10094750bea59b844ad1fcdac70be0c7f9646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026214"
---
# <a name="multicast-socket-option-behavior"></a>多播通訊端選項行為

此頁面描述以各種通訊端選項設定狀態為基礎的多播通訊端選項行為。

例如，此頁面描述在 \_ \_ \_ \_ \_ \_ 已使用相同網路介面上的指定群組/來源組設定了 ip 新增來源成員資格選項的通訊端上設定 ip 新增來源成員資格通訊端選項時的行為。 允許在 \_ \_ 不同的網路介面上呼叫 \_ 相同群組的 IP 新增來源成員資格。

此頁面可協助您正確設計和疑難排解 Windows 通訊端多播應用程式。 

<table>
<thead>
<tr class="header">
<th>初始通訊端選項</th>
<th>衝突的後續通訊端選項</th>
<th>傳回的錯誤</th>
<th>備註</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="4">IP_ADD_MEMBERSHIP $ {REMOVE} $<br />
</td>
<td>IP_ADD_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>請勿在相同的網路介面上多次呼叫相同群組的 IP_ADD_MEMBERSHIP。</td>
</tr>
<tr class="even">
<td>IP_ADD_SOURCE_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>請勿使用與先前在相同網路介面上 IP_ADD_MEMBERSHIP 呼叫的相同群組來呼叫 IP_ADD_SOURCE_MEMBERSHIP。</td>

</tr>
<tr class="odd">
<td>IP_DROP_SOURCE_MEMBERSHIP</td>
<td>WSAEINVAL</td>
<td>請改用 IP_BLOCK_SOURCE。</td>

</tr>
<tr class="even">
<td>IP_UNBLOCK_SOURCE</td>
<td>WSAEINVAL</td>
<td>嘗試解除封鎖先前未在相同網路介面上封鎖的群組/來源組時，會傳回錯誤。</td>

</tr>
<tr class="odd">
<td>IP_DROP_MEMBERSHIP</td>
<td>對相同群組或群組/來源配對的任何後續呼叫</td>
<td>WSAEINVAL</td>
<td>在群組或群組/來源組上進行通訊端選項呼叫，而目前不在包含清單中 (因為卸載成員資格，否則) 會導致錯誤。</td>
</tr>
<tr class="even">
<td rowspan="3">IP_ADD_SOURCE_MEMBERSHIP $ {REMOVE} $<br />
</td>
<td>IP_ADD_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>請勿使用與先前在相同網路介面上 IP_ADD_SOURCE_MEMBERSHIP 呼叫的相同群組來呼叫 IP_ADD_MEMBERSHIP。</td>
</tr>
<tr class="odd">
<td>IP_ADD_SOURCE_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>請勿使用先前以 IP_ADD_SOURCE_MEMBERSHIP 在相同網路介面上呼叫的相同群組/來源組來呼叫 IP_ADD_SOURCE_MEMBERSHIP。</td>

</tr>
<tr class="even">
<td>IP_UNBLOCK_SOURCE</td>
<td>WSAEINVAL</td>
<td>嘗試解除封鎖先前未在相同網路介面上封鎖的群組/來源組時，會傳回錯誤。</td>

</tr>
<tr class="odd">
<td rowspan="2">IP_DROP_SOURCE_MEMBERSHIP $ {REMOVE} $<br />
</td>
<td>IP_UNBLOCK_SOURCE</td>
<td>WSAEINVAL</td>
<td>嘗試解除封鎖先前未在相同網路介面上封鎖的群組/來源組時，會傳回錯誤。</td>
</tr>
<tr class="even">
<td>IP_DROP_SOURCE_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>嘗試卸載不在相同網路介面上包含清單中的群組/來源對時，傳回錯誤。</td>

</tr>
<tr class="odd">
<td rowspan="3">IP_BLOCK_SOURCE $ {REMOVE} $<br />
</td>
<td>IP_BLOCK_SOURCE</td>
<td>WSAEADDRNOTAVAIL</td>
<td>嘗試封鎖已在相同網路介面上封鎖的群組/來源組時，會傳回錯誤。</td>
</tr>
<tr class="even">
<td>IP_ADD_SOURCE_MEMBERSHIP</td>
<td>WSAEINVAL</td>
<td>請改用 IP_UNBLOCK_SOURCE。</td>

</tr>
<tr class="odd">
<td>IP_ADD_MEMBERSHIP</td>
<td>WSAEINVAL</td>
<td>請改用 IP_UNBLOCK_SOURCE。</td>

</tr>
<tr class="even">
<td>IP_UNBLOCK_SOURCE</td>
<td>IP_UNBLOCK_SOURCE</td>
<td>WSAEADDRNOTAVAIL</td>
<td>嘗試解除封鎖不在相同網路介面上封鎖清單中的群組/來源對時，傳回錯誤。</td>
</tr>
</tbody>
</table>



 

 

 



