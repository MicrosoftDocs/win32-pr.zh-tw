---
description: 深入瞭解： EsentRecoveryVerifyFailureException 類別
title: EsentRecoveryVerifyFailureException 類別
TOCTitle: EsentRecoveryVerifyFailureException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRecoveryVerifyFailureException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrecoveryverifyfailureexception(v=EXCHG.10)
ms:contentKeyID: 55102574
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRecoveryVerifyFailureException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRecoveryVerifyFailureException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ad3a052a4d2891a25e5b3ecce11d8f45f89a2292
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970385"
---
# <a name="esentrecoveryverifyfailureexception-class"></a><span data-ttu-id="c9f77-103">EsentRecoveryVerifyFailureException 類別</span><span class="sxs-lookup"><span data-stu-id="c9f77-103">EsentRecoveryVerifyFailureException class</span></span>

<span data-ttu-id="c9f77-104">JET_err 的基類。RecoveryVerifyFailure 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="c9f77-104">Base class for JET_err.RecoveryVerifyFailure exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="c9f77-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="c9f77-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="c9f77-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="c9f77-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="c9f77-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="c9f77-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="c9f77-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="c9f77-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="c9f77-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="c9f77-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="c9f77-110">EsentDataException （.）</span><span class="sxs-lookup"><span data-stu-id="c9f77-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="c9f77-111">EsentCorruptionException （.）</span><span class="sxs-lookup"><span data-stu-id="c9f77-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="c9f77-112">EsentRecoveryVerifyFailureException （.）</span><span class="sxs-lookup"><span data-stu-id="c9f77-112">Microsoft.Isam.Esent.Interop.EsentRecoveryVerifyFailureException</span></span>  

<span data-ttu-id="c9f77-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c9f77-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c9f77-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="c9f77-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c9f77-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9f77-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRecoveryVerifyFailureException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentRecoveryVerifyFailureException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRecoveryVerifyFailureException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="c9f77-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="c9f77-116">Thread safety</span></span>

<span data-ttu-id="c9f77-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="c9f77-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="c9f77-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="c9f77-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="c9f77-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c9f77-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c9f77-120">參考</span><span class="sxs-lookup"><span data-stu-id="c9f77-120">Reference</span></span>

[<span data-ttu-id="c9f77-121">EsentRecoveryVerifyFailureException 成員</span><span class="sxs-lookup"><span data-stu-id="c9f77-121">EsentRecoveryVerifyFailureException members</span></span>](./esentrecoveryverifyfailureexception-members.md)

[<span data-ttu-id="c9f77-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="c9f77-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
