---
description: 深入瞭解：資訊參數
title: 資訊參數
TOCTitle: Informational Parameters
ms:assetid: 48500fc9-6d89-45b8-92ad-afb997b729f3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269241(v=EXCHG.10)
ms:contentKeyID: 32765543
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a8923b544726e474775684f54fed47d8b4ba281e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691336"
---
# <a name="informational-parameters"></a>資訊參數


_**適用于：** Windows |Windows Server_

## <a name="informational-parameters"></a>資訊參數

本主題包含用來公開資料庫引擎相關資訊的參數。

*JET_paramKeyMost*  
134  

這個唯讀參數表示可針對目前資料庫頁面大小選取的最大可允許索引鍵長度， (如 JET_paramDatabasePageSize) 所設定。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p>JET_cbKeyMost4KBytePage</p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>整數</p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p>255–65535</p></td>
</tr>
<tr class="even">
<td><p>範圍：</p></td>
<td><p>全球</p></td>
</tr>
<tr class="odd">
<td><p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p></td>
<td><p>N/A</p></td>
</tr>
<tr class="even">
<td><p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p></td>
<td><p>N/A</p></td>
</tr>
<tr class="odd">
<td><p>會影響實體版面配置：</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>會影響可靠性：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>影響效能：</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>會影響資源：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>可用性：</p></td>
<td><p>從 Windows Server 2008 和 Windows Vista 開始</p></td>
</tr>
</tbody>
</table>


*JET_paramMaxColtyp*  
131  

這個唯讀參數會傳回該版本資料庫引擎的最大 [JET_COLTYP](./jet-coltyp.md) (JET_coltypMax) 。 這個值可以用來測試特定 [JET_COLTYP](./jet-coltyp.md)的支援。 如果給定的 [JET_COLTYP](./jet-coltyp.md) 小於這個參數的值，database engine 就會支援它。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p>JET_coltypUnsignedShort + 1</p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>整數</p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p>0-255</p></td>
</tr>
<tr class="even">
<td><p>範圍：</p></td>
<td><p>全球</p></td>
</tr>
<tr class="odd">
<td><p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p></td>
<td><p>N/A</p></td>
</tr>
<tr class="even">
<td><p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p></td>
<td><p>N/A</p></td>
</tr>
<tr class="odd">
<td><p>會影響實體版面配置：</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>會影響可靠性：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>影響效能：</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>會影響資源：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>可用性：</p></td>
<td><p>從 Windows Server 2008 和 Windows Vista 開始</p></td>
</tr>
</tbody>
</table>


*JET_paramLVChunkSizeMost*  
163  

唯讀參數，會根據設定的頁面大小傳回長值的區塊大小。 如果要使用多個 Jet {Set，抓取} 資料行呼叫來讀取或寫入較長的值，則使用大小是區塊大小倍數的緩衝區會更有效率。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p>2kb 頁面 = 1966 位元組<br />
4 kb 頁面 = 4014 個位元組<br />
8kb 頁面 = 8110 位元組<br />
16kb 頁面 = 4050 位元組<br />
32kb 頁面 = 8150 位元組</p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>整數</p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p>0-10000</p></td>
</tr>
<tr class="even">
<td><p>範圍：</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>會影響實體版面配置：</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>會影響可靠性：</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>影響效能：</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>會影響資源：</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>可用性：</p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>規格需求

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>用戶端</strong></p></td>
<td><p>需要 Windows Vista。</p></td>
</tr>
<tr class="even">
<td><p><strong>伺服器</strong></p></td>
<td><p>需要 Windows Server 2008。</p></td>
</tr>
<tr class="odd">
<td><p><strong>標頭</strong></p></td>
<td><p>宣告于 Esent. h 中。</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>另請參閱

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JET_COLTYP](./jet-coltyp.md)
