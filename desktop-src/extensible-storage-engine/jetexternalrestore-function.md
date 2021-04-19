---
description: 深入瞭解： JetExternalRestore 函數
title: JetExternalRestore 函式
TOCTitle: JetExternalRestore Function
ms:assetid: c930689a-3ea6-4c5a-9318-76f519f23343
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294088(v=EXCHG.10)
ms:contentKeyID: 32765703
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetExternalRestoreA
- JetExternalRestore
- JetExternalRestoreW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 087949817ac0bcbe2effe2ff136a6ce80084daa2
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "106981866"
---
# <a name="jetexternalrestore-function"></a>JetExternalRestore 函式


_**適用于：** Windows |Windows Server_

## <a name="jetexternalrestore-function"></a>JetExternalRestore 函式

**JetExternalRestore** 函式會還原使用外部備份 api 所建立的外部備份，並指定在還原過程中重新執行的記錄檔編號範圍。 這稱為「硬復原」，類似于 [JetInit](./jetinit-function.md) 函式所執行的軟復原。

```cpp
JET_ERR JET_API JetExternalRestore(
  __in          JET_PSTR szCheckpointFilePath,
  __in          JET_PSTR szLogPath,
  __in_opt      JET_RSTMAP* rgrstmap,
  __in          long crstfilemap,
  __in          JET_PSTR szBackupLogPath,
  __in          long genLow,
  __in          long genHigh,
  __in          JET_PFNSTATUS pfn
);
```

### <a name="parameters"></a>參數

*szCheckpointFilePath*

如果未指定 *szTargetInstanceCheckpointPath* ，或已經有使用中或執行中的實例時，要在復原期間使用的檢查點檔案的路徑。

*szLogPath*

最後一個階段記錄檔的路徑或目錄 (復原) 復原，也可能用於向前復原記錄。 此路徑可能與 *szBackupLogPath* 相同。

*rgrstmap*

這是 [JET_RSTMAP](./jet-rstmap-structure.md) 結構的陣列。 這是舊的和新的資料庫路徑或檔案名的對應。 這是使用的原因，是因為資料庫可能需要復原到與其備份來源位置不同的位置。 如果將多個資料庫附加至單一記錄集，則還原對應可以指定要還原的資料庫子集。

*crstfilemap*

*Rgrstmap* 陣列參數中的專案數。

*szBackupLogPath*

要還原記錄檔之目錄的路徑。 這些是在外部備份順序期間讀取的記錄。 此路徑可能與 szLogPath 相同。

*genLow*

要從 *szBackupLogPath* 重新執行的最小記錄檔編號。 不帶正負號長度的完整精確度應該保留下來，但在目前的引擎版本中，這個數位是從0x00000 到0xFFFFF 的範圍內的十六進位數位。 在未來版本中可能會有所變動。

*genHigh*

要從 *szBackupLogPath* 重新執行的最高記錄檔編號。 不帶正負號長度的完整精確度應該保留，但在目前的引擎版本中，這個數位是從0x00000 到0xFFFFF 的十六進位數位。 在未來版本中可能會有所變動。

*pfn*

狀態回呼，用來報告復原的進度。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>傳回碼</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>作業已成功完成。</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfMemory</p></td>
<td><p>作業失敗，因為無法配置足夠的記憶體來完成。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。 <strong>JetExternalRestore</strong>可能會發生這種情況，因此當<em>szTargetCheckpointPath</em>和<em>szTargetInstanceLogPath</em>都未指定，或未指定兩者皆未指定時。 也就是說，它們必須相符，而且兩者都指定或都未指定。</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseCorrupted</p></td>
<td><p>這表示資料庫已損毀或無法辨識的檔案。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileNotFound</p></td>
<td><p>作業失敗，因為它無法開啟要求的檔案，因為在指定的路徑中找不到該檔案。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidPath</p></td>
<td><p>因為找不到指定的路徑，所以操作失敗。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreOfNonBackupDatabase</p></td>
<td><p>如果還原期間指定的資料庫檔案不是使用外部備份進行備份的資料庫，就會傳回此錯誤。</p></td>
</tr>
<tr class="even">
<td><p>JET_errStartingRestoreLogTooHigh</p></td>
<td><p>如果 <em>szBackupLogPath</em>中的其中一個記錄檔產生低於 <em>genLow</em> 或 <em>pLogInfo</em>所指定的記錄檔，就會傳回此錯誤。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errEndingRestoreLogTooLow</p></td>
<td><p>如果 <em>szBackupLogPath</em>中記錄檔的記錄檔產生超過 <em>genHigh</em> 或 <em>pLogInfo</em>中指定的記錄檔，就會傳回此錯誤。</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadRestoreTargetInstance</p></td>
<td><p>指定的 <em>szTargetInstanceLogPath</em> 不屬於初始化的實例。 只有在 Windows XP 和更新版本中才會傳回此錯誤。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRunningInOneInstanceMode</p></td>
<td><p>資料庫引擎無法在單一實例模式中執行外部還原或硬復原。 只有在 Windows XP 和更新版本中才會傳回此錯誤。</p></td>
</tr>
</tbody>
</table>


