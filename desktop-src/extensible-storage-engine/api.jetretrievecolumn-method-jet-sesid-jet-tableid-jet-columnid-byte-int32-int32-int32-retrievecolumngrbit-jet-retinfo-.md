---
description: '深入瞭解： JetRetrieveColumn 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID、Byte、Int32、Int32、Int32、RetrieveColumnGrbit、JET_RETINFO) '
title: 'JetRetrieveColumn 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID、Byte、Int32、Int32、Int32、RetrieveColumnGrbit、JET_RETINFO) '
TOCTitle: JetRetrieveColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , Int32, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Byte[],System.Int32,System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit,Microsoft.Isam.Esent.Interop.JET_RETINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetretrievecolumn(v=EXCHG.10)
ms:contentKeyID: 55100792
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumn
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 832e6d6cc123e4a85a2cacb2df688348732fcc0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320816"
---
# <a name="apijetretrievecolumn-method-jet_sesid-jet_tableid-jet_columnid-byte--int32-int32-int32-retrievecolumngrbit-jet_retinfo"></a><span data-ttu-id="4ca65-103">JetRetrieveColumn 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID、Byte、Int32、Int32、Int32、RetrieveColumnGrbit、JET_RETINFO) </span><span class="sxs-lookup"><span data-stu-id="4ca65-103">Api.JetRetrieveColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , Int32, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)</span></span>

<span data-ttu-id="4ca65-104">從目前的記錄抓取單一資料行值。</span><span class="sxs-lookup"><span data-stu-id="4ca65-104">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="4ca65-105">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="4ca65-105">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="4ca65-106">或者，此函式可以從資料指標複製緩衝區中所建立的記錄取得資料行。</span><span class="sxs-lookup"><span data-stu-id="4ca65-106">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="4ca65-107">此函數也可以從參考目前記錄的索引項目抓取資料行資料。</span><span class="sxs-lookup"><span data-stu-id="4ca65-107">This function can also retrieve column data from an index entry that references the current record.</span></span> <span data-ttu-id="4ca65-108">除了取得實際的資料行值之外，JetRetrieveColumn 還可以用來取得資料行的大小，然後再抓取資料行資料本身，讓應用程式緩衝區可以適當地調整大小。</span><span class="sxs-lookup"><span data-stu-id="4ca65-108">In addition to retrieving the actual column value, JetRetrieveColumn can also be used to retrieve the size of a column, before retrieving the column data itself so that application buffers can be sized appropriately.</span></span>

<span data-ttu-id="4ca65-109">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4ca65-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4ca65-110">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="4ca65-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4ca65-111">語法</span><span class="sxs-lookup"><span data-stu-id="4ca65-111">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetRetrieveColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As Byte(), _
    dataSize As Integer, _
    dataOffset As Integer, _
    <OutAttribute> ByRef actualDataSize As Integer, _
    grbit As RetrieveColumnGrbit, _
    retinfo As JET_RETINFO _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As Byte()
Dim dataSize As Integer
Dim dataOffset As Integer
Dim actualDataSize As Integer
Dim grbit As RetrieveColumnGrbit
Dim retinfo As JET_RETINFO
Dim returnValue As JET_wrn

returnValue = Api.JetRetrieveColumn(sesid, _
    tableid, columnid, data, dataSize, _
    dataOffset, actualDataSize, grbit, _
    retinfo)
