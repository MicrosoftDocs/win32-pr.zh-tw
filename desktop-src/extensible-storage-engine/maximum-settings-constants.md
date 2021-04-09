---
description: 深入瞭解：設定常數上限
title: 最大設定常數
TOCTitle: Maximum Settings Constants
ms:assetid: 1111051f-55af-4c33-be38-6a3973c2c815
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269189(v=EXCHG.10)
ms:contentKeyID: 32765492
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
ms.openlocfilehash: 3754732e59c9a90c74366558d9904fc13376db7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848177"
---
# <a name="maximum-settings-constants"></a>最大設定常數


_**適用于：** Windows |Windows Server_

## <a name="maximum-settings-constants"></a>最大設定常數

這些常數會提供 ESE 資料庫中專案上所允許的最大設定。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>常數/值</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_BASE_NAME_LENGTH<br />
3</p></td>
<td><p>設定用來命名資料庫引擎所使用之檔案的前置詞長度。 此長度適用于為 <a href="gg269235(v=exchg.10).md">JET_paramBaseName</a> 系統參數設定的名稱。</p></td>
</tr>
<tr class="even">
<td><p>JET_MAX_COMPUTERNAME_LENGTH<br />
15</p></td>
<td><p>設定 <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a>的最大長度。</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbBookmarkMost<br />
256</p></td>
<td><p>書簽的預設大小上限。 當金鑰大小保留為其預設值時，這會是有效的。</p></td>
</tr>
<tr class="even">
<td><p>JET_cbBookmarkMostMost<br />
2000</p></td>
<td><p>當 esent 設定為具有最大的可用索引鍵時，書簽的大小上限。</p>
<p><strong>Windows 7：</strong> JET_cbBookmarkMostMost 是在 Windows 7 中引進的。</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbNameMost<br />
64</p></td>
<td><p>物件、資料行、索引或屬性名稱的最大長度。</p>
<p><strong>注意</strong>  若為 Unicode，則值為128。</p></td>
</tr>
<tr class="even">
<td><p>JET_cbFullNameMost<br />
255</p></td>
<td><p>&quot;Name.name.name ... 結構的最大長度。 &quot;</p>
<p><strong>注意</strong>  若為 Unicode，則值為510。</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbColumnLVPageOverhead<br />
82</p></td>
<td><p>此數位可用來計算資料庫引擎可在單一資料庫頁面上儲存之 BLOB 的最大數量。 公式的大小上限 = JET_paramDatabasePageSize – JET_cbColumnLVPageOverhead。</p>
<p>此值現在已過時。 應該使用 JET_paramLVChunkSizeMost 參數來取出長值的區塊大小。</p></td>
</tr>
<tr class="even">
<td><p>JET_cbColumnMost<br />
255</p></td>
<td><p>非 long 值資料行資料的大小上限。</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbLVDefaultValueMost<br />
255</p></td>
<td><p>長值 (LongBinary 或 LongText) 資料行預設值的大小上限。</p></td>
</tr>
<tr class="even">
<td><p>JET_cbKeyMost<br />
255</p></td>
<td><p>排序或索引鍵的預設大小上限。</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbKeyMostMost<br />
2000</p></td>
<td><p>任何頁面大小之排序或索引鍵可設定的最大大小。  (參閱 JET_INDEXCREATE2 cbKeyMost) </p>
<p><strong>Windows 7：</strong> JET_cbKeyMostMost 是在 Windows 7 作業系統中引進。</p></td>
</tr>
<tr class="even">
<td><p>JET_cbKeyMost2KBytePage<br />
500</p></td>
<td><p>使用2048位元組頁面的資料庫中，最大允許的索引鍵可設定的大小上限。 如需詳細資訊，請參閱 <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> 。</p>
<p><strong>Windows Vista：</strong> JET_cbKeyMost2KBytePage 是在 Windows Vista 作業系統中引進。</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbKeyMost4KBytePage<br />
1000</p></td>
<td><p>使用4096位元組頁面的資料庫中，最大允許的索引鍵可設定的大小上限。 如需詳細資訊，請參閱 <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> 。</p>
<p><strong>Windows Vista：</strong> JET_cbKeyMost4KBytePage 是在 Windows Vista 中引進。</p></td>
</tr>
<tr class="even">
<td><p>JET_cbKeyMost8KBytePage<br />
2000</p></td>
<td><p>使用8192位元組頁面的資料庫中，最大允許的索引鍵可設定的大小上限。 如需詳細資訊，請參閱 <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> 。</p>
<p><strong>Windows Vista：  </strong>Windows Vista 引進 JET_cbKeyMost8KBytePage</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbKeyMostMin<br />
255</p></td>
<td><p>索引鍵的最小允許大小上限。 如需詳細資訊，請參閱 <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> 。</p>
<p><strong>Windows Vista：  </strong>JET_cbKeyMostMin 是在 Windows Vista 中引進。</p></td>
</tr>
<tr class="even">
<td><p>JET_cbLimitKeyMost<br />
256</p></td>
<td><p>使用限制 <em>grbit</em>（例如在 <a href="gg269329(v=exchg.10).md">JetMakeKey</a> 函數中使用的 JET_bitStrLimit）來形成索引鍵時的最大索引鍵大小。</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbPrimaryKeyMost<br />
255</p></td>
<td><p>主要索引的大小上限。 這項功能現在已過時。</p></td>
</tr>
<tr class="even">
<td><p>JET_cbSecondaryKeyMost<br />
255</p></td>
<td><p>次要索引的大小上限。 這項功能現在已過時。</p></td>
</tr>
<tr class="odd">
<td><p>JET_ccolKeyMost<br />
12</p></td>
<td><p>排序或索引鍵中元件的最大數目。</p>
<p><strong>Windows Vista：  </strong>在 Windows Vista 和更新版本的 Windows 中，此值為16。</p></td>
</tr>
<tr class="even">
<td><p>JET_ccolMost<br />
0x0000fee0</p></td>
<td><p>資料表中允許的資料行數目上限。</p>
<p><strong>WINDOWS XP：  </strong>0x0000fee0 值用於 Windows XP 及更新版本的 Windows 中。</p>
<p><strong>Windows 2000：  </strong>0x00007ffe 值是在 Windows 2000 中使用。</p></td>
</tr>
<tr class="odd">
<td><p>JET_ccolFixedMost<br />
0x0000007f</p></td>
<td><p>資料表中允許的固定資料行數目上限（目前為127）。</p></td>
</tr>
<tr class="even">
<td><p>JET_ccolVarMost<br />
0x00000080</p></td>
<td><p>可包含在資料表中之可變長度資料行的最大數目，目前為128。</p></td>
</tr>
<tr class="odd">
<td><p>JET_ccolTaggedMost<br />
 ( JET_ccolMost 0x000000ff ) </p></td>
<td><p>可包含在資料表中的標記資料行數目上限，目前為64993。</p></td>
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
<td><p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p></td>
</tr>
<tr class="even">
<td><p><strong>伺服器</strong></p></td>
<td><p>需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</p></td>
</tr>
<tr class="odd">
<td><p><strong>標頭</strong></p></td>
<td><p>宣告于 Esent. h 中。</p></td>
</tr>
</tbody>
</table>

