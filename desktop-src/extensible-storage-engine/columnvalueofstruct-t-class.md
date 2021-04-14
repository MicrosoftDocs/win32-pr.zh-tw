---
description: 深入瞭解： ColumnValueOfStruct <T> 類別
title: ColumnValueOfStruct (T) 類別
TOCTitle: ColumnValueOfStruct(T) class
ms:assetid: T:Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1
ms:mtpsurl: https://msdn.microsoft.com/library/Dn334171(v=EXCHG.10)
ms:contentKeyID: 55100962
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 82083adcaaf0d9f5b4f2a720da83e95cd4b39401
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104321412"
---
# <a name="columnvalueofstructt-class"></a><span data-ttu-id="538d7-103">ColumnValueOfStruct \<T\> 類別</span><span class="sxs-lookup"><span data-stu-id="538d7-103">ColumnValueOfStruct\<T\> class</span></span>

<span data-ttu-id="538d7-104">設定結構類型的資料行 (例如 Int32/Guid) 。</span><span class="sxs-lookup"><span data-stu-id="538d7-104">Set a column of a struct type (e.g. Int32/Guid).</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="538d7-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="538d7-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="538d7-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="538d7-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="538d7-107">ColumnValue （.）</span><span class="sxs-lookup"><span data-stu-id="538d7-107">Microsoft.Isam.Esent.Interop.ColumnValue</span></span>](./columnvalue-class.md)  
    <span data-ttu-id="538d7-108">ColumnValueOfStruct （.）\<T\></span><span class="sxs-lookup"><span data-stu-id="538d7-108">Microsoft.Isam.Esent.Interop.ColumnValueOfStruct\<T\></span></span>  
      

<span data-ttu-id="538d7-109">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="538d7-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="538d7-110">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="538d7-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="538d7-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="538d7-111">Syntax</span></span>

``` vb
'Declaration
Public MustInherit Class ColumnValueOfStruct(Of T As {Structure, New, IEquatable(Of T)}) _
    Inherits ColumnValue
'Usage
Dim instance As ColumnValueOfStruct(Of T)
```

``` csharp
public abstract class ColumnValueOfStruct<T> : ColumnValue
where T : struct, new(), IEquatable<T>
```

#### <a name="type-parameters"></a><span data-ttu-id="538d7-112">型別參數</span><span class="sxs-lookup"><span data-stu-id="538d7-112">Type parameters</span></span>

  - <span data-ttu-id="538d7-113">T</span><span class="sxs-lookup"><span data-stu-id="538d7-113">T</span></span>  
    <span data-ttu-id="538d7-114">要設定的類型。</span><span class="sxs-lookup"><span data-stu-id="538d7-114">Type to set.</span></span>

## <a name="thread-safety"></a><span data-ttu-id="538d7-115">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="538d7-115">Thread safety</span></span>

<span data-ttu-id="538d7-116">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="538d7-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="538d7-117">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="538d7-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="538d7-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="538d7-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="538d7-119">參考</span><span class="sxs-lookup"><span data-stu-id="538d7-119">Reference</span></span>

[<span data-ttu-id="538d7-120">ColumnValueOfStruct \<T\> 成員</span><span class="sxs-lookup"><span data-stu-id="538d7-120">ColumnValueOfStruct\<T\> members</span></span>](./columnvalueofstruct-t-members.md)

[<span data-ttu-id="538d7-121">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="538d7-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="538d7-122">衍生類型</span><span class="sxs-lookup"><span data-stu-id="538d7-122">Derived types</span></span>

[<span data-ttu-id="538d7-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="538d7-123">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="538d7-124">ColumnValue （.）</span><span class="sxs-lookup"><span data-stu-id="538d7-124">Microsoft.Isam.Esent.Interop.ColumnValue</span></span>](./columnvalue-class.md)  
    <span data-ttu-id="538d7-125">ColumnValueOfStruct （.）\<T\></span><span class="sxs-lookup"><span data-stu-id="538d7-125">Microsoft.Isam.Esent.Interop.ColumnValueOfStruct\<T\></span></span>  
      [<span data-ttu-id="538d7-126">BoolColumnValue （.）</span><span class="sxs-lookup"><span data-stu-id="538d7-126">Microsoft.Isam.Esent.Interop.BoolColumnValue</span></span>](./boolcolumnvalue-class.md)  
      [<span data-ttu-id="538d7-127">ByteColumnValue （.）</span><span class="sxs-lookup"><span data-stu-id="538d7-127">Microsoft.Isam.Esent.Interop.ByteColumnValue</span></span>](./bytecolumnvalue-class.md)  
      [<span data-ttu-id="538d7-128">DateTimeColumnValue （.）</span><span class="sxs-lookup"><span data-stu-id="538d7-128">Microsoft.Isam.Esent.Interop.DateTimeColumnValue</span></span>](./datetimecolumnvalue-class.md)  
      [<span data-ttu-id="538d7-129">DoubleColumnValue （.）</span><span class="sxs-lookup"><span data-stu-id="538d7-129">Microsoft.Isam.Esent.Interop.DoubleColumnValue</span></span>](./doublecolumnvalue-class.md)  
      [<span data-ttu-id="538d7-130">FloatColumnValue （.）</span><span class="sxs-lookup"><span data-stu-id="538d7-130">Microsoft.Isam.Esent.Interop.FloatColumnValue</span></span>](./floatcolumnvalue-class.md)  
      [<span data-ttu-id="538d7-131">GuidColumnValue （.）</span><span class="sxs-lookup"><span data-stu-id="538d7-131">Microsoft.Isam.Esent.Interop.GuidColumnValue</span></span>](./guidcolumnvalue-class.md)  
      [<span data-ttu-id="538d7-132">Int16ColumnValue （.）</span><span class="sxs-lookup"><span data-stu-id="538d7-132">Microsoft.Isam.Esent.Interop.Int16ColumnValue</span></span>](./int16columnvalue-class.md)  
      [<span data-ttu-id="538d7-133">Int32ColumnValue （.）</span><span class="sxs-lookup"><span data-stu-id="538d7-133">Microsoft.Isam.Esent.Interop.Int32ColumnValue</span></span>](./int32columnvalue-class.md)  
      [<span data-ttu-id="538d7-134">Int64ColumnValue （.）</span><span class="sxs-lookup"><span data-stu-id="538d7-134">Microsoft.Isam.Esent.Interop.Int64ColumnValue</span></span>](./int64columnvalue-class.md)  
      [<span data-ttu-id="538d7-135">UInt16ColumnValue （.）</span><span class="sxs-lookup"><span data-stu-id="538d7-135">Microsoft.Isam.Esent.Interop.UInt16ColumnValue</span></span>](./uint16columnvalue-class.md)  
      [<span data-ttu-id="538d7-136">UInt32ColumnValue （.）</span><span class="sxs-lookup"><span data-stu-id="538d7-136">Microsoft.Isam.Esent.Interop.UInt32ColumnValue</span></span>](./uint32columnvalue-class.md)  
      [<span data-ttu-id="538d7-137">UInt64ColumnValue （.）</span><span class="sxs-lookup"><span data-stu-id="538d7-137">Microsoft.Isam.Esent.Interop.UInt64ColumnValue</span></span>](./uint64columnvalue-class.md)