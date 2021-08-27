---
description: 深入瞭解： JetSetSessionParameter 函數
title: JetSetSessionParameter 函式
TOCTitle: JetSetSessionParameter Function
ms:assetid: 11aecf42-22ef-4bea-a3d7-961a7bdc85aa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835038(v=EXCHG.10)
ms:contentKeyID: 49894660
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetSetSessionParameter
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9ce9c50908621f005ec69aa75da4afdfa722b8aa
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988401"
---
# <a name="jetsetsessionparameter-function"></a>JetSetSessionParameter 函式


_**適用于：** Windows |Windows伺服器_

**JetSetSessionParameter** 函數會設定 database engine。

``` c++
JET_ERR JET_API JetSetSessionParameter (
  __in_opt      JET_SESID sesid,
  __in          unsigned long sesparamid,
  __in_read_bytes_opt_(cbParam)  void* pvParam,
  __in          unsigned long cbParam
);
```

### <a name="parameters"></a>參數

*sesid*

指定此呼叫所要使用的會話。

指定時，會忽略指定的實例，並使用與會話相關聯的實例。

*sesparamid*

要設定之會話參數的識別碼。

*pvParam*

要在此會話參數中設定的資料。

*cbParam*

所提供資料的大小。

### <a name="return-value"></a>傳回值

此函數會傳回 [JET_ERR](./jet-err.md) 資料類型，其中包含下表所列的其中一個傳回碼。 如需可能的可延伸儲存體引擎 (ESE) 錯誤的詳細資訊，請參閱[可擴展的儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errAlreadyInitialized</p> | <p>已使用 <a href="gg294068(v=exchg.10).md">JetInit</a> 函式的呼叫來初始化實例，因此無法執行此作業。 當您嘗試在參數值變更之後設定系統參數，不會再影響資料庫引擎的狀態時，就會發生這種情況。</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>無法完成作業，因為與該會話相關聯之實例上的所有活動都已停止，因為呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a> 函數。</p> | 
| <p>JET_errIndexTuplesInvalidLimits</p> | <p>指定的元組索引參數不合法。 只有當 <em>JET_paramIndexTuplesLengthMin</em>、 <em>JET_paramIndexTuplesLengthMax</em>或 <em>JET_paramIndexTuplesToIndexMax</em> 參數設定為不合法的值時，才會傳回此錯誤。 如需這些參數的詳細資訊，請參閱 <a href="gg294119(v=exchg.10).md">索引參數</a>。</p> | 
| <p>JET_errInitInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在初始化。</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</p> | 
| <p>JET_errInvalidParameter</p> | <p>提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。 發生下列情況時可能會發生這種情況：</p><ul><li><p>指定的系統參數識別碼無效或不受支援。</p></li><li><p>嘗試以字串的長度設定字串值系統參數，其長度超出參數的合法範圍。</p></li><li><p>嘗試以檔案路徑設定字串值系統參數，其絕對路徑表示的長度超出該參數的合法範圍。</p></li><li><p>嘗試以參數的合法範圍以外的整數來設定整數值系統參數。</p></li><li><p>嘗試使用 null <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> 指標、不正確 LCID 或一組不支援的 <strong>LCMapString</strong> 旗標來設定 JET_paramUnicodeIndexDefault。</p></li><li><p>無法設定指定的系統參數，因為它是唯讀的。</p></li><li><p>嘗試在呼叫 <a href="gg294068(v=exchg.10).md">JetInit</a> 函數之後設定系統參數、資料庫引擎處於單一實例模式，且未指定會話。</p></li><li><p>指定的系統參數是全域的，且已嘗試為該系統參數設定實例特定的值。</p></li><li><p>指定的系統參數僅供每個實例使用，並嘗試設定該系統參數的全域值。</p></li></ul> | 
| <p>JET_errInvalidPath</p> | <p>指定的檔案系統路徑無效。 只有在設定代表檔案系統路徑的系統參數時， <strong>JetSetSessionParameter</strong> 才會傳回此錯誤。 例如， <em>JET_paramSystemPath</em> 參數可能會傳回此錯誤。 如需這個參數的詳細資訊，請參閱 <a href="gg269235(v=exchg.10).md">交易記錄參數</a>。</p> | 
| <p>JET_errNotInitialized</p> | <p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p> | 
| <p>JET_errRestoreInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p> | 
| <p>JET_errTermInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在關閉。</p> | 
| <p>JET_errInvalidSesid</p> | <p>會話控制碼無效或參考已關閉的會話。</p><p>在所有情況下，都不會傳回此錯誤。 控制碼只會根據最大努力進行驗證。</p> | 
| <p>JET_errInvalidInstance</p> | <p>實例控制碼無效，或參考已關閉的實例。</p><p>在所有情況下，都不會傳回此錯誤。 控制碼只會根據最大努力進行驗證。</p> | 



成功時，系統參數將會設定為提供的值。

失敗時，系統參數值會維持不變。

#### <a name="requirements"></a>規格需求


| 需求 | 值 |
|------------|----------|
| <p><strong>用戶端</strong></p> | <p>需要 Windows 8。</p> | 
| <p><strong>伺服器</strong></p> | <p>需要 Windows Server 2012。</p> | 
| <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 
| <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | 
| <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetGetSystemParameter](./jetgetsystemparameter-function.md)  
[JetInit](./jetinit-function.md)  
[系統參數](./extensible-storage-engine-system-parameters.md)
