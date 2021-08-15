---
description: 深入瞭解： JetExternalRestore2 函數
title: JetExternalRestore2 函式
TOCTitle: JetExternalRestore2 Function
ms:assetid: 66331be0-7abc-43a0-8b8b-dbdd227c918e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269272(v=EXCHG.10)
ms:contentKeyID: 32765574
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetExternalRestore2W
- JetExternalRestore2A
- JetExternalRestore2
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6d2cbd4a13555d754cdbc1f9c02011b5891d6d6fcfae3fea822ddf6ad9953b78
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119719188"
---
# <a name="jetexternalrestore2-function"></a>JetExternalRestore2 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetexternalrestore2-function"></a>JetExternalRestore2 函式

**JetExternalRestore2** 函式會還原使用外部備份 api 所建立的外部備份，並提供用於迴圈記錄作業的檢查點。 這稱為「硬復原」，這類似于 [JetInit](./jetinit-function.md) 函式所執行的軟復原。

**Windows xp： JetExternalRestore2** 是在 Windows xp 引進。

```cpp
    JET_ERR JET_API JetExternalRestore2(
      __in          JET_PSTR szCheckpointFilePath,
      __in          JET_PSTR szLogPath,
      __in_opt      JET_RSTMAP* rgrstmap,
      __in          long crstfilemap,
      __in          JET_PSTR szBackupLogPath,
      __in_out      JET_LOGINFO* pLogInfo,
      __in_opt      JET_PSTR szTargetInstanceName,
      __in_opt      JET_PSTR szTargetInstanceLogPath,
      __in_opt      JET_PSTR szTargetInstanceCheckpointPath,
      __in          JET_PFNSTATUS pfn
    );
```

### <a name="parameters"></a>參數

*szCheckpointFilePath*

如果未指定 *szTargetInstanceCheckpointPath* 或路徑具有使用中或執行中的實例時，要在復原期間使用的檢查點檔案的路徑。

*szLogPath*

最後階段記錄檔的路徑或目錄 (復原) 復原，而且可能會向前復原記錄檔。 此路徑可能與 *szBackupLogPath* 相同。

*rgrstmap*

這是 [JET_RSTMAP](./jet-rstmap-structure.md) 結構的陣列。 這是舊的和新的資料庫路徑或檔案名的對應。 這是使用的原因，是因為資料庫可能需要復原到與其備份來源位置不同的位置。 如果將多個資料庫附加至單一記錄集，則還原對應可以指定要還原的資料庫子集。

*crstfilemap*

*Rgrstmap* 陣列參數中的專案數。

*szBackupLogPath*

要還原記錄檔之目錄的路徑。 這些是在外部備份順序期間讀取的記錄。 此路徑可能與 *szLogPath* 相同。

*pLogInfo*

*PLogInfo* 描述要復原之備份記錄的幾個層面，此參數可讓 **JetExternalRestore2** 取得 **JetExternalRestore2** 具有的明確 *genLow* 和 *genHigh* 參數，以及基底記錄檔名稱，而不是 "edb" 的假設記錄基底名稱。

*szTargetInstanceName*

此參數已被取代，無法在您的應用程式中使用。

*szTargetInstanceLogPath*

如果您想要向前復原的記錄檔位置是在使用中的記錄集或實例中，則為向前復原記錄的路徑。 如果目標實例使用迴圈記錄，則不應指定此項。

*szTargetInstanceCheckpointPath*

如果此目標沒有執行中的實例，則為復原期間的檢查點路徑。 如果目標實例使用迴圈記錄，則不應指定此項。

*pfn*

狀態回呼，會報告復原的進度。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。

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
<td><p>JET_errBadRestoreTargetInstance</p></td>
<td><p>指定的 <em>szTargetInstanceLogPath</em> 不屬於初始化的實例。 此錯誤只會在 Windows XP 及更新版本中傳回。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseCorrupted</p></td>
<td><p>這表示資料庫已損毀或無法辨識的檔案。</p></td>
</tr>
<tr class="even">
<td><p>JET_errEndingRestoreLogTooLow</p></td>
<td><p>如果 <em>szBackupLogPath</em>中的記錄檔有一個以上的記錄檔產生，則會傳回此錯誤，該錯誤會在 <em>GenHigh</em> 或 <em>pLogInfo ulGenHigh</em>中指定。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileNotFound</p></td>
<td><p>作業失敗，因為它無法開啟要求的檔案，因為在指定的路徑中找不到該檔案。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。 <a href="gg294088(v=exchg.10).md">JetExternalRestore</a>可能會發生這種情況，因此當<em>szTargetCheckpointPath</em>和<em>szTargetInstanceLogPath</em>都未指定，或未指定兩者皆未指定時。 也就是說，它們必須相符，而且兩者都指定或都未指定。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidPath</p></td>
<td><p>因為找不到指定的路徑，所以操作失敗。</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfMemory</p></td>
<td><p>作業失敗，因為無法配置足夠的記憶體來完成。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreOfNonBackupDatabase</p></td>
<td><p>如果還原期間指定的資料庫檔案不是使用外部備份進行備份的資料庫，就會傳回此錯誤。</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInOneInstanceMode</p></td>
<td><p>資料庫引擎無法在單一實例模式中執行外部還原或硬復原。 此錯誤只會在 Windows XP 及更新版本中傳回。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errStartingRestoreLogTooHigh</p></td>
<td><p>如果 <em>szBackupLogPath</em>中的其中一個記錄檔產生低於 <em>genLow</em> 或 <em>pLogInfo</em>所指定的記錄檔，就會傳回此錯誤。</p></td>
</tr>
</tbody>
</table>


成功時， *rgrstmap* 中的所有資料庫都會完全復原並處於乾淨或一致狀態。 此時，可以將資料庫重新掛接至現有的實例。

失敗時，引擎無法復原資料庫。 資料庫處於無效狀態，若要重試強制進行修復，必須再次還原整個資料庫。 一般來說，這種情況的來源是磁片或記錄檔損毀，或是其他形式的記錄 mismanagement 或非連續記錄集。

#### <a name="remarks"></a>備註

請參閱 [JetExternalRestore](./jetexternalrestore-function.md)。

#### <a name="requirements"></a>規格需求

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>用戶端</strong></p></td>
<td><p>需要 Windows Vista 或 Windows XP。</p></td>
</tr>
<tr class="even">
<td><p><strong>伺服器</strong></p></td>
<td><p>需要 Windows server 2008 或 Windows server 2003。</p></td>
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
<td><p>實作為 <strong>JetExternalRestore2W</strong> (Unicode) 和 <strong>JetExternalRestore2A</strong> (ANSI) 。</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_LOGINFO](./jet-loginfo-structure.md)  
[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JET_RSTMAP](./jet-rstmap-structure.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetExternalRestore](./jetexternalrestore-function.md)  
[JetInit](./jetinit-function.md)
