---
description: 深入瞭解： EsentOutOfSessionsException 類別
title: EsentOutOfSessionsException 類別
TOCTitle: EsentOutOfSessionsException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOutOfSessionsException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoutofsessionsexception(v=EXCHG.10)
ms:contentKeyID: 55102494
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOutOfSessionsException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOutOfSessionsException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 70b3c466586551f67f451d8ecc6ad108da52089a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104386219"
---
# <a name="esentoutofsessionsexception-class"></a><span data-ttu-id="e197e-103">EsentOutOfSessionsException 類別</span><span class="sxs-lookup"><span data-stu-id="e197e-103">EsentOutOfSessionsException class</span></span>

<span data-ttu-id="e197e-104">JET_err 的基類。OutOfSessions 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="e197e-104">Base class for JET_err.OutOfSessions exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="e197e-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="e197e-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="e197e-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="e197e-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="e197e-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="e197e-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="e197e-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="e197e-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="e197e-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="e197e-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="e197e-110">EsentOperationException （.）</span><span class="sxs-lookup"><span data-stu-id="e197e-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="e197e-111">EsentResourceException （.）</span><span class="sxs-lookup"><span data-stu-id="e197e-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="e197e-112">EsentMemoryException （.）</span><span class="sxs-lookup"><span data-stu-id="e197e-112">Microsoft.Isam.Esent.Interop.EsentMemoryException</span></span>](./esentmemoryexception-class.md)  
              <span data-ttu-id="e197e-113">EsentOutOfSessionsException （.）</span><span class="sxs-lookup"><span data-stu-id="e197e-113">Microsoft.Isam.Esent.Interop.EsentOutOfSessionsException</span></span>  

<span data-ttu-id="e197e-114">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e197e-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e197e-115">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="e197e-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e197e-116">Syntax</span><span class="sxs-lookup"><span data-stu-id="e197e-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOutOfSessionsException _
    Inherits EsentMemoryException
'Usage
Dim instance As EsentOutOfSessionsException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOutOfSessionsException : EsentMemoryException
```

## <a name="thread-safety"></a><span data-ttu-id="e197e-117">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="e197e-117">Thread safety</span></span>

<span data-ttu-id="e197e-118">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="e197e-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="e197e-119">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="e197e-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="e197e-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e197e-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e197e-121">參考</span><span class="sxs-lookup"><span data-stu-id="e197e-121">Reference</span></span>

[<span data-ttu-id="e197e-122">EsentOutOfSessionsException 成員</span><span class="sxs-lookup"><span data-stu-id="e197e-122">EsentOutOfSessionsException members</span></span>](./esentoutofsessionsexception-members.md)

[<span data-ttu-id="e197e-123">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="e197e-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
