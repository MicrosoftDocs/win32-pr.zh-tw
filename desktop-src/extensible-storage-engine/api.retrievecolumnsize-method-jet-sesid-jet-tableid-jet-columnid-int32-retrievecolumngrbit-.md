---
description: '深入瞭解： RetrieveColumnSize 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID、Int32、RetrieveColumnGrbit) '
title: 'RetrieveColumnSize 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID、Int32、RetrieveColumnGrbit) '
TOCTitle: RetrieveColumnSize method (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnSize(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Int32,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnsize(v=EXCHG.10)
ms:contentKeyID: 55100912
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnSize
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: afd09ecca0362487d6c8e78f8e7c8d943f2f3269
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936571"
---
# <a name="apiretrievecolumnsize-method-jet_sesid-jet_tableid-jet_columnid-int32-retrievecolumngrbit"></a><span data-ttu-id="823c6-103">RetrieveColumnSize 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID、Int32、RetrieveColumnGrbit) </span><span class="sxs-lookup"><span data-stu-id="823c6-103">Api.RetrieveColumnSize method (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32, RetrieveColumnGrbit)</span></span>

<span data-ttu-id="823c6-104">從目前的記錄抓取單一資料行值的大小。</span><span class="sxs-lookup"><span data-stu-id="823c6-104">Retrieves the size of a single column value from the current record.</span></span> <span data-ttu-id="823c6-105">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="823c6-105">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="823c6-106">或者，此函式可以從資料指標複製緩衝區中所建立的記錄取得資料行。</span><span class="sxs-lookup"><span data-stu-id="823c6-106">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="823c6-107">此函數也可以從參考目前記錄的索引項目抓取資料行資料。</span><span class="sxs-lookup"><span data-stu-id="823c6-107">This function can also retrieve column data from an index entry that references the current record.</span></span>

<span data-ttu-id="823c6-108">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="823c6-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="823c6-109">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="823c6-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="823c6-110">語法</span><span class="sxs-lookup"><span data-stu-id="823c6-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnSize ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    itagSequence As Integer, _
    grbit As RetrieveColumnGrbit _
) As Nullable(Of Integer)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim itagSequence As Integer
Dim grbit As RetrieveColumnGrbit
Dim returnValue As Nullable(Of Integer)

returnValue = Api.RetrieveColumnSize(sesid, _
    tableid, columnid, itagSequence, _
    grbit)
```

``` csharp
public static Nullable<int> RetrieveColumnSize(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    int itagSequence,
    RetrieveColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="823c6-111">參數</span><span class="sxs-lookup"><span data-stu-id="823c6-111">Parameters</span></span>

  - <span data-ttu-id="823c6-112">sesid</span><span class="sxs-lookup"><span data-stu-id="823c6-112">sesid</span></span>  
    <span data-ttu-id="823c6-113">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="823c6-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="823c6-114">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="823c6-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="823c6-115">tableid</span><span class="sxs-lookup"><span data-stu-id="823c6-115">tableid</span></span>  
    <span data-ttu-id="823c6-116">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="823c6-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="823c6-117">從中取出資料行的資料指標。</span><span class="sxs-lookup"><span data-stu-id="823c6-117">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="823c6-118">columnid</span><span class="sxs-lookup"><span data-stu-id="823c6-118">columnid</span></span>  
    <span data-ttu-id="823c6-119">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="823c6-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="823c6-120">要取出的 columnid。</span><span class="sxs-lookup"><span data-stu-id="823c6-120">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="823c6-121">itagSequence</span><span class="sxs-lookup"><span data-stu-id="823c6-121">itagSequence</span></span>  
    <span data-ttu-id="823c6-122">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="823c6-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="823c6-123">多重值資料行中值的序號。</span><span class="sxs-lookup"><span data-stu-id="823c6-123">The sequence number of value in a multi-valued column.</span></span> <span data-ttu-id="823c6-124">值的陣列是以一為基礎。</span><span class="sxs-lookup"><span data-stu-id="823c6-124">The array of values is one-based.</span></span> <span data-ttu-id="823c6-125">第一個值是 sequence 1，不是0。</span><span class="sxs-lookup"><span data-stu-id="823c6-125">The first value is sequence 1, not 0.</span></span> <span data-ttu-id="823c6-126">如果 [記錄] 資料行只有一個值，則應該以 itagSequence 的形式傳遞1。</span><span class="sxs-lookup"><span data-stu-id="823c6-126">If the record column has only one value then 1 should be passed as the itagSequence.</span></span>

<!-- end list -->

  - <span data-ttu-id="823c6-127">grbit</span><span class="sxs-lookup"><span data-stu-id="823c6-127">grbit</span></span>  
    <span data-ttu-id="823c6-128">型別： [RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="823c6-128">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="823c6-129">取出資料行選項。</span><span class="sxs-lookup"><span data-stu-id="823c6-129">Retrieve column options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="823c6-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="823c6-130">Return value</span></span>

<span data-ttu-id="823c6-131">類型： [可為 null](/dotnet/api/system.nullable-1)\<[Int32](/dotnet/api/system.int32)\></span><span class="sxs-lookup"><span data-stu-id="823c6-131">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[Int32](/dotnet/api/system.int32)\></span></span>  
<span data-ttu-id="823c6-132">資料行的大小。</span><span class="sxs-lookup"><span data-stu-id="823c6-132">The size of the column.</span></span> <span data-ttu-id="823c6-133">如果資料行是 null，則為0。</span><span class="sxs-lookup"><span data-stu-id="823c6-133">0 if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="823c6-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="823c6-134">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="823c6-135">參考</span><span class="sxs-lookup"><span data-stu-id="823c6-135">Reference</span></span>

[<span data-ttu-id="823c6-136">Api 類別</span><span class="sxs-lookup"><span data-stu-id="823c6-136">Api class</span></span>](./api-class.md)

[<span data-ttu-id="823c6-137">Api 成員</span><span class="sxs-lookup"><span data-stu-id="823c6-137">Api members</span></span>](./api-members.md)

[<span data-ttu-id="823c6-138">RetrieveColumnSize 多載</span><span class="sxs-lookup"><span data-stu-id="823c6-138">RetrieveColumnSize overload</span></span>](./api.retrievecolumnsize-method.md)

[<span data-ttu-id="823c6-139">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="823c6-139">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
