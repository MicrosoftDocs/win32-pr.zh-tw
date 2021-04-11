---
description: 深入瞭解： Microsoft node.js 命名空間
title: " () 的 Isam 命名空間"
TOCTitle: '@NoTitle'
ms:assetid: N:Microsoft.Isam.Esent.Interop
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop(v=EXCHG.10)
ms:contentKeyID: 39515215
ms.date: 07/30/2014
ms.topic: article
f1_keywords:
- Microsoft.Isam.Esent.Interop
dev_langs:
- CSharp
- JScript
- VB
- other
ms.openlocfilehash: d66441e4db647e6f15c9434597a7e95a2006758a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944394"
---
# <a name="microsoftisamesentinterop-namespace"></a>Microsoft. Esent 命名空間

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
<td><a href="dn292211(v=exchg.10).md">Api</a></td>
<td>ESENT API 的受控版本。 這個類別包含對應至非受控 ESENT API 的靜態方法。 傳回錯誤時，這些方法會擲回例外狀況。 ESENT API 的 Helper 方法。 這些會包裝 JetMakeKey。 API 的僅限內部方法。 ESENT API 的 Helper 方法。 這些會針對 JetMakeKey 進行資料轉換。 ESENT API 的 Helper 方法。 這些方法會處理資料庫中繼資料。 ESENT API 的 Helper 方法。 這些都不是 API 的 interop 版本，但封裝了非常常見的函式用法。 標示為已淘汰的 API 成員。 ESENT API 的 Helper 方法。 這些都不是 API 的 interop 版本，但封裝了非常常見的函式用法。 ESENT API 的 Helper 方法。 這些作業會轉換資料行的資料。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334148(v=exchg.10).md">BoolColumnValue</a></td>
<td><a href="/dotnet/api/system.boolean">布林</a>資料行值。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334109(v=exchg.10).md">ByteColumnValue</a></td>
<td><a href="/dotnet/api/system.byte">位元組</a>資料行值。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334170(v=exchg.10).md">BytesColumnValue</a></td>
<td>位元組陣列資料行值。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334128(v=exchg.10).md">ColumnInfo</a></td>
<td>一個 Esent 資料行的相關資訊。 這不是 interop 類別，而是由中繼資料 helper 方法所使用。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334143(v=exchg.10).md">ColumnStream</a></td>
<td>這個類別會提供 long 值資料行的串流介面 (亦即 <a href="hh577895(v=exchg.10).md">LongBinary</a> 或) <a href="hh577895(v=exchg.10).md">LongText</a> 類型的資料行。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334206(v=exchg.10).md">ColumnValue</a></td>
<td>物件的基類，代表要設定的資料行值。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334171(v=exchg.10).md">ColumnValueOfStruct &lt; T&gt;</a></td>
<td>設定結構類型的資料行 (例如 Int32/Guid) 。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334230(v=exchg.10).md">轉換</a></td>
<td>提供在 Win32 與 .NET Framework 之間轉換資料和旗標的方法。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334238(v=exchg.10).md">DateTimeColumnValue</a></td>
<td><a href="/dotnet/api/system.guid">Guid</a>資料行值。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn273972(v=exchg.10).md">DoubleColumnValue</a></td>
<td><a href="/dotnet/api/system.double">雙</a>資料行值。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn273978(v=exchg.10).md">EsentAccessDeniedException</a></td>
<td>JET_err 的基類。AccessDenied 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334220(v=exchg.10).md">EsentAfterInitializationException</a></td>
<td>JET_err 的基類。AfterInitialization 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn273989(v=exchg.10).md">EsentAlreadyInitializedException</a></td>
<td>JET_err 的基類。AlreadyInitialized 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334228(v=exchg.10).md">EsentAlreadyPreparedException</a></td>
<td>JET_err 的基類。AlreadyPrepared 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334231(v=exchg.10).md">EsentApiException</a></td>
<td>API 例外狀況的基類。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334236(v=exchg.10).md">EsentAttachedDatabaseMismatchException</a></td>
<td>JET_err 的基類。AttachedDatabaseMismatch 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274014(v=exchg.10).md">EsentBackupAbortByServerException</a></td>
<td>JET_err 的基類。BackupAbortByServer 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn273970(v=exchg.10).md">EsentBackupDirectoryNotEmptyException</a></td>
<td>JET_err 的基類。BackupDirectoryNotEmpty 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274026(v=exchg.10).md">EsentBackupInProgressException</a></td>
<td>JET_err 的基類。BackupInProgress 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274032(v=exchg.10).md">EsentBackupNotAllowedYetException</a></td>
<td>JET_err 的基類。BackupNotAllowedYet 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn273987(v=exchg.10).md">EsentBadBackupDatabaseSizeException</a></td>
<td>JET_err 的基類。BadBackupDatabaseSize 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274043(v=exchg.10).md">EsentBadBookmarkException</a></td>
<td>JET_err 的基類。BadBookmark 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn273995(v=exchg.10).md">EsentBadCheckpointSignatureException</a></td>
<td>JET_err 的基類。BadCheckpointSignature 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274004(v=exchg.10).md">EsentBadColumnIdException</a></td>
<td>JET_err 的基類。BadColumnId 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274009(v=exchg.10).md">EsentBadDbSignatureException</a></td>
<td>JET_err 的基類。BadDbSignature 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274059(v=exchg.10).md">EsentBadEmptyPageException</a></td>
<td>JET_err 的基類。BadEmptyPage 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274018(v=exchg.10).md">EsentBadItagSequenceException</a></td>
<td>JET_err 的基類。BadItagSequence 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274072(v=exchg.10).md">EsentBadLogSignatureException</a></td>
<td>JET_err 的基類。BadLogSignature 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274023(v=exchg.10).md">EsentBadLogVersionException</a></td>
<td>JET_err 的基類。BadLogVersion 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274083(v=exchg.10).md">EsentBadPageLinkException</a></td>
<td>JET_err 的基類。BadPageLink 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274033(v=exchg.10).md">EsentBadParentPageLinkException</a></td>
<td>JET_err 的基類。BadParentPageLink 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274093(v=exchg.10).md">EsentBadPatchPageException</a></td>
<td>JET_err 的基類。BadPatchPage 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274044(v=exchg.10).md">EsentBadRestoreTargetInstanceException</a></td>
<td>JET_err 的基類。BadRestoreTargetInstance 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274107(v=exchg.10).md">EsentBadSLVSignatureException</a></td>
<td></td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274053(v=exchg.10).md">EsentBufferTooSmallException</a></td>
<td>JET_err 的基類。BufferTooSmall 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274120(v=exchg.10).md">EsentCallbackFailedException</a></td>
<td>JET_err 的基類。CallbackFailed 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274063(v=exchg.10).md">EsentCallbackNotResolvedException</a></td>
<td>JET_err 的基類。CallbackNotResolved 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274130(v=exchg.10).md">EsentCannotAddFixedVarColumnToDerivedTableException</a></td>
<td>JET_err 的基類。CannotAddFixedVarColumnToDerivedTable 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274074(v=exchg.10).md">EsentCannotBeTaggedException</a></td>
<td>JET_err 的基類。CannotBeTagged 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274139(v=exchg.10).md">EsentCannotDeleteSystemTableException</a></td>
<td>JET_err 的基類。CannotDeleteSystemTable 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274084(v=exchg.10).md">EsentCannotDeleteTemplateTableException</a></td>
<td>JET_err 的基類。CannotDeleteTemplateTable 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274088(v=exchg.10).md">EsentCannotDeleteTempTableException</a></td>
<td>JET_err 的基類。CannotDeleteTempTable 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274157(v=exchg.10).md">EsentCannotDisableVersioningException</a></td>
<td>JET_err 的基類。CannotDisableVersioning 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274099(v=exchg.10).md">EsentCannotIndexException</a></td>
<td>JET_err 的基類。CannotIndex 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274165(v=exchg.10).md">EsentCannotLogDuringRecoveryRedoException</a></td>
<td>JET_err 的基類。CannotLogDuringRecoveryRedo 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274102(v=exchg.10).md">EsentCannotMaterializeForwardOnlySortException</a></td>
<td>JET_err 的基類。CannotMaterializeForwardOnlySort 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274172(v=exchg.10).md">EsentCannotNestDDLException</a></td>
<td>JET_err 的基類。CannotNestDDL 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274174(v=exchg.10).md">EsentCannotNestDistributedTransactionsException</a></td>
<td>JET_err 的基類。CannotNestDistributedTransactions 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274117(v=exchg.10).md">EsentCannotSeparateIntrinsicLVException</a></td>
<td>JET_err 的基類。CannotSeparateIntrinsicLV 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274191(v=exchg.10).md">EsentCatalogCorruptedException</a></td>
<td>JET_err 的基類。CatalogCorrupted 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274132(v=exchg.10).md">EsentCheckpointCorruptException</a></td>
<td>JET_err 的基類。CheckpointCorrupt 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274195(v=exchg.10).md">EsentCheckpointDepthTooDeepException</a></td>
<td>JET_err 的基類。CheckpointDepthTooDeep 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274140(v=exchg.10).md">EsentCheckpointFileNotFoundException</a></td>
<td>JET_err 的基類。CheckpointFileNotFound 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274150(v=exchg.10).md">EsentClientRequestToStopJetServiceException</a></td>
<td>JET_err 的基類。ClientRequestToStopJetService 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274217(v=exchg.10).md">EsentColumnCannotBeCompressedException</a></td>
<td>JET_err 的基類。ColumnCannotBeCompressed 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334250(v=exchg.10).md">EsentColumnDoesNotFitException</a></td>
<td>JET_err 的基類。ColumnDoesNotFit 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274156(v=exchg.10).md">EsentColumnDuplicateException</a></td>
<td>JET_err 的基類。ColumnDuplicate 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274164(v=exchg.10).md">EsentColumnIndexedException</a></td>
<td>JET_err 的基類。ColumnIndexed 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334259(v=exchg.10).md">EsentColumnInRelationshipException</a></td>
<td>JET_err 的基類。ColumnInRelationship 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274180(v=exchg.10).md">EsentColumnInUseException</a></td>
<td>JET_err 的基類。ColumnInUse 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334271(v=exchg.10).md">EsentColumnLongException</a></td>
<td>JET_err 的基類。ColumnLong 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274190(v=exchg.10).md">EsentColumnNoChunkException</a></td>
<td>JET_err 的基類。ColumnNoChunk 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274196(v=exchg.10).md">EsentColumnNotFoundException</a></td>
<td>JET_err 的基類。ColumnNotFound 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334291(v=exchg.10).md">EsentColumnNotUpdatableException</a></td>
<td>JET_err 的基類。ColumnNotUpdatable 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274198(v=exchg.10).md">EsentColumnRedundantException</a></td>
<td>JET_err 的基類。ColumnRedundant 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334298(v=exchg.10).md">EsentColumnTooBigException</a></td>
<td>JET_err 的基類。ColumnTooBig 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274206(v=exchg.10).md">EsentCommittedLogFileCorruptException</a></td>
<td>JET_err 的基類（Base class）。 CommittedLogFileCorrupt 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334311(v=exchg.10).md">EsentCommittedLogFilesMissingException</a></td>
<td>JET_err 的基類（Base class）。 CommittedLogFilesMissing 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274215(v=exchg.10).md">EsentConsistentTimeMismatchException</a></td>
<td>JET_err 的基類。ConsistentTimeMismatch 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334323(v=exchg.10).md">EsentContainerNotEmptyException</a></td>
<td>JET_err 的基類。ContainerNotEmpty 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274225(v=exchg.10).md">EsentCorruptionException</a></td>
<td>損毀例外狀況的基類。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334249(v=exchg.10).md">EsentCurrencyStackOutOfMemoryException</a></td>
<td>JET_err 的基類。CurrencyStackOutOfMemory 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334342(v=exchg.10).md">EsentDatabase200FormatException</a></td>
<td>JET_err 的基類。Database200Format 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334253(v=exchg.10).md">EsentDatabase400FormatException</a></td>
<td>JET_err 的基類。Database400Format 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334350(v=exchg.10).md">EsentDatabase500FormatException</a></td>
<td>JET_err 的基類。Database500Format 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334266(v=exchg.10).md">EsentDatabaseAlreadyRunningMaintenanceException</a></td>
<td>JET_err 的基類。DatabaseAlreadyRunningMaintenance 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334272(v=exchg.10).md">EsentDatabaseAlreadyUpgradedException</a></td>
<td>JET_err 的基類。DatabaseAlreadyUpgraded 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334366(v=exchg.10).md">EsentDatabaseBufferDependenciesCorruptedException</a></td>
<td>JET_err 的基類。DatabaseBufferDependenciesCorrupted 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334279(v=exchg.10).md">EsentDatabaseCorruptedException</a></td>
<td>JET_err 的基類。DatabaseCorrupted 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334384(v=exchg.10).md">EsentDatabaseCorruptedNoRepairException</a></td>
<td>JET_err 的基類。DatabaseCorruptedNoRepair 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334290(v=exchg.10).md">EsentDatabaseDirtyShutdownException</a></td>
<td>JET_err 的基類。DatabaseDirtyShutdown 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334296(v=exchg.10).md">EsentDatabaseDuplicateException</a></td>
<td>JET_err 的基類。DatabaseDuplicate 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334404(v=exchg.10).md">EsentDatabaseFailedIncrementalReseedException</a></td>
<td>JET_err 的基類。DatabaseFailedIncrementalReseed 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334306(v=exchg.10).md">EsentDatabaseFileReadOnlyException</a></td>
<td>JET_err 的基類。DatabaseFileReadOnly 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334396(v=exchg.10).md">EsentDatabaseIdInUseException</a></td>
<td>JET_err 的基類。DatabaseIdInUse 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334412(v=exchg.10).md">EsentDatabaseIncompleteIncrementalReseedException</a></td>
<td>JET_err 的基類。DatabaseIncompleteIncrementalReseed 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334320(v=exchg.10).md">EsentDatabaseIncompleteUpgradeException</a></td>
<td>JET_err 的基類。DatabaseIncompleteUpgrade 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334322(v=exchg.10).md">EsentDatabaseInUseException</a></td>
<td>JET_err 的基類。DatabaseInUse 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334430(v=exchg.10).md">EsentDatabaseInvalidIncrementalReseedException</a></td>
<td>JET_err 的基類。DatabaseInvalidIncrementalReseed 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334450(v=exchg.10).md">EsentDatabaseInvalidNameException</a></td>
<td>JET_err 的基類。DatabaseInvalidName 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334339(v=exchg.10).md">EsentDatabaseInvalidPagesException</a></td>
<td>JET_err 的基類。DatabaseInvalidPages 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334460(v=exchg.10).md">EsentDatabaseInvalidPathException</a></td>
<td>JET_err 的基類。DatabaseInvalidPath 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334349(v=exchg.10).md">EsentDatabaseLeakInSpaceException</a></td>
<td>JET_err 的基類。DatabaseLeakInSpace 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334474(v=exchg.10).md">EsentDatabaseLockedException</a></td>
<td>JET_err 的基類。DatabaseLocked 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334359(v=exchg.10).md">EsentDatabaseLogSetMismatchException</a></td>
<td>JET_err 的基類。DatabaseLogSetMismatch 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334481(v=exchg.10).md">EsentDatabaseNotFoundException</a></td>
<td>JET_err 的基類。DatabaseNotFound 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334483(v=exchg.10).md">EsentDatabasePatchFileMismatchException</a></td>
<td>JET_err 的基類。DatabasePatchFileMismatch 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334374(v=exchg.10).md">EsentDatabaseSharingViolationException</a></td>
<td>JET_err 的基類。DatabaseSharingViolation 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334488(v=exchg.10).md">EsentDatabaseSignInUseException</a></td>
<td>JET_err 的基類。DatabaseSignInUse 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334386(v=exchg.10).md">EsentDatabasesNotFromSameSnapshotException</a></td>
<td>JET_err 的基類。DatabasesNotFromSameSnapshot 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334493(v=exchg.10).md">EsentDatabaseStreamingFileMismatchException</a></td>
<td>JET_err 的基類。DatabaseStreamingFileMismatch 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274227(v=exchg.10).md">EsentDatabaseUnavailableException</a></td>
<td>JET_err 的基類。DatabaseUnavailable 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334392(v=exchg.10).md">EsentDataException</a></td>
<td>資料例外狀況的基類。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334397(v=exchg.10).md">EsentDataHasChangedException</a></td>
<td>JET_err 的基類。DataHasChanged 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274236(v=exchg.10).md">EsentDbTimeCorruptedException</a></td>
<td>JET_err 的基類。DbTimeCorrupted 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334407(v=exchg.10).md">EsentDbTimeTooNewException</a></td>
<td>JET_err 的基類。DbTimeTooNew 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274245(v=exchg.10).md">EsentDbTimeTooOldException</a></td>
<td>JET_err 的基類。DbTimeTooOld 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334413(v=exchg.10).md">EsentDDLNotInheritableException</a></td>
<td>JET_err 的基類。DDLNotInheritable 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274251(v=exchg.10).md">EsentDecompressionFailedException</a></td>
<td>JET_err 的基類。DecompressionFailed 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334424(v=exchg.10).md">EsentDefaultValueTooBigException</a></td>
<td>JET_err 的基類。DefaultValueTooBig 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274267(v=exchg.10).md">EsentDeleteBackupFileFailException</a></td>
<td>JET_err 的基類。DeleteBackupFileFail 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334433(v=exchg.10).md">EsentDensityInvalidException</a></td>
<td>JET_err 的基類。DensityInvalid 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274270(v=exchg.10).md">EsentDerivedColumnCorruptionException</a></td>
<td>JET_err 的基類。DerivedColumnCorruption 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334452(v=exchg.10).md">EsentDirtyShutdownException</a></td>
<td>JET_err 的基類。DirtyShutdown 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274277(v=exchg.10).md">EsentDisabledFunctionalityException</a></td>
<td>JET_err 的基類。DisabledFunctionality 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334464(v=exchg.10).md">EsentDiskException</a></td>
<td>磁片例外狀況的基類。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334461(v=exchg.10).md">EsentDiskFullException</a></td>
<td>JET_err 的基類。DiskFull 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274289(v=exchg.10).md">EsentDiskIOException</a></td>
<td>JET_err 的基類。DiskIO 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274287(v=exchg.10).md">EsentDiskReadVerificationFailureException</a></td>
<td>JET_err 的基類。DiskReadVerificationFailure 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334490(v=exchg.10).md">EsentDistributedTransactionAlreadyPreparedToCommitException</a></td>
<td>JET_err 的基類。DistributedTransactionAlreadyPreparedToCommit 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274293(v=exchg.10).md">EsentDistributedTransactionNotYetPreparedToCommitException</a></td>
<td>JET_err 的基類。DistributedTransactionNotYetPreparedToCommit 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334500(v=exchg.10).md">EsentDTCCallbackUnexpectedErrorException</a></td>
<td>JET_err 的基類。DTCCallbackUnexpectedError 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334508(v=exchg.10).md">EsentDTCMissingCallbackException</a></td>
<td>JET_err 的基類。DTCMissingCallback 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274310(v=exchg.10).md">EsentDTCMissingCallbackOnRecoveryException</a></td>
<td>JET_err 的基類。DTCMissingCallbackOnRecovery 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274239(v=exchg.10).md">EsentEndingRestoreLogTooLowException</a></td>
<td>JET_err 的基類。EndingRestoreLogTooLow 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274309(v=exchg.10).md">EsentEntryPointNotFoundException</a></td>
<td>JET_err 的基類。EntryPointNotFound 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274314(v=exchg.10).md">EsentErrorException</a></td>
<td>ESENT 錯誤例外狀況的基類。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274257(v=exchg.10).md">EsentExclusiveTableLockRequiredException</a></td>
<td>JET_err 的基類。ExclusiveTableLockRequired 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274318(v=exchg.10).md">EsentExistingLogFileHasBadSignatureException</a></td>
<td>JET_err 的基類。ExistingLogFileHasBadSignature 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274260(v=exchg.10).md">EsentExistingLogFileIsNotContiguousException</a></td>
<td>JET_err 的基類。ExistingLogFileIsNotContiguous 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274321(v=exchg.10).md">EsentFatalException</a></td>
<td>嚴重例外狀況的基類。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274291(v=exchg.10).md">EsentFeatureNotAvailableException</a></td>
<td>JET_err 的基類。FeatureNotAvailable 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274324(v=exchg.10).md">EsentFileAccessDeniedException</a></td>
<td>JET_err 的基類。FileAccessDenied 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274332(v=exchg.10).md">EsentFileCloseException</a></td>
<td>JET_err 的基類。FileClose 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274343(v=exchg.10).md">EsentFileCompressedException</a></td>
<td>JET_err 的基類。FileCompressed 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274337(v=exchg.10).md">EsentFileInvalidTypeException</a></td>
<td>JET_err 的基類。FileInvalidType 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274355(v=exchg.10).md">EsentFileIOAbortException</a></td>
<td>JET_err 的基類。FileIOAbort 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274354(v=exchg.10).md">EsentFileIOBeyondEOFException</a></td>
<td>JET_err 的基類。FileIOBeyondEOF 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274360(v=exchg.10).md">EsentFileIOFailException</a></td>
<td>JET_err 的基類。FileIOFail 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274364(v=exchg.10).md">EsentFileIORetryException</a></td>
<td>JET_err 的基類。FileIORetry 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274375(v=exchg.10).md">EsentFileIOSparseException</a></td>
<td>JET_err 的基類。FileIOSparse 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274377(v=exchg.10).md">EsentFileNotFoundException</a></td>
<td>JET_err 的基類。FileNotFound 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274381(v=exchg.10).md">EsentFileSystemCorruptionException</a></td>
<td>JET_err 的基類。FileSystemCorruption 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn274384(v=exchg.10).md">EsentFilteredMoveNotSupportedException</a></td>
<td>JET_err 的基類。FilteredMoveNotSupported 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350411(v=exchg.10).md">EsentFixedDDLException</a></td>
<td>JET_err 的基類。FixedDDL 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350413(v=exchg.10).md">EsentFixedInheritedDDLException</a></td>
<td>JET_err 的基類。FixedInheritedDDL 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350463(v=exchg.10).md">EsentForceDetachNotAllowedException</a></td>
<td>JET_err 的基類。ForceDetachNotAllowed 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350462(v=exchg.10).md">EsentFragmentationException</a></td>
<td>片段例外狀況的基類。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350421(v=exchg.10).md">EsentGivenLogFileHasBadSignatureException</a></td>
<td>JET_err 的基類。GivenLogFileHasBadSignature 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350479(v=exchg.10).md">EsentGivenLogFileIsNotContiguousException</a></td>
<td>JET_err 的基類。GivenLogFileIsNotContiguous 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350477(v=exchg.10).md">EsentIllegalOperationException</a></td>
<td>JET_err 的基類。IllegalOperation 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350488(v=exchg.10).md">EsentInconsistentException</a></td>
<td>不一致例外狀況的基類。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350493(v=exchg.10).md">EsentIndexBuildCorruptedException</a></td>
<td>JET_err 的基類。IndexBuildCorrupted 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350436(v=exchg.10).md">EsentIndexCantBuildException</a></td>
<td>JET_err 的基類。IndexCantBuild 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350438(v=exchg.10).md">EsentIndexDuplicateException</a></td>
<td>JET_err 的基類。IndexDuplicate 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350439(v=exchg.10).md">EsentIndexHasPrimaryException</a></td>
<td>JET_err 的基類。IndexHasPrimary 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350505(v=exchg.10).md">EsentIndexInUseException</a></td>
<td>JET_err 的基類。IndexInUse 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319396(v=exchg.10).md">EsentIndexInvalidDefException</a></td>
<td>JET_err 的基類。IndexInvalidDef 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319399(v=exchg.10).md">EsentIndexMustStayException</a></td>
<td>JET_err 的基類。IndexMustStay 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350459(v=exchg.10).md">EsentIndexNotFoundException</a></td>
<td>JET_err 的基類。IndexNotFound 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319401(v=exchg.10).md">EsentIndexTuplesCannotRetrieveFromIndexException</a></td>
<td>JET_err 的基類。IndexTuplesCannotRetrieveFromIndex 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319411(v=exchg.10).md">EsentIndexTuplesInvalidLimitsException</a></td>
<td>JET_err 的基類。IndexTuplesInvalidLimits 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350474(v=exchg.10).md">EsentIndexTuplesKeyTooSmallException</a></td>
<td>JET_err 的基類。IndexTuplesKeyTooSmall 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319420(v=exchg.10).md">EsentIndexTuplesNonUniqueOnlyException</a></td>
<td>JET_err 的基類。IndexTuplesNonUniqueOnly 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350485(v=exchg.10).md">EsentIndexTuplesSecondaryIndexOnlyException</a></td>
<td>JET_err 的基類。IndexTuplesSecondaryIndexOnly 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350490(v=exchg.10).md">EsentIndexTuplesTextBinaryColumnsOnlyException</a></td>
<td>JET_err 的基類。IndexTuplesTextBinaryColumnsOnly 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319427(v=exchg.10).md">EsentIndexTuplesTooManyColumnsException</a></td>
<td>JET_err 的基類。IndexTuplesTooManyColumns 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319430(v=exchg.10).md">EsentIndexTuplesVarSegMacNotAllowedException</a></td>
<td>JET_err 的基類。IndexTuplesVarSegMacNotAllowed 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350503(v=exchg.10).md">EsentInitInProgressException</a></td>
<td>JET_err.InitInProgress 例外狀況的基類。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319385(v=exchg.10).md">EsentInstanceNameInUseException</a></td>
<td>JET_err 的基類。InstanceNameInUse 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319387(v=exchg.10).md">EsentInstanceUnavailableDueToFatalLogDiskFullException</a></td>
<td>JET_err 的基類。InstanceUnavailableDueToFatalLogDiskFull 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319441(v=exchg.10).md">EsentInstanceUnavailableException</a></td>
<td>JET_err 的基類。InstanceUnavailable 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319452(v=exchg.10).md">EsentInternalErrorException</a></td>
<td>JET_err 的基類。InternalError 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319457(v=exchg.10).md">EsentInTransactionException</a></td>
<td>JET_err 的基類。InTransaction 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319406(v=exchg.10).md">EsentInvalidBackupException</a></td>
<td>JET_err 的基類。InvalidBackup 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319414(v=exchg.10).md">EsentInvalidBackupSequenceException</a></td>
<td>JET_err 的基類。InvalidBackupSequence 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319464(v=exchg.10).md">EsentInvalidBookmarkException</a></td>
<td>JET_err 的基類。InvalidBookmark 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319475(v=exchg.10).md">EsentInvalidBufferSizeException</a></td>
<td>JET_err 的基類。InvalidBufferSize 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319443(v=exchg.10).md">EsentInvalidCodePageException</a></td>
<td>JET_err 的基類。InvalidCodePage 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319487(v=exchg.10).md">EsentInvalidColumnException</a></td>
<td>當資料行轉換失敗時擲回例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319454(v=exchg.10).md">EsentInvalidColumnTypeException</a></td>
<td>JET_err 的基類。InvalidColumnType 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319498(v=exchg.10).md">EsentInvalidCountryException</a></td>
<td>JET_err 的基類。InvalidCountry 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319468(v=exchg.10).md">EsentInvalidCreateDbVersionException</a></td>
<td>JET_err 的基類。InvalidCreateDbVersion 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319507(v=exchg.10).md">EsentInvalidCreateIndexException</a></td>
<td>JET_err 的基類。InvalidCreateIndex 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319474(v=exchg.10).md">EsentInvalidDatabaseException</a></td>
<td>JET_err 的基類。InvalidDatabase 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319512(v=exchg.10).md">EsentInvalidDatabaseIdException</a></td>
<td>JET_err 的基類。InvalidDatabaseId 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319486(v=exchg.10).md">EsentInvalidDatabaseVersionException</a></td>
<td>JET_err 的基類。InvalidDatabaseVersion 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319520(v=exchg.10).md">EsentInvalidFilenameException</a></td>
<td>JET_err 的基類。InvalidFilename 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319518(v=exchg.10).md">EsentInvalidGrbitException</a></td>
<td>JET_err 的基類。InvalidGrbit 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319523(v=exchg.10).md">EsentInvalidIndexIdException</a></td>
<td>JET_err 的基類。InvalidIndexId 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319502(v=exchg.10).md">EsentInvalidInstanceException</a></td>
<td>JET_err 的基類。InvalidInstance 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319529(v=exchg.10).md">EsentInvalidLanguageIdException</a></td>
<td>JET_err 的基類。InvalidLanguageId 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319538(v=exchg.10).md">EsentInvalidLCMapStringFlagsException</a></td>
<td>JET_err 的基類。InvalidLCMapStringFlags 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319536(v=exchg.10).md">EsentInvalidLogDataSequenceException</a></td>
<td>JET_err 的基類。InvalidLogDataSequence 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319548(v=exchg.10).md">EsentInvalidLogDirectoryException</a></td>
<td>JET_err 的基類。InvalidLogDirectory 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319545(v=exchg.10).md">EsentInvalidLoggedOperationException</a></td>
<td>JET_err 的基類。InvalidLoggedOperation 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319554(v=exchg.10).md">EsentInvalidLogSequenceException</a></td>
<td>JET_err 的基類。InvalidLogSequence 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319541(v=exchg.10).md">EsentInvalidNameException</a></td>
<td>JET_err 的基類。InvalidName 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319564(v=exchg.10).md">EsentInvalidObjectException</a></td>
<td>JET_err 的基類。InvalidObject 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319570(v=exchg.10).md">EsentInvalidOnSortException</a></td>
<td>JET_err 的基類。InvalidOnSort 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319571(v=exchg.10).md">EsentInvalidOperationException</a></td>
<td>JET_err 的基類。InvalidOperation 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319601(v=exchg.10).md">EsentInvalidParameterException</a></td>
<td>JET_err 的基類。InvalidParameter 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319577(v=exchg.10).md">EsentInvalidPathException</a></td>
<td>JET_err 的基類。InvalidPath 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319579(v=exchg.10).md">EsentInvalidPlaceholderColumnException</a></td>
<td>JET_err 的基類。InvalidPlaceholderColumn 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334516(v=exchg.10).md">EsentInvalidPrereadException</a></td>
<td>JET_err 的基類。InvalidPreread 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319584(v=exchg.10).md">EsentInvalidSesidException</a></td>
<td>JET_err 的基類。InvalidSesid 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334521(v=exchg.10).md">EsentInvalidSettingsException</a></td>
<td>JET_err 的基類。InvalidSettings 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334526(v=exchg.10).md">EsentInvalidSystemPathException</a></td>
<td>JET_err 的基類。InvalidSystemPath 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334527(v=exchg.10).md">EsentInvalidTableIdException</a></td>
<td>JET_err 的基類。InvalidTableId 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319595(v=exchg.10).md">EsentIOException</a></td>
<td>IO 例外狀況的基類。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319605(v=exchg.10).md">EsentKeyBoundaryException</a></td>
<td>JET_err 的基類。KeyBoundary 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319603(v=exchg.10).md">EsentKeyDuplicateException</a></td>
<td>JET_err 的基類。KeyDuplicate 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334548(v=exchg.10).md">EsentKeyIsMadeException</a></td>
<td>JET_err 的基類。KeyIsMade 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334554(v=exchg.10).md">EsentKeyNotMadeException</a></td>
<td>JET_err 的基類。KeyNotMade 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319610(v=exchg.10).md">EsentKeyTooBigException</a></td>
<td>JET_err 的基類。KeyTooBig 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334565(v=exchg.10).md">EsentKeyTruncatedException</a></td>
<td>JET_err 的基類。KeyTruncated 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334570(v=exchg.10).md">EsentLanguageNotSupportedException</a></td>
<td>JET_err 的基類。LanguageNotSupported 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334571(v=exchg.10).md">EsentLinkNotSupportedException</a></td>
<td>JET_err 的基類。LinkNotSupported 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334573(v=exchg.10).md">EsentLogBufferTooSmallException</a></td>
<td>JET_err 的基類。LogBufferTooSmall 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319628(v=exchg.10).md">EsentLogCorruptDuringHardRecoveryException</a></td>
<td>JET_err 的基類。LogCorruptDuringHardRecovery 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334512(v=exchg.10).md">EsentLogCorruptDuringHardRestoreException</a></td>
<td>JET_err 的基類。LogCorruptDuringHardRestore 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334510(v=exchg.10).md">EsentLogCorruptedException</a></td>
<td>JET_err 的基類。LogCorrupted 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334591(v=exchg.10).md">EsentLogDisabledDueToRecoveryFailureException</a></td>
<td>JET_err 的基類。LogDisabledDueToRecoveryFailure 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334539(v=exchg.10).md">EsentLogDiskFullException</a></td>
<td>JET_err 的基類。LogDiskFull 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334601(v=exchg.10).md">EsentLogFileCorruptException</a></td>
<td>JET_err 的基類。LogFileCorrupt 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334541(v=exchg.10).md">EsentLogFileNotCopiedException</a></td>
<td>JET_err 的基類。LogFileNotCopied 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334545(v=exchg.10).md">EsentLogFilePathInUseException</a></td>
<td>JET_err 的基類。LogFilePathInUse 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334552(v=exchg.10).md">EsentLogFileSizeMismatchDatabasesConsistentException</a></td>
<td>JET_err 的基類。LogFileSizeMismatchDatabasesConsistent 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334627(v=exchg.10).md">EsentLogFileSizeMismatchException</a></td>
<td>JET_err 的基類。LogFileSizeMismatch 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334564(v=exchg.10).md">EsentLogGenerationMismatchException</a></td>
<td>JET_err 的基類。LogGenerationMismatch 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334582(v=exchg.10).md">EsentLoggingDisabledException</a></td>
<td>JET_err 的基類。LoggingDisabled 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334583(v=exchg.10).md">EsentLogReadVerifyFailureException</a></td>
<td>JET_err 的基類。LogReadVerifyFailure 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334645(v=exchg.10).md">EsentLogSectorSizeMismatchDatabasesConsistentException</a></td>
<td>JET_err 的基類。LogSectorSizeMismatchDatabasesConsistent 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334646(v=exchg.10).md">EsentLogSectorSizeMismatchException</a></td>
<td>JET_err 的基類。LogSectorSizeMismatch 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334651(v=exchg.10).md">EsentLogSequenceEndDatabasesConsistentException</a></td>
<td>JET_err 的基類。LogSequenceEndDatabasesConsistent 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334652(v=exchg.10).md">EsentLogSequenceEndException</a></td>
<td>JET_err 的基類。LogSequenceEnd 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334657(v=exchg.10).md">EsentLogTornWriteDuringHardRecoveryException</a></td>
<td>JET_err 的基類。LogTornWriteDuringHardRecovery 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334605(v=exchg.10).md">EsentLogTornWriteDuringHardRestoreException</a></td>
<td>JET_err 的基類。LogTornWriteDuringHardRestore 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334607(v=exchg.10).md">EsentLogWriteFailException</a></td>
<td>JET_err 的基類。LogWriteFail 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334614(v=exchg.10).md">EsentLSAlreadySetException</a></td>
<td>JET_err 的基類。LSAlreadySet 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334617(v=exchg.10).md">EsentLSCallbackNotSpecifiedException</a></td>
<td>JET_err 的基類。LSCallbackNotSpecified 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334676(v=exchg.10).md">EsentLSNotSetException</a></td>
<td>JET_err 的基類。LSNotSet 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334680(v=exchg.10).md">EsentLVCorruptedException</a></td>
<td>JET_err 的基類。LVCorrupted 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334692(v=exchg.10).md">EsentMakeBackupDirectoryFailException</a></td>
<td>JET_err 的基類。MakeBackupDirectoryFail 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334636(v=exchg.10).md">EsentMemoryException</a></td>
<td>記憶體例外狀況的基類。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334701(v=exchg.10).md">EsentMissingCurrentLogFilesException</a></td>
<td>JET_err 的基類。MissingCurrentLogFiles 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334656(v=exchg.10).md">EsentMissingFileToBackupException</a></td>
<td>JET_err 的基類。MissingFileToBackup 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334670(v=exchg.10).md">EsentMissingFullBackupException</a></td>
<td>JET_err 的基類。MissingFullBackup 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334746(v=exchg.10).md">EsentMissingLogFileException</a></td>
<td>JET_err 的基類。MissingLogFile 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334679(v=exchg.10).md">EsentMissingPatchPageException</a></td>
<td>JET_err 的基類。MissingPatchPage 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334685(v=exchg.10).md">EsentMissingPreviousLogFileException</a></td>
<td>JET_err 的基類。MissingPreviousLogFile 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334755(v=exchg.10).md">EsentMissingRestoreLogFilesException</a></td>
<td>JET_err 的基類。MissingRestoreLogFiles 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334758(v=exchg.10).md">EsentMultiValuedColumnMustBeTaggedException</a></td>
<td>JET_err 的基類。MultiValuedColumnMustBeTagged 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334700(v=exchg.10).md">EsentMultiValuedDuplicateAfterTruncationException</a></td>
<td>JET_err 的基類。MultiValuedDuplicateAfterTruncation 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319652(v=exchg.10).md">EsentMultiValuedDuplicateException</a></td>
<td>JET_err 的基類。MultiValuedDuplicate 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334706(v=exchg.10).md">EsentMultiValuedIndexViolationException</a></td>
<td>JET_err 的基類。MultiValuedIndexViolation 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334710(v=exchg.10).md">EsentMustBeSeparateLongValueException</a></td>
<td>JET_err 的基類。MustBeSeparateLongValue 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319638(v=exchg.10).md">EsentMustCommitDistributedTransactionToLevel0Exception</a></td>
<td>JET_err 的基類。MustCommitDistributedTransactionToLevel0 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319640(v=exchg.10).md">EsentMustDisableLoggingForDbUpgradeException</a></td>
<td>JET_err 的基類。MustDisableLoggingForDbUpgrade 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319646(v=exchg.10).md">EsentMustRollbackException</a></td>
<td>JET_err 的基類。MustRollback 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334719(v=exchg.10).md">EsentNoAttachmentsFailedIncrementalReseedException</a></td>
<td>JET_err 的基類。NoAttachmentsFailedIncrementalReseed 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319659(v=exchg.10).md">EsentNoBackupDirectoryException</a></td>
<td>JET_err 的基類。NoBackupDirectory 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334724(v=exchg.10).md">EsentNoBackupException</a></td>
<td>JET_err 的基類。NoBackup 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334726(v=exchg.10).md">EsentNoCurrentIndexException</a></td>
<td>JET_err 的基類。NoCurrentIndex 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334730(v=exchg.10).md">EsentNoCurrentRecordException</a></td>
<td>JET_err 的基類。NoCurrentRecord 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334734(v=exchg.10).md">EsentNotInDistributedTransactionException</a></td>
<td>JET_err 的基類。NotInDistributedTransaction 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334741(v=exchg.10).md">EsentNotInitializedException</a></td>
<td>JET_err 的基類。NotInitialized 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334745(v=exchg.10).md">EsentNotInTransactionException</a></td>
<td>JET_err 的基類。NotInTransaction 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334749(v=exchg.10).md">EsentNTSystemCallFailedException</a></td>
<td>JET_err 的基類。NTSystemCallFailed 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319698(v=exchg.10).md">EsentNullInvalidException</a></td>
<td>JET_err 的基類。NullInvalid 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319701(v=exchg.10).md">EsentNullKeyDisallowedException</a></td>
<td>JET_err 的基類。NullKeyDisallowed 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319723(v=exchg.10).md">EsentObjectDuplicateException</a></td>
<td>JET_err 的基類。ObjectDuplicate 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319660(v=exchg.10).md">EsentObjectNotFoundException</a></td>
<td>JET_err 的基類。ObjectNotFound 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319668(v=exchg.10).md">EsentObsoleteException</a></td>
<td>已淘汰例外狀況的基類。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319719(v=exchg.10).md">EsentOneDatabasePerSessionException</a></td>
<td>JET_err 的基類。OneDatabasePerSession 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319727(v=exchg.10).md">EsentOperationException</a></td>
<td>作業例外狀況的基類。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319729(v=exchg.10).md">EsentOSSnapshotInvalidSequenceException</a></td>
<td>JET_err 的基類。OSSnapshotInvalidSequence 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319741(v=exchg.10).md">EsentOSSnapshotInvalidSnapIdException</a></td>
<td>JET_err 的基類。OSSnapshotInvalidSnapId 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319702(v=exchg.10).md">EsentOSSnapshotNotAllowedException</a></td>
<td>JET_err 的基類。OSSnapshotNotAllowed 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319704(v=exchg.10).md">EsentOSSnapshotTimeOutException</a></td>
<td>JET_err 的基類。OSSnapshotTimeOut 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319752(v=exchg.10).md">EsentOutOfAutoincrementValuesException</a></td>
<td>JET_err 的基類。OutOfAutoincrementValues 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319715(v=exchg.10).md">EsentOutOfBuffersException</a></td>
<td>JET_err 的基類。OutOfBuffers 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319764(v=exchg.10).md">EsentOutOfCursorsException</a></td>
<td>JET_err 的基類。OutOfCursors 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319717(v=exchg.10).md">EsentOutOfDatabaseSpaceException</a></td>
<td>JET_err 的基類。OutOfDatabaseSpace 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319775(v=exchg.10).md">EsentOutOfDbtimeValuesException</a></td>
<td>JET_err 的基類。OutOfDbtimeValues 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319728(v=exchg.10).md">EsentOutOfFileHandlesException</a></td>
<td>JET_err 的基類。OutOfFileHandles 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319790(v=exchg.10).md">EsentOutOfLongValueIDsException</a></td>
<td>JET_err 的基類。OutOfLongValueIDs 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319786(v=exchg.10).md">EsentOutOfMemoryException</a></td>
<td>JET_err 的基類。OutOfMemory 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319746(v=exchg.10).md">EsentOutOfObjectIDsException</a></td>
<td>JET_err 的基類。OutOfObjectIDs 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319807(v=exchg.10).md">EsentOutOfSequentialIndexValuesException</a></td>
<td>JET_err 的基類。OutOfSequentialIndexValues 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319800(v=exchg.10).md">EsentOutOfSessionsException</a></td>
<td>JET_err 的基類。OutOfSessions 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319762(v=exchg.10).md">EsentOutOfThreadsException</a></td>
<td>JET_err 的基類。OutOfThreads 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319768(v=exchg.10).md">EsentPageBoundaryException</a></td>
<td>JET_err 的基類。PageBoundary 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319771(v=exchg.10).md">EsentPageNotInitializedException</a></td>
<td>JET_err 的基類。PageNotInitialized 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319780(v=exchg.10).md">EsentPageSizeMismatchException</a></td>
<td>JET_err 的基類。PageSizeMismatch 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319835(v=exchg.10).md">EsentPartiallyAttachedDBException</a></td>
<td>JET_err 的基類。PartiallyAttachedDB 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319782(v=exchg.10).md">EsentPatchFileMissingException</a></td>
<td>JET_err 的基類。PatchFileMissing 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319785(v=exchg.10).md">EsentPermissionDeniedException</a></td>
<td>JET_err 的基類。PermissionDenied 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319852(v=exchg.10).md">EsentPreviousVersionException</a></td>
<td>JET_err 的基類。PreviousVersion 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319793(v=exchg.10).md">EsentPrimaryIndexCorruptedException</a></td>
<td>JET_err 的基類。PrimaryIndexCorrupted 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319805(v=exchg.10).md">EsentQueryNotSupportedException</a></td>
<td>JET_err 的基類。QueryNotSupported 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319806(v=exchg.10).md">EsentQuotaException</a></td>
<td>配額例外狀況的基類。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319812(v=exchg.10).md">EsentReadLostFlushVerifyFailureException</a></td>
<td>JET_err 的基類。ReadLostFlushVerifyFailure 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319871(v=exchg.10).md">EsentReadPgnoVerifyFailureException</a></td>
<td>JET_err 的基類。ReadPgnoVerifyFailure 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319876(v=exchg.10).md">EsentReadVerifyFailureException</a></td>
<td>JET_err 的基類。ReadVerifyFailure 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319818(v=exchg.10).md">EsentRecordDeletedException</a></td>
<td>JET_err 的基類。RecordDeleted 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319884(v=exchg.10).md">EsentRecordFormatConversionFailedException</a></td>
<td>JET_err 的基類。RecordFormatConversionFailed 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350517(v=exchg.10).md">EsentRecordNoCopyException</a></td>
<td>JET_err 的基類。RecordNoCopy 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350508(v=exchg.10).md">EsentRecordNotDeletedException</a></td>
<td>JET_err 的基類。RecordNotDeleted 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319846(v=exchg.10).md">EsentRecordNotFoundException</a></td>
<td>JET_err 的基類。RecordNotFound 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319853(v=exchg.10).md">EsentRecordPrimaryChangedException</a></td>
<td>JET_err 的基類。RecordPrimaryChanged 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319857(v=exchg.10).md">EsentRecordTooBigException</a></td>
<td>JET_err 的基類。RecordTooBig 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350529(v=exchg.10).md">EsentRecordTooBigForBackwardCompatibilityException</a></td>
<td>JET_err 的基類。RecordTooBigForBackwardCompatibility 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319863(v=exchg.10).md">EsentRecoveredWithErrorsException</a></td>
<td>JET_err 的基類。RecoveredWithErrors 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350538(v=exchg.10).md">EsentRecoveredWithoutUndoDatabasesConsistentException</a></td>
<td>JET_err 的基類。RecoveredWithoutUndoDatabasesConsistent 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350537(v=exchg.10).md">EsentRecoveredWithoutUndoException</a></td>
<td>JET_err 的基類。RecoveredWithoutUndo 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319891(v=exchg.10).md">EsentRecoveryVerifyFailureException</a></td>
<td>JET_err 的基類。RecoveryVerifyFailure 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319858(v=exchg.10).md">EsentRedoAbruptEndedException</a></td>
<td>JET_err 的基類。RedoAbruptEnded 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350548(v=exchg.10).md">EsentRequiredLogFilesMissingException</a></td>
<td>JET_err 的基類。RequiredLogFilesMissing 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn319890(v=exchg.10).md">EsentResource</a></td>
<td>這是所有 esent 資源物件的基類。 此類別的子類別可以配置及釋放非受控資源。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350557(v=exchg.10).md">EsentResourceException</a></td>
<td>資源例外狀況的基類。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350560(v=exchg.10).md">EsentRestoreInProgressException</a></td>
<td>JET_err 的基類。RestoreInProgress 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350584(v=exchg.10).md">EsentRestoreOfNonBackupDatabaseException</a></td>
<td>JET_err 的基類。RestoreOfNonBackupDatabase 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350565(v=exchg.10).md">EsentRfsFailureException</a></td>
<td>JET_err 的基類。RfsFailure 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350589(v=exchg.10).md">EsentRfsNotArmedException</a></td>
<td>JET_err 的基類。RfsNotArmed 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350592(v=exchg.10).md">EsentRollbackErrorException</a></td>
<td>JET_err 的基類。RollbackError 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350571(v=exchg.10).md">EsentRollbackRequiredException</a></td>
<td>JET_err 的基類。RollbackRequired 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350596(v=exchg.10).md">EsentRunningInMultiInstanceModeException</a></td>
<td>JET_err 的基類。RunningInMultiInstanceMode 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350604(v=exchg.10).md">EsentRunningInOneInstanceModeException</a></td>
<td>JET_err 的基類。RunningInOneInstanceMode 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350606(v=exchg.10).md">EsentSecondaryIndexCorruptedException</a></td>
<td>JET_err 的基類。SecondaryIndexCorrupted 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350610(v=exchg.10).md">EsentSectorSizeNotSupportedException</a></td>
<td>JET_err 的基類。SectorSizeNotSupported 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350615(v=exchg.10).md">EsentSeparatedLongValueException</a></td>
<td>JET_err 的基類。SeparatedLongValue 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350621(v=exchg.10).md">EsentSesidTableIdMismatchException</a></td>
<td>JET_err 的基類。SesidTableIdMismatch 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350632(v=exchg.10).md">EsentSessionCoNtextAlreadySetException</a></td>
<td>JET_err 的基類。SessionCoNtextAlreadySet 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350627(v=exchg.10).md">EsentSessionCoNtextNotSetByThisThreadException</a></td>
<td>JET_err 的基類。SessionCoNtextNotSetByThisThread 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350638(v=exchg.10).md">EsentSessionInUseException</a></td>
<td>JET_err 的基類。SessionInUse 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350642(v=exchg.10).md">EsentSessionSharingViolationException</a></td>
<td>JET_err 的基類。SessionSharingViolation 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350646(v=exchg.10).md">EsentSessionWriteConflictException</a></td>
<td>JET_err 的基類。SessionWriteConflict 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350651(v=exchg.10).md">EsentSLVBufferTooSmallException</a></td>
<td></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350654(v=exchg.10).md">EsentSLVColumnCannotDeleteException</a></td>
<td></td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350661(v=exchg.10).md">EsentSLVColumnDefaultValueNotAllowedException</a></td>
<td></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350672(v=exchg.10).md">EsentSLVCorruptedException</a></td>
<td></td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350668(v=exchg.10).md">EsentSLVDatabaseMissingException</a></td>
<td></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350681(v=exchg.10).md">EsentSLVEAListCorruptException</a></td>
<td></td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350686(v=exchg.10).md">EsentSLVEAListTooBigException</a></td>
<td></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350689(v=exchg.10).md">EsentSLVEAListZeroAllocationException</a></td>
<td></td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350725(v=exchg.10).md">EsentSLVFileAccessDeniedException</a></td>
<td></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350728(v=exchg.10).md">EsentSLVFileInUseException</a></td>
<td></td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350694(v=exchg.10).md">EsentSLVFileInvalidPathException</a></td>
<td></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350696(v=exchg.10).md">EsentSLVFileIOException</a></td>
<td></td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334780(v=exchg.10).md">EsentSLVFileNotFoundException</a></td>
<td></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334783(v=exchg.10).md">EsentSLVFileStaleException</a></td>
<td></td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334785(v=exchg.10).md">EsentSLVFileUnknownException</a></td>
<td></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350706(v=exchg.10).md">EsentSLVHeaderBadChecksumException</a></td>
<td></td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334793(v=exchg.10).md">EsentSLVHeaderCorruptedException</a></td>
<td></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334798(v=exchg.10).md">EsentSLVInvalidPathException</a></td>
<td></td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334804(v=exchg.10).md">EsentSLVOwnerMapAlreadyExistsException</a></td>
<td></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350716(v=exchg.10).md">EsentSLVOwnerMapCorruptedException</a></td>
<td></td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350722(v=exchg.10).md">EsentSLVOwnerMapPageNotFoundException</a></td>
<td></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350720(v=exchg.10).md">EsentSLVPagesNotCommittedException</a></td>
<td></td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350724(v=exchg.10).md">EsentSLVPagesNotDeletedException</a></td>
<td></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350715(v=exchg.10).md">EsentSLVPagesNotFreeException</a></td>
<td></td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350735(v=exchg.10).md">EsentSLVPagesNotReservedException</a></td>
<td></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334827(v=exchg.10).md">EsentSLVProviderNotLoadedException</a></td>
<td></td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350740(v=exchg.10).md">EsentSLVProviderVersionMismatchException</a></td>
<td></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334832(v=exchg.10).md">EsentSLVReadVerifyFailureException</a></td>
<td></td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334835(v=exchg.10).md">EsentSLVRootNotSpecifiedException</a></td>
<td></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334837(v=exchg.10).md">EsentSLVRootPathInvalidException</a></td>
<td></td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350749(v=exchg.10).md">EsentSLVRootStillOpenException</a></td>
<td></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350755(v=exchg.10).md">EsentSLVSpaceCorruptedException</a></td>
<td></td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350752(v=exchg.10).md">EsentSLVSpaceWriteConflictException</a></td>
<td></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334850(v=exchg.10).md">EsentSLVStreamingFileAlreadyExistsException</a></td>
<td></td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350758(v=exchg.10).md">EsentSLVStreamingFileFullException</a></td>
<td></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334857(v=exchg.10).md">EsentSLVStreamingFileInUseException</a></td>
<td></td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334870(v=exchg.10).md">EsentSLVStreamingFileMissingException</a></td>
<td></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334768(v=exchg.10).md">EsentSLVStreamingFileNotCreatedException</a></td>
<td></td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334778(v=exchg.10).md">EsentSLVStreamingFileReadOnlyException</a></td>
<td></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334788(v=exchg.10).md">EsentSoftRecoveryOnBackupDatabaseException</a></td>
<td>JET_err 的基類。SoftRecoveryOnBackupDatabase 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334794(v=exchg.10).md">EsentSoftRecoveryOnSnapshotException</a></td>
<td>JET_err 的基類。SoftRecoveryOnSnapshot 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334800(v=exchg.10).md">EsentSpaceHintsInvalidException</a></td>
<td>JET_err 的基類。SpaceHintsInvalid 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334906(v=exchg.10).md">EsentSPAvailExtCacheOutOfMemoryException</a></td>
<td>JET_err 的基類。SPAvailExtCacheOutOfMemory 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334808(v=exchg.10).md">EsentSPAvailExtCacheOutOfSyncException</a></td>
<td>JET_err 的基類。SPAvailExtCacheOutOfSync 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334914(v=exchg.10).md">EsentSPAvailExtCorruptedException</a></td>
<td>JET_err 的基類。SPAvailExtCorrupted 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334917(v=exchg.10).md">EsentSPOwnExtCorruptedException</a></td>
<td>JET_err 的基類。SPOwnExtCorrupted 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334854(v=exchg.10).md">EsentSQLLinkNotSupportedException</a></td>
<td>JET_err 的基類。SQLLinkNotSupported 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334858(v=exchg.10).md">EsentStartingRestoreLogTooHighException</a></td>
<td>JET_err 的基類。StartingRestoreLogTooHigh 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334920(v=exchg.10).md">EsentStateException</a></td>
<td>狀態例外狀況的基類。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334867(v=exchg.10).md">EsentStopwatch</a></td>
<td>提供一組方法和屬性，您可以使用這些方法和屬性來測量執行緒的 ESENT 工作統計資料。 如果最新版本的 ESENT 不支援 <a href="dn351264(v=exchg.10).md">JetGetThreadStats (JET_THREADSTATS) </a> 那麼所有 ESENT 統計資料都會是0。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334874(v=exchg.10).md">EsentStreamingDataNotLoggedException</a></td>
<td>JET_err 的基類。StreamingDataNotLogged 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334878(v=exchg.10).md">EsentSurrogateBackupInProgressException</a></td>
<td>JET_err 的基類。SurrogateBackupInProgress 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334938(v=exchg.10).md">EsentSystemParamsAlreadySetException</a></td>
<td>JET_err.SystemParamsAlreadySet 例外狀況的基類。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334943(v=exchg.10).md">EsentSystemPathInUseException</a></td>
<td>JET_err.SystemPathInUse 例外狀況的基類。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334948(v=exchg.10).md">EsentTableDuplicateException</a></td>
<td>JET_err 的基類。TableDuplicate 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334903(v=exchg.10).md">EsentTableInUseException</a></td>
<td>JET_err 的基類。TableInUse 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334909(v=exchg.10).md">EsentTableLockedException</a></td>
<td>JET_err 的基類。TableLocked 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334941(v=exchg.10).md">EsentTableNotEmptyException</a></td>
<td>JET_err 的基類。TableNotEmpty 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334954(v=exchg.10).md">EsentTaggedNotNullException</a></td>
<td>JET_err 的基類。TaggedNotNull 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334958(v=exchg.10).md">EsentTaskDroppedException</a></td>
<td>JET_err 的基類。TaskDropped 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334964(v=exchg.10).md">EsentTempFileOpenErrorException</a></td>
<td>JET_err 的基類。TempFileOpenError 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334969(v=exchg.10).md">EsentTempPathInUseException</a></td>
<td>JET_err 的基類。TempPathInUse 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334979(v=exchg.10).md">EsentTermInProgressException</a></td>
<td>JET_err 的基類。TermInProgress 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334978(v=exchg.10).md">EsentTestInjectionNotSupportedException</a></td>
<td>JET_err 的基類。TestInjectionNotSupported 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334984(v=exchg.10).md">EsentTooManyActiveUsersException</a></td>
<td>JET_err 的基類。TooManyActiveUsers 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn335011(v=exchg.10).md">EsentTooManyAttachedDatabasesException</a></td>
<td>JET_err 的基類。TooManyAttachedDatabases 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334989(v=exchg.10).md">EsentTooManyColumnsException</a></td>
<td>JET_err 的基類。TooManyColumns 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334994(v=exchg.10).md">EsentTooManyIndexesException</a></td>
<td>JET_err 的基類。TooManyIndexes 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn335021(v=exchg.10).md">EsentTooManyInstancesException</a></td>
<td>JET_err 的基類。TooManyInstances 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn335003(v=exchg.10).md">EsentTooManyIOException</a></td>
<td>JET_err 的基類。TooManyIO 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn334998(v=exchg.10).md">EsentTooManyKeysException</a></td>
<td>JET_err 的基類。TooManyKeys 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350776(v=exchg.10).md">EsentTooManyMempoolEntriesException</a></td>
<td>JET_err 的基類。TooManyMempoolEntries 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350781(v=exchg.10).md">EsentTooManyOpenDatabasesException</a></td>
<td>JET_err 的基類。TooManyOpenDatabases 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350784(v=exchg.10).md">EsentTooManyOpenIndexesException</a></td>
<td>JET_err 的基類。TooManyOpenIndexes 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350787(v=exchg.10).md">EsentTooManyOpenTablesAndCleanupTimedOutException</a></td>
<td>JET_err 的基類。TooManyOpenTablesAndCleanupTimedOut 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350769(v=exchg.10).md">EsentTooManyOpenTablesException</a></td>
<td>JET_err 的基類。TooManyOpenTables 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350779(v=exchg.10).md">EsentTooManySortsException</a></td>
<td>JET_err 的基類。TooManySorts 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350850(v=exchg.10).md">EsentTooManySplitsException</a></td>
<td>JET_err 的基類。TooManySplits 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350799(v=exchg.10).md">EsentTooManyTestInjectionsException</a></td>
<td>JET_err 的基類。TooManyTestInjections 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350809(v=exchg.10).md">EsentTransReadOnlyException</a></td>
<td>JET_err 的基類。TransReadOnly 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350808(v=exchg.10).md">EsentTransTooDeepException</a></td>
<td>JET_err 的基類。TransTooDeep 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350816(v=exchg.10).md">EsentUnicodeLanguageValidationFailureException</a></td>
<td>JET_err 的基類。UnicodeLanguageValidationFailure 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350818(v=exchg.10).md">EsentUnicodeNormalizationNotSupportedException</a></td>
<td>JET_err 的基類。UnicodeNormalizationNotSupported 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350843(v=exchg.10).md">EsentUnicodeTranslationBufferTooSmallException</a></td>
<td>JET_err 的基類。UnicodeTranslationBufferTooSmall 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350826(v=exchg.10).md">EsentUnicodeTranslationFailException</a></td>
<td>JET_err 的基類。UnicodeTranslationFail 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350835(v=exchg.10).md">EsentUnloadableOSFunctionalityException</a></td>
<td>JET_err 的基類。UnloadableOSFunctionality 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350839(v=exchg.10).md">EsentUpdateMustVersionException</a></td>
<td>JET_err 的基類。UpdateMustVersion 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350844(v=exchg.10).md">EsentUpdateNotPreparedException</a></td>
<td>JET_err 的基類。UpdateNotPrepared 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350849(v=exchg.10).md">EsentUsageException</a></td>
<td>使用例外狀況的基類。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn335007(v=exchg.10).md">EsentVersion</a></td>
<td>提供所使用之 ESENT 版本的相關資訊。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350862(v=exchg.10).md">EsentVersionStoreEntryTooBigException</a></td>
<td>JET_err 的基類。VersionStoreEntryTooBig 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350869(v=exchg.10).md">EsentVersionStoreOutOfMemoryAndCleanupTimedOutException</a></td>
<td>JET_err 的基類。VersionStoreOutOfMemoryAndCleanupTimedOut 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350874(v=exchg.10).md">EsentVersionStoreOutOfMemoryException</a></td>
<td>JET_err 的基類。VersionStoreOutOfMemory 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350876(v=exchg.10).md">EsentWriteConflictException</a></td>
<td>JET_err 的基類。WriteConflict 例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350897(v=exchg.10).md">EsentWriteConflictPrimaryIndexException</a></td>
<td>JET_err 的基類。WriteConflictPrimaryIndex 例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350880(v=exchg.10).md">FloatColumnValue</a></td>
<td><a href="/dotnet/api/system.single">單一</a>資料行值。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350902(v=exchg.10).md">GuidColumnValue</a></td>
<td><a href="/dotnet/api/system.guid">Guid</a>資料行值。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350919(v=exchg.10).md">IndexInfo</a></td>
<td>一個 esent 索引的相關資訊。 這不是 interop 類別，而是由中繼資料 helper 方法所使用。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350912(v=exchg.10).md">IndexSegment</a></td>
<td>描述索引的一個區段。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350923(v=exchg.10).md">執行個體</a></td>
<td>封裝可處置物件中之 <a href="hh564593(v=exchg.10).md">JET_INSTANCE</a> 的類別。 實例必須最後關閉，且關閉實例會釋放實例的所有其他資源。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350942(v=exchg.10).md">InstanceParameters</a></td>
<td>這個類別會提供屬性，以在 ESENT 實例上設定和取得系統參數。 這個類別提供靜態屬性來設定和取得每個實例的 ESENT 系統參數。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn351017(v=exchg.10).md">Int16ColumnValue</a></td>
<td><a href="/dotnet/api/system.int16">Int16</a>資料行值。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn350992(v=exchg.10).md">Int32ColumnValue</a></td>
<td><a href="/dotnet/api/system.int32">Int32</a>資料行值。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn351016(v=exchg.10).md">Int64ColumnValue</a></td>
<td><a href="/dotnet/api/system.int64">Int64</a>資料行值。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn335045(v=exchg.10).md">JET_COLUMNBASE</a></td>
<td>描述 ESENT 資料庫之資料表中的資料行。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn335028(v=exchg.10).md">JET_COLUMNCREATE</a></td>
<td>描述 ESENT 資料庫之資料表中的資料行。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn335038(v=exchg.10).md">JET_COLUMNDEF</a></td>
<td>描述 ESENT 資料庫之資料表中的資料行。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn335047(v=exchg.10).md">JET_COLUMNLIST</a></td>
<td>臨時表的相關資訊，其中包含指定資料表之所有資料行的相關資訊。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn335053(v=exchg.10).md">JET_CONDITIONALCOLUMN</a></td>
<td>定義如何針對指定的索引執行條件式索引編制。 條件式索引僅包含符合指定條件之資料列的索引項目目。 不過，條件資料行不是索引索引鍵的一部分，而只會控制索引項目是否存在。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn335061(v=exchg.10).md">JET_CONVERT</a></td>
<td><strong>已淘汰。</strong> JetCompact (的轉換選項 <a href="dn292112(v=exchg.10).md">JET_SESID、字串、字串、JET_PFNSTATUS、JET_CONVERT、CompactGrbit) </a>。 這項功能已在 Windows Server 2003 中停用。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="hh538867(v=exchg.10).md">JET_DBINFOMISC</a></td>
<td>保存資料庫的其他相關資訊。 這是包含在資料庫標頭中的資訊。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a></td>
<td>使用 JetEnumerateColumns 函數來列舉記錄的資料行值。 JetEnumerateColumns 會傳回 JET_ENUMCOLUMNVALUE 結構的陣列。 陣列會在使用提供給該函式之回呼配置的記憶體中傳回。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn335139(v=exchg.10).md">JET_ENUMCOLUMNID</a></td>
<td>當使用 JetEnumerateColumns 函式時，列舉一組特定的資料行，並選擇性地列舉這些資料行的一組特定的多重值。 JetEnumerateColumns 會選擇性地採用 JET_ENUMCOLUMNID 結構的陣列。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn335142(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a></td>
<td>使用 JetEnumerateColumns 函數來列舉記錄的資料行值。 <a href="dn292148(v=exchg.10).md">JetEnumerateColumns (JET_SESID、JET_TABLEID、Int32、[]、int32、[]、JET_PFNREALLOC、IntPtr、int32、EnumerateColumnsGrbit) </a> 會傳回 JET_ENUMCOLUMNVALUE 結構的陣列。 陣列會在使用提供給該函式之回呼配置的記憶體中傳回。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn335112(v=exchg.10).md">JET_INDEXCREATE</a></td>
<td>包含在 ESE 資料庫的資料上建立索引所需的資訊。 包含在 ESE 資料庫的資料上建立索引所需的資訊。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a></td>
<td>臨時表的相關資訊，其中包含指定資料表之所有索引的相關資訊。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn335175(v=exchg.10).md">JET_INDEXRANGE</a></td>
<td>識別搭配 JetIntersectIndexes 函式使用的索引範圍。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn335182(v=exchg.10).md">JET_INSTANCE_INFO</a></td>
<td>當搭配 JetGetInstanceInfo 和 JetOSSnapshotFreeze 函數使用時，接收有關執行中資料庫實例的資訊。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn335219(v=exchg.10).md">JET_OBJECTINFO</a></td>
<td>JET_OBJECTINFO 結構會保存物件的相關資訊。 資料表是目前唯一支援的物件類型。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn335206(v=exchg.10).md">JET_OBJECTLIST</a></td>
<td>臨時表的相關資訊，其中包含指定資料庫的所有資料表的相關資訊。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn335223(v=exchg.10).md">JET_RECORDLIST</a></td>
<td>臨時表的相關資訊，其中包含指定資料表之所有索引的相關資訊。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn335256(v=exchg.10).md">JET_RECPOS</a></td>
<td>表示索引內的小數位置。 這是由 JetGotoPosition 和 JetGetRecordPosition 所使用。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn335277(v=exchg.10).md">JET_RETINFO</a></td>
<td>包含 JetRetrieveColumn 的選擇性輸入和輸出參數。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn351033(v=exchg.10).md">JET_RETRIEVECOLUMN</a></td>
<td>包含 <a href="dn334004(v=exchg.10).md">JetRetrieveColumns (JET_SESID、JET_TABLEID、[]、Int32) </a>的輸入和輸出參數。 結構中的欄位描述要取出的資料行值、如何取出它，以及要儲存結果的位置。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn335235(v=exchg.10).md">JET_RSTINFO</a></td>
<td>包含 JetRetrieveColumn 的選擇性輸入和輸出參數。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn351048(v=exchg.10).md">JET_RSTMAP</a></td>
<td>在復原期間啟用儲存在交易記錄中的資料庫檔案路徑的對應。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn335260(v=exchg.10).md">JET_SETCOLUMN</a></td>
<td>包含 <a href="dn334006(v=exchg.10).md">JetSetColumns (JET_SESID、JET_TABLEID、[]、Int32) </a>的輸入和輸出參數。 結構中的欄位描述要設定的資料行值、如何設定它，以及要在哪裡取得資料行集資料。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn351059(v=exchg.10).md">JET_SETINFO</a></td>
<td>JetSetColumn 的設定。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn351044(v=exchg.10).md">JET_SNPROG</a></td>
<td>包含長時間執行之作業進度的相關資訊。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn351095(v=exchg.10).md">JET_SPACEHINTS</a></td>
<td>描述 ESENT 資料庫之資料表中的資料行。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn351072(v=exchg.10).md">JET_TABLECREATE</a></td>
<td>包含在 ESE 資料庫中建立資料表所需的資訊。 包含在 ESE 資料庫中建立資料表所需的資訊。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn351106(v=exchg.10).md">JET_UNICODEINDEX</a></td>
<td>自訂在 Unicode 資料行上建立索引時，如何將 Unicode 資料正規化。 自訂在 Unicode 資料行上建立索引時，如何將 Unicode 資料正規化。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn351164(v=exchg.10).md">工作階段</a></td>
<td>封裝可處置物件中之 JET_SESID 的類別。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn351135(v=exchg.10).md">StringColumnValue</a></td>
<td>Unicode 字串資料行值。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn351139(v=exchg.10).md">SystemParameters</a></td>
<td>ESENT API 的常數。 這些都不需要透過系統參數進行查閱。 此類別提供靜態屬性來設定和取得全域 ESENT 系統參數。 此類別提供靜態屬性來設定和取得全域 ESENT 系統參數。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn351163(v=exchg.10).md">資料表</a></td>
<td>封裝可處置物件中之 JET_TABLEID 的類別。 這會開啟現有的資料表。 若要建立資料表，請使用 JetCreateTable 方法。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn351174(v=exchg.10).md">交易</a></td>
<td>在 JET_SESID 上封裝交易的類別。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn351247(v=exchg.10).md">UInt16ColumnValue</a></td>
<td><a href="/dotnet/api/system.uint16">UInt16</a>資料行值。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn351251(v=exchg.10).md">UInt32ColumnValue</a></td>
<td><a href="/dotnet/api/system.uint32">UInt32</a>資料行值。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn351190(v=exchg.10).md">UInt64ColumnValue</a></td>
<td><a href="/dotnet/api/system.uint64">UInt64</a>資料行值。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="公用類別" alt="Public class" /></td>
<td><a href="dn351191(v=exchg.10).md">更新</a></td>
<td>封裝 JET_TABLEID 上之更新的類別。</td>
</tr>
</tbody>
</table>


## <a name="structures"></a>結構

<table>
<thead>
<tr class="header">
<th> </th>
<th>結構</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596136.pubstructure(exchg.10).gif" title="公用結構" alt="Public structure" /></td>
<td><a href="hh577892(v=exchg.10).md">JET_BKINFO</a></td>
<td>保存有關特定備份事件的資料集合。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubstructure(exchg.10).gif" title="公用結構" alt="Public structure" /></td>
<td><a href="hh557662(v=exchg.10).md">JET_BKLOGTIME</a></td>
<td>描述備份發生的日期/時間。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubstructure(exchg.10).gif" title="公用結構" alt="Public structure" /></td>
<td><a href="hh564510(v=exchg.10).md">JET_COLUMNID</a></td>
<td>JET_COLUMNID 識別資料表內的資料行。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubstructure(exchg.10).gif" title="公用結構" alt="Public structure" /></td>
<td><a href="hh596176(v=exchg.10).md">JET_DBID</a></td>
<td>JET_DBID 包含資料庫的控制碼。 資料庫控制碼是用來管理資料庫的架構。 它也可以用來管理該資料庫內的資料表。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubstructure(exchg.10).gif" title="公用結構" alt="Public structure" /></td>
<td><a href="hh558081(v=exchg.10).md">JET_HANDLE</a></td>
<td>JET_HANDLE 包含泛型控制碼。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubstructure(exchg.10).gif" title="公用結構" alt="Public structure" /></td>
<td><a href="hh557060(v=exchg.10).md">JET_INDEXID</a></td>
<td>保存索引識別碼。 索引識別碼是用來加速使用 JetSetCurrentIndex 來選取目前索引的提示。 當資料表的索引數量非常龐大時，最有用。 您可以使用 JetGetIndexInfo 或 JetGetTableIndexInfo 來取出索引識別碼。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubstructure(exchg.10).gif" title="公用結構" alt="Public structure" /></td>
<td><a href="hh564593(v=exchg.10).md">JET_INSTANCE</a></td>
<td>JET_INSTANCE 包含資料庫實例的控制碼，可用於呼叫 JET API。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubstructure(exchg.10).gif" title="公用結構" alt="Public structure" /></td>
<td><a href="hh578063(v=exchg.10).md">JET_LGPOS</a></td>
<td>描述記錄順序中的位移。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubstructure(exchg.10).gif" title="公用結構" alt="Public structure" /></td>
<td><a href="hh557188(v=exchg.10).md">JET_LOGTIME</a></td>
<td>描述日期/時間。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubstructure(exchg.10).gif" title="公用結構" alt="Public structure" /></td>
<td><a href="hh557499(v=exchg.10).md">JET_LS</a></td>
<td>ESENT 控制碼的本機儲存體。 由 <a href="dn292177(v=exchg.10).md">JetGetLS (JET_SESID、JET_TABLEID、JET_LS、LsGrbit) </a> 和 <a href="dn334015(v=exchg.10).md">JetSetLS (JET_SESID、JET_TABLEID、JET_LS、LsGrbit) </a>使用。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubstructure(exchg.10).gif" title="公用結構" alt="Public structure" /></td>
<td><a href="hh558483(v=exchg.10).md">JET_OSSNAPID</a></td>
<td>JET_OSSNAPID 包含資料庫快照集的控制碼。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubstructure(exchg.10).gif" title="公用結構" alt="Public structure" /></td>
<td><a href="hh596745(v=exchg.10).md">JET_SESID</a></td>
<td>JET_SESID 包含會話的控制碼，可用於呼叫 JET APIr。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubstructure(exchg.10).gif" title="公用結構" alt="Public structure" /></td>
<td><a href="hh564644(v=exchg.10).md">JET_SIGNATURE</a></td>
<td>JET_SIGNATURE 結構包含可唯一識別資料庫或記錄檔順序的資訊。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubstructure(exchg.10).gif" title="公用結構" alt="Public structure" /></td>
<td><a href="hh566310(v=exchg.10).md">JET_TABLEID</a></td>
<td>JET_TABLEID 包含資料庫資料指標的控制碼，可用於呼叫 JET API。 資料指標只能搭配用來開啟該資料指標的會話使用。</td>
</tr>
</tbody>
</table>


## <a name="interfaces"></a>介面

<table>
<thead>
<tr class="header">
<th> </th>
<th>介面</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596136.pubinterface(exchg.10).gif" title="公用介面" alt="Public interface" /></td>
<td><a href="hh578046(v=exchg.10).md">IContentEquatable &lt; T&gt;</a></td>
<td>物件的介面，其內容可以彼此比較。 這應該用於覆寫 Equals () 的可變參考物件的相等比較，而 GetHashCode () 並不是個好主意。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubinterface(exchg.10).gif" title="公用介面" alt="Public interface" /></td>
<td><a href="hh565368(v=exchg.10).md">IDeepCloneable &lt; T&gt;</a></td>
<td>可以複製之物件的介面。 這會建立物件的深層複本。 它是用來複製中繼資料物件。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubinterface(exchg.10).gif" title="公用介面" alt="Public interface" /></td>
<td><a href="hh596687(v=exchg.10).md">IJET_LOGTIME</a></td>
<td>JET_LOGTIME 和 JET_BKLOGTIME 之間的通用方法介面。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubinterface(exchg.10).gif" title="公用介面" alt="Public interface" /></td>
<td><a href="hh578599(v=exchg.10).md">INullableJetStruct</a></td>
<td>可為 null (可以有 null 值的 Jet 結構介面) 。</td>
</tr>
</tbody>
</table>


## <a name="delegates"></a>委派

<table>
<thead>
<tr class="header">
<th> </th>
<th>代理人</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596136.pubdelegate(exchg.10).gif" title="公用委派" alt="Public delegate" /></td>
<td><a href="hh566065(v=exchg.10).md">JET_CALLBACK</a></td>
<td>資料庫引擎使用的多用途回呼函式，用來通知應用程式涉及線上磁碟重組和資料指標狀態通知。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubdelegate(exchg.10).gif" title="公用委派" alt="Public delegate" /></td>
<td><a href="hh566077(v=exchg.10).md">JET_PFNREALLOC</a></td>
<td>JetEnumerateColumns 用來為其輸出緩衝區配置記憶體的回呼。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubdelegate(exchg.10).gif" title="公用委派" alt="Public delegate" /></td>
<td><a href="hh565966(v=exchg.10).md">JET_PFNSTATUS</a></td>
<td>接收長時間執行之作業進度的相關資訊，例如磁碟重組、備份或還原作業。 在這類作業期間，資料庫引擎會呼叫此回呼函數，以提供作業進度的更新。</td>
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
<td><a href="hh579378(v=exchg.10).md">AttachDatabaseGrbit</a></td>
<td>JetAttachDatabase 的選項。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh557664(v=exchg.10).md">BackupGrbit</a></td>
<td><a href="dn292102(v=exchg.10).md">JetBackupInstance (JET_INSTANCE、String、BackupGrbit JET_PFNSTATUS) </a>的選項。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh557018(v=exchg.10).md">BeginExternalBackupGrbit</a></td>
<td><a href="dn292104(v=exchg.10).md">JetBeginExternalBackupInstance (JET_INSTANCE、BeginExternalBackupGrbit) </a>的選項。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh558568(v=exchg.10).md">BeginTransactionGrbit</a></td>
<td><a href="dn292106(v=exchg.10).md">JetBeginTransaction2 (JET_SESID、BeginTransactionGrbit) </a>的選項。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh578203(v=exchg.10).md">CloseDatabaseGrbit</a></td>
<td><a href="dn292107(v=exchg.10).md">JetCloseDatabase (JET_SESID、JET_DBID、CloseDatabaseGrbit) </a>的選項。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh578986(v=exchg.10).md">ColumndefGrbit</a></td>
<td>JET_COLUMNDEF 結構的選項。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh564415(v=exchg.10).md">CommitTransactionGrbit</a></td>
<td>JetCommitTransaction 的選項。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh556919(v=exchg.10).md">CompactGrbit</a></td>
<td><a href="dn292112(v=exchg.10).md">JetCompact (的選項 JET_SESID、字串、字串、JET_PFNSTATUS、JET_CONVERT、CompactGrbit) </a>。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh578990(v=exchg.10).md">ConditionalColumnGrbit</a></td>
<td>JET_CONDITIONALCOLUMN 結構的選項。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh596559(v=exchg.10).md">CreateDatabaseGrbit</a></td>
<td><a href="dn292118(v=exchg.10).md">JetCreateDatabase (JET_SESID、string、string、JET_DBID、CreateDatabaseGrbit) </a>的選項。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh578433(v=exchg.10).md">CreateIndexGrbit</a></td>
<td>JetCreateIndex 的選項。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh566808(v=exchg.10).md">CreateInstanceGrbit</a></td>
<td>JetCreateInstance2 的選項。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh566466(v=exchg.10).md">CreateTableColumnIndexGrbit</a></td>
<td>JetCreateTableColumnIndex 的選項。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh596803(v=exchg.10).md">DefragGrbit</a></td>
<td><a href="dn292130(v=exchg.10).md">JetDefragment (JET_SESID、JET_DBID、String、int32、int32、DefragGrbit) </a>的選項。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh565122(v=exchg.10).md">DeleteColumnGrbit</a></td>
<td><a href="dn292132(v=exchg.10).md">JetDeleteColumn2 (JET_SESID、JET_TABLEID、String、DeleteColumnGrbit) </a>的選項。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="dn334195(v=exchg.10).md">DetachDatabaseGrbit</a></td>
<td><a href="dn292136(v=exchg.10).md">JetDetachDatabase2 (JET_SESID、String、DetachDatabaseGrbit) </a>的選項。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh558129(v=exchg.10).md">DupCursorGrbit</a></td>
<td><a href="dn292137(v=exchg.10).md">JetDupCursor (JET_SESID、JET_TABLEID、JET_TABLEID、DupCursorGrbit) </a>的選項。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh566745(v=exchg.10).md">EndExternalBackupGrbit</a></td>
<td><a href="dn292142(v=exchg.10).md">JetEndExternalBackupInstance (JET_INSTANCE) </a>的選項。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh578244(v=exchg.10).md">EndSessionGrbit</a></td>
<td>JetEndSession 的選項。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh566564(v=exchg.10).md">EnumerateColumnsGrbit</a></td>
<td>JetEnumerateColumns 的選項。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh565476(v=exchg.10).md">EscrowUpdateGrbit</a></td>
<td>JetEscrowUpdate 的選項。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="dn350898(v=exchg.10).md">EventLoggingLevels</a></td>
<td>EventLoggingLevel 的選項。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh578647(v=exchg.10).md">GetLockGrbit</a></td>
<td>JetGetLock 的選項。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh565815(v=exchg.10).md">GetRecordSizeGrbit</a></td>
<td><a href="dn335320(v=exchg.10).md">JetGetRecordSize (JET_SESID、JET_TABLEID、JET_RECSIZE、GetRecordSizeGrbit) </a>的選項。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh564940(v=exchg.10).md">GetSecondaryIndexBookmarkGrbit</a></td>
<td><a href="dn292180(v=exchg.10).md">JetGetSecondaryIndexBookmark (JET_SESID、JET_TABLEID、[]、int32、int32、[]、int32、int32、GetSecondaryIndexBookmarkGrbit) </a>的選項。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh596145(v=exchg.10).md">GotoSecondaryIndexBookmarkGrbit</a></td>
<td><a href="dn292205(v=exchg.10).md">JetGotoSecondaryIndexBookmark (JET_SESID、JET_TABLEID、[]、int32、[]、int32、GotoSecondaryIndexBookmarkGrbit) </a>的選項。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh565607(v=exchg.10).md">IdleGrbit</a></td>
<td><a href="dn292208(v=exchg.10).md">JetIdle (JET_SESID、IdleGrbit) </a>的選項。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a></td>
<td>索引鍵定義 grbits。 在抓取索引的相關資訊時使用。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh558064(v=exchg.10).md">IndexRangeGrbit</a></td>
<td>JET_INDEXRANGE 物件的選項。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh596658(v=exchg.10).md">InitGrbit</a></td>
<td><a href="dn292214(v=exchg.10).md">JetInit2 (JET_INSTANCE、InitGrbit) </a>的選項。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh577525(v=exchg.10).md">IntersectIndexesGrbit</a></td>
<td>JetIntersectIndexes 的選項。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh564847(v=exchg.10).md">JET_cbtyp</a></td>
<td>要報告的進度類型。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh577895(v=exchg.10).md">JET_coltyp</a></td>
<td>ESENT 資料行類型。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh558581(v=exchg.10).md">JET_CP</a></td>
<td>ESENT 資料行的字碼頁。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh163267(v=exchg.10).md">JET_DbInfo</a></td>
<td>用於抓取資料庫資訊的資訊層級。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh578316(v=exchg.10).md">JET_dbstate</a></td>
<td><a href="hh538867(v=exchg.10).md">JET_DBINFOMISC</a>) 中使用的資料庫狀態 (。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh564840(v=exchg.10).md">JET_err</a></td>
<td>ESENT 錯誤碼。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="dn335150(v=exchg.10).md">JET_ExceptionAction</a></td>
<td>要搭配 JET_paramExceptionAction 使用的常數。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh566739(v=exchg.10).md">JET_filetype</a></td>
<td>Esent 檔案類型。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh565119(v=exchg.10).md">JET_IdxInfo</a></td>
<td>使用 JetGetIndexInfo 取得索引資訊的資訊層級。 和 JetGetTableIndexInfo。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh558184(v=exchg.10).md">JET_Move</a></td>
<td>JetMove 的位移。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh565069(v=exchg.10).md">JET_objtyp</a></td>
<td>ESENT 物件的型別。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh596135(v=exchg.10).md">JET_param</a></td>
<td>ESENT 系統參數。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh557183(v=exchg.10).md">JET_prep</a></td>
<td>更新 JetPrepareUpdate 的類型。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh577944(v=exchg.10).md">JET_SNP</a></td>
<td>報告進度的作業類型。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh577987(v=exchg.10).md">JET_SNT</a></td>
<td>要報告的進度類型。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh557667(v=exchg.10).md">JET_TblInfo</a></td>
<td>使用 JetGetTableInfo 來抓取資料表資訊的資訊層級。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh557250(v=exchg.10).md">JET_wrn</a></td>
<td>ESENT 警告碼。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh579487(v=exchg.10).md">LsGrbit</a></td>
<td><a href="dn334015(v=exchg.10).md">JetSetLS (JET_SESID、JET_TABLEID、JET_LS、LsGrbit) </a>和<a href="dn292177(v=exchg.10).md">JetGetLS (JET_SESID、JET_TABLEID、JET_LS、LsGrbit) </a>的選項。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh578182(v=exchg.10).md">MakeKeyGrbit</a></td>
<td>JetMakeKey 的選項。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh558238(v=exchg.10).md">MoveGrbit</a></td>
<td>JetMove 的選項。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh566138(v=exchg.10).md">ObjectInfoFlags</a></td>
<td> (資料表) 之 ESENT 物件的旗標。 用於 <a href="dn335219(v=exchg.10).md">JET_OBJECTINFO</a>。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh163294(v=exchg.10).md">ObjectInfoGrbit</a></td>
<td><a href="dn335219(v=exchg.10).md">JET_OBJECTINFO</a>中使用的資料表選項。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh579532(v=exchg.10).md">OpenDatabaseGrbit</a></td>
<td><a href="dn292219(v=exchg.10).md">JetOpenDatabase (JET_SESID、string、string、JET_DBID、OpenDatabaseGrbit) </a>的選項。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh557460(v=exchg.10).md">OpenTableGrbit</a></td>
<td>JetOpenTable 的選項。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh577800(v=exchg.10).md">RenameColumnGrbit</a></td>
<td><a href="dn332990(v=exchg.10).md">JetRenameColumn (JET_SESID、JET_TABLEID、字串、字串、RenameColumnGrbit) </a>的選項。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh596202(v=exchg.10).md">ResetTableSequentialGrbit</a></td>
<td>JetResetTableSequential 的選項。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh578120(v=exchg.10).md">RetrieveColumnGrbit</a></td>
<td>JetRetrieveColumn 的選項。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh564639(v=exchg.10).md">RetrieveKeyGrbit</a></td>
<td>JetRetrieveKey 的選項。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh565408(v=exchg.10).md">RollbackTransactionGrbit</a></td>
<td>JetRollbackTransaction 的選項。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh566176(v=exchg.10).md">SeekGrbit</a></td>
<td>JetSeek 的選項。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh596297(v=exchg.10).md">SetColumnDefaultValueGrbit</a></td>
<td><a href="dn334010(v=exchg.10).md">JetSetColumnDefaultValue (JET_SESID、JET_DBID、string、string、[]、Int32、SetColumnDefaultValueGrbit) </a>的選項。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh538951(v=exchg.10).md">SetColumnGrbit</a></td>
<td>JetSetColumn 的選項。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh558524(v=exchg.10).md">SetCurrentIndexGrbit</a></td>
<td><a href="dn334005(v=exchg.10).md">JetSetCurrentIndex2 (JET_SESID、JET_TABLEID、string、SetCurrentIndexGrbit) </a>和<a href="dn334012(v=exchg.10).md">JetSetCurrentIndex3 (JET_SESID、JET_TABLEID、string、SetCurrentIndexGrbit、Int32) </a>的選項。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh558634(v=exchg.10).md">SetIndexRangeGrbit</a></td>
<td>JetSetIndexRange 的選項。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh565734(v=exchg.10).md">SetTableSequentialGrbit</a></td>
<td>JetSetTableSequential 的選項。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh558163(v=exchg.10).md">SnapshotFreezeGrbit</a></td>
<td><a href="dn332998(v=exchg.10).md">JetOSSnapshotFreeze (JET_OSSNAPID、Int32、[]、SnapshotFreezeGrbit) </a>的選項。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh566001(v=exchg.10).md">SnapshotPrepareGrbit</a></td>
<td><a href="dn292235(v=exchg.10).md">JetOSSnapshotPrepare (JET_OSSNAPID、SnapshotPrepareGrbit) </a>的選項。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh579066(v=exchg.10).md">SnapshotThawGrbit</a></td>
<td><a href="dn332986(v=exchg.10).md">JetOSSnapshotThaw (JET_OSSNAPID、SnapshotThawGrbit) </a>的選項。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh163400(v=exchg.10).md">SpaceHintsGrbit</a></td>
<td><a href="dn351095(v=exchg.10).md">JET_SPACEHINTS</a>的選項。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh558517(v=exchg.10).md">TempTableGrbit</a></td>
<td>建立臨時表的選項。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="公用列舉類型" alt="Public enumeration" /></td>
<td><a href="hh577872(v=exchg.10).md">TermGrbit</a></td>
<td><a href="dn334037(v=exchg.10).md">JetTerm2 (JET_INSTANCE、TermGrbit) </a>的選項。</td>
</tr>
</tbody>
</table>
