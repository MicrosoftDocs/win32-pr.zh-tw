---
description: 深入瞭解：使用者定義的資料行
title: 使用者定義資料行
TOCTitle: User Defined Columns
ms:assetid: cccfc97c-acde-4328-a87f-ee7dcc54203c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294091(v=EXCHG.10)
ms:contentKeyID: 32765706
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 57212f49fe97f276677a2ca4396a23d672e175a86eb067f1d276b9c20a46b891
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117890069"
---
# <a name="user-defined-columns"></a>使用者定義資料行


_**適用于：** Windows |Windows伺服器_

## <a name="user-defined-columns"></a>使用者定義資料行

使用者定義的資料行是由回呼函數提供其預設值的資料行。 這些資料行一律會加上標記，並設定為回呼函數所計算的值。 針對資料表中的每個資料列，這個值必須是穩定的。 只有當應用程式或資料庫引擎本身需要讀取指定資料列的資料行值時，才會使用回呼函數。 應用程式可以選擇覆寫預設值，並設定資料行中的特定值。 當資料行中的預設值遭到覆寫時，就會使用資料列中的空間，否則使用者定義的預設資料行會不會使用記錄中的空間。

使用者定義的預設值選項是在呼叫 [JetAddColumn](./jetaddcolumn-function.md)的 [JET_COLUMNDEF](./jet-columndef-structure.md)結構的 **grbit** 成員中設定。 [JetAddColumn](./jetaddcolumn-function.md)函數的 *pvDefault* 參數會指向 [JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md)結構，其中包含 **szCallback** 成員中的回呼函式名稱，以及在 **pbUserData** 成員中傳遞給回呼的資料。
