---
description: '深入瞭解：資料表隱含轉換 (資料表至 JET_TABLEID) '
title: '資料表隱含轉換 (資料表至 JET_TABLEID) '
TOCTitle: Implicit conversion (Table to JET_TABLEID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Table.op_Implicit(Microsoft.Isam.Esent.Interop.Table)~Microsoft.Isam.Esent.Interop.JET_TABLEID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.table.op_implicit(v=EXCHG.10)
ms:contentKeyID: 55104156
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Table.Implicit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Table.Implicit
- Microsoft.Isam.Esent.Interop.Table.op_Implicit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 886f5085ee09020730b36269255279836b31562a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997551"
---
# <a name="table-implicit-conversion-table-to-jet_tableid"></a><span data-ttu-id="89c3b-103">資料表隱含轉換 (資料表至 JET_TABLEID) </span><span class="sxs-lookup"><span data-stu-id="89c3b-103">Table Implicit conversion (Table to JET_TABLEID)</span></span>

<span data-ttu-id="89c3b-104">從資料表到 JET_TABLEID 的隱含轉換運算子。</span><span class="sxs-lookup"><span data-stu-id="89c3b-104">Implicit conversion operator from a Table to a JET_TABLEID.</span></span> <span data-ttu-id="89c3b-105">這可讓資料表與預期 JET_TABLEID 的 Api 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="89c3b-105">This allows a Table to be used with APIs which expect a JET_TABLEID.</span></span>

<span data-ttu-id="89c3b-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="89c3b-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="89c3b-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="89c3b-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="89c3b-108">語法</span><span class="sxs-lookup"><span data-stu-id="89c3b-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Widening Operator CType ( _
    table As Table _
) As JET_TABLEID
'Usage
Dim input As Table
Dim output As JET_TABLEID

output = CType(input, JET_TABLEID)
```

``` csharp
public static implicit operator JET_TABLEID (
    Table table
)
```

#### <a name="parameters"></a><span data-ttu-id="89c3b-109">參數</span><span class="sxs-lookup"><span data-stu-id="89c3b-109">Parameters</span></span>

  - <span data-ttu-id="89c3b-110">資料表</span><span class="sxs-lookup"><span data-stu-id="89c3b-110">table</span></span>  
    <span data-ttu-id="89c3b-111">類型： [Microsoft. Isam](./table-class.md) 。</span><span class="sxs-lookup"><span data-stu-id="89c3b-111">Type: [Microsoft.Isam.Esent.Interop.Table](./table-class.md)</span></span>  
    
    <span data-ttu-id="89c3b-112">要轉換的資料表。</span><span class="sxs-lookup"><span data-stu-id="89c3b-112">The table to convert.</span></span>

#### <a name="return-value"></a><span data-ttu-id="89c3b-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="89c3b-113">Return value</span></span>

<span data-ttu-id="89c3b-114">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="89c3b-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
<span data-ttu-id="89c3b-115">資料表的 JET_TABLEID。</span><span class="sxs-lookup"><span data-stu-id="89c3b-115">The JET_TABLEID of the table.</span></span>  

## <a name="see-also"></a><span data-ttu-id="89c3b-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="89c3b-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="89c3b-117">參考</span><span class="sxs-lookup"><span data-stu-id="89c3b-117">Reference</span></span>

[<span data-ttu-id="89c3b-118">Table 類別</span><span class="sxs-lookup"><span data-stu-id="89c3b-118">Table class</span></span>](./table-class.md)

[<span data-ttu-id="89c3b-119">資料表成員</span><span class="sxs-lookup"><span data-stu-id="89c3b-119">Table members</span></span>](./table-members.md)

[<span data-ttu-id="89c3b-120">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="89c3b-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
