---
description: 深入瞭解： EsentFatalException 類別
title: EsentFatalException 類別
TOCTitle: EsentFatalException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFatalException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfatalexception(v=EXCHG.10)
ms:contentKeyID: 55101653
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFatalException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFatalException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c38df447f2eb816772713ba930204e75aa38a88c
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104195682"
---
# <a name="esentfatalexception-class"></a><span data-ttu-id="fa72d-103">EsentFatalException 類別</span><span class="sxs-lookup"><span data-stu-id="fa72d-103">EsentFatalException class</span></span>

<span data-ttu-id="fa72d-104">嚴重例外狀況的基類。</span><span class="sxs-lookup"><span data-stu-id="fa72d-104">Base class for Fatal exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="fa72d-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="fa72d-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="fa72d-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="fa72d-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="fa72d-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="fa72d-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="fa72d-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="fa72d-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="fa72d-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="fa72d-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="fa72d-110">EsentOperationException （.）</span><span class="sxs-lookup"><span data-stu-id="fa72d-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          <span data-ttu-id="fa72d-111">EsentFatalException （.）</span><span class="sxs-lookup"><span data-stu-id="fa72d-111">Microsoft.Isam.Esent.Interop.EsentFatalException</span></span>  
            

<span data-ttu-id="fa72d-112">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fa72d-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="fa72d-113">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="fa72d-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fa72d-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa72d-114">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentFatalException _
    Inherits EsentOperationException
'Usage
Dim instance As EsentFatalException
```

``` csharp
[SerializableAttribute]
public abstract class EsentFatalException : EsentOperationException
```

## <a name="thread-safety"></a><span data-ttu-id="fa72d-115">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="fa72d-115">Thread safety</span></span>

<span data-ttu-id="fa72d-116">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="fa72d-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="fa72d-117">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="fa72d-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="fa72d-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fa72d-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fa72d-119">參考</span><span class="sxs-lookup"><span data-stu-id="fa72d-119">Reference</span></span>

[<span data-ttu-id="fa72d-120">EsentFatalException 成員</span><span class="sxs-lookup"><span data-stu-id="fa72d-120">EsentFatalException members</span></span>](./esentfatalexception-members.md)

[<span data-ttu-id="fa72d-121">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="fa72d-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="fa72d-122">衍生類型</span><span class="sxs-lookup"><span data-stu-id="fa72d-122">Derived types</span></span>

[<span data-ttu-id="fa72d-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="fa72d-123">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="fa72d-124">System.Exception</span><span class="sxs-lookup"><span data-stu-id="fa72d-124">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="fa72d-125">EsentException。</span><span class="sxs-lookup"><span data-stu-id="fa72d-125">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="fa72d-126">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="fa72d-126">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="fa72d-127">EsentOperationException （.）</span><span class="sxs-lookup"><span data-stu-id="fa72d-127">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          <span data-ttu-id="fa72d-128">EsentFatalException （.）</span><span class="sxs-lookup"><span data-stu-id="fa72d-128">Microsoft.Isam.Esent.Interop.EsentFatalException</span></span>  
            [<span data-ttu-id="fa72d-129">EsentInstanceUnavailableDueToFatalLogDiskFullException （.）</span><span class="sxs-lookup"><span data-stu-id="fa72d-129">Microsoft.Isam.Esent.Interop.EsentInstanceUnavailableDueToFatalLogDiskFullException</span></span>](./esentinstanceunavailableduetofatallogdiskfullexception-class.md)  
            [<span data-ttu-id="fa72d-130">EsentInstanceUnavailableException （.）</span><span class="sxs-lookup"><span data-stu-id="fa72d-130">Microsoft.Isam.Esent.Interop.EsentInstanceUnavailableException</span></span>](./esentinstanceunavailableexception-class.md)  
            [<span data-ttu-id="fa72d-131">EsentLogDisabledDueToRecoveryFailureException （.）</span><span class="sxs-lookup"><span data-stu-id="fa72d-131">Microsoft.Isam.Esent.Interop.EsentLogDisabledDueToRecoveryFailureException</span></span>](./esentlogdisabledduetorecoveryfailureexception-class.md)  
            [<span data-ttu-id="fa72d-132">EsentRollbackErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="fa72d-132">Microsoft.Isam.Esent.Interop.EsentRollbackErrorException</span></span>](./esentrollbackerrorexception-class.md)  
            [<span data-ttu-id="fa72d-133">EsentSectorSizeNotSupportedException （.）</span><span class="sxs-lookup"><span data-stu-id="fa72d-133">Microsoft.Isam.Esent.Interop.EsentSectorSizeNotSupportedException</span></span>](./esentsectorsizenotsupportedexception-class.md)  
            [<span data-ttu-id="fa72d-134">EsentUnloadableOSFunctionalityException （.）</span><span class="sxs-lookup"><span data-stu-id="fa72d-134">Microsoft.Isam.Esent.Interop.EsentUnloadableOSFunctionalityException</span></span>](./esentunloadableosfunctionalityexception-class.md)