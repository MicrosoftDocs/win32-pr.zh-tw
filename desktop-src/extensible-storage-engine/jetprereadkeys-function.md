---
description: 深入瞭解： JetPrereadKeys 函數
title: JetPrereadKeys 函式
TOCTitle: JetPrereadKeys Function
ms:assetid: fc2f46bc-1f81-4af2-aa63-9757e819efc2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294143(v=EXCHG.10)
ms:contentKeyID: 32765757
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetPrereadKeys
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 067fe72e2e00fc01b433dbda819d5e89336fc68c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467185"
---
# <a name="jetprereadkeys-function"></a>JetPrereadKeys 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetprereadkeys-function"></a>JetPrereadKeys 函式

**JetPrereadKeys** 函式會讀取索引鍵值，以改善版本存放區清除的效能。

**Windows 7： PrereadKeys** 函數是在 Windows 7 中引進。

```cpp
    JET_ERR JET_API JetPrereadKeys(
      __in JET_SESID sesid,
      __in JET_TABLEID tableid,
      __in_ecount(ckeys) const void ** rgpvKeys,
      __in_ecount(ckeys) const unsigned long * rgcbKeys,
      __in long ckeys,
      __out_opt long * pckeysPreread,
      __in JET_GRBIT grbit
     );
```

### <a name="parameters"></a>參數

*sesid*

要用於 API 呼叫的資料庫會話內容。

*tableid*

要用於此呼叫的資料指標。

*rgpvKeys*

索引鍵指標的陣列。 您可以使用 [JetMakeKey](./jetmakekey-function.md) 或使用 [JetGetBookmark](./jetgetbookmark-function.md)來取得金鑰。 索引鍵必須依照傳遞的 grbit，以遞增或遞減順序排序。 您可以使用 memcmp 來排序索引鍵。

*rgcbKeys*

金鑰長度的陣列。 rgpvKeys \[ n \] 應指向長度為 rgcbKeys n 的索引鍵 \[\]

*ckeys*

索引鍵數目。 rgpvKeys 和 rgcbKeys 都必須指向至少具有 ckeys 元素的陣列。

*pckeysPreread*

傳回 prereads 實際發出的索引鍵數目。 此參數可以是 Null。

*grbit*

這必須是 JET_bitPrereadForward 或 JET_bitPrereadBackward。 如果 JET_bitPrereadForward grbit，索引鍵必須以遞增順序排序。 如果 JET_bitPrereadBackward grbit，索引鍵必須以遞減順序排序。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。

可能會傳回各種 i/o 錯誤以及這些 API 使用錯誤：


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errInvalidGrbit</p> | <p>Grbit 不是 JET_bitPrereadForward 也不 JET_bitPrereadBackward。</p> | 
| <p>JET_errInvalidBufferSize</p> | <p>傳入了不正確的金鑰大小。 索引鍵不可以是0，也不能超過資料表的最大索引鍵長度。</p> | 
| <p>JET_errInvalidParameter</p> | <p>傳入了不正確參數。 這可能是因為必要參數的 null 值，或可能表示金鑰陣列未正確排序。</p> | 



**JetPrereadKeys** 會遍歷 b 型樹狀目錄的內部頁面，以判斷哪些分葉頁面包含 RgpvKeys/rgcbKeys 所指定的索引鍵。 分葉頁面清單會排序，然後針對頁面的範圍發出 prereads。 可以 preread 的頁面數目有限，因此可能不會 preread 所有索引鍵。 在此情況下，會在 pckeysPreread 中傳回實際 preread 的索引鍵數目。

#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows 7。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows Server 2008 R2。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 

