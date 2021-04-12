---
description: 深入瞭解： EsentCannotMaterializeForwardOnlySortException 類別
title: EsentCannotMaterializeForwardOnlySortException 類別
TOCTitle: EsentCannotMaterializeForwardOnlySortException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentCannotMaterializeForwardOnlySortException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcannotmaterializeforwardonlysortexception(v=EXCHG.10)
ms:contentKeyID: 55101164
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentCannotMaterializeForwardOnlySortException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentCannotMaterializeForwardOnlySortException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: af0f56012c462ecb3b82a7b44006e93e0de4d3f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320176"
---
# <a name="esentcannotmaterializeforwardonlysortexception-class"></a><span data-ttu-id="5b80f-103">EsentCannotMaterializeForwardOnlySortException 類別</span><span class="sxs-lookup"><span data-stu-id="5b80f-103">EsentCannotMaterializeForwardOnlySortException class</span></span>

<span data-ttu-id="5b80f-104">JET_err 的基類。CannotMaterializeForwardOnlySort 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="5b80f-104">Base class for JET_err.CannotMaterializeForwardOnlySort exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="5b80f-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="5b80f-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="5b80f-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="5b80f-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="5b80f-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="5b80f-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="5b80f-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="5b80f-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="5b80f-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="5b80f-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="5b80f-110">EsentApiException （.）</span><span class="sxs-lookup"><span data-stu-id="5b80f-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="5b80f-111">EsentUsageException （.）</span><span class="sxs-lookup"><span data-stu-id="5b80f-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="5b80f-112">EsentCannotMaterializeForwardOnlySortException （.）</span><span class="sxs-lookup"><span data-stu-id="5b80f-112">Microsoft.Isam.Esent.Interop.EsentCannotMaterializeForwardOnlySortException</span></span>  

<span data-ttu-id="5b80f-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5b80f-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5b80f-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="5b80f-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5b80f-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b80f-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentCannotMaterializeForwardOnlySortException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentCannotMaterializeForwardOnlySortException
```

``` csharp
[SerializableAttribute]
public sealed class EsentCannotMaterializeForwardOnlySortException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="5b80f-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="5b80f-116">Thread safety</span></span>

<span data-ttu-id="5b80f-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="5b80f-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="5b80f-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="5b80f-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="5b80f-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5b80f-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5b80f-120">參考</span><span class="sxs-lookup"><span data-stu-id="5b80f-120">Reference</span></span>

[<span data-ttu-id="5b80f-121">EsentCannotMaterializeForwardOnlySortException 成員</span><span class="sxs-lookup"><span data-stu-id="5b80f-121">EsentCannotMaterializeForwardOnlySortException members</span></span>](./esentcannotmaterializeforwardonlysortexception-members.md)

[<span data-ttu-id="5b80f-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="5b80f-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
