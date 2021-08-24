---
description: 深入瞭解： Windows8 命名空間。
title: Windows8 命名空間 () 的
TOCTitle: '@NoTitle'
ms:assetid: N:Microsoft.Isam.Esent.Interop.Windows8
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8(v=EXCHG.10)
ms:contentKeyID: 55104389
ms.date: 07/30/2014
ms.topic: article
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8
dev_langs:
- CSharp
- JScript
- VB
- other
ms.openlocfilehash: 768064e19af76a03aa0d4f11c087f8d7ff7086b04cd1de46edfb504ba8e6be2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614471"
---
# <a name="microsoftisamesentinteropwindows8-namespace"></a>Windows8 命名空間。

## <a name="classes"></a>類別

<table>
<thead>
<tr class="header">
<th> </th>
<th>類別</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn335323(v=exchg.10).md">DurableCommitCallback</a></td>
<td>包裝回呼處理永久性認可。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn335448(v=exchg.10).md">JET_COMMIT_ID</a></td>
<td>資訊內容會括住從 JET_PFNEMITLOGDATA 發出的資料。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn335334(v=exchg.10).md">JET_ERRINFOBASIC</a></td>
<td>包含錯誤的相關資訊。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn335349(v=exchg.10).md">JET_INDEX_COLUMN</a></td>
<td>包含 <a href="dn335382(v=exchg.10).md">JetPrereadIndexRanges (JET_SESID、JET_TABLEID、[]、int32、int32、int32、[]、PrereadIndexRangesGrbit) </a> 和 <a href="dn335383(v=exchg.10).md">JetSetCursorFilter (JET_SESID、JET_TABLEID、[]、CursorFilterGrbit) </a>的篩選定義。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn335481(v=exchg.10).md">JET_INDEX_RANGE</a></td>
<td>包含 <a href="dn335382(v=exchg.10).md">JetPrereadIndexRanges (JET_SESID、JET_TABLEID、[]、int32、int32、int32、[]、PrereadIndexRangesGrbit) </a>的定義。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn335490(v=exchg.10).md">Windows8Api</a></td>
<td>Windows 8 中引進的 Api 呼叫。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn335391(v=exchg.10).md">Windows8Grbits</a></td>
<td>Windows 8 中引進的系統參數。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn335399(v=exchg.10).md">Windows8IdxInfo</a></td>
<td>已加入至 Windows 8 版本之 ESENT 的資料行資訊層級。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn335398(v=exchg.10).md">Windows8Param</a></td>
<td>Windows 8 中引進的系統參數。</td>
</tr>
</tbody>
</table>


## <a name="delegates"></a>委派

<table>
<thead>
<tr class="header">
<th> </th>
<th>代理人</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596136.pubdelegate(exchg.10).gif" title="公用委派" alt="Public delegate" /></td>
<td><a href="dn335363(v=exchg.10).md">JET_PFNDURABLECOMMITCALLBACK</a></td>
<td>JET_paramDurableCommitCallback 的回呼。</td>
</tr>
</tbody>
</table>


## <a name="enumerations"></a>列舉

<table>
<thead>
<tr class="header">
<th> </th>
<th>列舉型別</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="dn335440(v=exchg.10).md">CursorFilterGrbit</a></td>
<td>設定資料指標篩選時所傳遞的選項。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="dn335446(v=exchg.10).md">DurableCommitCallbackGrbit</a></td>
<td>傳遞至記錄排清回呼的選項。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="dn335447(v=exchg.10).md">ErrorInfoGrbit</a></td>
<td><a href="dn335493(v=exchg.10).md">JetGetErrorInfo (JET_err 的選項，JET_ERRINFOBASIC) </a>。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="dn335469(v=exchg.10).md">JET_ERRCAT</a></td>
<td>錯誤類別。 階層如下： JET_errcatError | |--JET_errcatOperation | |--JET_errcatFatal | |--JET_errcatIO//錯誤的 IO 問題，可能或可能不是暫時性問題。 | |--JET_errcatResource | |--JET_errcatMemory//記憶體不足 (所有變體) | |--JET_errcatQuota | |--JET_errcatDisk//磁碟空間 (所有變體) |--JET_errcatData | |--JET_errcatCorruption | |--JET_errcatInconsistent//通常是由使用者承載錯誤處理所造成 | |--JET_errcatFragmentation |--JET_errcatApi |--JET_errcatUsage |--JET_errcatState |--JET_errcatObsolete</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="dn335352(v=exchg.10).md">JET_ErrorInfo</a></td>
<td>適用于 JetGetErrorInfo 的 InfoLevel 有效值。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="dn335486(v=exchg.10).md">JET_sesparam</a></td>
<td>ESENT 會話參數。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="dn335365(v=exchg.10).md">JetIndexColumnGrbit</a></td>
<td><a href="dn335349(v=exchg.10).md">JET_INDEX_COLUMN</a>的選項。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="dn335491(v=exchg.10).md">JetRelop</a></td>
<td>篩選準則定義為 <a href="dn335349(v=exchg.10).md">JET_INDEX_COLUMN</a>的比較作業。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="dn335366(v=exchg.10).md">PrereadIndexRangesGrbit</a></td>
<td><a href="dn335382(v=exchg.10).md">JetPrereadIndexRanges (JET_SESID、JET_TABLEID、[]、int32、int32、int32、[]、PrereadIndexRangesGrbit) </a>的選項。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="dn335369(v=exchg.10).md">ResizeDatabaseGrbit</a></td>
<td><a href="dn335496(v=exchg.10).md">JetResizeDatabase (JET_SESID、JET_DBID、int32、int32、ResizeDatabaseGrbit) </a>的選項。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="dn335370(v=exchg.10).md">StopServiceGrbit</a></td>
<td><a href="dn335494(v=exchg.10).md">JetStopServiceInstance2 (JET_INSTANCE、StopServiceGrbit) </a>的選項。</td>
</tr>
</tbody>
</table>

