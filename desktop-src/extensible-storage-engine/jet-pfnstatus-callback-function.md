---
description: 深入瞭解： JET_PFNSTATUS 回呼函數
title: JET_PFNSTATUS 回呼函數
TOCTitle: JET_PFNSTATUS Callback Function
ms:assetid: 8b0cf5bf-a4ee-4d8f-8dd7-556c35cd269d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269326(v=EXCHG.10)
ms:contentKeyID: 32765616
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d10de8491379a3e19217bcdb4a28f3546ebc009f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482914"
---
# <a name="jet_pfnstatus-callback-function"></a>JET_PFNSTATUS 回呼函數


_**適用于：** Windows |Windows伺服器_

## <a name="jet_pfnstatus-callback-function"></a>JET_PFNSTATUS 回呼函數

**JET_PFNSTATUS** 回呼函式會接收長時間執行之作業進度的相關資訊，例如磁碟重組、備份或還原作業。 在這類作業期間，資料庫引擎會呼叫此回呼函數，以提供作業進度的更新。

```cpp
    JET_ERR JET_API JET_PFNSTATUS(
                           JET_SESID  sesid,
                           JET_SNP snp,
                           JET_SNT snt,
                           void* pv
    );
```

### <a name="parameters"></a>參數

*sesid*

呼叫長時間執行之函式 [JET_SESID](./jet-sesid.md) 類型的會話。

*Snp*

[JET_SNP](./jet-snp.md)中指定的作業類型。 作業類型包括修復、壓縮、還原、備份、更新、清除和更新記錄格式。

*snt*

作業的狀態。 狀態類型包括開始、進行中、完成或失敗。 狀態會以 [JET_SNT](./jet-snt.md)類型的第三個參數來指定。

*光伏*

[JET_SNPROG](./jet-snprog-structure.md)類型之結構的選擇性指標。

### <a name="return-value"></a>傳回值

此函式會傳回具有其中一個可延伸[儲存體引擎錯誤碼](./extensible-storage-engine-error-codes.md)的[JET_ERR](./jet-err.md)資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。

成功時，發出回呼的作業可以正常執行。 在某些情況下，回呼可能會傳回會影響該作業的警告。

失敗時，發出回呼的作業可能會正常進行，或可能會失敗。

### <a name="remarks"></a>備註

這個回呼函式將用於進度通知，其中結構會指出進度的目前狀態。 請注意，您可能會針對作業的進度多次呼叫回呼函數。

### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 



### <a name="see-also"></a>另請參閱

[可擴充的儲存體引擎錯誤碼](./extensible-storage-engine-error-codes.md)  
[可擴充的儲存體引擎錯誤](./extensible-storage-engine-errors.md)  
[JET_SESID](./jet-sesid.md)  
[JET_SNP](./jet-snp.md)  
[JET_SNPROG](./jet-snprog-structure.md)  
[JET_SNT](./jet-snt.md)
