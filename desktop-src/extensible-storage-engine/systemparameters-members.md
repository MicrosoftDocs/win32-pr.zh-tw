---
description: 深入瞭解： SystemParameters 成員
title: SystemParameters 成員
TOCTitle: SystemParameters members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.SystemParameters
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters_members(v=EXCHG.10)
ms:contentKeyID: 55104101
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: d2ad43871c768955f98c0e372adde37cd731f8f4689bcb05b21f7e169bed715c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118070978"
---
# <a name="systemparameters-members"></a>SystemParameters 成員

包含受保護的成員  
包含繼承的成員  

ESENT API 的常數。 這些都不需要透過系統參數進行查閱。 此類別提供靜態屬性來設定和取得全域 ESENT 系統參數。 此類別提供靜態屬性來設定和取得全域 ESENT 系統參數。

[SystemParameters](./systemparameters-class.md)類型會公開下列成員。

## <a name="properties"></a>屬性

<table>
<thead>
<tr class="header">
<th> </th>
<th>名稱</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn351215(v=exchg.10).md">BookmarkMost</a></td>
<td>取得書簽的大小上限。 <a href="dn292149(v=exchg.10).md">JetGetBookmark (JET_SESID、JET_TABLEID、[]、int32、int32) </a>。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn351214(v=exchg.10).md">CacheSize</a></td>
<td>取得或設定頁面中資料庫快取的大小。 根據預設，資料庫快取會自動調整其大小，將此屬性設定為非零值會導致快取將本身調整為目標大小。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn351149(v=exchg.10).md">CacheSizeMax</a></td>
<td>取得或設定資料庫頁面快取的大小上限。 大小是在資料庫頁面中。 如果此參數保留為其預設值，則在呼叫 JetInit 時，會將快取的大小上限設定為實體記憶體的大小。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn351216(v=exchg.10).md">CacheSizeMin</a></td>
<td>取得或設定資料庫頁面中資料庫頁面快取的大小下限。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn351151(v=exchg.10).md">ColumnsKeyMost</a></td>
<td>取得排序或索引鍵中元件的最大數目。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn351218(v=exchg.10).md">Configuration</a></td>
<td>取得或設定值，這個值會指定整個系統參數集的預設值。 當此參數設定為特定設定時，所有系統參數值都會重設為該設定的預設值。 如果設定特定實例的設定，則全域系統參數將不會重設為其預設值。 Small Configuration (0) ：資料庫引擎已針對記憶體使用量優化。 舊版設定 (1) ：資料庫引擎有其傳統預設值。 Windows Vista 和更新的支援。 在 Windows XP 和 Windows Server 2003 上略過。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn351153(v=exchg.10).md">DatabasePageSize</a></td>
<td>取得或設定資料庫頁面的大小（以位元組為單位）。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn351221(v=exchg.10).md">EnableAdvanced</a></td>
<td>取得或設定值，這個值表示資料庫引擎是否接受或拒絕系統參數子集的變更。 此參數會搭配 <a href="dn351218(v=exchg.10).md">設定使用，以防止</a> 某些系統參數從選取的設定的預設值中退出。 Windows Vista 和更新的支援。 在 Windows XP 和 Windows Server 2003 上略過。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn351152(v=exchg.10).md">EnableFileCache</a></td>
<td>取得或設定值，這個值表示資料庫引擎是否應使用所有 managed 檔案的 OS 檔案快取。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn351220(v=exchg.10).md">EnableViewCache</a></td>
<td>取得或設定值，這個值表示資料庫引擎是否應針對資料庫檔案使用記憶體對應的檔案 i/o。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn351223(v=exchg.10).md">EventLoggingLevel</a></td>
<td>取得或設定資料庫引擎發出至 eventlog 的 eventlog 訊息詳細層級。 較高的數位將會產生更詳細的事件記錄檔訊息。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn351154(v=exchg.10).md">ExceptionAction</a></td>
<td>取得或設定在 JET 內產生之例外狀況的編碼方式。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn351227(v=exchg.10).md">HungIOActions</a></td>
<td>取得或設定要在出現無回應的 IOs 上執行的動作集合。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn351155(v=exchg.10).md">HungIOThreshold</a></td>
<td>取得或設定視為應採取動作之無反應 IO 的臨界值。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn351156(v=exchg.10).md">KeyMost</a></td>
<td>取得最大索引鍵大小。 這取決於 Esent 版本和資料庫頁面大小。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn351229(v=exchg.10).md">LegacyFileNames</a></td>
<td>取得或設定與舊版資料庫引擎的檔案命名慣例的回溯相容性。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn351157(v=exchg.10).md">LVChunkSizeMost</a></td>
<td>取得 lv 區塊大小。 這取決於資料庫頁面大小。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn351230(v=exchg.10).md">MaxInstances</a></td>
<td>取得或設定可建立的實例數目上限。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn351160(v=exchg.10).md">MinDataForXpress</a></td>
<td>取得或設定應壓縮為 xpress 壓縮的最小資料量。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn351159(v=exchg.10).md">OutstandingIOMax</a></td>
<td>此參數控制一次可在主機作業系統中的每個磁片佇列的資料庫檔案 i/o 數目。 較大的參數值可大幅協助大型資料庫應用程式的效能。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn351158(v=exchg.10).md">ProcessFriendlyName</a></td>
<td>取得或設定這個進程實例的易記名稱。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn351161(v=exchg.10).md">StartFlushThreshold</a></td>
<td>取得或設定資料庫頁面快取開始從快取收回頁面的閾值，以騰出空間給未快取的頁面。 當快取中的頁面緩衝區數目降到低於此閾值時，就會啟動背景進程來補充該可用緩衝區集區。 此臨界值一律相對於 JET_paramCacheSizeMax 所設定的最大快取大小。 此臨界值也必須小於 JET_paramStopFlushThreshold 所設定的停止閾值。 開始閾值的距離高度將決定資料庫頁面快取在應用程式需要之前產生可用緩衝區所必須擁有的回應時間。 高啟動臨界值可讓背景進程更有時間回應。 不過，高啟動閾值表示較高的停止閾值，而且會減少資料庫頁面快取的有效大小。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn351231(v=exchg.10).md">StopFlushThreshold</a></td>
<td>取得或設定資料庫頁面快取結束從快取收回頁面的閾值，以騰出空間給未快取的頁面。 當快取中的頁面緩衝區數目超過此臨界值時，就會停止已開始補充該可用緩衝區集區的背景進程。 此臨界值一律相對於 JET_paramCacheSizeMax 所設定的最大快取大小。 此臨界值也必須大於 JET_paramStartFlushThreshold 所設定的 [開始] 閾值。 開始閾值和停止臨界值之間的距離，會影響背景進程清除資料庫頁面的效率。 較大的間距將可讓您更有可能合併對相鄰頁面的寫入。 不過，高停止閾值將會減少資料庫頁面快取的有效大小。</td>
</tr>
</tbody>
</table>


