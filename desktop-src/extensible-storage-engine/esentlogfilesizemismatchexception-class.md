---
description: 深入瞭解： EsentLogFileSizeMismatchException 類別
title: EsentLogFileSizeMismatchException 類別
TOCTitle: EsentLogFileSizeMismatchException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLogFileSizeMismatchException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlogfilesizemismatchexception(v=EXCHG.10)
ms:contentKeyID: 55102188
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLogFileSizeMismatchException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLogFileSizeMismatchException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9ba56300f5815d9a6f79bb3b36f36ae357374c58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983731"
---
# <a name="esentlogfilesizemismatchexception-class"></a><span data-ttu-id="76fac-103">EsentLogFileSizeMismatchException 類別</span><span class="sxs-lookup"><span data-stu-id="76fac-103">EsentLogFileSizeMismatchException class</span></span>

<span data-ttu-id="76fac-104">JET_err 的基類。LogFileSizeMismatch 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="76fac-104">Base class for JET_err.LogFileSizeMismatch exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="76fac-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="76fac-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="76fac-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="76fac-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="76fac-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="76fac-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="76fac-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="76fac-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="76fac-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="76fac-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="76fac-110">EsentApiException （.）</span><span class="sxs-lookup"><span data-stu-id="76fac-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="76fac-111">EsentUsageException （.）</span><span class="sxs-lookup"><span data-stu-id="76fac-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="76fac-112">EsentLogFileSizeMismatchException （.）</span><span class="sxs-lookup"><span data-stu-id="76fac-112">Microsoft.Isam.Esent.Interop.EsentLogFileSizeMismatchException</span></span>  

<span data-ttu-id="76fac-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="76fac-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="76fac-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="76fac-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="76fac-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="76fac-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLogFileSizeMismatchException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentLogFileSizeMismatchException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLogFileSizeMismatchException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="76fac-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="76fac-116">Thread safety</span></span>

<span data-ttu-id="76fac-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="76fac-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="76fac-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="76fac-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="76fac-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="76fac-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="76fac-120">參考</span><span class="sxs-lookup"><span data-stu-id="76fac-120">Reference</span></span>

[<span data-ttu-id="76fac-121">EsentLogFileSizeMismatchException 成員</span><span class="sxs-lookup"><span data-stu-id="76fac-121">EsentLogFileSizeMismatchException members</span></span>](./esentlogfilesizemismatchexception-members.md)

[<span data-ttu-id="76fac-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="76fac-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
