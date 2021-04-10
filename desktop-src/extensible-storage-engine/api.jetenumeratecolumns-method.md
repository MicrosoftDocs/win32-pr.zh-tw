---
description: 深入瞭解： JetEnumerateColumns 方法
title: JetEnumerateColumns 方法
TOCTitle: 'JetEnumerateColumns method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetEnumerateColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Int32,Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID[],System.Int32@,Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN[]@,Microsoft.Isam.Esent.Interop.JET_PFNREALLOC,System.IntPtr,System.Int32,Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetenumeratecolumns(v=EXCHG.10)
ms:contentKeyID: 55100695
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetEnumerateColumns
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetEnumerateColumns
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c9a9848d4470d54cc2a146098343b664c9bd3419
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026150"
---
# <a name="apijetenumeratecolumns-method"></a><span data-ttu-id="d1207-103">JetEnumerateColumns 方法</span><span class="sxs-lookup"><span data-stu-id="d1207-103">Api.JetEnumerateColumns method</span></span>

<span data-ttu-id="d1207-104">有效率地從資料指標的目前記錄或該資料指標的複製緩衝區，抓取一組資料行和其值。</span><span class="sxs-lookup"><span data-stu-id="d1207-104">Efficiently retrieves a set of columns and their values from the current record of a cursor or the copy buffer of that cursor.</span></span> <span data-ttu-id="d1207-105">您可以使用資料行識別碼、itagSequence 數位和其他特性的清單來限制抓取的資料行和值。</span><span class="sxs-lookup"><span data-stu-id="d1207-105">The columns and values retrieved can be restricted by a list of column IDs, itagSequence numbers, and other characteristics.</span></span> <span data-ttu-id="d1207-106">此資料行抓取 API 是唯一的，因為它會將資訊傳回給動態配置的記憶體，而這些記憶體是使用使用者提供的 realloc 相容回呼所取得。</span><span class="sxs-lookup"><span data-stu-id="d1207-106">This column retrieval API is unique in that it returns information in dynamically allocated memory that is obtained using a user-provided realloc compatible callback.</span></span> <span data-ttu-id="d1207-107">這項新的彈性可讓您有效率地抓取具有特定特性 (的資料行資料，例如呼叫端未知) 大小和多重性。</span><span class="sxs-lookup"><span data-stu-id="d1207-107">This new flexibility permits the efficient retrieval of column data with specific characteristics (such as size and multiplicity) that are unknown to the caller.</span></span> <span data-ttu-id="d1207-108">如此一來，就不需要使用 JetRetrieveColumn 的探索模式來判斷這些特性，以便設定 JetRetrieveColumn 的最後一個呼叫，以成功取得所需的資料。</span><span class="sxs-lookup"><span data-stu-id="d1207-108">This eliminates the need for the use of the discovery modes of JetRetrieveColumn to determine those characteristics in order to setup a final call to JetRetrieveColumn that will successfully retrieve the desired data.</span></span>

<span data-ttu-id="d1207-109">此 API 不符合 CLS 規範。</span><span class="sxs-lookup"><span data-stu-id="d1207-109">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="d1207-110">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d1207-110">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d1207-111">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="d1207-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d1207-112">語法</span><span class="sxs-lookup"><span data-stu-id="d1207-112">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function JetEnumerateColumns ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    numColumnids As Integer, _
    columnids As JET_ENUMCOLUMNID(), _
    <OutAttribute> ByRef numColumnValues As Integer, _
    <OutAttribute> ByRef columnValues As JET_ENUMCOLUMN(), _
    allocator As JET_PFNREALLOC, _
    allocatorContext As IntPtr, _
    maxDataSize As Integer, _
    grbit As EnumerateColumnsGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim numColumnids As Integer
Dim columnids As JET_ENUMCOLUMNID()
Dim numColumnValues As Integer
Dim columnValues As JET_ENUMCOLUMN()
Dim allocator As JET_PFNREALLOC
Dim allocatorContext As IntPtr
Dim maxDataSize As Integer
Dim grbit As EnumerateColumnsGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetEnumerateColumns(sesid, _
    tableid, numColumnids, columnids, _
    numColumnValues, columnValues, allocator, _
    allocatorContext, maxDataSize, grbit)
