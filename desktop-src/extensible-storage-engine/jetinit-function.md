---
description: 深入瞭解： JetInit 函數
title: JetInit 函式
TOCTitle: JetInit Function
ms:assetid: b7f78cca-7268-4045-bda2-20746b1d6370
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294068(v=EXCHG.10)
ms:contentKeyID: 32765683
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetInit
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 308c012bc5eb144e0ac0d608c64d63ccf39aeca1
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "104323463"
---
# <a name="jetinit-function"></a>JetInit 函式


_**適用于：** Windows |Windows Server_

## <a name="jetinit-function"></a>JetInit 函式

**JetInit** 函式會將資料庫引擎置於可支援資料庫檔案之應用程式使用的狀態。 引擎必須已正確設定，才能使用 [JetSetSystemParameter](./jetsetsystemparameter-function.md)進行初始化。 資料庫損毀復原會在初始化過程中自動執行。

```cpp
JET_ERR JET_API JetInit(
  __in_out_opt  JET_INSTANCE* pinstance
);
```

### <a name="parameters"></a>參數

*pinstance*

此呼叫所要使用的實例。

若為 Windows 2000，則會忽略此參數，且應一律為 Null。

若為 Windows XP 和更新版本，則使用這個參數取決於引擎的操作模式。 如果引擎是在舊版模式下運作 (Windows 2000 相容性模式) 只支援一個實例，此參數可以是 Null，也可以設定為有效的輸出緩衝區，它會傳回做為初始化的副作用而建立的全域實例控制碼。 此輸出緩衝區必須設定為 Null 或 JET_instanceNil。 然後，這個實例控制碼可以傳遞給任何其他使用實例的函數。 如果引擎是在多重實例模式中作業，則這個參數必須設定為有效的輸入緩衝區，其中包含正在初始化的 [JetCreateInstance](./jetcreateinstance-function.md) 函式實例所傳回的實例控制碼。


#### <a name="remarks"></a>備註

必須先使用 **JetInit** 的呼叫來初始化實例，才能由 [JetSetSystemParameter](./jetsetsystemparameter-function.md)以外的任何人使用。

實例會透過呼叫 [JetTerm](./jetterm-function.md) 函式終結，即使該實例從未使用 **JetInit** 初始化也是一樣。 實例是 database engine 的復原單位。 它會控制所有檔案的生命週期，用來保護一組資料庫檔案中資料的完整性。 這些檔案包括檢查點檔案和交易記錄檔。

可以在任何時間建立的實例數目上限是由 [JET_paramMaxInstances](./resource-parameters.md)所控制，可以透過呼叫 [JetSetSystemParameter](./jetsetsystemparameter-function.md)來設定。 當資料庫引擎第一次初始化時， **JetInit** 會建立一組初始的檔案，以支援該實例。 這些檔案包含名為 (的檢查點檔案 \<[JET_paramBaseName](./transaction-log-parameters.md)\> 。.CHK) 是一組名為 RES1 (的保留交易記錄檔。記錄檔和 RES2。記錄) ， (名為的初始交易記錄檔 \<[JET_paramBaseName](./transaction-log-parameters.md)\> 。記錄) 和暫存資料庫檔案 (根據 [JET_paramTempPath](./temporary-database-parameters.md)) 進行命名。 如果 [JET_paramRecovery](./transaction-log-parameters.md) 設定為 [關閉]，則不會建立檢查點檔案和記錄檔。 如果 [JET_paramMaxTemporaryTables](./temporary-database-parameters.md) 設定為零，則不會建立暫存資料庫檔案。 這些檔案代表實例的磁片使用量，且必須小心管理。 如果這些檔案是個別損毀或彼此相關，則與實例相關聯之資料庫中儲存的資料可能會遺失。

使用一組現有的交易記錄檔初始化資料庫引擎時，系統會檢查這些檔案，以查看先前的具現化身是否遇到損毀。 如果偵測到損毀，則會自動執行損毀復原。 此程式會在先前化身引擎期間重建附加至實例的資料庫，並將變更儲存回資料庫檔案。 結果會是交易一致的資料庫。 如果要對資料庫重新執行的交易記錄檔數目很大，則此程式可能需要很長的時間。

由於 **JetInit** 會執行損毀復原，因此在發生失敗的情況下，幾乎可能會傳回任何資料庫引擎錯誤。 在實務上，部署中的大部分錯誤都分為兩種類別：資料損毀和檔案 mismanagement。 資料損毀的資訊清單本身通常會出現在下列或類似的錯誤中：

  - JET_errReadVerifyFailure

  - JET_errLogFileCorrupt

  - JET_errCheckpointCorrupt

這些錯誤幾乎都是由硬體問題所造成，因此無法避免。 檔案 mismanagement 會在下列或類似的錯誤中最常出現的資訊清單：

  - JET_errMissingLogFile

  - JET_errAttachedDatabaseMismatch

  - JET_errDatabaseSharingViolation

  - JET_errInvalidLogSequence

如果復原是在一組記錄檔上執行，而且並非所有資料庫都存在 (這會在正常) 情況下傳回錯誤 JET_errAttachedDatabaseMismatch，而且用戶端想要復原以 JET_ 繼續進行可用的資料庫的復原。 這些錯誤是由應用程式所 preventable。 應用程式必須小心保護這些檔案的存放庫，使其不受使用者或其他應用程式這類外部強制操作的影響。 如果應用程式想要完全終結實例，則必須刪除與該實例相關聯的所有檔案。 這些包括檢查點檔案、交易記錄檔，以及附加至實例的任何資料庫檔案。

在 Windows 2000 和更新版本之間， **JetInit** 函式的行為與附加至實例的資料庫檔案有不同的行為。

**Windows 2000：**  在 Windows 2000 中，在先前化身實例期間附加至實例的任何資料庫，在 **JetInit** 順利完成之後仍會附加至實例。 在 **JetInit** 之後不需要呼叫 [JetAttachDatabase](./jetattachdatabase-function.md) ，以確保日後的資料庫存取。 如果在 **JetInit** 函數之後呼叫 [JetAttachDatabase](./jetattachdatabase-function.md)函數，則會傳回 JET_wrnDatabaseAttached 警告。 此警告表示已保留資料庫附件，而且可以忽略。

**WINDOWS XP：**  在 Windows XP 和更新版本中， **JetInit** 會自動將所有資料庫從實例卸離。 這表示在這種情況下，必須一律在 **JetInit** 之後呼叫 [JetAttachDatabase](./jetattachdatabase-function.md) 。

任何撰寫為在 Windows 2000 和更新版本上執行的應用程式，在 **JetInit** 之後都必須一律呼叫 [JetAttachDatabase](./jetattachdatabase-function.md) 。 如果應用程式在 Windows 2000 上執行，則在某些情況下，它必須預期會有 JET_wrnDatabaseAttached。 如需詳細資訊，請參閱 [JetAttachDatabase](./jetattachdatabase-function.md) 。

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
</tbody>
</table>


#### <a name="see-also"></a>另請參閱

[可擴充儲存引擎檔案](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_paramMaxTemporaryTables](./temporary-database-parameters.md)  
[JET_paramRecovery](./transaction-log-parameters.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit3](./jetinit3-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
