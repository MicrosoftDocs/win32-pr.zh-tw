---
description: 深入瞭解： JetInit3 函數
title: JetInit3 函式
TOCTitle: JetInit3 Function
ms:assetid: 752589b6-1b8f-4b6f-a14a-00f4b1405db5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269296(v=EXCHG.10)
ms:contentKeyID: 32765588
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetInit3
- JetInit3A
- JetInit3W
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0a0c73343550768a9ccd061c702fae89d562d095
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477904"
---
# <a name="jetinit3-function"></a>JetInit3 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetinit3-function"></a>JetInit3 函式

**JetInit3** 函式會將資料庫引擎置於可支援資料庫檔案應用程式使用的狀態。 引擎必須已正確設定初始化，您可以使用 [JetSetSystemParameter](./jetsetsystemparameter-function.md) 函數完成此操作。 請注意，資料庫損毀復原會在初始化過程中自動進行。

**Windows vista：****JetInit3** 是 Windows vista 引進。  

```cpp
    JET_ERR JET_API JetInit3(
      __in_out_opt  JET_INSTANCE* pinstance,
      __in_opt      JET_RSTINFO* prstInfo,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>參數

*pinstance*

用於特定呼叫的實例。 此參數的使用取決於引擎的操作模式。 如果引擎是在舊版模式下運作 (Windows 2000 相容性模式) ，其中只支援一個實例，您可以將此參數設定為 **null** 或包含 **null** 或 JET_instanceNil 的有效輸出緩衝區，這會傳回建立為初始化副作用的全域實例控制碼。 然後，這個實例控制碼可以傳遞給任何其他接受實例的 API。 如果引擎是在多重實例模式中作業，您必須將此參數設定為有效的輸入緩衝區，其中包含正在初始化的 [JetCreateInstance](./jetcreateinstance-function.md) 函數所傳回的實例控制碼。

*prstInfo*

在復原期間用來重新對應資料庫的其他修復參數，用於設定復原將停止的位置，或用來判斷目前的復原狀態。

*grbit*

一組位，指定下表所列和定義的零或多個選項。


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>JET_bitReplayReplicatedLogFiles</p> | <p>這個值已保留供未來使用</p> | 
| <p>JET_bitCreateSFSVolumeIfNotExist</p> | <p>這個值已保留供未來使用</p> | 
| <p>JET_bitReplayIgnoreMissingDB</p> | <p>此值可讓使用者在一組記錄檔上執行復原，即使在某個時間點沒有附加至記錄檔的資料庫也一樣。</p> | 
| <p>JET_bitRecoveryWithoutUndo</p> | <p>此值可讓使用者執行復原，但最多隻能 (且不包括) 的復原階段。 使用這個值，可以在中複製及套用其他交易記錄。</p> | 
| <p>JET_bitTruncateLogsAfterRecovery</p> | <p>此值會在成功的軟復原期間，讓記錄檔被截斷。</p> | 
| <p>JET_bitReplayMissingMapEntryDB</p> | <p>此值會導致遺失的資料庫對應專案預設為相同的位置。</p> | 
| <p>JET_bitReplayIgnoreLostLogs</p> | <p>此值會導致復原期間遺失記錄資料流程結尾的記錄檔。</p><p><strong>Windows 7： JET_bitReplayIgnoreLostLogs</strong>是 Windows 7 中引進的。</p> | 



### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能的可延伸儲存體引擎 (ESE) 錯誤的詳細資訊，請參閱[可擴展的儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


#### <a name="remarks"></a>備註

您必須使用 **JetInit3** 函式的呼叫來初始化實例，才能將其用於 [JetSetSystemParameter](./jetsetsystemparameter-function.md) 函數以外的任何其他作業。

實例會透過呼叫 [JetTerm](./jetterm-function.md) 函式終結，即使該實例從未使用 [JetInit](./jetinit-function.md) 函數初始化也是一樣。 實例是 database engine 的復原單位。 它會控制所有檔案的生命週期，用來保護一組資料庫檔案中資料的完整性。 這些檔案包括檢查點檔案和交易記錄檔。 請注意，如果 **JetInit3** 函式失敗，則不應呼叫 [JetTerm](./jetterm-function.md) 。 但是，如果從未呼叫 **JetInit3** 或 **JetInit3** 成功， **JetCreateInstance2** 建立的所有實例仍應呼叫 [JetTerm](./jetterm-function.md) 。

如果復原是在一組不是所有相關資料庫的記錄中執行 (這會在正常情況下傳回錯誤 JET_errAttachedDatabaseMismatch，而用戶端想要在遺失資料庫的) 情況下，讓用戶端繼續復原，則會使用 JET_bitReplayIgnoreMissingDB 錯誤來繼續復原可用的資料庫。

因為損毀復原通常不會發生在同一部電腦上 (而且具有與當機時相同的設定) ，所以資料庫通常不會變更位置。 在某些情況下，例如將檔案移至不同的電腦，或將快照集備份還原到不同的位置，這已不再成立。 **JetInit3** 函式可讓您指定對應 (使用 [JET_RSTINFO](./jet-rstinfo-structure.md) ，以及在舊的資料庫位置與新位置之間) [JET_RSTMAP](./jet-rstmap-structure.md)結構。 事實上，只要資料庫檔案存在於該位置，您就只需要新的位置。 一旦您知道已還原資料庫的位置，資料庫簽章將用來透過還原程式來識別資料庫。 只有當您需要重新建立資料庫時，才需要使用原始的資料庫位置，此時就會知道簽章。

此外，如果您需要在復原作業之後停止復原，則可以指定復原將停止的特定記錄檔位置。 請注意，如果指定的位置是產生的一部分，但超過實際記錄檔的結尾，則這包括在特定記錄產生的結尾處停止的功能。

如需詳細資訊，請參閱 [JetInit](./jetinit-function.md) 主題中的「備註」一節。

#### <a name="requirements"></a>規格需求


| | | <p>用戶端</p> | <p>需要 Windows Vista。</p> | | <p>伺服器</p> | <p>需要 Windows Server 2008。</p> | | <p>標頭</p> | <p>宣告于 Esent. h 中。</p> | | <p>程式庫</p> | <p>使用 ESENT。</p> | | <p>DLL</p> | <p>需要 ESENT.dll。</p> | | <p>Unicode</p> | <p>實作為 <strong>JetInit3W</strong> (Unicode) 和 <strong>JetInit3A</strong> (ANSI) 。</p> | 



#### <a name="see-also"></a>另請參閱

[可擴充的儲存體引擎檔案](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_RSTINFO](./jet-rstinfo-structure.md)  
[JET_RSTMAP](./jet-rstmap-structure.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetInit2](./jetinit2-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[資源參數](./resource-parameters.md)
