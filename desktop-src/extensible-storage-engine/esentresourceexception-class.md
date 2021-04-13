---
description: 深入瞭解： EsentResourceException 類別
title: EsentResourceException 類別
TOCTitle: EsentResourceException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentResourceException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentresourceexception(v=EXCHG.10)
ms:contentKeyID: 55102627
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentResourceException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentResourceException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a7d4964bb4ed9c1305652d9425170bd934c9274e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193400"
---
# <a name="esentresourceexception-class"></a><span data-ttu-id="30f9b-103">EsentResourceException 類別</span><span class="sxs-lookup"><span data-stu-id="30f9b-103">EsentResourceException class</span></span>

<span data-ttu-id="30f9b-104">資源例外狀況的基類。</span><span class="sxs-lookup"><span data-stu-id="30f9b-104">Base class for Resource exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="30f9b-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="30f9b-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="30f9b-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="30f9b-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="30f9b-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="30f9b-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="30f9b-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="30f9b-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="30f9b-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="30f9b-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="30f9b-110">EsentOperationException （.）</span><span class="sxs-lookup"><span data-stu-id="30f9b-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          <span data-ttu-id="30f9b-111">EsentResourceException （.）</span><span class="sxs-lookup"><span data-stu-id="30f9b-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>  
            [<span data-ttu-id="30f9b-112">EsentDiskException （.）</span><span class="sxs-lookup"><span data-stu-id="30f9b-112">Microsoft.Isam.Esent.Interop.EsentDiskException</span></span>](./esentdiskexception-class.md)  
            [<span data-ttu-id="30f9b-113">EsentMemoryException （.）</span><span class="sxs-lookup"><span data-stu-id="30f9b-113">Microsoft.Isam.Esent.Interop.EsentMemoryException</span></span>](./esentmemoryexception-class.md)  
            [<span data-ttu-id="30f9b-114">EsentQuotaException （.）</span><span class="sxs-lookup"><span data-stu-id="30f9b-114">Microsoft.Isam.Esent.Interop.EsentQuotaException</span></span>](./esentquotaexception-class.md)  
            [<span data-ttu-id="30f9b-115">EsentTaskDroppedException （.）</span><span class="sxs-lookup"><span data-stu-id="30f9b-115">Microsoft.Isam.Esent.Interop.EsentTaskDroppedException</span></span>](./esenttaskdroppedexception-class.md)  
            [<span data-ttu-id="30f9b-116">EsentTooManyIOException （.）</span><span class="sxs-lookup"><span data-stu-id="30f9b-116">Microsoft.Isam.Esent.Interop.EsentTooManyIOException</span></span>](./esenttoomanyioexception-class.md)  

<span data-ttu-id="30f9b-117">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="30f9b-117">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="30f9b-118">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="30f9b-118">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="30f9b-119">Syntax</span><span class="sxs-lookup"><span data-stu-id="30f9b-119">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentResourceException _
    Inherits EsentOperationException
'Usage
Dim instance As EsentResourceException
```

``` csharp
[SerializableAttribute]
public abstract class EsentResourceException : EsentOperationException
```

## <a name="thread-safety"></a><span data-ttu-id="30f9b-120">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="30f9b-120">Thread safety</span></span>

<span data-ttu-id="30f9b-121">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="30f9b-121">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="30f9b-122">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="30f9b-122">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="30f9b-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="30f9b-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="30f9b-124">參考</span><span class="sxs-lookup"><span data-stu-id="30f9b-124">Reference</span></span>

[<span data-ttu-id="30f9b-125">EsentResourceException 成員</span><span class="sxs-lookup"><span data-stu-id="30f9b-125">EsentResourceException members</span></span>](./esentresourceexception-members.md)

[<span data-ttu-id="30f9b-126">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="30f9b-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
