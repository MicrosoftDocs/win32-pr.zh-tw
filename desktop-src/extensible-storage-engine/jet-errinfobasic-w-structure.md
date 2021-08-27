---
description: 深入瞭解： JET_ERRINFOBASIC_W 結構
title: JET_ERRINFOBASIC_W 結構
TOCTitle: JET_ERRINFOBASIC_W Structure
ms:assetid: fcc55cb7-718d-419a-a473-15e030c23abd
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475861(v=EXCHG.10)
ms:contentKeyID: 37033567
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: c02d9f8081040293bd154137163e13cc9d313a32
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984031"
---
# <a name="jet_errinfobasic_w-structure"></a>JET_ERRINFOBASIC_W 結構


_**適用于：** Windows |Windows伺服器_

## <a name="jet_errinfobasic_w-structure"></a>JET_ERRINFOBASIC_W 結構

**JET_ERRINFOBASIC_W** 結構會定義傳入 JET_ErrorInfoSpecificErr InfoLevel 時，從 [JetGetErrorInfo ()](./jetgeterrorinfow-function.md)方法傳回的資料。

注意：本檔是以可延伸儲存體引擎的初步發行版本為基礎。 此資訊可能隨時變更。

```cpp
typedef struct { 
    unsigned long cbStruct; 
    JET_ERR errValue; 
    JET_ERRCAT errcatMostSpecific; 
    unsigned char rgCategoricalHierarchy[8]; 
    unsigned long lSourceLine; 
    WCHAR rgszSourceFile[64]; 
} JET_ERRINFOBASIC_W;
```

### <a name="members"></a>成員

**cbStruct**

結構的大小（以位元組為單位）。 它必須設定為 sizeof ( JET_ERRINFOBASIC ) 。

**errValue**

針對 [JetGetErrorInfo ()](./jetgeterrorinfow-function.md)的 *pvResult* 引數所傳遞的錯誤值。

**errcatMostSpecific**

與錯誤相關聯的最低層級 [JET_ERRCAT](./jet-errcat.md) 常數;亦即，在 [JET_ERRCAT](./jet-errcat.md)中記載的類別目錄階層中的分葉層級類別。

**rgCategoricalHierarchy \[ 8\]**

與錯誤相關聯的錯誤類別目錄階層。 位置0是 [JET_ERRCAT](./jet-errcat.md)階層中的最高層級，其餘則是子類別，直到設定了最特定的類別為止，之後所有的類別都是 JET_errcatUnknown。

**lSourceLine**

保留的。

**rgszSourceFile \[ 64\]**

保留的。

### <a name="requirements"></a>規格需求


| 需求 | 值 |
|------------|----------|
| <p><strong>用戶端</strong></p> | <p>需要 Windows 8。</p> | 
| <p><strong>伺服器</strong></p> | <p>需要 Windows 8 Server。</p> | 
| <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 

