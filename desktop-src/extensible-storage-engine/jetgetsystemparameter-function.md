---
description: 深入瞭解： JetGetSystemParameter 函數
title: JetGetSystemParameter 函式
TOCTitle: JetGetSystemParameter Function
ms:assetid: 6e6ddb49-702c-4c45-ac9f-35ae817696dd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269291(v=EXCHG.10)
ms:contentKeyID: 32765583
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetSystemParameter
- JetGetSystemParameterA
- JetGetSystemParameterW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 608a9c464ca645668483934a28a3f79945cd443d
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984741"
---
# <a name="jetgetsystemparameter-function"></a>JetGetSystemParameter 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetgetsystemparameter-function"></a>JetGetSystemParameter 函式

**JetGetSystemParameter** 函式會讀取資料庫引擎的許多設定。

```cpp
    JET_ERR JET_API JetGetSystemParameter(
      __in          JET_INSTANCE instance,
      __in          JET_SESID sesid,
      __in          unsigned long paramid,
      __in_out_opt  JET_API_PTR* plParam,
      __out_opt     JET_PSTR szParam,
      __in          unsigned long cbMax
    );
```

### <a name="parameters"></a>參數

*實例*

此呼叫所要使用的實例。

針對 Windows 2000，此參數會被忽略，且應該一律為 **Null**。

在 Windows XP 和更新版本中，這個參數有點多載。 如果引擎在舊版模式下運作 (Windows 2000 相容性模式) 只支援一個實例，此參數可能是 **Null** ，或可能包含 [JetInit](./jetinit-function.md)所傳回的實際實例。 無論是哪一種情況，所有系統參數設定都是從一個實例讀取的。 如果引擎是在多重實例模式中作業，這個參數可以是 **Null** 或使用 [JetInit](./jetinit-function.md) 或 [JetCreateInstance](./jetcreateinstance-function.md)所建立之實例的指標。 當此參數為 **Null** 時，會讀取全域系統參數設定 (或預設) 。 如果這個參數是實例，則會讀取該實例的系統參數設定。

*sesid*

此呼叫所要使用的會話。

指定時，會忽略指定的實例，並使用與會話相關聯的實例。

*paramid*

將讀取之系統參數的識別碼。

請參閱 [系統參數](./extensible-storage-engine-system-parameters.md) ，以取得系統參數及其屬性的完整清單。

*plParam*

輸出緩衝區，如果該系統參數是整數類型，則會接收所選系統參數的值。

*szParam*

輸出緩衝區，如果系統參數是字串類型，則會接收所選系統參數的值。

*cbMax*

字串輸出緩衝區的大小上限（以位元組為單位）。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</p> | 
| <p>JET_errInitInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在初始化。</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。 只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errInvalidParameter</p> | <p>提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。</p><p>在下列情況下， <strong>JetGetSystemParameter</strong> 可能會發生：</p><ul><li><p>指定的系統參數識別碼無效或不受支援。</p></li><li><p>指定的系統參數需要提供整數輸出緩衝區，而且輸出緩衝區指標為 <strong>Null</strong>。</p></li><li><p>指定的系統參數需要提供字串輸出緩衝區，而且輸出緩衝區指標為 <strong>Null</strong>。</p><p><strong>Windows Vista：</strong>這只會發生在 Windows Vista 和更新版本上。</p></li><li><p>指定的系統參數需要提供字串輸出緩衝區，而且輸出緩衝區的大小太小，無法接受以 null 結尾的字串。</p><p><strong>Windows Vista：</strong>這只會發生在 Windows Vista 和更新版本上。</p></li><li><p>無法讀取指定的系統參數，因為它是唯讀的。</p></li><li><p>指定的系統參數是全域的，而且嘗試讀取該系統參數的實例特定值。 這只會發生在 Windows XP 和更新版本上。</p></li><li><p>指定的系統參數僅供每個實例使用，並嘗試讀取該系統參數的全域值。 這只會發生在 Windows XP 和更新版本上。</p></li></ul> | 
| <p>JET_errNotInitialized</p> | <p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p> | 
| <p>JET_errRestoreInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p> | 
| <p>JET_errTermInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在關閉。</p> | 
| <p>JET_errInvalidSesid</p> | <p>會話控制碼無效或參考已關閉的會話。 在所有情況下，都不會傳回此錯誤。 控制碼只會根據最大努力進行驗證。</p> | 
| <p>JET_errInvalidInstance</p> | <p>實例控制碼無效，或參考已經關閉的實例。 在所有情況下，都不會傳回此錯誤。 控制碼只會根據最大努力進行驗證。</p><p><strong>Windows Vista：</strong>只有 Windows Vista 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_wrnBufferTruncated</p> | <p>作業已順利完成，但輸出緩衝區太小，無法接收整個系統參數設定。</p><p>輸出緩衝區已填滿系統參數設定的大小。 如果輸出緩衝區的長度至少要有一個字元，則該輸出緩衝區中的字串會以 null 結束。</p><p><strong>注意  </strong>所有版本都不會傳回此錯誤。 如需詳細資訊，請參閱「備註」一節。</p> | 
| <p>JET_errBufferTooSmall</p> | <p>因為輸出緩衝區太小而無法接收整個系統參數設定，所以操作失敗。</p><p><strong>注意  </strong>在某些情況下不會傳回此錯誤，以保留應用程式相容性。 如需詳細資訊，請參閱「備註」一節。</p><p><strong>Windows Vista：</strong>只有 Windows Vista 和更新版本才會傳回此錯誤。</p> | 



成功時，適用于所要求系統參數的輸出緩衝區將會設定為該系統參數的值。

失敗時，輸出緩衝區的狀態將會是未定義的。

#### <a name="remarks"></a>備註

此 API 存在所有版本中的重要問題。 如果要求具有字串值的系統參數，而且輸出緩衝區太小而無法接收整個系統參數設定，則不會傳回 JET_wrnBufferTruncated。 改為傳回 JET_errSuccess。 如果傳回字串的長度等於輸出緩衝區的大小，但不是 **Null** 結束字元，則呼叫端應該會像是傳回 JET_wrnBufferTruncated 一樣回應。 如果指定了零大小的字串輸出緩衝區，呼叫端應該會像是傳回 JET_errInvalidParameter 一樣回應。

#### <a name="requirements"></a>規格需求


| 需求 | 值 |
|------------|----------|
| <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | 
| <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | 
| <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 
| <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | 
| <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 
| <p><strong>Unicode</strong></p> | <p>實作為 <strong>JetGetSystemParameterW</strong> (Unicode) 和 <strong>JetGetSystemParameterA</strong> (ANSI) 。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)  
[系統參數](./extensible-storage-engine-system-parameters.md)