```

``` csharp
public static JET_wrn JetRetrieveColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    byte[] data,
    int dataSize,
    int dataOffset,
    out int actualDataSize,
    RetrieveColumnGrbit grbit,
    JET_RETINFO retinfo
)
```

#### <a name="parameters"></a><span data-ttu-id="4ca65-112">參數</span><span class="sxs-lookup"><span data-stu-id="4ca65-112">Parameters</span></span>

  - <span data-ttu-id="4ca65-113">sesid</span><span class="sxs-lookup"><span data-stu-id="4ca65-113">sesid</span></span>  
    <span data-ttu-id="4ca65-114">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4ca65-114">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="4ca65-115">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="4ca65-115">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="4ca65-116">tableid</span><span class="sxs-lookup"><span data-stu-id="4ca65-116">tableid</span></span>  
    <span data-ttu-id="4ca65-117">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4ca65-117">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="4ca65-118">從中取出資料行的資料指標。</span><span class="sxs-lookup"><span data-stu-id="4ca65-118">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="4ca65-119">columnid</span><span class="sxs-lookup"><span data-stu-id="4ca65-119">columnid</span></span>  
    <span data-ttu-id="4ca65-120">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4ca65-120">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="4ca65-121">要取出的 columnid。</span><span class="sxs-lookup"><span data-stu-id="4ca65-121">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="4ca65-122">data</span><span class="sxs-lookup"><span data-stu-id="4ca65-122">data</span></span>  
    <span data-ttu-id="4ca65-123">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="4ca65-123">Type: \[\]</span></span>  
    
    <span data-ttu-id="4ca65-124">要取出的資料緩衝區。</span><span class="sxs-lookup"><span data-stu-id="4ca65-124">The data buffer to be retrieved into.</span></span>

<!-- end list -->

  - <span data-ttu-id="4ca65-125">dataSize</span><span class="sxs-lookup"><span data-stu-id="4ca65-125">dataSize</span></span>  
    <span data-ttu-id="4ca65-126">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="4ca65-126">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="4ca65-127">資料緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="4ca65-127">The size of the data buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="4ca65-128">dataOffset</span><span class="sxs-lookup"><span data-stu-id="4ca65-128">dataOffset</span></span>  
    <span data-ttu-id="4ca65-129">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="4ca65-129">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="4ca65-130">要將資料讀入資料緩衝區的位移。</span><span class="sxs-lookup"><span data-stu-id="4ca65-130">Offset into the data buffer to read data into.</span></span>

<!-- end list -->

  - <span data-ttu-id="4ca65-131">actualDataSize</span><span class="sxs-lookup"><span data-stu-id="4ca65-131">actualDataSize</span></span>  
    <span data-ttu-id="4ca65-132">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="4ca65-132">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="4ca65-133">傳回資料緩衝區的實際大小。</span><span class="sxs-lookup"><span data-stu-id="4ca65-133">Returns the actual size of the data buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="4ca65-134">grbit</span><span class="sxs-lookup"><span data-stu-id="4ca65-134">grbit</span></span>  
    <span data-ttu-id="4ca65-135">型別： [RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="4ca65-135">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="4ca65-136">取出資料行選項。</span><span class="sxs-lookup"><span data-stu-id="4ca65-136">Retrieve column options.</span></span>

<!-- end list -->

  - <span data-ttu-id="4ca65-137">retinfo</span><span class="sxs-lookup"><span data-stu-id="4ca65-137">retinfo</span></span>  
    <span data-ttu-id="4ca65-138">類型： [Microsoft.Isam.Esent.Interop.JET_RETINFO](./jet-retinfo-class.md)</span><span class="sxs-lookup"><span data-stu-id="4ca65-138">Type: [Microsoft.Isam.Esent.Interop.JET_RETINFO](./jet-retinfo-class.md)</span></span>  
    
    <span data-ttu-id="4ca65-139">如果 pretinfo 為 Null，則函式的行為就如同 itagSequence 為1，而 ibLongValue 為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="4ca65-139">If pretinfo is give as NULL then the function behaves as though an itagSequence of 1 and an ibLongValue of 0 (zero) were given.</span></span> <span data-ttu-id="4ca65-140">這會導致資料行抓取抓取多重值資料行的第一個值，並在位移 0 (零) 取出長資料。</span><span class="sxs-lookup"><span data-stu-id="4ca65-140">This causes column retrieval to retrieve the first value of a multi-valued column, and to retrieve long data at offset 0 (zero).</span></span>

#### <a name="return-value"></a><span data-ttu-id="4ca65-141">傳回值</span><span class="sxs-lookup"><span data-stu-id="4ca65-141">Return value</span></span>

<span data-ttu-id="4ca65-142">類型： [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="4ca65-142">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="4ca65-143">ESENT 警告碼。</span><span class="sxs-lookup"><span data-stu-id="4ca65-143">An ESENT warning code.</span></span>  

## <a name="remarks"></a><span data-ttu-id="4ca65-144">備註</span><span class="sxs-lookup"><span data-stu-id="4ca65-144">Remarks</span></span>

<span data-ttu-id="4ca65-145">這是採用緩衝區位移和大小的內部方法。</span><span class="sxs-lookup"><span data-stu-id="4ca65-145">This is an internal method that takes a buffer offset as well as size.</span></span>

## <a name="see-also"></a><span data-ttu-id="4ca65-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4ca65-146">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4ca65-147">參考</span><span class="sxs-lookup"><span data-stu-id="4ca65-147">Reference</span></span>

[<span data-ttu-id="4ca65-148">Api 類別</span><span class="sxs-lookup"><span data-stu-id="4ca65-148">Api class</span></span>](./api-class.md)

[<span data-ttu-id="4ca65-149">Api 成員</span><span class="sxs-lookup"><span data-stu-id="4ca65-149">Api members</span></span>](./api-members.md)

[<span data-ttu-id="4ca65-150">JetRetrieveColumn 多載</span><span class="sxs-lookup"><span data-stu-id="4ca65-150">JetRetrieveColumn overload</span></span>](./api.jetretrievecolumn-method.md)

[<span data-ttu-id="4ca65-151">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="4ca65-151">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
