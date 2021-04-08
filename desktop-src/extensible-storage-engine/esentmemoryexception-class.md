---
description: 深入瞭解： EsentMemoryException 類別
title: EsentMemoryException 類別
TOCTitle: EsentMemoryException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMemoryException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmemoryexception(v=EXCHG.10)
ms:contentKeyID: 55102197
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMemoryException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMemoryException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6a7090fdedee2969e5dd3658b7068fd8739e9365
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "103853259"
---
# <a name="esentmemoryexception-class"></a><span data-ttu-id="c0d35-103">EsentMemoryException 類別</span><span class="sxs-lookup"><span data-stu-id="c0d35-103">EsentMemoryException class</span></span>

<span data-ttu-id="c0d35-104">記憶體例外狀況的基類。</span><span class="sxs-lookup"><span data-stu-id="c0d35-104">Base class for Memory exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="c0d35-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="c0d35-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="c0d35-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="c0d35-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="c0d35-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="c0d35-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="c0d35-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="c0d35-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="c0d35-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="c0d35-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="c0d35-110">EsentOperationException （.）</span><span class="sxs-lookup"><span data-stu-id="c0d35-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="c0d35-111">EsentResourceException （.）</span><span class="sxs-lookup"><span data-stu-id="c0d35-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            <span data-ttu-id="c0d35-112">EsentMemoryException （.）</span><span class="sxs-lookup"><span data-stu-id="c0d35-112">Microsoft.Isam.Esent.Interop.EsentMemoryException</span></span>  
              

<span data-ttu-id="c0d35-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c0d35-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c0d35-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="c0d35-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c0d35-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0d35-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentMemoryException _
    Inherits EsentResourceException
'Usage
Dim instance As EsentMemoryException
```

``` csharp
[SerializableAttribute]
public abstract class EsentMemoryException : EsentResourceException
```

## <a name="thread-safety"></a><span data-ttu-id="c0d35-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="c0d35-116">Thread safety</span></span>

<span data-ttu-id="c0d35-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="c0d35-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="c0d35-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="c0d35-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="c0d35-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c0d35-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c0d35-120">參考</span><span class="sxs-lookup"><span data-stu-id="c0d35-120">Reference</span></span>

[<span data-ttu-id="c0d35-121">EsentMemoryException 成員</span><span class="sxs-lookup"><span data-stu-id="c0d35-121">EsentMemoryException members</span></span>](./esentmemoryexception-members.md)

[<span data-ttu-id="c0d35-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="c0d35-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="c0d35-123">衍生類型</span><span class="sxs-lookup"><span data-stu-id="c0d35-123">Derived types</span></span>

[<span data-ttu-id="c0d35-124">System.Object</span><span class="sxs-lookup"><span data-stu-id="c0d35-124">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="c0d35-125">System.Exception</span><span class="sxs-lookup"><span data-stu-id="c0d35-125">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="c0d35-126">EsentException。</span><span class="sxs-lookup"><span data-stu-id="c0d35-126">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="c0d35-127">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="c0d35-127">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="c0d35-128">EsentOperationException （.）</span><span class="sxs-lookup"><span data-stu-id="c0d35-128">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="c0d35-129">EsentResourceException （.）</span><span class="sxs-lookup"><span data-stu-id="c0d35-129">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            <span data-ttu-id="c0d35-130">EsentMemoryException （.）</span><span class="sxs-lookup"><span data-stu-id="c0d35-130">Microsoft.Isam.Esent.Interop.EsentMemoryException</span></span>  
              [<span data-ttu-id="c0d35-131">EsentOutOfBuffersException （.）</span><span class="sxs-lookup"><span data-stu-id="c0d35-131">Microsoft.Isam.Esent.Interop.EsentOutOfBuffersException</span></span>](./esentoutofbuffersexception-class.md)  
              [<span data-ttu-id="c0d35-132">EsentOutOfCursorsException （.）</span><span class="sxs-lookup"><span data-stu-id="c0d35-132">Microsoft.Isam.Esent.Interop.EsentOutOfCursorsException</span></span>](./esentoutofcursorsexception-class.md)  
              [<span data-ttu-id="c0d35-133">EsentOutOfFileHandlesException （.）</span><span class="sxs-lookup"><span data-stu-id="c0d35-133">Microsoft.Isam.Esent.Interop.EsentOutOfFileHandlesException</span></span>](./esentoutoffilehandlesexception-class.md)  
              [<span data-ttu-id="c0d35-134">EsentOutOfMemoryException （.）</span><span class="sxs-lookup"><span data-stu-id="c0d35-134">Microsoft.Isam.Esent.Interop.EsentOutOfMemoryException</span></span>](./esentoutofmemoryexception-class.md)  
              [<span data-ttu-id="c0d35-135">EsentOutOfSessionsException （.）</span><span class="sxs-lookup"><span data-stu-id="c0d35-135">Microsoft.Isam.Esent.Interop.EsentOutOfSessionsException</span></span>](./esentoutofsessionsexception-class.md)  
              [<span data-ttu-id="c0d35-136">EsentOutOfThreadsException （.）</span><span class="sxs-lookup"><span data-stu-id="c0d35-136">Microsoft.Isam.Esent.Interop.EsentOutOfThreadsException</span></span>](./esentoutofthreadsexception-class.md)  
              [<span data-ttu-id="c0d35-137">EsentTooManyMempoolEntriesException （.）</span><span class="sxs-lookup"><span data-stu-id="c0d35-137">Microsoft.Isam.Esent.Interop.EsentTooManyMempoolEntriesException</span></span>](./esenttoomanymempoolentriesexception-class.md)  
              [<span data-ttu-id="c0d35-138">EsentTooManyOpenIndexesException （.）</span><span class="sxs-lookup"><span data-stu-id="c0d35-138">Microsoft.Isam.Esent.Interop.EsentTooManyOpenIndexesException</span></span>](./esenttoomanyopenindexesexception-class.md)  
              [<span data-ttu-id="c0d35-139">EsentTooManySortsException （.）</span><span class="sxs-lookup"><span data-stu-id="c0d35-139">Microsoft.Isam.Esent.Interop.EsentTooManySortsException</span></span>](./esenttoomanysortsexception-class.md)