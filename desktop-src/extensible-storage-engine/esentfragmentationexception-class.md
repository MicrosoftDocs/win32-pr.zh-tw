---
description: 深入瞭解： EsentFragmentationException 類別
title: EsentFragmentationException 類別
TOCTitle: EsentFragmentationException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFragmentationException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfragmentationexception(v=EXCHG.10)
ms:contentKeyID: 55101771
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFragmentationException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFragmentationException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 081198a696be9982e1fd8a7e4f1468e6d63d1c97
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106997595"
---
# <a name="esentfragmentationexception-class"></a><span data-ttu-id="3a8d5-103">EsentFragmentationException 類別</span><span class="sxs-lookup"><span data-stu-id="3a8d5-103">EsentFragmentationException class</span></span>

<span data-ttu-id="3a8d5-104">片段例外狀況的基類。</span><span class="sxs-lookup"><span data-stu-id="3a8d5-104">Base class for Fragmentation exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="3a8d5-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="3a8d5-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="3a8d5-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="3a8d5-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="3a8d5-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="3a8d5-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="3a8d5-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="3a8d5-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="3a8d5-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="3a8d5-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="3a8d5-110">EsentDataException （.）</span><span class="sxs-lookup"><span data-stu-id="3a8d5-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          <span data-ttu-id="3a8d5-111">EsentFragmentationException （.）</span><span class="sxs-lookup"><span data-stu-id="3a8d5-111">Microsoft.Isam.Esent.Interop.EsentFragmentationException</span></span>  
            

<span data-ttu-id="3a8d5-112">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3a8d5-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3a8d5-113">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="3a8d5-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3a8d5-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a8d5-114">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentFragmentationException _
    Inherits EsentDataException
'Usage
Dim instance As EsentFragmentationException
```

``` csharp
[SerializableAttribute]
public abstract class EsentFragmentationException : EsentDataException
```

## <a name="thread-safety"></a><span data-ttu-id="3a8d5-115">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="3a8d5-115">Thread safety</span></span>

<span data-ttu-id="3a8d5-116">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="3a8d5-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="3a8d5-117">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="3a8d5-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="3a8d5-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3a8d5-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3a8d5-119">參考</span><span class="sxs-lookup"><span data-stu-id="3a8d5-119">Reference</span></span>

[<span data-ttu-id="3a8d5-120">EsentFragmentationException 成員</span><span class="sxs-lookup"><span data-stu-id="3a8d5-120">EsentFragmentationException members</span></span>](./esentfragmentationexception-members.md)

[<span data-ttu-id="3a8d5-121">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="3a8d5-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="3a8d5-122">衍生類型</span><span class="sxs-lookup"><span data-stu-id="3a8d5-122">Derived types</span></span>

[<span data-ttu-id="3a8d5-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="3a8d5-123">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="3a8d5-124">System.Exception</span><span class="sxs-lookup"><span data-stu-id="3a8d5-124">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="3a8d5-125">EsentException。</span><span class="sxs-lookup"><span data-stu-id="3a8d5-125">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="3a8d5-126">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="3a8d5-126">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="3a8d5-127">EsentDataException （.）</span><span class="sxs-lookup"><span data-stu-id="3a8d5-127">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          <span data-ttu-id="3a8d5-128">EsentFragmentationException （.）</span><span class="sxs-lookup"><span data-stu-id="3a8d5-128">Microsoft.Isam.Esent.Interop.EsentFragmentationException</span></span>  
            [<span data-ttu-id="3a8d5-129">EsentLogSectorSizeMismatchException （.）</span><span class="sxs-lookup"><span data-stu-id="3a8d5-129">Microsoft.Isam.Esent.Interop.EsentLogSectorSizeMismatchException</span></span>](./esentlogsectorsizemismatchexception-class.md)  
            [<span data-ttu-id="3a8d5-130">EsentLogSequenceEndDatabasesConsistentException （.）</span><span class="sxs-lookup"><span data-stu-id="3a8d5-130">Microsoft.Isam.Esent.Interop.EsentLogSequenceEndDatabasesConsistentException</span></span>](./esentlogsequenceenddatabasesconsistentexception-class.md)  
            [<span data-ttu-id="3a8d5-131">EsentLogSequenceEndException （.）</span><span class="sxs-lookup"><span data-stu-id="3a8d5-131">Microsoft.Isam.Esent.Interop.EsentLogSequenceEndException</span></span>](./esentlogsequenceendexception-class.md)  
            [<span data-ttu-id="3a8d5-132">EsentOutOfAutoincrementValuesException （.）</span><span class="sxs-lookup"><span data-stu-id="3a8d5-132">Microsoft.Isam.Esent.Interop.EsentOutOfAutoincrementValuesException</span></span>](./esentoutofautoincrementvaluesexception-class.md)  
            [<span data-ttu-id="3a8d5-133">EsentOutOfDbtimeValuesException （.）</span><span class="sxs-lookup"><span data-stu-id="3a8d5-133">Microsoft.Isam.Esent.Interop.EsentOutOfDbtimeValuesException</span></span>](./esentoutofdbtimevaluesexception-class.md)  
            [<span data-ttu-id="3a8d5-134">EsentOutOfLongValueIDsException （.）</span><span class="sxs-lookup"><span data-stu-id="3a8d5-134">Microsoft.Isam.Esent.Interop.EsentOutOfLongValueIDsException</span></span>](./esentoutoflongvalueidsexception-class.md)  
            [<span data-ttu-id="3a8d5-135">EsentOutOfObjectIDsException （.）</span><span class="sxs-lookup"><span data-stu-id="3a8d5-135">Microsoft.Isam.Esent.Interop.EsentOutOfObjectIDsException</span></span>](./esentoutofobjectidsexception-class.md)  
            [<span data-ttu-id="3a8d5-136">EsentOutOfSequentialIndexValuesException （.）</span><span class="sxs-lookup"><span data-stu-id="3a8d5-136">Microsoft.Isam.Esent.Interop.EsentOutOfSequentialIndexValuesException</span></span>](./esentoutofsequentialindexvaluesexception-class.md)