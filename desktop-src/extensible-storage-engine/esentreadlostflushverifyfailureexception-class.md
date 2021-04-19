---
description: 深入瞭解： EsentReadLostFlushVerifyFailureException 類別
title: EsentReadLostFlushVerifyFailureException 類別
TOCTitle: EsentReadLostFlushVerifyFailureException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentReadLostFlushVerifyFailureException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentreadlostflushverifyfailureexception(v=EXCHG.10)
ms:contentKeyID: 55102493
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentReadLostFlushVerifyFailureException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentReadLostFlushVerifyFailureException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: deddb54a6d22783270765e11a62070cd559ed2b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989930"
---
# <a name="esentreadlostflushverifyfailureexception-class"></a><span data-ttu-id="fb4d2-103">EsentReadLostFlushVerifyFailureException 類別</span><span class="sxs-lookup"><span data-stu-id="fb4d2-103">EsentReadLostFlushVerifyFailureException class</span></span>

<span data-ttu-id="fb4d2-104">JET_err 的基類。ReadLostFlushVerifyFailure 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="fb4d2-104">Base class for JET_err.ReadLostFlushVerifyFailure exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="fb4d2-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="fb4d2-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="fb4d2-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="fb4d2-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="fb4d2-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="fb4d2-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="fb4d2-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="fb4d2-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="fb4d2-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="fb4d2-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="fb4d2-110">EsentDataException （.）</span><span class="sxs-lookup"><span data-stu-id="fb4d2-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="fb4d2-111">EsentCorruptionException （.）</span><span class="sxs-lookup"><span data-stu-id="fb4d2-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="fb4d2-112">EsentReadLostFlushVerifyFailureException （.）</span><span class="sxs-lookup"><span data-stu-id="fb4d2-112">Microsoft.Isam.Esent.Interop.EsentReadLostFlushVerifyFailureException</span></span>  

<span data-ttu-id="fb4d2-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fb4d2-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="fb4d2-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="fb4d2-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fb4d2-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb4d2-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentReadLostFlushVerifyFailureException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentReadLostFlushVerifyFailureException
```

``` csharp
[SerializableAttribute]
public sealed class EsentReadLostFlushVerifyFailureException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="fb4d2-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="fb4d2-116">Thread safety</span></span>

<span data-ttu-id="fb4d2-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="fb4d2-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="fb4d2-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="fb4d2-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="fb4d2-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fb4d2-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fb4d2-120">參考</span><span class="sxs-lookup"><span data-stu-id="fb4d2-120">Reference</span></span>

[<span data-ttu-id="fb4d2-121">EsentReadLostFlushVerifyFailureException 成員</span><span class="sxs-lookup"><span data-stu-id="fb4d2-121">EsentReadLostFlushVerifyFailureException members</span></span>](./esentreadlostflushverifyfailureexception-members.md)

[<span data-ttu-id="fb4d2-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="fb4d2-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
