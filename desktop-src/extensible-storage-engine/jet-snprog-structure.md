---
description: 深入瞭解： JET_SNPROG 結構
title: JET_SNPROG 結構
TOCTitle: JET_SNPROG Structure
ms:assetid: 8b4224e4-ad4d-440f-8915-8eb43b0885f0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269328(v=EXCHG.10)
ms:contentKeyID: 32765618
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
ms.openlocfilehash: ab132d203ca2dc81e2ed3c3d8a0ce25c76a2cc71
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987731"
---
# <a name="jet_snprog-structure"></a>JET_SNPROG 結構


_**適用于：** Windows |Windows伺服器_

## <a name="jet_snprog-structure"></a>JET_SNPROG 結構

**JET_SNPROG** 結構包含長時間執行之作業進度的相關資訊。 當呼叫回呼函式來通知作業的狀態，而且作業仍在進行時，回呼函式的最後一個參數就是 **JET_SNPROG** 結構的指標。

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cunitDone;
      unsigned long cunitTotal;
    } JET_SNPROG;
```

### <a name="members"></a>成員

**cbStruct**

**JET_SNPROG** 結構的大小（以位元組為單位）。 此值會確認下欄欄位是否存在。

**cunitDone**

長時間執行的函式期間已完成的工作單位數目。

**cunitTotal**

需要完成的工作單位數目。 此值應該一律大於或等於 **cunitDone**。

### <a name="requirements"></a>規格需求


| 需求 | 值 |
|------------|----------|
| <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | 
| <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | 
| <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 


