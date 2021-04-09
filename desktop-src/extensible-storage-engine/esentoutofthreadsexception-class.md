---
description: 深入瞭解： EsentOutOfThreadsException 類別
title: EsentOutOfThreadsException 類別
TOCTitle: EsentOutOfThreadsException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOutOfThreadsException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoutofthreadsexception(v=EXCHG.10)
ms:contentKeyID: 55102450
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOutOfThreadsException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOutOfThreadsException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 05a1427383a12c286ba37eee6f4ddfcd0b655350
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945380"
---
# <a name="esentoutofthreadsexception-class"></a><span data-ttu-id="4726f-103">EsentOutOfThreadsException 類別</span><span class="sxs-lookup"><span data-stu-id="4726f-103">EsentOutOfThreadsException class</span></span>

<span data-ttu-id="4726f-104">JET_err 的基類。OutOfThreads 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="4726f-104">Base class for JET_err.OutOfThreads exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="4726f-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="4726f-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="4726f-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="4726f-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="4726f-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="4726f-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="4726f-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="4726f-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="4726f-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="4726f-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="4726f-110">EsentOperationException （.）</span><span class="sxs-lookup"><span data-stu-id="4726f-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="4726f-111">EsentResourceException （.）</span><span class="sxs-lookup"><span data-stu-id="4726f-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="4726f-112">EsentMemoryException （.）</span><span class="sxs-lookup"><span data-stu-id="4726f-112">Microsoft.Isam.Esent.Interop.EsentMemoryException</span></span>](./esentmemoryexception-class.md)  
              <span data-ttu-id="4726f-113">EsentOutOfThreadsException （.）</span><span class="sxs-lookup"><span data-stu-id="4726f-113">Microsoft.Isam.Esent.Interop.EsentOutOfThreadsException</span></span>  

<span data-ttu-id="4726f-114">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4726f-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4726f-115">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="4726f-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4726f-116">Syntax</span><span class="sxs-lookup"><span data-stu-id="4726f-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOutOfThreadsException _
    Inherits EsentMemoryException
'Usage
Dim instance As EsentOutOfThreadsException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOutOfThreadsException : EsentMemoryException
```

## <a name="thread-safety"></a><span data-ttu-id="4726f-117">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="4726f-117">Thread safety</span></span>

<span data-ttu-id="4726f-118">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="4726f-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="4726f-119">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="4726f-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="4726f-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4726f-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4726f-121">參考</span><span class="sxs-lookup"><span data-stu-id="4726f-121">Reference</span></span>

[<span data-ttu-id="4726f-122">EsentOutOfThreadsException 成員</span><span class="sxs-lookup"><span data-stu-id="4726f-122">EsentOutOfThreadsException members</span></span>](./esentoutofthreadsexception-members.md)

[<span data-ttu-id="4726f-123">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="4726f-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
