---
description: 深入瞭解： Windows7Param 欄位
title: Windows7Param 欄位 (最為理想) 中
TOCTitle: Windows7Param fields
ms:assetid: Fields.T:Microsoft.Isam.Esent.Interop.Windows7.Windows7Param
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows7.windows7param_fields(v=EXCHG.10)
ms:contentKeyID: 55104278
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 9eed2113b63ccf297611c6ecaa807a042ffe8ea114e497ecad390081131c6b3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967178"
---
# <a name="windows7param-fields"></a>Windows7Param 欄位

包含受保護的成員  
包含繼承的成員  

[Windows7Param](./windows7param-class.md)類型會公開下列成員。

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
<td><a href="dn335314(v=exchg.10).md">DbScanIntervalMaxSec</a></td>
<td>允許資料庫掃描完成的最大間隔（以秒為單位）。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn335431(v=exchg.10).md">DbScanIntervalMinSec</a></td>
<td>重複資料庫掃描的最小間隔（以秒為單位）。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn335316(v=exchg.10).md">DbScanThrottle</a></td>
<td>資料庫掃描的節流（以毫秒為單位）。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn335434(v=exchg.10).md">EnableDbScanInRecovery</a></td>
<td>在復原期間啟用資料庫維護。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn335318(v=exchg.10).md">LVChunkSizeMost</a></td>
<td>這個參數是用來取出 long 值 (blob) 資料的區塊大小。 以這個大小的倍數設定和抓取資料可提高效率。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn335433(v=exchg.10).md">MaxCoalesceReadGapSize</a></td>
<td>接合的讀取 IO 作業可能會有空隙的最大位元組數目。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn335435(v=exchg.10).md">MaxCoalesceReadSize</a></td>
<td>合併的讀取作業可分組的最大位元組數目。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn335322(v=exchg.10).md">MaxCoalesceWriteGapSize</a></td>
<td>接合的寫入 IO 作業可能會有空隙的最大位元組數目。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn335437(v=exchg.10).md">MaxCoalesceWriteSize</a></td>
<td>合併寫入作業可分組的最大位元組數目。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn335438(v=exchg.10).md">WaypointLatency</a></td>
<td>此參數會設定 esent 將延遲資料庫排清的記錄檔數目。 如果失敗導致記錄檔遺失，這可以用來提高資料庫復原能力。</td>
</tr>
</tbody>
</table>


頁首

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Windows7Param 類別](./windows7param-class.md)

[最為理想命名空間。](./microsoft.isam.esent.interop.windows7-namespace.md)