```

``` csharp
[CLSCompliantAttribute(false)]
public static JET_wrn JetEnumerateColumns(
    JET_SESID sesid,
    JET_TABLEID tableid,
    int numColumnids,
    JET_ENUMCOLUMNID[] columnids,
    out int numColumnValues,
    out JET_ENUMCOLUMN[] columnValues,
    JET_PFNREALLOC allocator,
    IntPtr allocatorContext,
    int maxDataSize,
    EnumerateColumnsGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="d1207-113">參數</span><span class="sxs-lookup"><span data-stu-id="d1207-113">Parameters</span></span>

  - <span data-ttu-id="d1207-114">sesid</span><span class="sxs-lookup"><span data-stu-id="d1207-114">sesid</span></span>  
    <span data-ttu-id="d1207-115">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d1207-115">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="d1207-116">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="d1207-116">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="d1207-117">tableid</span><span class="sxs-lookup"><span data-stu-id="d1207-117">tableid</span></span>  
    <span data-ttu-id="d1207-118">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d1207-118">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="d1207-119">要從中取出資料的資料指標。</span><span class="sxs-lookup"><span data-stu-id="d1207-119">The cursor to retrieve data from.</span></span>

<!-- end list -->

  - <span data-ttu-id="d1207-120">numColumnids</span><span class="sxs-lookup"><span data-stu-id="d1207-120">numColumnids</span></span>  
    <span data-ttu-id="d1207-121">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="d1207-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="d1207-122">JET_ENUMCOLUMNIDS 的數目。</span><span class="sxs-lookup"><span data-stu-id="d1207-122">The numbers of JET_ENUMCOLUMNIDS.</span></span>

<!-- end list -->

  - <span data-ttu-id="d1207-123">columnids</span><span class="sxs-lookup"><span data-stu-id="d1207-123">columnids</span></span>  
    <span data-ttu-id="d1207-124">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="d1207-124">Type: \[\]</span></span>  
    
    <span data-ttu-id="d1207-125">一個選擇性的資料行識別碼陣列，每個都有一個選擇性的 itagSequence 數位陣列來列舉。</span><span class="sxs-lookup"><span data-stu-id="d1207-125">An optional array of column IDs, each with an optional array of itagSequence numbers to enumerate.</span></span>

<!-- end list -->

  - <span data-ttu-id="d1207-126">numColumnValues</span><span class="sxs-lookup"><span data-stu-id="d1207-126">numColumnValues</span></span>  
    <span data-ttu-id="d1207-127">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="d1207-127">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="d1207-128">傳回抓取的資料行值數目。</span><span class="sxs-lookup"><span data-stu-id="d1207-128">Returns the number of column values retrieved.</span></span>

<!-- end list -->

  - <span data-ttu-id="d1207-129">columnValues</span><span class="sxs-lookup"><span data-stu-id="d1207-129">columnValues</span></span>  
    <span data-ttu-id="d1207-130">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="d1207-130">Type: \[\]</span></span>  
    
    <span data-ttu-id="d1207-131">傳回列舉的資料行值。</span><span class="sxs-lookup"><span data-stu-id="d1207-131">Returns the enumerated column values.</span></span>

<!-- end list -->

  - <span data-ttu-id="d1207-132">allocator</span><span class="sxs-lookup"><span data-stu-id="d1207-132">allocator</span></span>  
    <span data-ttu-id="d1207-133">類型： [Microsoft.Isam.Esent.Interop.JET_PFNREALLOC](./jet-pfnrealloc-delegate.md)</span><span class="sxs-lookup"><span data-stu-id="d1207-133">Type: [Microsoft.Isam.Esent.Interop.JET_PFNREALLOC](./jet-pfnrealloc-delegate.md)</span></span>  
    
    <span data-ttu-id="d1207-134">用來配置記憶體的回呼。</span><span class="sxs-lookup"><span data-stu-id="d1207-134">Callback used to allocate memory.</span></span>

<!-- end list -->

  - <span data-ttu-id="d1207-135">allocatorCoNtext</span><span class="sxs-lookup"><span data-stu-id="d1207-135">allocatorContext</span></span>  
    <span data-ttu-id="d1207-136">類型： [system.object](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="d1207-136">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="d1207-137">配置回呼的內容。</span><span class="sxs-lookup"><span data-stu-id="d1207-137">Context for the allocation callback.</span></span>

<!-- end list -->

  - <span data-ttu-id="d1207-138">maxDataSize</span><span class="sxs-lookup"><span data-stu-id="d1207-138">maxDataSize</span></span>  
    <span data-ttu-id="d1207-139">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="d1207-139">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="d1207-140">設定要從長文字或長二進位資料行傳回的資料量上限。</span><span class="sxs-lookup"><span data-stu-id="d1207-140">Sets a cap on the amount of data to return from a long text or long binary column.</span></span> <span data-ttu-id="d1207-141">您可以使用這個參數來防止列舉非常大的資料行值。</span><span class="sxs-lookup"><span data-stu-id="d1207-141">This parameter can be used to prevent the enumeration of an extremely large column value.</span></span>

<!-- end list -->

  - <span data-ttu-id="d1207-142">grbit</span><span class="sxs-lookup"><span data-stu-id="d1207-142">grbit</span></span>  
    <span data-ttu-id="d1207-143">型別： [EnumerateColumnsGrbit](./enumeratecolumnsgrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="d1207-143">Type: [Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit](./enumeratecolumnsgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="d1207-144">取出選項。</span><span class="sxs-lookup"><span data-stu-id="d1207-144">Retrieve options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="d1207-145">傳回值</span><span class="sxs-lookup"><span data-stu-id="d1207-145">Return value</span></span>

<span data-ttu-id="d1207-146">類型： [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="d1207-146">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="d1207-147">警告或成功。</span><span class="sxs-lookup"><span data-stu-id="d1207-147">A warning or success.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d1207-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d1207-148">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d1207-149">參考</span><span class="sxs-lookup"><span data-stu-id="d1207-149">Reference</span></span>

[<span data-ttu-id="d1207-150">Api 類別</span><span class="sxs-lookup"><span data-stu-id="d1207-150">Api class</span></span>](./api-class.md)

[<span data-ttu-id="d1207-151">Api 成員</span><span class="sxs-lookup"><span data-stu-id="d1207-151">Api members</span></span>](./api-members.md)

[<span data-ttu-id="d1207-152">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="d1207-152">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
