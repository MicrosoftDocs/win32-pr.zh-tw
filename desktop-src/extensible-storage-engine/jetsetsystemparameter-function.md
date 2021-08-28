---
description: 深入瞭解： JetSetSystemParameter 函數
title: JetSetSystemParameter 函式
TOCTitle: JetSetSystemParameter Function
ms:assetid: a244b5c9-6f6e-49d1-a6f7-9248feb9b92d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294044(v=EXCHG.10)
ms:contentKeyID: 32765643
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetSystemParameterA
- JetSetSystemParameterW
- JetSetSystemParameter
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4da3dc4c0d211039378b5cc1301a84e35f67ab24
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475794"
---
# <a name="jetsetsystemparameter-function"></a>JetSetSystemParameter 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetsetsystemparameter-function"></a>JetSetSystemParameter 函式

**JetSetSystemParameter** 函式是用來設定資料庫引擎的許多設定。

```cpp
    JET_ERR JET_API JetSetSystemParameter(
      __in_out_opt  JET_INSTANCE* pinstance,
      __in          JET_SESID sesid,
      __in          unsigned long paramid,
      __in          JET_API_PTR lParam,
      __in_opt      JET_PCSTR szParam
    );
```

### <a name="parameters"></a>參數

*pinstance*

指定要用於此呼叫的實例。

**Windows 2000：** 針對 Windows 2000，此參數會被忽略，且應該一律為 **Null**。

**Windows XP：** 在 Windows XP 和更新版本中，這個參數有點多載。 如果引擎在舊版模式下運作 (Windows 2000 相容性模式) 只支援一個實例，此參數可能是 **Null** ，或可能包含 [JetInit](./jetinit-function.md)所傳回的實際實例。 無論是哪一種情況，所有系統參數設定都是從一個實例讀取的。 如果引擎以多重實例模式運作，則此參數可以是 **Null** 或使用 [JetInit](./jetinit-function.md) 或 [JetCreateIndex](./jetcreateindex-function.md)所建立之實例的指標。 當此參數為 **Null** 時，會讀取全域系統參數設定 (或預設) 。 如果這個參數是實例，則會讀取該實例的系統參數設定。

雖然這在技術上是 out 參數，但此 API 永遠不會修改所提供緩衝區的內容。

*sesid*

指定此呼叫所要使用的會話。

指定時，會忽略指定的實例，並使用與會話相關聯的實例。

*paramid*

將設定之系統參數的識別碼。 請參閱 [系統參數](./extensible-storage-engine-system-parameters.md) ，以取得系統參數及其屬性的完整清單。

*lParam*

如果系統參數是整數類型，則提供要為選取的系統參數設定的值。

*szParam*

