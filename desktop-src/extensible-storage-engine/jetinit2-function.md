---
description: 深入瞭解： JetInit2 函數
title: JetInit2 函式
TOCTitle: JetInit2 Function
ms:assetid: b5541429-6ce6-457b-88cf-673d267f6209
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294065(v=EXCHG.10)
ms:contentKeyID: 32765680
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetInit2
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7874c475dc18beb5d7f6849b9f628ea06cbc32a3
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470453"
---
# <a name="jetinit2-function"></a>JetInit2 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetinit2-function"></a>JetInit2 函式

**JetInit2** 函式會將資料庫引擎置於可支援資料庫檔案之應用程式使用的狀態。 引擎必須已正確設定，才能使用 [JetSetSystemParameter](./jetsetsystemparameter-function.md)進行初始化。 資料庫損毀復原會在初始化過程中自動執行。

**Windows xp：****JetInit2** 是在 Windows xp 引進。  

此函式已過時。 請改用 [JetInit3](./jetinit3-function.md) 。

```cpp
JET_ERR JET_API JetInit2(
  __in_out_opt  JET_INSTANCE* pinstance,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a>參數

*pinstance*

此呼叫所要使用的實例。

針對 Windows 2000，此參數會被忽略，且應該一律為 Null。

針對 Windows XP 和更新版本，此參數的使用取決於引擎的作業模式。 如果引擎在舊版模式下運作 (Windows 2000 相容性模式) 只支援一個實例，此參數可能是 null 或設定為有效的輸出緩衝區，其中包含 null 或 JET_instanceNil，它會傳回做為初始化的副作用所建立的全域實例控制碼。 然後，這個實例控制碼可以傳遞給任何其他接受實例的 API。 如果引擎是在多重實例模式中作業，這個參數必須設定為有效的輸入緩衝區，其中包含正在初始化的 [JetCreateInstance](./jetcreateinstance-function.md) 所傳回的實例控制碼。

*grbit*

指定零或多個下列選項的位群組。


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>JET_bitReplayReplicatedLogFiles</p> | <p>保留供未來使用。</p> | 
| <p>JET_bitCreateSFSVolumeIfNotExist</p> | <p>保留供未來使用。</p> | 
| <p>JET_bitReplayIgnoreMissingDB</p> | <p>此選項可讓使用者在一組記錄檔上執行復原，而不會有所有資料庫都在記錄集的某個點附加。</p> | 
| <p>JET_bitRecoveryWithoutUndo</p> | <p>執行復原，但在恢復階段停止。 這可讓您在中複製及套用其他交易記錄。</p> | 
| <p>JET_bitTruncateLogsAfterRecovery</p> | <p>在成功的軟修復上，截斷記錄檔。</p> | 
| <p>JET_bitReplayMissingMapEntryDB</p> | <p>遺漏資料庫對應專案預設為相同的位置。</p> | 
| <p>JET_bitReplayIgnoreLostLogs</p> | <p>略過記錄資料流程結尾遺失的記錄檔。</p><p><strong>Windows 7： JET_bitReplayIgnoreLostLogs</strong>是 Windows 7 中引進的。</p> | 



### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


#### <a name="remarks"></a>備註

必須先使用 **JetInit2** 的呼叫來初始化實例，才能由 [JetSetSystemParameter](./jetsetsystemparameter-function.md)以外的任何人使用。

實例會透過呼叫 [JetTerm](./jetterm-function.md) 函式終結，即使該實例從未使用 [JetInit](./jetinit-function.md)初始化也是一樣。 實例是 database engine 的復原單位。 它會控制所有檔案的生命週期，用來保護一組資料庫檔案中資料的完整性。 這些檔案包括檢查點檔案和交易記錄檔。

如果復原是在一組記錄檔上執行，但並非所有資料庫都存在 (這會在正常情況下傳回錯誤 JET_errAttachedDatabaseMismatch，而且用戶端希望復原在一般) 情況下仍繼續使用，而用戶端則會使用 JET_ bitReplayIgnoreMissingDB 來繼續復原可用的資料庫。

如需詳細資訊，請參閱 [JetInit](./jetinit-function.md) 中的「備註」一節。

#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista 或 Windows XP。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008 或 Windows server 2003。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 



#### <a name="see-also"></a>另請參閱

[可擴充的儲存體引擎檔案](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetInit3](./jetinit3-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[資源參數](./resource-parameters.md)
