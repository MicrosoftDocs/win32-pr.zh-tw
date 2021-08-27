---
description: 深入瞭解： JET_PFNREALLOC 回呼函數
title: JET_PFNREALLOC 回呼函數
TOCTitle: JET_PFNREALLOC Callback Function
ms:assetid: 443d0b7e-1c3b-4584-9bc3-938724527313
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269237(v=EXCHG.10)
ms:contentKeyID: 32765539
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
ms.openlocfilehash: f7427a28752384f6c30e050458e5844dcaedd1a7
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122989141"
---
# <a name="jet_pfnrealloc-callback-function"></a>JET_PFNREALLOC 回呼函數


_**適用于：** Windows |Windows伺服器_

## <a name="jet_pfnrealloc-callback-function"></a>JET_PFNREALLOC 回呼函數

JET_PFNREALLOC 函式是[JetEnumerateColumns](./jetenumeratecolumns-function.md)用來為其輸出緩衝區配置記憶體的[realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019)相容回呼。

```cpp
    void * JET_API JET_PFNREALLOC(
      [in]                 void* pvContext,
      [in]                 void* pv,
      [in]                 unsigned long cb
    );
```

### <a name="parameters"></a>參數

*pvCoNtext*

提供給 [JetEnumerateColumns](./jetenumeratecolumns-function.md)的內容指標。 此內容指標可用來將 [JetEnumerateColumns](./jetenumeratecolumns-function.md) 呼叫端的狀態，傳遞給這個回呼的實作為。

*光伏*

如果非 Null，則指定此回呼先前配置之記憶體區塊的指標。 如果是 Null，則會配置所要求大小的新記憶體區塊。

*Cb*

記憶體區塊的新大小（以位元組為單位）。 如果這個參數是 0 (零) 而且指定了記憶體區塊，就會釋放該記憶體區塊。

### <a name="return-value"></a>傳回值

因為呼叫此函式，所以系統可能會產生成功或失敗的代碼。 如需如何將這些程式碼傳回為 Hresult 的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)。


| <p>傳回碼</p> | <p>描述</p> | 
|--------------------|--------------------|
| <p>Success</p> | <p>如果指定了先前配置的記憶體區塊，且指定了新的大小為零，則會釋放該區塊，並傳回 Null。 如果指定了先前配置的記憶體區塊，但指定了非零的新大小，則會傳回重新配置的記憶體區塊。 如果未指定記憶體區塊，則會傳回指定大小的新配置記憶體區塊。</p> | 
| <p>失敗</p> | <p>將會傳回 Null。 如果提供了先前配置的記憶體區塊，該區塊將維持配置狀態。</p> | 



### <a name="requirements"></a>規格需求


| 需求 | 值 |
|------------|----------|
| <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | 
| <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | 
| <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 



### <a name="see-also"></a>另請參閱

[JetEnumerateColumns](./jetenumeratecolumns-function.md)
