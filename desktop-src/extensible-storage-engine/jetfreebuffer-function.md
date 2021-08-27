---
description: 深入瞭解： JetFreeBuffer 函數
title: JetFreeBuffer 函式
TOCTitle: JetFreeBuffer Function
ms:assetid: f37d35f6-4bea-46ba-a334-7b8ad7a1568c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294134(v=EXCHG.10)
ms:contentKeyID: 32765748
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetFreeBuffer
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c7d7b56c38bde931cfe0c1a2e95579a515cf3538
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476434"
---
# <a name="jetfreebuffer-function"></a>JetFreeBuffer 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetfreebuffer-function"></a>JetFreeBuffer 函式

**JetFreeBuffer** 函式會釋出由 database engine 呼叫所配置的記憶體。

**Windows xp： JetFreeBuffer** 是在 Windows xp 引進。

```cpp
    JET_ERR JET_API JetFreeBuffer(
      __in          char* pbBuf
    );
```

### <a name="parameters"></a>參數

*pbBuf*

先前由資料庫引擎的呼叫所配置的記憶體區域指標。 **Null** 是可接受的，將會被忽略。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 



#### <a name="remarks"></a>備註

未定義的行為會將資料庫引擎未配置的記憶體傳遞給 *pbBuf*。

#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista 或 Windows XP。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008 或 Windows server 2003。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JetGetInstanceInfo](./jetgetinstanceinfo-function.md)