成功時， *rgrstmap* 中的所有資料庫都會完全復原並處於乾淨或一致狀態。 此時，可以將資料庫重新掛接至現有的實例。

失敗時，引擎無法復原資料庫。 資料庫處於無效狀態，若要重試強制進行修復，必須再次還原整個資料庫。 一般來說，這種情況的來源是磁片或記錄檔損毀，或是其他形式的記錄 mismanagement 或非連續記錄集。

#### <a name="remarks"></a>備註

若要瞭解「硬性」復原的運作方式，您必須瞭解有三個階段的復原，而第二個階段可以有兩個部分。 在第一個階段中，必須有記錄才能將備份的資料庫帶入一致性 (或者可以) 使用初始增量記錄集。 在第二階段中，可以使用任何其他可用的向前復原記錄檔，讓資料庫保持一致。 此外，還會重複執行其他向前復原記錄。 第 III 階段是復原的復原階段。

階段 I：重新執行一組必須還原的記錄檔，以便讓資料庫進入一致的狀態 (或執行一組初始的記錄檔) 。 基本上，這是針對正在還原的資料庫，重新執行不是選擇性的一組記錄檔。 如果記錄檔範圍中有遺失的記錄，則還原將會失敗。 這些記錄檔應該放在 *szBackupLogPath* 參數所指定的目錄中。

第二階段：選擇性地，可能會有一些記錄檔，這些記錄檔是從增量或差異備份和使用中實例的記錄檔向前復原記錄檔。 如果是來自增量或差異備份的記錄檔，記錄檔可以放在 *szBackupLogPath* 或 *szTargetInstanceLogPath* 參數所指定的目錄中，而前者是建議的目錄。 用於向前復原階段 (階段 II) 的記錄，應該來自第一系列階段中所播放的相同記錄檔系列，而且應該持續遞增記錄檔編號，而不會有與記錄階段之間的差距。 若要使用目前正在使用中實例的記錄檔來完全更新資料庫，必須指定 *szTargetInstanceLogPath* 和 *szTargetInstanceCheckpointPath* 參數。 即使其他資料庫附加至該記錄集，也可以這麼做。

第 III 階段：在復原的最後一個階段中，會回復任何未認可的交易，而這需要產生新的記錄檔和更新檢查點檔案。 這個階段有時稱為「復原」。 在此階段中使用的檢查點檔案路徑是類似于階段 III 記錄檔位置的路徑，亦即，如果 *szLogPath* 用於階段 iii，則會使用 szCheckpointFilePath，如果 *SzTargetInstanceLogPath* 用於復原 *szTargetInstanceCheckpointPath* 的第三階段，將會使用 。

若要瞭解路徑的運作方式，請使用此流程圖：

![ESE_Documentation_ese1](images/Gg294088.ESE_Documentation_ese1(EXCHG.10).gif "ESE_Documentation_ese1")

#### <a name="requirements"></a>規格需求

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
<tr class="even">
<td><p><strong>程式庫</strong></p></td>
<td><p>使用 ESENT。</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>需要 ESENT.dll。</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>實作為 <strong>JetExternalRestoreW</strong> (Unicode) 和 <strong>JetExternalRestoreA</strong> (ANSI) 。</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JET_RSTMAP](./jet-rstmap-structure.md)  
[JET_LOGINFO](./jet-loginfo-structure.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetInit](./jetinit-function.md)
