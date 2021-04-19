---
description: '深入瞭解： RetrieveColumn 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID、RetrieveColumnGrbit、JET_RETINFO) '
title: 'RetrieveColumn 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID、RetrieveColumnGrbit、JET_RETINFO) '
TOCTitle: RetrieveColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit,Microsoft.Isam.Esent.Interop.JET_RETINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumn(v=EXCHG.10)
ms:contentKeyID: 55100853
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 43657ec60e521795ba4d474306de9380618cd21f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991668"
---
# <a name="apiretrievecolumn-method-jet_sesid-jet_tableid-jet_columnid-retrievecolumngrbit-jet_retinfo"></a><span data-ttu-id="25485-103">RetrieveColumn 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID、RetrieveColumnGrbit、JET_RETINFO) </span><span class="sxs-lookup"><span data-stu-id="25485-103">Api.RetrieveColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)</span></span>

<span data-ttu-id="25485-104">從目前的記錄抓取單一資料行值。</span><span class="sxs-lookup"><span data-stu-id="25485-104">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="25485-105">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="25485-105">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="25485-106">或者，此函式可以從資料指標複製緩衝區中所建立的記錄取得資料行。</span><span class="sxs-lookup"><span data-stu-id="25485-106">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="25485-107">此函數也可以從參考目前記錄的索引項目抓取資料行資料。</span><span class="sxs-lookup"><span data-stu-id="25485-107">This function can also retrieve column data from an index entry that references the current record.</span></span> <span data-ttu-id="25485-108">除了取得實際的資料行值之外，JetRetrieveColumn 還可以用來取得資料行的大小，然後再抓取資料行資料本身，讓應用程式緩衝區可以適當地調整大小。</span><span class="sxs-lookup"><span data-stu-id="25485-108">In addition to retrieving the actual column value, JetRetrieveColumn can also be used to retrieve the size of a column, before retrieving the column data itself so that application buffers can be sized appropriately.</span></span>

<span data-ttu-id="25485-109">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="25485-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="25485-110">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="25485-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="25485-111">語法</span><span class="sxs-lookup"><span data-stu-id="25485-111">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    grbit As RetrieveColumnGrbit, _
    retinfo As JET_RETINFO _
) As Byte()
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim grbit As RetrieveColumnGrbit
Dim retinfo As JET_RETINFO
Dim returnValue As Byte()

returnValue = Api.RetrieveColumn(sesid, _
    tableid, columnid, grbit, retinfo)
```

``` csharp
public static byte[] RetrieveColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    RetrieveColumnGrbit grbit,
    JET_RETINFO retinfo
)
```

#### <a name="parameters"></a><span data-ttu-id="25485-112">參數</span><span class="sxs-lookup"><span data-stu-id="25485-112">Parameters</span></span>

  - <span data-ttu-id="25485-113">sesid</span><span class="sxs-lookup"><span data-stu-id="25485-113">sesid</span></span>  
    <span data-ttu-id="25485-114">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="25485-114">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="25485-115">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="25485-115">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="25485-116">tableid</span><span class="sxs-lookup"><span data-stu-id="25485-116">tableid</span></span>  
    <span data-ttu-id="25485-117">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="25485-117">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="25485-118">從中取出資料行的資料指標。</span><span class="sxs-lookup"><span data-stu-id="25485-118">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="25485-119">columnid</span><span class="sxs-lookup"><span data-stu-id="25485-119">columnid</span></span>  
    <span data-ttu-id="25485-120">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="25485-120">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="25485-121">要取出的 columnid。</span><span class="sxs-lookup"><span data-stu-id="25485-121">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="25485-122">grbit</span><span class="sxs-lookup"><span data-stu-id="25485-122">grbit</span></span>  
    <span data-ttu-id="25485-123">型別： [RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="25485-123">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="25485-124">取出資料行選項。</span><span class="sxs-lookup"><span data-stu-id="25485-124">Retrieve column options.</span></span>

<!-- end list -->

  - <span data-ttu-id="25485-125">retinfo</span><span class="sxs-lookup"><span data-stu-id="25485-125">retinfo</span></span>  
    <span data-ttu-id="25485-126">類型： [Microsoft.Isam.Esent.Interop.JET_RETINFO](./jet-retinfo-class.md)</span><span class="sxs-lookup"><span data-stu-id="25485-126">Type: [Microsoft.Isam.Esent.Interop.JET_RETINFO](./jet-retinfo-class.md)</span></span>  
    
    <span data-ttu-id="25485-127">如果 pretinfo 為 Null，則函式的行為就如同 itagSequence 為1，而 ibLongValue 為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="25485-127">If pretinfo is give as NULL then the function behaves as though an itagSequence of 1 and an ibLongValue of 0 (zero) were given.</span></span> <span data-ttu-id="25485-128">這會導致資料行抓取抓取多重值資料行的第一個值，並在位移 0 (零) 取出長資料。</span><span class="sxs-lookup"><span data-stu-id="25485-128">This causes column retrieval to retrieve the first value of a multi-valued column, and to retrieve long data at offset 0 (zero).</span></span>

#### <a name="return-value"></a><span data-ttu-id="25485-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="25485-129">Return value</span></span>

<span data-ttu-id="25485-130">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="25485-130">Type: \[\]</span></span>  
<span data-ttu-id="25485-131">從資料行中取出的資料。</span><span class="sxs-lookup"><span data-stu-id="25485-131">The data retrieved from the column.</span></span> <span data-ttu-id="25485-132">如果資料行是 null，則為 null。</span><span class="sxs-lookup"><span data-stu-id="25485-132">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="25485-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="25485-133">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="25485-134">參考</span><span class="sxs-lookup"><span data-stu-id="25485-134">Reference</span></span>

[<span data-ttu-id="25485-135">Api 類別</span><span class="sxs-lookup"><span data-stu-id="25485-135">Api class</span></span>](./api-class.md)

[<span data-ttu-id="25485-136">Api 成員</span><span class="sxs-lookup"><span data-stu-id="25485-136">Api members</span></span>](./api-members.md)

[<span data-ttu-id="25485-137">RetrieveColumn 多載</span><span class="sxs-lookup"><span data-stu-id="25485-137">RetrieveColumn overload</span></span>](./api.retrievecolumn-method.md)

[<span data-ttu-id="25485-138">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="25485-138">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
