---
description: 深入瞭解： EsentSPAvailExtCacheOutOfMemoryException 類別
title: EsentSPAvailExtCacheOutOfMemoryException 類別
TOCTitle: EsentSPAvailExtCacheOutOfMemoryException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentSPAvailExtCacheOutOfMemoryException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentspavailextcacheoutofmemoryexception(v=EXCHG.10)
ms:contentKeyID: 55102972
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentSPAvailExtCacheOutOfMemoryException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentSPAvailExtCacheOutOfMemoryException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e32168db9530bbef45add078260004b51cb1c98e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027378"
---
# <a name="esentspavailextcacheoutofmemoryexception-class"></a><span data-ttu-id="06d28-103">EsentSPAvailExtCacheOutOfMemoryException 類別</span><span class="sxs-lookup"><span data-stu-id="06d28-103">EsentSPAvailExtCacheOutOfMemoryException class</span></span>

<span data-ttu-id="06d28-104">JET_err 的基類。SPAvailExtCacheOutOfMemory 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="06d28-104">Base class for JET_err.SPAvailExtCacheOutOfMemory exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="06d28-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="06d28-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="06d28-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="06d28-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="06d28-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="06d28-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="06d28-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="06d28-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="06d28-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="06d28-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="06d28-110">EsentApiException （.）</span><span class="sxs-lookup"><span data-stu-id="06d28-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="06d28-111">EsentObsoleteException （.）</span><span class="sxs-lookup"><span data-stu-id="06d28-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="06d28-112">EsentSPAvailExtCacheOutOfMemoryException （.）</span><span class="sxs-lookup"><span data-stu-id="06d28-112">Microsoft.Isam.Esent.Interop.EsentSPAvailExtCacheOutOfMemoryException</span></span>  

<span data-ttu-id="06d28-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="06d28-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="06d28-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="06d28-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="06d28-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="06d28-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentSPAvailExtCacheOutOfMemoryException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentSPAvailExtCacheOutOfMemoryException
```

``` csharp
[SerializableAttribute]
public sealed class EsentSPAvailExtCacheOutOfMemoryException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="06d28-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="06d28-116">Thread safety</span></span>

<span data-ttu-id="06d28-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="06d28-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="06d28-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="06d28-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="06d28-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="06d28-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="06d28-120">參考</span><span class="sxs-lookup"><span data-stu-id="06d28-120">Reference</span></span>

[<span data-ttu-id="06d28-121">EsentSPAvailExtCacheOutOfMemoryException 成員</span><span class="sxs-lookup"><span data-stu-id="06d28-121">EsentSPAvailExtCacheOutOfMemoryException members</span></span>](./esentspavailextcacheoutofmemoryexception-members.md)

[<span data-ttu-id="06d28-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="06d28-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
