---
description: 深入瞭解： EsentQuotaException 類別
title: EsentQuotaException 類別
TOCTitle: EsentQuotaException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentQuotaException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentquotaexception(v=EXCHG.10)
ms:contentKeyID: 55102495
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentQuotaException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentQuotaException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 53b108a4d55553788a6c2d316f93f4f8efc76035
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978127"
---
# <a name="esentquotaexception-class"></a><span data-ttu-id="8a478-103">EsentQuotaException 類別</span><span class="sxs-lookup"><span data-stu-id="8a478-103">EsentQuotaException class</span></span>

<span data-ttu-id="8a478-104">配額例外狀況的基類。</span><span class="sxs-lookup"><span data-stu-id="8a478-104">Base class for Quota exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="8a478-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="8a478-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="8a478-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="8a478-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="8a478-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="8a478-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="8a478-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="8a478-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="8a478-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="8a478-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="8a478-110">EsentOperationException （.）</span><span class="sxs-lookup"><span data-stu-id="8a478-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="8a478-111">EsentResourceException （.）</span><span class="sxs-lookup"><span data-stu-id="8a478-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            <span data-ttu-id="8a478-112">EsentQuotaException （.）</span><span class="sxs-lookup"><span data-stu-id="8a478-112">Microsoft.Isam.Esent.Interop.EsentQuotaException</span></span>  
              [<span data-ttu-id="8a478-113">EsentOutOfDatabaseSpaceException （.）</span><span class="sxs-lookup"><span data-stu-id="8a478-113">Microsoft.Isam.Esent.Interop.EsentOutOfDatabaseSpaceException</span></span>](./esentoutofdatabasespaceexception-class.md)  
              [<span data-ttu-id="8a478-114">EsentTooManyInstancesException （.）</span><span class="sxs-lookup"><span data-stu-id="8a478-114">Microsoft.Isam.Esent.Interop.EsentTooManyInstancesException</span></span>](./esenttoomanyinstancesexception-class.md)  
              [<span data-ttu-id="8a478-115">EsentTooManyOpenTablesException （.）</span><span class="sxs-lookup"><span data-stu-id="8a478-115">Microsoft.Isam.Esent.Interop.EsentTooManyOpenTablesException</span></span>](./esenttoomanyopentablesexception-class.md)  
              [<span data-ttu-id="8a478-116">EsentVersionStoreOutOfMemoryException （.）</span><span class="sxs-lookup"><span data-stu-id="8a478-116">Microsoft.Isam.Esent.Interop.EsentVersionStoreOutOfMemoryException</span></span>](./esentversionstoreoutofmemoryexception-class.md)  

<span data-ttu-id="8a478-117">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8a478-117">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8a478-118">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="8a478-118">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8a478-119">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a478-119">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentQuotaException _
    Inherits EsentResourceException
'Usage
Dim instance As EsentQuotaException
```

``` csharp
[SerializableAttribute]
public abstract class EsentQuotaException : EsentResourceException
```

## <a name="thread-safety"></a><span data-ttu-id="8a478-120">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="8a478-120">Thread safety</span></span>

<span data-ttu-id="8a478-121">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="8a478-121">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="8a478-122">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="8a478-122">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="8a478-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8a478-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8a478-124">參考</span><span class="sxs-lookup"><span data-stu-id="8a478-124">Reference</span></span>

[<span data-ttu-id="8a478-125">EsentQuotaException 成員</span><span class="sxs-lookup"><span data-stu-id="8a478-125">EsentQuotaException members</span></span>](./esentquotaexception-members.md)

[<span data-ttu-id="8a478-126">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="8a478-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
