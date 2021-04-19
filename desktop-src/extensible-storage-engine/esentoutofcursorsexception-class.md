---
description: 深入瞭解： EsentOutOfCursorsException 類別
title: EsentOutOfCursorsException 類別
TOCTitle: EsentOutOfCursorsException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOutOfCursorsException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoutofcursorsexception(v=EXCHG.10)
ms:contentKeyID: 55102451
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOutOfCursorsException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOutOfCursorsException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 14bbccde7e986768451c0e42c27527ab572c1660
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106988751"
---
# <a name="esentoutofcursorsexception-class"></a><span data-ttu-id="6b3c6-103">EsentOutOfCursorsException 類別</span><span class="sxs-lookup"><span data-stu-id="6b3c6-103">EsentOutOfCursorsException class</span></span>

<span data-ttu-id="6b3c6-104">JET_err 的基類。OutOfCursors 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="6b3c6-104">Base class for JET_err.OutOfCursors exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="6b3c6-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="6b3c6-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="6b3c6-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="6b3c6-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="6b3c6-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="6b3c6-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="6b3c6-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="6b3c6-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="6b3c6-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="6b3c6-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="6b3c6-110">EsentOperationException （.）</span><span class="sxs-lookup"><span data-stu-id="6b3c6-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="6b3c6-111">EsentResourceException （.）</span><span class="sxs-lookup"><span data-stu-id="6b3c6-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="6b3c6-112">EsentMemoryException （.）</span><span class="sxs-lookup"><span data-stu-id="6b3c6-112">Microsoft.Isam.Esent.Interop.EsentMemoryException</span></span>](./esentmemoryexception-class.md)  
              <span data-ttu-id="6b3c6-113">EsentOutOfCursorsException （.）</span><span class="sxs-lookup"><span data-stu-id="6b3c6-113">Microsoft.Isam.Esent.Interop.EsentOutOfCursorsException</span></span>  

<span data-ttu-id="6b3c6-114">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6b3c6-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6b3c6-115">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="6b3c6-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6b3c6-116">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b3c6-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOutOfCursorsException _
    Inherits EsentMemoryException
'Usage
Dim instance As EsentOutOfCursorsException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOutOfCursorsException : EsentMemoryException
```

## <a name="thread-safety"></a><span data-ttu-id="6b3c6-117">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="6b3c6-117">Thread safety</span></span>

<span data-ttu-id="6b3c6-118">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="6b3c6-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="6b3c6-119">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="6b3c6-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="6b3c6-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6b3c6-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6b3c6-121">參考</span><span class="sxs-lookup"><span data-stu-id="6b3c6-121">Reference</span></span>

[<span data-ttu-id="6b3c6-122">EsentOutOfCursorsException 成員</span><span class="sxs-lookup"><span data-stu-id="6b3c6-122">EsentOutOfCursorsException members</span></span>](./esentoutofcursorsexception-members.md)

[<span data-ttu-id="6b3c6-123">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="6b3c6-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
