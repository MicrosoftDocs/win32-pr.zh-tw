---
description: 深入瞭解：可擴充儲存引擎錯誤碼
title: 可擴充儲存引擎錯誤碼
TOCTitle: Extensible Storage Engine Error Codes
ms:assetid: 7534370d-aed6-4980-b1ca-c3d063507e31
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269297(v=EXCHG.10)
ms:contentKeyID: 32765589
ms.date: 09/22/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9de4bd8157e0b7210315352ba0760293a892f087
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984691"
---
# <a name="extensible-storage-engine-error-codes"></a>可擴充儲存引擎錯誤碼


_**適用于：** Windows |Windows Server_

## <a name="extensible-storage-engine-error-codes"></a>可擴充儲存引擎錯誤碼

下列錯誤碼 (旗標) 可延伸儲存引擎 API 中的函式使用。

[JET_ERR](./jet-err.md)值為零應該會被視為成功。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Success</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess 0</p></td>
<td><p>此函數已成功。</p></td>
</tr>
</tbody>
</table>


大於零的 [JET_ERR](./jet-err.md) 值應解釋為警告。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>警告</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_wrnRemainingVersions<br />
321</p></td>
<td><p>版本存放區仍處於使用中狀態。 目錄管理員會傳回此錯誤。</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnUniqueKey<br />
345</p></td>
<td><p>非唯一索引的搜尋產生了唯一索引鍵。 目錄管理員會傳回此錯誤。</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnSeparateLongValue<br />
406</p></td>
<td><p>資料庫資料行是分隔的 long 值。 記錄管理員會傳回這個錯誤。</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnExistingLogFileHasBadSignature<br />
558</p></td>
<td><p>現有的記錄檔有錯誤的簽章。</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnExistingLogFileIsNotContiguous<br />
559</p></td>
<td><p>現有的記錄檔不是連續的。</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnSkipThisRecord<br />
564</p></td>
<td><p>此錯誤僅供內部使用。</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnTargetInstanceRunning<br />
578</p></td>
<td><p>為還原指定的 TargetInstance 正在執行中。</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnDatabaseRepaired<br />
595</p></td>
<td><p>資料庫損毀已修復。</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnNull<br />
1004</p></td>
<td><p>資料行具有 <strong>Null</strong> 值。</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnBufferTruncated<br />
1006</p></td>
<td><p>緩衝區對資料而言太小。</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnDatabaseAttached<br />
1007</p></td>
<td><p>資料庫已附加。</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnSortOverflow<br />
1009</p></td>
<td><p>所嘗試的排序沒有足夠的記憶體可完成。</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnSeekNotEqual<br />
1039</p></td>
<td><p>搜尋期間找不到完全相符的。</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnRecordFoundGreater<br />
JET_wrnSeekNotEqual</p></td>
<td><p>搜尋期間找不到完全相符的。 記錄管理員會傳回這個錯誤。</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnRecordFoundLess<br />
JET_wrnSeekNotEqual</p></td>
<td><p>搜尋期間找不到完全相符的。 記錄管理員會傳回這個錯誤。</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnNoErrorInfo<br />
1055</p></td>
<td><p>沒有任何延伸的錯誤資訊。</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnNoIdleActivity<br />
1058</p></td>
<td><p>未發生任何閒置活動。</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnNoWriteLock<br />
1067</p></td>
<td><p>交易層級0沒有寫入鎖定。</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnSetNull<br />
1068</p></td>
<td><p>此資料行設定為 <strong>Null</strong> 值。</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnTableEmpty<br />
1301</p></td>
<td><p>已開啟空白資料表。</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnTableInUseBySystem<br />
1327</p></td>
<td><p>系統清除會在資料表上開啟資料指標。</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnCorruptIndexDeleted<br />
1415</p></td>
<td><p>必須移除過期的索引。</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnMaxTruncated<br />
1512</p></td>
<td><p>最大長度太大且已被截斷。</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnCopyLongValue<br />
1520</p></td>
<td><p>BLOB 值已從記錄移至不同的大型 Blob 儲存體。</p>
<p><strong>注意</strong> 此錯誤僅供內部使用。</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnSkipped<br />
1531</p></td>
<td><p>因為對應的資料行識別碼或 <em>itagSequence</em> 成員來自要求列舉的 <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a> 結構，所以不會傳回資料行值為 null。</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnNotLocal<br />
1532</p></td>
<td><p>因為無法從現有的資料重建資料行值，所以不會傳回這些值。</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnMoreTags<br />
1533</p></td>
<td><p>未要求列舉的現有資料行值。</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnTruncated<br />
1534</p></td>
<td><p>在列舉期間，資料行值已被截斷為要求的大小限制。</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnPresent<br />
1535</p></td>
<td><p>資料行值存在但未由要求傳回。</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnSingleValue<br />
1536</p></td>
<td><p>因為設定 JET_bitEnumerateCompressOutput，所以 JET_COLUMNENUM 中傳回資料行值。</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnDefault<br />
1537</p></td>
<td><p>資料行值會設定為數據行的預設值。</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnDataHasChanged<br />
1610</p></td>
<td><p>資料已經變更。</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnKeyChanged<br />
1618</p></td>
<td><p>正在使用新的金鑰。</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnFileOpenReadOnly<br />
1813</p></td>
<td><p>資料庫檔案是唯讀的。</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnIdleFull<br />
1908</p></td>
<td><p>閒置登錄已滿。</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnDefragAlreadyRunning<br />
2000</p></td>
<td><p>已在指定的資料庫上執行線上磁碟重組。</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnDefragNotRunning<br />
2001</p></td>
<td><p>未在指定的資料庫上執行線上磁碟重組。</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnCallbackNotRegistered<br />
2100</p></td>
<td><p>不存在的回呼函數已取消註冊。</p></td>
</tr>
</tbody>
</table>