如果系統參數是字串類型，則提供所選取系統參數的值。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p><p><strong>Windows Vista：</strong> 在 Windows Vista 和更新版本上，您可以在不變更系統參數值的情況下傳回成功。 如需詳細資訊，請參閱 <a href="gg269346(v=exchg.10).md">中繼參數</a> 主題中的 JET_paramEnableAdvanced 系統參數。</p> | 
| <p>JET_errAlreadyInitialized</p> | <p>此實例已使用 <a href="gg294068(v=exchg.10).md">JetInit</a> 呼叫初始化，因此無法執行此作業。 當您嘗試在值的變更之後設定系統參數，而不影響資料庫引擎的狀態時，就會發生這種情況 <strong>JetSetSystemParameter</strong> 。</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</p> | 
| <p>JET_errIndexTuplesInvalidLimits</p> | <p>指定的元組索引參數不合法。 只有將<a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMin</a>、 <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>或<a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesToIndexMax</a>設定為不合法的值時， <strong>JetSetSystemParameter</strong>才會傳回此錯誤。</p><p><strong>Windows XP 和 Windows Server 2003：</strong> 這只能在 Windows XP 和 Windows Server 2003 上發生。</p> | 
| <p>JET_errInitInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在初始化。</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</p><p><strong>Windows XP：</strong> 只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errInvalidParameter</p> | <p>提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。 在下列情況下， <strong>JetSetSystemParameter</strong> 可能會發生：</p><ul><li><p>指定的系統參數識別碼無效或不受支援。</p></li><li><p>已嘗試使用長度超出參數合法範圍的字串來設定字串值系統參數。</p></li><li><p>嘗試以檔案路徑設定字串值系統參數，其絕對路徑表示的長度超出該參數的合法範圍。</p><p><strong>Windows Vista：</strong> 這只會發生在 Windows Vista 和更新版本上。</p></li><li><p>嘗試以參數的合法範圍以外的整數來設定整數值系統參數。</p></li><li><p>嘗試使用 <strong>Null</strong><a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> 指標、不正確 LCID 或一組不支援的 LCMapString 旗標來設定 JET_paramUnicodeIndexDefault。</p><p><strong>Windows Vista：</strong> 這只會發生在 Windows Vista 和更新版本上。</p></li><li><p>無法設定指定的系統參數，因為它是唯讀的。</p></li><li><p>嘗試在呼叫 <a href="gg294068(v=exchg.10).md">JetInit</a> 之後設定系統參數、資料庫引擎處於單一實例模式，且未指定會話。</p><p><strong>Windows XP 和 Windows Server 2003：</strong> 這只能在 Windows XP 和 Windows Server 2003 上發生。</p></li><li><p>指定的系統參數是全域的，且已嘗試為該系統參數設定實例的特定值。</p><p><strong>Windows XP 和 Windows Server 2003：</strong> 這只能在 Windows XP 和 Windows Server 2003 上發生。</p></li><li><p>指定的系統參數僅供每個實例使用，並嘗試設定該系統參數的全域值。</p><p><strong>Windows XP 和 Windows Server 2003：</strong> 這只能在 Windows XP 和 Windows Server 2003 上發生。</p></li></ul> | 
| <p>JET_errInvalidPath</p> | <p>指定的檔案系統路徑無效。 只有在設定代表檔案系統路徑的系統參數時， <strong>JetSetSystemParameter</strong> 才會傳回此錯誤。 例如， <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> 可能會傳回此錯誤。</p> | 
| <p>JET_errNotInitialized</p> | <p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p> | 
| <p>JET_errRestoreInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p> | 
| <p>JET_errTermInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在關閉。</p> | 
| <p>JET_errInvalidSesid</p> | <p>會話控制碼無效或參考已關閉的會話。</p><p>在所有情況下，都不會傳回此錯誤。 控制碼只會根據最大努力進行驗證。</p> | 
| <p>JET_errInvalidInstance</p> | <p>實例控制碼無效，或參考已經關閉的實例。</p><p>在所有情況下，都不會傳回此錯誤。 控制碼只會根據最大努力進行驗證。</p><p><strong>Windows Vista：</strong> 只有 Windows Vista 和更新版本才會傳回此錯誤。</p> | 



成功時，系統參數的設定將會設定為提供的值。

失敗時，系統參數的設定將維持不變。

#### <a name="remarks"></a>備註

**JetSetSystemParameter** 在驗證每個系統參數所選擇的設定時，會執行不佳的作業。 請務必小心，不要依賴此驗證來強制執行良好的設定。 請密切注意每個系統參數的描述，並遵循這些指導方針以取得良好的系統參數設定。

您應該一律設定一組系統參數，以保證資料庫引擎能如預期運作。 具體而言，您應該一律設定任何會影響 database engine 所使用之檔案實體配置的系統參數。 如需詳細資訊，請參閱 [系統參數](./extensible-storage-engine-system-parameters.md)。

每個系統參數都有預設值。 這些預設值會隨著時間而進化，而且非常任意。 強烈建議應用程式評估所有預設值，以確保它們是適當的。 如果不適用，則應該由應用程式設定。 這點很重要，因為許多參數可能會大幅影響資料庫引擎的可靠性、效能和資源使用率。

#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | | <p><strong>Unicode</strong></p> | <p>實作為 <strong>JetSetSystemParameterW</strong> (Unicode) 和 <strong>JetSetSystemParameterA</strong> (ANSI) 。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetGetSystemParameter](./jetgetsystemparameter-function.md)  
[JetInit](./jetinit-function.md)  
[系統參數](./extensible-storage-engine-system-parameters.md)
