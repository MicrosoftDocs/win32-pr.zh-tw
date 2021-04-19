---
title: Active Directory Domain Services 中函式的記錄和復原錯誤
description: 本主題列出 Active Directory Domain Services 中函數的記錄和復原錯誤傳回值。
ms.assetid: b927073a-8bbc-45d4-b9d3-25f3aa6c6f53
ms.tgt_platform: multiple
keywords:
- Active Directory 記錄和復原錯誤廣告
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6fba921a63eb399d6ed4f44ef8569ed05370403
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969433"
---
# <a name="logging-and-recovery-errors-in-functions-in-active-directory-domain-services"></a>Active Directory Domain Services 中函式的記錄和復原錯誤

本主題列出 Active Directory Domain Services 中函數的記錄和復原錯誤傳回值。



| 值                                | 描述                                                                                                                      |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| **hrLogFileCorrupt**                 | 記錄檔已損毀。                                                                                                         |
| **hrNoBackupDirectory**              | 未提供備份目錄。                                                                                                   |
| **hrBackupDirectoryNotEmpty**        | 備份目錄不是空的。                                                                                               |
| **hrBackupInProgress**               | 備份正在使用中。                                                                                                                |
| **hrMissingPreviousLogFile**         | 檢查點的記錄檔遺失。                                                                                        |
| **hrLogWriteFail**                   | 無法寫入記錄檔。                                                                                                 |
| **hrBadLogVersion**                  | 記錄檔的版本與 (NTDS) 的 Windows NT/Windows 2000 目錄服務資料庫版本不相容。 |
| **hrInvalidLogSequence**             | 下一個記錄檔中的時間戳記與預期的不符。                                                                 |
| **hrLoggingDisabled**                | 記錄檔並非使用中。                                                                                                           |
| **hrLogBufferTooSmall**              | 記錄緩衝區太小而無法復原。                                                                                     |
| **hrLogSequenceEnd**                 | 已超過記錄檔的最大數目。                                                                               |
| **hrNoBackup**                       | 沒有進行中的備份。                                                                                                  |
| **hrInvalidBackupSequence**          | 備份呼叫順序不是。                                                                                              |
| **hrBackupNotAllowedYet**            | 目前無法執行備份。                                                                                                  |
| **hrDeleteBackupFileFail**           | 無法刪除備份檔案。                                                                                                |
| **hrMakeBackupDirectoryFail**        | 無法制作備份臨時目錄。                                                                                     |
| **hrInvalidBackup**                  | 啟用迴圈記錄時，無法執行增量備份。                                                      |
| **hrRecoveredWithErrors**            | 修復過程中發生錯誤。                                                                               |
| **hrMissingLogFile**                 | 遺失目前的記錄檔。                                                                                                 |
| **hrLogDiskFull**                    | 記錄磁碟已滿。                                                                                                            |
| **hrBadLogSignature**                | 記錄檔已損毀。                                                                                                           |
| **hrBadDbSignature**                 | 資料庫檔案已損毀。                                                                                                      |
| **hrBadCheckpointSignature**         | 檢查點檔案已損毀。                                                                                                    |
| **hrCheckpointCorrupt**              | 找不到檢查點檔案或其已損毀。                                                                       |
| **hrDatabaseInconsistent**           | 資料庫已損毀。                                                                                                         |
| **hrConsistentTimeMismatch**         | 資料庫的上次一致時間不相符。                                                                      |
| **hrPatchFileMismatch**              | 此備份不會產生修補檔案。                                                                                |
| **hrRestoreLogTooLow**               | 開始記錄檔編號太低，無法進行還原。                                                                              |
| **hrRestoreLogTooHigh**              | 還原的起始記錄檔編號過高。                                                                             |
| **hrGivenLogFileHasBadSignature**    | 從磁帶下載的記錄檔已損毀。                                                                                |
| **hrGivenLogFileIsNotContiguous**    | 下載磁帶之後，找不到強制的記錄檔。                                                               |
| **hrMissingRestoreLogFiles**         | 因為缺少某些記錄檔，所以未完全還原資料。                                                               |
| **hrExistingLogFileHasBadSignature** | 記錄檔路徑中的記錄檔已損毀。                                                                                    |
| **hrExistingLogFileIsNotContiguous** | 在記錄檔路徑中找不到強制的記錄檔。                                                                        |
| **hrMissingFullBackup**              | 資料庫在增量備份之前遺漏了先前的完整備份。                                                        |
| **hrBadBackupDatabaseSize**          | 備份資料庫大小必須是 4000 (4096 位元組) 的倍數。                                                                |
| **hrTermInProgress**                 | 資料庫即將關閉。                                                                                                 |
| **hrFeatureNotAvailable**            | 無法使用此功能。                                                                                                    |
| **hrInvalidName**                    | 名稱無效。                                                                                                             |
| **hrInvalidParameter**               | 參數無效。                                                                                                        |
| **hrColumnNull**                     | 資料行的值為 null。                                                                                                 |
| **hrBufferTruncated**                | 緩衝區對資料而言太小。                                                                                                |
| **hrDatabaseAttached**               | 資料庫已附加。                                                                                                |
| **hrInvalidDatabaseId**              | 資料庫識別碼無效。                                                                                                      |
| **hrOutOfMemory**                    | 電腦記憶體不足。                                                                                                   |
| **hrOutOfDatabaseSpace**             | 資料庫已達到 16 GB 的大小上限。                                                                              |
| **hrOutOfCursors**                   | 資料表外資料指標。                                                                                                            |
| **hrOutOfBuffers**                   | 超出資料庫頁面緩衝區。                                                                                                    |
| **hrTooManyIndexes**                 | 有太多索引。                                                                                                      |
| **hrTooManyKeys**                    | 索引中有太多資料行。                                                                                          |
| **hrRecordDeleted**                  | 記錄已刪除。                                                                                                     |
| **hrReadVerifyFailure**              | 發生讀取驗證錯誤。                                                                                              |
| **hrOutOfFileHandles**               | 檔案控制代碼用完。                                                                                                             |
| **hrDiskIO**                         | 發生磁片 i/o 錯誤。                                                                                                       |
| **hrInvalidPath**                    | 檔案的路徑無效。                                                                                                 |
| **hrRecordTooBig**                   | 記錄已超過大小上限。                                                                                        |
| **hrTooManyOpenDatabases**           | 開啟的資料庫太多。                                                                                               |
| **hrInvalidDatabase**                | 檔案不是資料庫檔案。                                                                                                 |
| **hrNotInitialized**                 | 尚未呼叫資料庫。                                                                                                 |
| **hrAlreadyInitialized**             | 已呼叫資料庫。                                                                                                 |
| **hrFileAccessDenied**               | 無法存取檔案。                                                                                                       |
| **hrBufferTooSmall**                 | 緩衝區太小。                                                                                                         |
| **hrSeekNotEqual**                   | SeekLE 或 SeekGE 都找不到完全相符的。                                                                              |
| **hrTooManyColumns**                 | 定義的資料行太多。                                                                                              |
| **hrContainerNotEmpty**              | 容器不是空的。                                                                                                      |
| **hrInvalidFilename**                | 檔案名無效。                                                                                                         |
| **hrInvalidBookmark**                | 書簽無效。                                                                                                         |
| **hrColumnInUse**                    | 資料行用於索引中。                                                                                                  |
| **hrInvalidBufferSize**              | 資料緩衝區不符合資料行大小。                                                                                  |
| **hrColumnNotUpdatable**             | 無法設定資料行值。                                                                                                  |
| **hrIndexInUse**                     | 索引正在使用中。                                                                                                             |
| **hrNullKeyDisallowed**              | 索引上不允許 Null 索引鍵。                                                                                           |
| **hrNotInTransaction**               | 作業必須位於交易內。                                                                                      |
| **hrNoIdleActivity**                 | 未發生任何閒置活動。                                                                                                       |
| **hrTooManyActiveUsers**             | 有太多活動資料庫使用者。                                                                                        |
| **hrInvalidCountry**                 | 國家或地區代碼未知或無效。                                                                    |
| **hrInvalidLanguageId**              | 語言識別項未知或無效。                                                                               |
| **hrInvalidCodePage**                | 字碼頁未知或無效。                                                                                 |
| **hrNoWriteLock**                    | 交易層級0沒有寫入鎖定。                                                                                   |
| **hrColumnSetNull**                  | 資料行值設定為 null。                                                                                                 |
| **hrVersionStoreOutOfMemory**        | LMaxVerPages 超過 (XJET 只) 。                                                                                           |
| **hrCurrencyStackOutOfMemory**       | 資料指標外。                                                                                                                  |
| **hrOutOfSessions**                  | 會話不足。                                                                                                                 |
| **hrWriteConflict**                  | 寫入鎖定因未處理的寫入鎖定而失敗。                                                                          |
| **hrTransTooDeep**                   | 交易的嵌套太深。                                                                                          |
| **hrInvalidSesid**                   | 會話控制碼無效。                                                                                                   |
| **hrSessionWriteConflict**           | 另一個會話具有頁面的私用版本。                                                                               |
| **hrInTransaction**                  | 交易內不允許此作業。                                                                               |
| **hrDatabaseDuplicate**              | 資料庫已經存在。                                                                                                     |
| **hrDatabaseInUse**                  | 資料庫正在使用中。                                                                                                          |
| **hrDatabaseNotFound**               | 資料庫不存在。                                                                                                     |
| **hrDatabaseInvalidName**            | 資料庫名稱無效。                                                                                                    |
| **hrDatabaseInvalidPages**           | 頁面的數目無效。                                                                                                  |
| **hrDatabaseCorrupted**              | 資料庫檔案可能已損毀或找不到。                                                                          |
| **hrDatabaseLocked**                 | 資料庫已鎖定。                                                                                                          |
| **hrTableEmpty**                     | 已開啟空白資料表。                                                                                                       |
| **hrTableLocked**                    | 資料表已鎖定。                                                                                                             |
| **hrTableDuplicate**                 | 資料表已經存在。                                                                                                        |
| **hrTableInUse**                     | 因為資料表已在使用中，所以無法將其鎖定。                                                                           |
| **hrObjectNotFound**                 | 資料表或物件不存在。                                                                                              |
| **hrCannotRename**                   | 無法重新命名暫存檔案。                                                                                             |
| **hrDensityInvalid**                 | 檔案/索引密度無效。                                                                                               |
| **hrTableNotEmpty**                  | 無法定義叢集索引。                                                                                            |
| **hrInvalidTableId**                 | 資料表識別碼無效。                                                                                                         |
| **hrTooManyOpenTables**              | 無法開啟任何其他資料表。                                                                                                  |
| **hrIllegalOperation**               | 資料表不支援此作業。                                                                                        |
| **hrObjectDuplicate**                | 資料表或物件名稱已在使用中。                                                                                  |
| **hrInvalidObject**                  | 物件對作業無效。                                                                                             |
| **hrIndexCantBuild**                 | 無法建立叢集索引。                                                                                               |
| **hrIndexHasPrimary**                | 已定義主要索引。                                                                                            |
| **hrIndexDuplicate**                 | 已定義索引。                                                                                                    |
| **hrIndexNotFound**                  | 索引不存在。                                                                                                        |
| **hrIndexMustStay**                  | 無法刪除叢集索引。                                                                                              |
| **hrIndexInvalidDef**                | 索引定義不合法。                                                                                                 |
| **hrIndexHasClustered**              | 已定義叢集索引。                                                                                          |
| **hrCreateIndexFailed**              | 無法建立索引，因為建立資料表時發生錯誤。                                                     |
| **hrTooManyOpenIndexes**             | 索引描述區塊外。                                                                                                 |
| **hrColumnLong**                     | 資料行值太長。                                                                                                    |
| **hrColumnDoesNotFit**               | 欄位將無法放入記錄中。                                                                                            |
| **hrNullInvalid**                    | 此值不能是 null。                                                                                                        |
| **hrColumnIndexed**                  | 因為資料行已編制索引，所以無法刪除。                                                                                  |
| **hrColumnTooBig**                   | 欄位的長度超過255個位元組的最大長度。                                                                 |
| **hrColumnNotFound**                 | 找不到資料行。                                                                                                       |
| **hrColumnDuplicate**                | 欄位已經定義。                                                                                                    |
| **hrColumn2ndSysMaint**              | 每個資料表只允許有一個自動遞增或版本資料行。                                                                  |
| **hrInvalidColumnType**              | 資料行資料類型無效。                                                                                                 |
| **hrColumnMaxTruncated**             | 因為資料行超過最大長度255個位元組，所以已截斷。                                                    |
| **hrColumnCannotIndex**              | 無法編制 long 值資料行的索引。                                                                                             |
| **hrTaggedNotNull**                  | 標記的資料行不可以是 null。                                                                                                   |
| **hrNoCurrentIndex**                 | 專案無效，沒有目前的索引。                                                                                    |
| **hrKeyIsMade**                      | 金鑰已完成。                                                                                                             |
| **hrBadColumnId**                    | 資料行識別碼不正確。                                                                                                      |
| **hrBadItagSequence**                | 多重值資料行有不正確的實例識別碼。                                                                     |
| **hrCannotBeTagged**                 | 自動遞增和版本不能是多重值。                                                                                 |
| **hrRecordNotFound**                 | 找不到索引鍵。                                                                                                          |
| **hrNoCurrentRecord**                | 貨幣不在記錄上。                                                                                                 |
| **hrRecordClusteredChanged**         | 叢集索引鍵無法變更。                                                                                               |
| **hrKeyDuplicate**                   | 機碼已存在。                                                                                                          |
| **hrAlreadyPrepared**                | 目前的專案已複製或清除。                                                                            |
| **hrKeyNotMade**                     | 未建立任何金鑰。                                                                                                                 |
| **hrUpdateNotPrepared**              | 尚未準備更新。                                                                                                         |
| **hrwrnDataHasChanged**              | 資料已變更。                                                                                                                |
| **hrerrDataHasChanged**              | 已放棄作業，因為資料已變更。                                                                            |
| **hrKeyChanged**                     | 移至新的機碼。                                                                                                              |
| **hrTooManySorts**                   | 排序處理常式太多。                                                                                               |
| **hrInvalidOnSort**                  | 排序中發生不正確作業。                                                                               |
| **hrTempFileOpenError**              | 無法開啟暫存檔案。                                                                                               |
| **hrTooManyAttachedDatabases**       | 開啟了太多資料庫。                                                                                               |
| **hrDiskFull**                       | 磁碟已滿。                                                                                                                |
| **hrPermissionDenied**               | 許可權遭到拒絕。                                                                                                            |
| **hrFileNotFound**                   | 找不到檔案。                                                                                                         |
| **hrFileOpenReadOnly**               | 資料庫檔案是唯讀的。                                                                                                  |
| **hrAfterInitialization**            | 無法在初始化之後還原。                                                                                          |
| **hrLogCorrupted**                   | 資料庫記錄檔已損毀。                                                                                              |
| **hrInvalidOperation**               | 作業無效。                                                                                                        |
| **hrAccessDenied**                   | 存取遭到拒絕。                                                                                                                |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

「成功」
</dt> <dt>

[Active Directory Domain Services 中的備份錯誤](backup-errors-in-active-directory-domain-services.md)
</dt> <dt>

[Active Directory Domain Services 中的系統錯誤](system-errors-in-active-directory-domain-services.md)
</dt> <dt>

[目錄管理員錯誤](directory-manager-errors.md)
</dt> <dt>

[Active Directory Domain Services 中函數的傳回值](return-values-for-functions-in-active-directory-domain-services.md)
</dt> </dl>

 

 