小於零的 [JET_ERR](./jet-err.md) 值應視為錯誤。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Errors</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_wrnNyi<br />
-1</p></td>
<td><p>函數尚未執行。</p></td>
</tr>
<tr class="even">
<td><p>JET_errRfsFailure<br />
-100</p></td>
<td><p>資源失敗模擬器失敗。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRfsNotArmed<br />
-101</p></td>
<td><p>資源失敗模擬器尚未初始化。</p></td>
</tr>
<tr class="even">
<td><p>JET_errFileClose<br />
-102</p></td>
<td><p>無法關閉檔案。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfThreads<br />
-103</p></td>
<td><p>無法啟動執行緒。</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyIO<br />
-105</p></td>
<td><p>因為 IOs 太多，所以系統正在忙碌中。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTaskDropped<br />
-106</p></td>
<td><p>無法執行要求的非同步工作。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInternalError<br />
-107</p></td>
<td><p>發生嚴重的內部錯誤。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseBufferDependenciesCorrupted<br />
-255</p></td>
<td><p>緩衝區相依性設定不正確，且發生復原失敗。</p></td>
</tr>
<tr class="even">
<td><p>JET_errPreviousVersion<br />
-322</p></td>
<td><p>版本已經存在，而且發生復原失敗。 目錄管理員會傳回此錯誤。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errPageBoundary<br />
-323</p></td>
<td><p>已達到頁面界限。 目錄管理員會傳回此錯誤。</p></td>
</tr>
<tr class="even">
<td><p>JET_errKeyBoundary<br />
-324</p></td>
<td><p>已達到金鑰界限。 目錄管理員會傳回此錯誤。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadPageLink<br />
-327</p></td>
<td><p>資料庫已損毀。 目錄管理員會傳回此錯誤。</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadBookmark<br />
-328</p></td>
<td><p>書簽在資料庫中沒有對應的位址。 目錄管理員會傳回此錯誤。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNTSystemCallFailed<br />
-334</p></td>
<td><p>作業系統的呼叫失敗。 目錄管理員會傳回此錯誤。</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadParentPageLink<br />
-338</p></td>
<td><p>父資料庫已損毀。 目錄管理員會傳回此錯誤。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSPAvailExtCacheOutOfSync<br />
-340</p></td>
<td><p>AvailExt 快取不符合 B + 樹狀結構。 目錄管理員會傳回此錯誤。</p></td>
</tr>
<tr class="even">
<td><p>JET_errSPAvailExtCorrupted<br />
-341</p></td>
<td><p>AllAvailExt 空間樹狀結構已損毀。 目錄管理員會傳回此錯誤。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSPAvailExtCacheOutOfMemory<br />
-342</p></td>
<td><p>配置 AvailExt 快取節點時發生記憶體不足的錯誤。 目錄管理員會傳回此錯誤。</p></td>
</tr>
<tr class="even">
<td><p>JET_errSPOwnExtCorrupted<br />
-343</p></td>
<td><p>OwnExt 空間樹狀結構已損毀。 目錄管理員會傳回此錯誤。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDbTimeCorrupted<br />
-344</p></td>
<td><p>目前頁面上的 Dbtime 大於全域資料庫 Dbtime。 目錄管理員會傳回此錯誤。</p></td>
</tr>
<tr class="even">
<td><p>JET_errKeyTruncated<br />
-346</p></td>
<td><p>嘗試建立索引項目的索引鍵失敗，因為索引鍵會被截斷，而且索引定義不允許索引鍵截斷。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errKeyTooBig<br />
-408</p></td>
<td><p>金鑰太大。 記錄管理員會傳回這個錯誤。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLoggedOperation<br />
-500</p></td>
<td><p>無法重做記錄的作業。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogFileCorrupt<br />
-501</p></td>
<td><p>記錄檔已損毀。</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoBackupDirectory<br />
-503</p></td>
<td><p>未提供備份目錄。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBackupDirectoryNotEmpty<br />
-504</p></td>
<td><p>備份目錄不是空的。</p></td>
</tr>
<tr class="even">
<td><p>JET_errBackupInProgress<br />
-505</p></td>
<td><p>備份已在使用中。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress<br />
-506</p></td>
<td><p>還原進行中。</p></td>
</tr>
<tr class="even">
<td><p>JET_errMissingPreviousLogFile<br />
-509</p></td>
<td><p>檢查點缺少記錄檔。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogWriteFail<br />
-510</p></td>
<td><p>寫入記錄檔時發生錯誤。</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogDisabledDueToRecoveryFailure<br />
-511</p></td>
<td><p>復原失敗後，嘗試寫入記錄檔。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCannotLogDuringRecoveryRedo<br />
-512</p></td>
<td><p>復原重做失敗時，嘗試寫入記錄檔。</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogGenerationMismatch<br />
-513</p></td>
<td><p>記錄檔的名稱與內部世代編號不相符。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadLogVersion<br />
-514</p></td>
<td><p>記錄檔的版本與 ESE 版本不相容。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLogSequence<br />
-515</p></td>
<td><p>下一個記錄檔中的時間戳記不符合預期的時間戳記。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLoggingDisabled<br />
-516</p></td>
<td><p>記錄檔並非使用中。</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogBufferTooSmall<br />
-517</p></td>
<td><p>記錄緩衝區太小，無法進行復原。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogSequenceEnd<br />
-519</p></td>
<td><p>已超過記錄檔的最大數目。</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoBackup<br />
-520</p></td>
<td><p>沒有進行中的備份。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidBackupSequence<br />
-521</p></td>
<td><p>備份呼叫順序不是。</p></td>
</tr>
<tr class="even">
<td><p>JET_errBackupNotAllowedYet<br />
-523</p></td>
<td><p>目前無法執行備份。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDeleteBackupFileFail<br />
-524</p></td>
<td><p>無法刪除備份檔案。</p></td>
</tr>
<tr class="even">
<td><p>JET_errMakeBackupDirectoryFail<br />
-525</p></td>
<td><p>無法建立備份臨時目錄。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidBackup<br />
-526</p></td>
<td><p>已啟用迴圈記錄;無法執行增量備份。</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecoveredWithErrors<br />
-527</p></td>
<td><p>資料已還原，但發生錯誤。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errMissingLogFile<br />
-528</p></td>
<td><p>遺失目前的記錄檔。</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogDiskFull<br />
-529</p></td>
<td><p>記錄磁碟已滿。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadLogSignature<br />
-530</p></td>
<td><p>記錄檔有錯誤的簽章。</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadDbSignature<br />
-531</p></td>
<td><p>資料庫檔案有錯誤的簽章。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadCheckpointSignature<br />
-532</p></td>
<td><p>檢查點檔案有錯誤的簽章。</p></td>
</tr>
<tr class="even">
<td><p>JET_errCheckpointCorrupt<br />
-533</p></td>
<td><p>找不到檢查點檔案或已損毀。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errMissingPatchPage<br />
-534</p></td>
<td><p>復原期間找不到 [資料庫修補檔案] 頁面。</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadPatchPage<br />
-535</p></td>
<td><p>資料庫修補檔案頁面無效。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRedoAbruptEnded<br />
-536</p></td>
<td><p>因為從記錄檔讀取記錄檔突然失敗，所以重做突然終止。</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadSLVSignature<br />
-537</p></td>
<td><p>此旗標為保留。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errPatchFileMissing<br />
-538</p></td>
<td><p>硬還原偵測到備份組遺失資料庫修補檔案。</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseLogSetMismatch<br />
-539</p></td>
<td><p>資料庫不屬於目前的記錄檔集。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseStreamingFileMismatch<br />
-540</p></td>
<td><p>此旗標為保留。</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogFileSizeMismatch<br />
-541</p></td>
<td><p>實際的記錄檔大小與 <a href="gg269235(v=exchg.10).md">JET_paramLogFileSize</a>不相符。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCheckpointFileNotFound<br />
-542</p></td>
<td><p>找不到檢查點檔案。</p></td>
</tr>
<tr class="even">
<td><p>JET_errRequiredLogFilesMissing<br />
-543</p></td>
<td><p>遺漏修復所需的記錄檔。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSoftRecoveryOnBackupDatabase<br />
-544</p></td>
<td><p>當您應該改為使用還原時，就必須在備份資料庫上使用軟復原。</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogFileSizeMismatchDatabasesConsistent<br />
-545</p></td>
<td><p>已復原資料庫，但復原期間使用的記錄檔大小與 <a href="gg269235(v=exchg.10).md">JET_paramLogFileSize</a>不相符。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogSectorSizeMismatch<br />
-546</p></td>
<td><p>記錄檔磁區大小不符合目前磁片區的磁區大小。</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogSectorSizeMismatchDatabasesConsistent<br />
-547</p></td>
<td><p>已復原資料庫，但在復原期間使用的記錄檔磁區大小 () 不符合目前磁片區的磁區大小。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogSequenceEndDatabasesConsistent<br />
-548</p></td>
<td><p>已復原資料庫，但目前的順序中所有可能的記錄層代都已使用。 必須刪除所有記錄檔和檢查點檔案，而且必須備份資料庫，才能繼續進行。</p></td>
</tr>
<tr class="even">
<td><p>JET_errStreamingDataNotLogged<br />
-549</p></td>
<td><p>重新執行未記錄資料的串流檔案作業時發生不合法的嘗試。 這可能是因為嘗試向前復原已啟用迴圈記錄所致。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseDirtyShutdown<br />
-550</p></td>
<td><p>資料庫未完全關閉。 必須先執行復原，才能適當完成先前關機的資料庫作業。</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseInconsistent<br />
JET_errDatabaseDirtyShutdown</p></td>
<td><p>此錯誤已淘汰，且已由 JET_errDatabaseDirtyShutdown 取代。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errConsistentTimeMismatch<br />
-551</p></td>
<td><p>資料庫的上次一致時間尚未相符。</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabasePatchFileMismatch<br />
-552</p></td>
<td><p>此備份不會產生資料庫修補檔案。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errEndingRestoreLogTooLow<br />
-553</p></td>
<td><p>開始記錄檔編號太低，無法進行還原。</p></td>
</tr>
<tr class="even">
<td><p>JET_errStartingRestoreLogTooHigh<br />
-554</p></td>
<td><p>還原的起始記錄檔編號過高。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errGivenLogFileHasBadSignature<br />
-555</p></td>
<td><p>還原記錄檔有錯誤的簽章。</p></td>
</tr>
<tr class="even">
<td><p>JET_errGivenLogFileIsNotContiguous<br />
-556</p></td>
<td><p>還原記錄檔不是連續的。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errMissingRestoreLogFiles<br />
-557</p></td>
<td><p>有些還原記錄檔遺失。</p></td>
</tr>
<tr class="even">
<td><p>JET_errMissingFullBackup<br />
-560</p></td>
<td><p>資料庫在嘗試執行增量備份之前，遺漏了先前的完整備份。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadBackupDatabaseSize<br />
-561</p></td>
<td><p>備份資料庫大小不是資料庫頁面大小的倍數。</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseAlreadyUpgraded<br />
-562</p></td>
<td><p>目前嘗試升級資料庫已停止，因為資料庫已經是最新的。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseIncompleteUpgrade<br />
-563</p></td>
<td><p>資料庫只會部分轉換為目前的格式。 您必須從備份還原資料庫。</p></td>
</tr>
<tr class="even">
<td><p>JET_errMissingCurrentLogFiles<br />
-565</p></td>
<td><p>部分目前的記錄檔遺漏了連續還原。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDbTimeTooOld<br />
-566</p></td>
<td><p>頁面上的 dbtime 小於記錄中的 dbtimeBefore。</p></td>
</tr>
<tr class="even">
<td><p>JET_errDbTimeTooNew<br />
-567</p></td>
<td><p>頁面上的 dbtime 會在記錄中的 dbtimeBefore 之前。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errMissingFileToBackup<br />
-569</p></td>
<td><p>備份期間缺少某些記錄檔或資料庫修補檔案。</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogTornWriteDuringHardRestore<br />
-570</p></td>
<td><p>在硬還原期間設定的備份中偵測到寫入損毀。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogTornWriteDuringHardRecovery<br />
-571</p></td>
<td><p>在硬復原期間偵測到寫入損毀 (記錄檔不是備份組) 的一部分。</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogCorruptDuringHardRestore<br />
-573</p></td>
<td><p>在硬還原期間于備份組中偵測到損毀。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogCorruptDuringHardRecovery<br />
-574</p></td>
<td><p>硬碟上偵測到損毀 (記錄檔不是備份組) 的一部分。</p></td>
</tr>
<tr class="even">
<td><p>JET_errMustDisableLoggingForDbUpgrade<br />
-575</p></td>
<td><p>嘗試升級資料庫時，無法啟用記錄。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadRestoreTargetInstance<br />
-577</p></td>
<td><p>找不到為還原指定的 TargetInstance 或記錄檔不相符。</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecoveredWithoutUndo<br />
-579</p></td>
<td><p>資料庫引擎已成功重新執行交易記錄中的所有作業，以執行損毀復原，但呼叫端選擇停止復原而不回復未認可的更新。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabasesNotFromSameSnapshot<br />
-580</p></td>
<td><p>要還原的資料庫不是來自相同的陰影複本備份。</p></td>
</tr>
<tr class="even">
<td><p>JET_errSoftRecoveryOnSnapshot<br />
-581</p></td>
<td><p>您可以從陰影複本備份集的資料庫進行軟復原。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errUnicodeTranslationBufferTooSmall<br />
-601</p></td>
<td><p>Unicode 轉譯緩衝區太小。</p></td>
</tr>
<tr class="even">
<td><p>JET_errUnicodeTranslationFail<br />
-602</p></td>
<td><p>Unicode 正規化失敗。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errUnicodeNormalizationNotSupported<br />
-603</p></td>
<td><p>作業系統未提供 Unicode 正規化的支援，且未指定正規化回呼。</p></td>
</tr>
<tr class="even">
<td><p>JET_errExistingLogFileHasBadSignature<br />
-610</p></td>
<td><p>現有的記錄檔有錯誤的簽章。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errExistingLogFileIsNotContiguous<br />
-611</p></td>
<td><p>現有的記錄檔不是連續的。</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogReadVerifyFailure<br />
-612</p></td>
<td><p>備份期間在記錄檔中發現總和檢查碼錯誤。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSLVReadVerifyFailure<br />
-613</p></td>
<td><p>此旗標為保留。</p></td>
</tr>
<tr class="even">
<td><p>JET_errCheckpointDepthTooDeep<br />
-614</p></td>
<td><p>檢查點和目前世代之間有太多未完成的層代。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreOfNonBackupDatabase<br />
-615</p></td>
<td><p>在非備份資料庫的資料庫上嘗試進行硬復原。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidGrbit<br />
-900</p></td>
<td><p>有不正確 grbit 參數。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress<br />
-1000</p></td>
<td><p>終止正在進行中。</p></td>
</tr>
<tr class="even">
<td><p>JET_errFeatureNotAvailable<br />
-1001</p></td>
<td><p>不支援此 API 元素。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidName<br />
-1002</p></td>
<td><p>使用了不正確名稱。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter<br />
-1003</p></td>
<td><p>使用了不正確 API 參數。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseFileReadOnly<br />
-1008</p></td>
<td><p>嘗試附加至唯讀資料庫檔案以進行讀取/寫入作業。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidDatabaseId<br />
-1010</p></td>
<td><p>有不正確資料庫識別碼。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfMemory<br />
-1011</p></td>
<td><p>系統記憶體不足。</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfDatabaseSpace<br />
-1012</p></td>
<td><p>已達到資料庫大小上限。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfCursors<br />
-1013</p></td>
<td><p>資料表已超出資料指標。</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfBuffers<br />
-1014</p></td>
<td><p>資料庫超出頁面緩衝區。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyIndexes<br />
-1015</p></td>
<td><p>有太多索引。</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyKeys<br />
-1016</p></td>
<td><p>索引中有太多資料行。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordDeleted<br />
-1017</p></td>
<td><p>記錄已刪除。</p></td>
</tr>
<tr class="even">
<td><p>JET_errReadVerifyFailure<br />
-1018</p></td>
<td><p>資料庫頁面上發生總和檢查碼錯誤。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errPageNotInitialized<br />
-1019</p></td>
<td><p>有空白的資料庫頁面。</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfFileHandles<br />
-1020</p></td>
<td><p>沒有檔案控制代碼。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDiskIO<br />
-1022</p></td>
<td><p>發生磁片 IO 錯誤。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidPath<br />
-1023</p></td>
<td><p>檔案路徑無效。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidSystemPath<br />
-1024</p></td>
<td><p>有不正確系統路徑。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLogDirectory<br />
-1025</p></td>
<td><p>有不正確記錄檔目錄。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordTooBig<br />
-1026</p></td>
<td><p>記錄大於大小上限。</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyOpenDatabases<br />
-1027</p></td>
<td><p>開啟的資料庫太多。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidDatabase<br />
-1028</p></td>
<td><p>這不是資料庫檔案。</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized<br />
-1029</p></td>
<td><p>資料庫引擎尚未初始化。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errAlreadyInitialized<br />
-1030</p></td>
<td><p>資料庫引擎已初始化。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInitInProgress<br />
-1031</p></td>
<td><p>資料庫引擎正在初始化。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileAccessDenied<br />
-1032</p></td>
<td><p>無法存取檔案，因為檔案已鎖定或正在使用中。</p></td>
</tr>
<tr class="even">
<td><p>JET_errBufferTooSmall<br />
-1038</p></td>
<td><p>緩衝區太小。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyColumns<br />
-1040</p></td>
<td><p>定義的資料行太多。</p></td>
</tr>
<tr class="even">
<td><p>JET_errContainerNotEmpty<br />
-1043</p></td>
<td><p>容器不是空的。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidFilename<br />
-1044</p></td>
<td><p>檔案名無效。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBookmark<br />
-1045</p></td>
<td><p>有不正確書簽。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnInUse<br />
-1046</p></td>
<td><p>使用的資料行位於索引中。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBufferSize<br />
-1047</p></td>
<td><p>資料緩衝區不符合資料行大小。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNotUpdatable<br />
-1048</p></td>
<td><p>無法設定資料行值。</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexInUse<br />
-1051</p></td>
<td><p>索引正在使用中。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLinkNotSupported<br />
-1052</p></td>
<td><p>連結支援無法使用。</p></td>
</tr>
<tr class="even">
<td><p>JET_errNullKeyDisallowed<br />
-1053</p></td>
<td><p>索引上不允許 Null 索引鍵。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInTransaction<br />
-1054</p></td>
<td><p>作業必須在交易內發生。</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyActiveUsers<br />
-1059</p></td>
<td><p>有太多活動資料庫使用者</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidCountry<br />
-1061</p></td>
<td><p>有無效或未知的國家/地區代碼。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLanguageId<br />
-1062</p></td>
<td><p>有無效或未知的語言識別項。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidCodePage<br />
-1063</p></td>
<td><p>有無效或未知的字碼頁。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLCMapStringFlags<br />
-1064</p></td>
<td><p><a href="/windows/win32/api/winnls/nf-winnls-lcmapstringa">LCMapString</a>使用了不正確旗標。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errVersionStoreEntryTooBig<br />
-1065</p></td>
<td><p>嘗試建立的版本存放區專案 (大於版本值區的 RCE) 。</p></td>
</tr>
<tr class="even">
<td><p>JET_errVersionStoreOutOfMemoryAndCleanupTimedOut<br />
-1066</p></td>
<td><p>版本存放區的記憶體不足，因此清理嘗試無法完成。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errVersionStoreOutOfMemory<br />
-1069</p></td>
<td><p>版本存放區記憶體不足，已嘗試清除) 。</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotIndex<br />
-1071</p></td>
<td><p>無法編制 [保管] 和 [SLV] 資料行的索引。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordNotDeleted<br />
-1072</p></td>
<td><p>尚未刪除記錄。</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyMempoolEntries<br />
-1073</p></td>
<td><p>已要求太多 mempool 專案。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfObjectIDs<br />
-1074</p></td>
<td><p>資料庫超出 B + 樹狀 Objectid，因此必須執行離線磁碟重組，才能回收釋放或未使用的 Objectid。</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfLongValueIDs<br />
-1075</p></td>
<td><p>長值識別碼計數器已達最大值。 您必須執行離線磁碟重組，才能回收免費或未使用的 LongValueIDs。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfAutoincrementValues<br />
-1076</p></td>
<td><p>自動遞增計數器已達最大值。 離線磁碟重組將無法) 回收免費或未使用的自動遞增值。</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfDbtimeValues<br />
-1077</p></td>
<td><p>Dbtime 計數器已達到最大值。 您必須執行離線磁碟重組，才能回收免費或未使用的 Dbtime 值。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfSequentialIndexValues<br />
-1078</p></td>
<td><p>連續索引計數器已達到最大值。 您必須執行離線磁碟重組，才能回收免費或未使用的 SequentialIndex 值。</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInOneInstanceMode<br />
-1080</p></td>
<td><p>這個多重實例呼叫已啟用單一實例模式。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRunningInMultiInstanceMode<br />
-1081</p></td>
<td><p>此單一實例呼叫已啟用多重實例模式。</p></td>
</tr>
<tr class="even">
<td><p>JET_errSystemParamsAlreadySet<br />
-1082</p></td>
<td><p>全域系統參數已設定。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSystemPathInUse<br />
-1083</p></td>
<td><p>系統路徑已被另一個資料庫實例使用中。</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogFilePathInUse<br />
-1084</p></td>
<td><p>記錄檔路徑已被另一個資料庫實例使用中。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTempPathInUse<br />
-1085</p></td>
<td><p>已有另一個資料庫實例正在使用暫存資料庫的路徑。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceNameInUse<br />
-1086</p></td>
<td><p>實例名稱已在使用中。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable<br />
-1090</p></td>
<td><p>因為發生嚴重錯誤，所以無法使用這個實例。</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseUnavailable<br />
-1091</p></td>
<td><p>無法使用此資料庫，因為發生嚴重錯誤。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailableDueToFatalLogDiskFull<br />
-1092</p></td>
<td><p>無法使用這個實例，因為它在執行作業時遇到了記錄磁片-full 錯誤 (例如無法容忍失敗的交易回復) 。</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfSessions<br />
-1101</p></td>
<td><p>資料庫不在會話中。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errWriteConflict<br />
-1102</p></td>
<td><p>因為有未處理的寫入鎖定，所以寫入鎖定失敗。</p></td>
</tr>
<tr class="even">
<td><p>JET_errTransTooDeep<br />
-1103</p></td>
<td><p>交易的嵌套太深。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidSesid<br />
-1104</p></td>
<td><p>有不正確會話控制碼。</p></td>
</tr>
<tr class="even">
<td><p>JET_errWriteConflictPrimaryIndex<br />
-1105</p></td>
<td><p>嘗試在未認可的主要索引上進行更新。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInTransaction<br />
-1108</p></td>
<td><p>交易內不允許此作業。</p></td>
</tr>
<tr class="even">
<td><p>JET_errRollbackRequired<br />
-1109</p></td>
<td><p>目前的交易必須回復。 無法認可，且無法啟動新的。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTransReadOnly<br />
-1110</p></td>
<td><p>唯讀交易嘗試修改資料庫。</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionWriteConflict<br />
-1111</p></td>
<td><p>在相同的會話中，嘗試以兩個不同的資料指標取代相同的記錄。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordTooBigForBackwardCompatibility<br />
-1112</p></td>
<td><p>如果以舊版 Jet 的資料庫格式表示，記錄會太大。</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotMaterializeForwardOnlySort<br />
-1113</p></td>
<td><p>因為與 JET_bitTTForwardOnly 衝突的參數，所以無法建立臨時表。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSesidTableIdMismatch<br />
-1114</p></td>
<td><p>會話控制碼無法與資料表識別碼搭配使用，因為它不是用來建立它。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidInstance<br />
-1115</p></td>
<td><p>實例控制碼無效，或參考已關閉的實例。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errReadLostFlushVerifyFailure<br />
-1119</p></td>
<td><p>從磁片讀取的資料庫頁面上有先前的寫入未在頁面上表示。 適用于用戶端的 Windows 8 和更新版本，以及適用于伺服器的 Windows Server 2012 和更新版本。</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseDuplicate<br />
-1201</p></td>
<td><p>資料庫已經存在。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInUse<br />
-1202</p></td>
<td><p>使用中的資料庫。</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseNotFound<br />
-1203</p></td>
<td><p>沒有這類資料庫。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInvalidName<br />
-1204</p></td>
<td><p>資料庫名稱無效。</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseInvalidPages<br />
-1205</p></td>
<td><p>有不正確頁面數目。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseCorrupted<br />
-1206</p></td>
<td><p>有非資料庫檔案或損毀的資料庫。</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseLocked<br />
-1207</p></td>
<td><p>以獨佔方式鎖定資料庫。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCannotDisableVersioning<br />
-1208</p></td>
<td><p>無法停用此資料庫的版本控制。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidDatabaseVersion<br />
-1209</p></td>
<td><p>資料庫引擎與資料庫不相容。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabase200Format<br />
-1210</p></td>
<td><p>資料庫是舊版 (200) 格式。 如果設定<a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> ， <a href="gg294068(v=exchg.10).md">JetInit</a>會傳回此錯誤。 僅 Windows NT 用戶端。</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabase400Format<br />
-1211</p></td>
<td><p>資料庫是舊版 (400) 格式。 如果設定<a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> ， <a href="gg294068(v=exchg.10).md">JetInit</a>會傳回此錯誤。 僅 Windows NT 用戶端。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabase500Format<br />
-1212</p></td>
<td><p>資料庫是舊版 (500) 格式。 如果設定<a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> ， <a href="gg294068(v=exchg.10).md">JetInit</a>會傳回此錯誤。 僅 Windows NT 用戶端。</p></td>
</tr>
<tr class="even">
<td><p>JET_errPageSizeMismatch<br />
-1213</p></td>
<td><p>資料庫頁面大小與引擎不相符。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyInstances<br />
-1214</p></td>
<td><p>沒有其他資料庫實例可以啟動。</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseSharingViolation<br />
-1215</p></td>
<td><p>不同的資料庫實例正在使用這個資料庫。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errAttachedDatabaseMismatch<br />
-1216</p></td>
<td><p>在復原的開頭或結尾偵測到未處理的資料庫附件，但資料庫遺失或不符合附件資訊。</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseInvalidPath<br />
-1217</p></td>
<td><p>指定的資料庫檔案路徑不合法。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseIdInUse<br />
-1218</p></td>
<td><p>正在將已在使用中的識別碼指派給資料庫。</p></td>
</tr>
<tr class="even">
<td><p>JET_errForceDetachNotAllowed<br />
-1219</p></td>
<td><p>只有在因為發生錯誤而停止一般卸離時，才允許強制卸離。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCatalogCorrupted<br />
-1220</p></td>
<td><p>在目錄中偵測到損毀。</p></td>
</tr>
<tr class="even">
<td><p>JET_errPartiallyAttachedDB<br />
-1221</p></td>
<td><p>資料庫只會部分附加，且無法完成附加作業。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseSignInUse<br />
-1222</p></td>
<td><p>使用相同簽章的資料庫已在使用中。</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseCorruptedNoRepair<br />
-1224</p></td>
<td><p>資料庫已損毀，但不允許修復。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidCreateDbVersion<br />
-1225</p></td>
<td><p>資料庫引擎嘗試從交易記錄重新執行建立資料庫作業，但因為該作業的版本不相容而失敗。</p></td>
</tr>
<tr class="even">
<td><p>JET_errTableLocked<br />
-1302</p></td>
<td><p>資料表會被獨佔鎖定。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTableDuplicate<br />
-1303</p></td>
<td><p>資料表已經存在。</p></td>
</tr>
<tr class="even">
<td><p>JET_errTableInUse<br />
-1304</p></td>
<td><p>資料表正在使用中，因此無法鎖定。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errObjectNotFound<br />
-1305</p></td>
<td><p>沒有這類資料表或物件。</p></td>
</tr>
<tr class="even">
<td><p>JET_errDensityInvalid<br />
-1307</p></td>
<td><p>檔案或索引密度不正確。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTableNotEmpty<br />
-1308</p></td>
<td><p>資料表不是空的。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidTableId<br />
-1310</p></td>
<td><p>資料表識別碼無效。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyOpenTables<br />
-1311</p></td>
<td><p>即使在執行內部清除工作之後，也無法開啟其他資料表。</p></td>
</tr>
<tr class="even">
<td><p>JET_errIllegalOperation<br />
-1312</p></td>
<td><p>資料表不支援此作業。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyOpenTablesAndCleanupTimedOut<br />
-1313</p></td>
<td><p>因為清除嘗試無法完成，所以無法開啟其他資料表。</p></td>
</tr>
<tr class="even">
<td><p>JET_errObjectDuplicate<br />
-1314</p></td>
<td><p>資料表或物件名稱正在使用中。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidObject<br />
-1316</p></td>
<td><p>物件對作業無效。</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotDeleteTempTable<br />
-1317</p></td>
<td><p>您必須使用<a href="gg294087(v=exchg.10).md">JetCloseTable</a>而非<a href="gg294128(v=exchg.10).md">JetDeleteTable</a>來刪除臨時表。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCannotDeleteSystemTable<br />
-1318</p></td>
<td><p>刪除系統資料表時發生不合法的嘗試。</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotDeleteTemplateTable<br />
-1319</p></td>
<td><p>刪除範本資料表時發生不合法的嘗試。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errExclusiveTableLockRequired<br />
-1322</p></td>
<td><p>資料表上必須有獨佔鎖定。</p></td>
</tr>
<tr class="even">
<td><p>JET_errFixedDDL<br />
-1323</p></td>
<td><p>此資料表禁止 DDL 作業。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFixedInheritedDDL<br />
-1324</p></td>
<td><p>在衍生的資料表上，ddl 的繼承部分禁止 DDL 作業。</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotNestDDL<br />
-1325</p></td>
<td><p>目前不支援階層式 DDL 的嵌套。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDDLNotInheritable<br />
-1326</p></td>
<td><p>嘗試從未標示為範本資料表的資料表繼承 DDL。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidSettings<br />
-1328</p></td>
<td><p>系統參數設定不正確。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService<br />
-1329</p></td>
<td><p>用戶端已要求停止服務。</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotAddFixedVarColumnToDerivedTable<br />
-1330</p></td>
<td><p>範本資料表是使用 NoFixedVarColumnsInDerivedTables 旗標集所建立。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexCantBuild<br />
-1401</p></td>
<td><p>索引建立失敗。</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexHasPrimary<br />
-1402</p></td>
<td><p>已定義主要索引。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexDuplicate<br />
-1403</p></td>
<td><p>已定義索引。</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexNotFound<br />
-1404</p></td>
<td><p>沒有這類索引。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexMustStay<br />
-1405</p></td>
<td><p>無法刪除叢集索引。</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexInvalidDef<br />
-1406</p></td>
<td><p>索引定義無效。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidCreateIndex<br />
-1409</p></td>
<td><p>索引描述的建立無效。</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyOpenIndexes<br />
-1410</p></td>
<td><p>資料庫超出索引描述區塊。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errMultiValuedIndexViolation<br />
-1411</p></td>
<td><p>針對多重值索引產生了非唯一的內部記錄索引鍵。</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexBuildCorrupted<br />
-1412</p></td>
<td><p>正確反映主要索引的次要索引無法建立。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errPrimaryIndexCorrupted<br />
-1413</p></td>
<td><p>主要索引已損毀，且資料庫必須經過磁碟重組。</p></td>
</tr>
<tr class="even">
<td><p>JET_errSecondaryIndexCorrupted<br />
-1414</p></td>
<td><p>次要索引已損毀，且資料庫必須經過磁碟重組。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidIndexId<br />
-1416</p></td>
<td><p>索引識別碼無效。</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesSecondaryIndexOnly<br />
-1430</p></td>
<td><p>元組索引只能針對次要索引進行設定。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesTooManyColumns<br />
-1431</p></td>
<td><p>元組索引的索引定義包含更多資料庫引擎可支援的索引鍵資料行。</p>
<p><strong>注意  </strong>JET_errIndexTuplesOneColumnOnly 錯誤已淘汰，且已由 JET_errIndexTuplesTooManyColumns 取代。</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesNonUniqueOnly<br />
-1432</p></td>
<td><p>元組索引必須是非唯一的索引。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesTextBinaryColumnsOnly<br />
-1433</p></td>
<td><p>元組索引定義只能包含具有文字或二進位資料行類型的索引鍵資料行。</p>
<p><strong>注意  </strong>JET_errIndexTuplesTextColumnsOnly 錯誤已淘汰，且已由 JET_errIndexTuplesTextBinaryColumnsOnly 取代。</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesVarSegMacNotAllowed<br />
-1434</p></td>
<td><p>元組索引不允許設定 cbVarSegMac。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesInvalidLimits<br />
-1435</p></td>
<td><p>最小/最大元組長度或為索引指定的最大字元數無效。</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesCannotRetrieveFromIndex<br />
-1436</p></td>
<td><p>在元組索引上抓取資料行時，無法使用 JET_bitRetrieveFromIndex 旗標來呼叫<a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> 。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesKeyTooSmall<br />
-1437</p></td>
<td><p>指定的索引鍵不符合最小元組長度。</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnLong<br />
-1501</p></td>
<td><p>資料行值為 long。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNoChunk<br />
-1502</p></td>
<td><p>長值沒有這類區塊。</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnDoesNotFit<br />
-1503</p></td>
<td><p>欄位將無法放入記錄中。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNullInvalid<br />
-1504</p></td>
<td><p>Null 無效。</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnIllegalNull<br />
JET_errNullInvalid</p></td>
<td><p>Null 無效。 記錄管理員會傳回這個錯誤。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnIndexed-1505</p></td>
<td><p>資料行已編制索引，無法刪除。</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnTooBig-1506</p></td>
<td><p>欄位長度大於允許的長度上限。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNotFound-1507</p></td>
<td><p>沒有這類資料行。</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnDuplicate-1508</p></td>
<td><p>這個欄位已經定義過了。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errMultiValuedColumnMustBeTagged-1509</p></td>
<td><p>嘗試建立多重值資料行，但資料行未標記。</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnRedundant-1510</p></td>
<td><p>有第二個自動遞增或版本資料行。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidColumnType-1511</p></td>
<td><p>資料行資料類型無效。</p></td>
</tr>
<tr class="even">
<td><p>JET_errTaggedNotNull-1514</p></td>
<td><p>沒有非 Null 的標記資料行。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentIndex-1515</p></td>
<td><p>資料庫無效，因為它不包含目前的索引。</p></td>
</tr>
<tr class="even">
<td><p>JET_errKeyIsMade-1516</p></td>
<td><p>金鑰完全由您決定。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadColumnId-1517</p></td>
<td><p>資料行識別碼不正確。</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadItagSequence-1518</p></td>
<td><p>標記的資料行有不正確的 itagSequence。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnInRelationship-1519</p></td>
<td><p>無法刪除資料行，因為它是關聯性的一部分。</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotBeTagged-1521</p></td>
<td><p>自動遞增和版本無法標記。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDefaultValueTooBig-1524</p></td>
<td><p>預設值超過大小上限。</p></td>
</tr>
<tr class="even">
<td><p>JET_errMultiValuedDuplicate-1525</p></td>
<td><p>在唯一多重值資料行上偵測到重複的值。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLVCorrupted-1526</p></td>
<td><p>在長值樹狀結構中發生損毀。</p></td>
</tr>
<tr class="even">
<td><p>JET_errMultiValuedDuplicateAfterTruncation-1528</p></td>
<td><p>在資料正規化之後，在唯一多重值資料行上偵測到重複的值，並且在比較之前正規化資料截斷。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDerivedColumnCorruption-1529</p></td>
<td><p>衍生資料表中有不正確資料行。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidPlaceholderColumn-1530</p></td>
<td><p>嘗試將資料行轉換為主要索引預留位置，但資料行不符合必要的準則。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordNotFound-1601</p></td>
<td><p>找不到索引鍵。</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecordNoCopy-1602</p></td>
<td><p>沒有可運作的緩衝區。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord-1603</p></td>
<td><p>目前沒有記錄。</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecordPrimaryChanged-1604</p></td>
<td><p>主鍵可能不會變更。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errKeyDuplicate-1605</p></td>
<td><p>有不合法的重複索引鍵。</p></td>
</tr>
<tr class="even">
<td><p>JET_errAlreadyPrepared-1607</p></td>
<td><p>已嘗試在記錄更新進行時更新記錄。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errKeyNotMade-1608</p></td>
<td><p>未對 <a href="gg269329(v=exchg.10).md">JetMakeKey</a>進行呼叫。</p></td>
</tr>
<tr class="even">
<td><p>JET_errUpdateNotPrepared-1609</p></td>
<td><p>未對 <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>進行呼叫。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDataHasChanged-1611</p></td>
<td><p>資料已變更，且作業已中止。</p></td>
</tr>
<tr class="even">
<td><p>JET_errLanguageNotSupported-1619</p></td>
<td><p>此 Windows 安裝不支援選取的語言。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManySorts-1701</p></td>
<td><p>排序處理常式太多。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidOnSort-1702</p></td>
<td><p>排序期間發生不正確操作。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTempFileOpenError-1803</p></td>
<td><p>無法開啟暫存檔。</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyAttachedDatabases-1805</p></td>
<td><p>開啟太多資料庫。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDiskFull-1808</p></td>
<td><p>磁片上沒有剩餘的空間。</p></td>
</tr>
<tr class="even">
<td><p>JET_errPermissionDenied-1809</p></td>
<td><p>許可權遭到拒絕。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileNotFound-1811</p></td>
<td><p>找不到檔案。</p></td>
</tr>
<tr class="even">
<td><p>JET_errFileInvalidType-1812</p></td>
<td><p>檔案類型無效。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errAfterInitialization-1850</p></td>
<td><p>無法在初始化之後啟動還原。</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogCorrupted-1852</p></td>
<td><p>無法解讀記錄。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidOperation-1906</p></td>
<td><p>作業無效。</p></td>
</tr>
<tr class="even">
<td><p>JET_errAccessDenied-1907</p></td>
<td><p>存取遭到拒絕。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManySplits-1909</p></td>
<td><p>無限分割。</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation-1910</p></td>
<td><p>多個執行緒使用相同的會話。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errEntryPointNotFound-1911</p></td>
<td><p>找不到必要 DLL 中的進入點。</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionCoNtextAlreadySet-1912</p></td>
<td><p>指定的會話已經有會話內容集。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionCoNtextNotSetByThisThread-1913</p></td>
<td><p>嘗試重設會話內容，但目前的執行緒不是設定會話內容的原始執行緒。</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionInUse-1914</p></td>
<td><p>嘗試終止目前使用中的會話。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordFormatConversionFailed-1915</p></td>
<td><p>動態記錄格式轉換期間發生內部錯誤。</p></td>
</tr>
<tr class="even">
<td><p>JET_errOneDatabasePerSession-1916</p></td>
<td><p> (，您可以在建立資料庫) 期間設定 <a href="gg269337(v=exchg.10).md">JET_paramOneDatabasePerSession</a> 旗標，藉以指定每個會話只會有一個開啟的使用者資料庫。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRollbackError-1917</p></td>
<td><p>復原期間發生錯誤。</p></td>
</tr>
<tr class="even">
<td><p>JET_errCallbackFailed-2101</p></td>
<td><p>回呼函數調用失敗。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCallbackNotResolved-2102</p></td>
<td><p>找不到回呼函數。</p></td>
</tr>
<tr class="even">
<td><p>JET_errOSSnapshotInvalidSequence-2401</p></td>
<td><p>作業系統陰影複製 API 使用了不正確順序。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotTimeOut-2402</p></td>
<td><p>作業系統陰影複製以超時時間結束。</p></td>
</tr>
<tr class="even">
<td><p>JET_errOSSnapshotNotAllowed-2403</p></td>
<td><p>不允許作業系統陰影複製，因為中的備份或復原正在進行中。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSnapId-2404</p></td>
<td><p>操作失敗，因為指定的作業系統陰影複製控制碼無效。</p></td>
</tr>
<tr class="even">
<td><p>JET_errLSCallbackNotSpecified-3000</p></td>
<td><p>嘗試在未指定回呼函數的情況下使用本機儲存體。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLSAlreadySet-3001</p></td>
<td><p>嘗試為已設定的物件設定本機儲存體。</p></td>
</tr>
<tr class="even">
<td><p>JET_errLSNotSet-3002</p></td>
<td><p>嘗試從沒有設定它的物件中取出本機儲存體。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileIOSparse-4000</p></td>
<td><p>I/o 作業失敗，因為它是針對檔案未配置的區域嘗試。</p></td>
</tr>
<tr class="even">
<td><p>JET_errFileIOBeyondEOF-4001</p></td>
<td><p>讀取已發出至 EOF 以外的位置 (寫入將會展開檔案) 。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileIOAbort-4002</p></td>
<td><p>此旗標會指示 JET_ABORTRETRYFAILCALLBACK 呼叫端中止指定的 i/o。</p></td>
</tr>
<tr class="even">
<td><p>JET_errFileIORetry-4003</p></td>
<td><p>此旗標會指示 JET_ABORTRETRYFAILCALLBACK 呼叫端重試指定的 i/o。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileIOFail-4004</p></td>
<td><p>此旗標會指示 JET_ABORTRETRYFAILCALLBACK 呼叫端使指定的 i/o 失敗。</p></td>
</tr>
<tr class="even">
<td><p>JET_errFileCompressed-4005</p></td>
<td><p>壓縮檔案不支援讀取/寫入存取。</p></td>
</tr>
</tbody>
</table>


### <a name="remarks"></a>備註

一般情況下，大於零的值應解釋為警告、值為零應解讀為成功，而小於零的值則應視為錯誤。 這些值中的其他模式（例如值的範圍）應該是由應用程式所依賴。

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


### <a name="see-also"></a>另請參閱

[錯誤處理參數](./error-handling-parameters.md)  
[可擴充儲存引擎錯誤](./extensible-storage-engine-errors.md)  
[可擴充儲存引擎檔案](./extensible-storage-engine-files.md)
