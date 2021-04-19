---
description: 深入瞭解： EsentInvalidOnSortException 類別
title: EsentInvalidOnSortException 類別
TOCTitle: EsentInvalidOnSortException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidOnSortException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidonsortexception(v=EXCHG.10)
ms:contentKeyID: 55102006
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidOnSortException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidOnSortException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a44245c7a087e748702debb8fd99aa7ef49f5023
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980095"
---
# <a name="esentinvalidonsortexception-class"></a><span data-ttu-id="ae835-103">EsentInvalidOnSortException 類別</span><span class="sxs-lookup"><span data-stu-id="ae835-103">EsentInvalidOnSortException class</span></span>

<span data-ttu-id="ae835-104">JET_err 的基類。InvalidOnSort 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="ae835-104">Base class for JET_err.InvalidOnSort exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="ae835-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="ae835-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="ae835-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="ae835-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="ae835-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="ae835-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="ae835-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="ae835-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="ae835-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="ae835-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="ae835-110">EsentApiException （.）</span><span class="sxs-lookup"><span data-stu-id="ae835-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="ae835-111">EsentObsoleteException （.）</span><span class="sxs-lookup"><span data-stu-id="ae835-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="ae835-112">EsentInvalidOnSortException （.）</span><span class="sxs-lookup"><span data-stu-id="ae835-112">Microsoft.Isam.Esent.Interop.EsentInvalidOnSortException</span></span>  

<span data-ttu-id="ae835-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ae835-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ae835-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="ae835-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ae835-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae835-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidOnSortException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentInvalidOnSortException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidOnSortException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="ae835-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="ae835-116">Thread safety</span></span>

<span data-ttu-id="ae835-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="ae835-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="ae835-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="ae835-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="ae835-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ae835-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ae835-120">參考</span><span class="sxs-lookup"><span data-stu-id="ae835-120">Reference</span></span>

[<span data-ttu-id="ae835-121">EsentInvalidOnSortException 成員</span><span class="sxs-lookup"><span data-stu-id="ae835-121">EsentInvalidOnSortException members</span></span>](./esentinvalidonsortexception-members.md)

[<span data-ttu-id="ae835-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="ae835-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
