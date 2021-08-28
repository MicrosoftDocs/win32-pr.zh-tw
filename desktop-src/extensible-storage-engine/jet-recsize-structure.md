---
description: 深入瞭解： JET_RECSIZE 結構
title: JET_RECSIZE 結構
TOCTitle: JET_RECSIZE Structure
ms:assetid: bb2a63bb-7956-46c2-9791-0d0678a6c366
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294072(v=EXCHG.10)
ms:contentKeyID: 32765687
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a7ea4520a75e83c77a6403a583e9131a15df337b
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988224"
---
# <a name="jet_recsize-structure"></a>JET_RECSIZE 結構


_**適用于：** Windows |Windows伺服器_

## <a name="jet_recsize-structure"></a>JET_RECSIZE 結構

[JetGetRecordSize](./jetgetrecordsize-function.md)會使用 **JET_RECSIZE** 結構來傳回有關使用者資料空間、集合資料行數目、值數目，以及 ESE 記錄結構額外空間之記錄使用需求的資訊。

**Windows Vista：** Windows Vista 引進了 **JET_RECSIZE** 結構。

```cpp
    typedef struct {
      unsigned __int64 cbData;
      unsigned __int64 cbLongValueData;
      unsigned __int64 cbOverhead;
      unsigned __int64 cbLongValueOverhead;
      unsigned __int64 cNonTaggedColumns;
      unsigned __int64 cTaggedColumns;
      unsigned __int64 cLongValues;
      unsigned __int64 cMultiValues;
    } JET_RECSIZE;
```

### <a name="members"></a>成員

**cbData**

記錄中的使用者資料集。

**注意**  金鑰大小並未包含在此中。

**cbLongValueData**

與記錄相關聯但儲存在長值樹狀結構中的使用者資料。

**注意**  這不會計算內建的 long 值。

**cbOverhead**

此記錄的 ESE 記錄結構的額外負荷。 這包括記錄的金鑰大小。

**cbLongValueOverhead**

長數值資料的額外負荷。

**注意**  這不會計算內建的 long 值。

**cNonTaggedColumns**

此記錄中設定的固定和變數資料行總數。

**cTaggedColumns**

此記錄中設定的標記資料行總數。

**cLongValues**

此記錄的長值樹狀結構中儲存的完整值總數。

**注意**  這不會計算內建的 long 值。

**cMultiValues**

記錄中所有資料行之第一個資料行的總值總數。

### <a name="remarks"></a>備註

記錄中的值總數會是 **cMultiValues**  +  **cNonTaggedColumns**  +  **cTaggedColumns**。

### <a name="requirements"></a>規格需求


| 需求 | 值 |
|------------|----------|
| <p><strong>用戶端</strong></p> | <p>需要 Windows Vista。</p> | 
| <p><strong>伺服器</strong></p> | <p>需要 Windows Server 2008。</p> | 
| <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 



### <a name="see-also"></a>另請參閱

[JetGetRecordSize](./jetgetrecordsize-function.md)