頁首

## <a name="fields"></a>欄位

<table>
<thead>
<tr class="header">
<th> </th>
<th>名稱</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn351208(v=exchg.10).md">BaseNameLength</a></td>
<td>用來命名資料庫引擎所使用之檔案的前置詞長度。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn351146(v=exchg.10).md">ColumnMost</a></td>
<td>未 JET_coltyp 資料行的大小上限。LongBinary 或 JET_coltyp。LongText.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn351210(v=exchg.10).md">ColumnsFixedMost</a></td>
<td>資料表中允許的固定資料行數目上限。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn351140(v=exchg.10).md">ColumnsMost</a></td>
<td>資料表中允許的資料行數目上限。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn351148(v=exchg.10).md">ColumnsTaggedMost</a></td>
<td>資料表中允許的標記資料行數目上限。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn351212(v=exchg.10).md">ColumnsVarMost</a></td>
<td>資料表中允許的可變長度資料行數目上限。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn351141(v=exchg.10).md">LocaleNameMaxLength</a></td>
<td>地區設定名稱的最大長度 (從 winnt. h) LOCALE_NAME_MAX_LENGTH。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn351213(v=exchg.10).md">NameMost</a></td>
<td>資料表/資料行/索引名稱的大小上限。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn351211(v=exchg.10).md">PageTempDBSmallest</a></td>
<td>提供最小可能暫存資料庫的頁面數目。</td>
</tr>
</tbody>
</table>


頁首

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[SystemParameters 類別](./systemparameters-class.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
