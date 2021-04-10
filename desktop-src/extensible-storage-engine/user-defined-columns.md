---
description: 深入瞭解：使用者定義的資料行
title: 使用者定義資料行
TOCTitle: User Defined Columns
ms:assetid: cccfc97c-acde-4328-a87f-ee7dcc54203c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294091(v=EXCHG.10)
ms:contentKeyID: 32765706
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 624a916ee2048d9069c7695c79824e3357b511f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026473"
---
# <a name="user-defined-columns"></a><span data-ttu-id="ff636-103">使用者定義資料行</span><span class="sxs-lookup"><span data-stu-id="ff636-103">User Defined Columns</span></span>


<span data-ttu-id="ff636-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ff636-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="user-defined-columns"></a><span data-ttu-id="ff636-105">使用者定義資料行</span><span class="sxs-lookup"><span data-stu-id="ff636-105">User Defined Columns</span></span>

<span data-ttu-id="ff636-106">使用者定義的資料行是由回呼函數提供其預設值的資料行。</span><span class="sxs-lookup"><span data-stu-id="ff636-106">User defined columns are columns whose default values are provided by a callback function.</span></span> <span data-ttu-id="ff636-107">這些資料行一律會加上標記，並設定為回呼函數所計算的值。</span><span class="sxs-lookup"><span data-stu-id="ff636-107">These columns are always tagged and set to the value computed by the callback function.</span></span> <span data-ttu-id="ff636-108">針對資料表中的每個資料列，這個值必須是穩定的。</span><span class="sxs-lookup"><span data-stu-id="ff636-108">This value must be stable for each row in the table.</span></span> <span data-ttu-id="ff636-109">只有當應用程式或資料庫引擎本身需要讀取指定資料列的資料行值時，才會使用回呼函數。</span><span class="sxs-lookup"><span data-stu-id="ff636-109">The callback function is only used when either the application or the database engine itself needs to read the value of the column for a given row.</span></span> <span data-ttu-id="ff636-110">應用程式可以選擇覆寫預設值，並設定資料行中的特定值。</span><span class="sxs-lookup"><span data-stu-id="ff636-110">The application has the option to override the default value and set a specific value in the column.</span></span> <span data-ttu-id="ff636-111">當資料行中的預設值遭到覆寫時，就會使用資料列中的空間，否則使用者定義的預設資料行會不會使用記錄中的空間。</span><span class="sxs-lookup"><span data-stu-id="ff636-111">When the default value is overridden in the columns, it uses space in the row, otherwise user defined default columns do not use space in the record.</span></span>

<span data-ttu-id="ff636-112">使用者定義的預設值選項是在呼叫 [JetAddColumn](./jetaddcolumn-function.md)的 [JET_COLUMNDEF](./jet-columndef-structure.md)結構的 **grbit** 成員中設定。</span><span class="sxs-lookup"><span data-stu-id="ff636-112">User defined defaults option is set in the **grbit** member of the [JET_COLUMNDEF](./jet-columndef-structure.md) structure in the call to [JetAddColumn](./jetaddcolumn-function.md).</span></span> <span data-ttu-id="ff636-113">[JetAddColumn](./jetaddcolumn-function.md)函數的 *pvDefault* 參數會指向 [JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md)結構，其中包含 **szCallback** 成員中的回呼函式名稱，以及在 **pbUserData** 成員中傳遞給回呼的資料。</span><span class="sxs-lookup"><span data-stu-id="ff636-113">The *pvDefault* parameter of the [JetAddColumn](./jetaddcolumn-function.md) function points to a [JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md) structure, that contains the name of the callback function in the **szCallback** member, and the data that is passed to the callback in the **pbUserData** member.</span></span>
