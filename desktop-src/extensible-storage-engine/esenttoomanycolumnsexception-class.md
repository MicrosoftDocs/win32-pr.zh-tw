---
description: 深入瞭解： EsentTooManyColumnsException 類別
title: EsentTooManyColumnsException 類別
TOCTitle: EsentTooManyColumnsException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTooManyColumnsException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttoomanycolumnsexception(v=EXCHG.10)
ms:contentKeyID: 55103051
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTooManyColumnsException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTooManyColumnsException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2191abd07aea85dac6275f3c42f34acd13376035
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978346"
---
# <a name="esenttoomanycolumnsexception-class"></a><span data-ttu-id="2860d-103">EsentTooManyColumnsException 類別</span><span class="sxs-lookup"><span data-stu-id="2860d-103">EsentTooManyColumnsException class</span></span>

<span data-ttu-id="2860d-104">JET_err 的基類。TooManyColumns 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="2860d-104">Base class for JET_err.TooManyColumns exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="2860d-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="2860d-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="2860d-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="2860d-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="2860d-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="2860d-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="2860d-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="2860d-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="2860d-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="2860d-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="2860d-110">EsentApiException （.）</span><span class="sxs-lookup"><span data-stu-id="2860d-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="2860d-111">EsentUsageException （.）</span><span class="sxs-lookup"><span data-stu-id="2860d-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="2860d-112">EsentTooManyColumnsException （.）</span><span class="sxs-lookup"><span data-stu-id="2860d-112">Microsoft.Isam.Esent.Interop.EsentTooManyColumnsException</span></span>  

<span data-ttu-id="2860d-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2860d-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2860d-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="2860d-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2860d-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="2860d-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTooManyColumnsException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentTooManyColumnsException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTooManyColumnsException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="2860d-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="2860d-116">Thread safety</span></span>

<span data-ttu-id="2860d-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="2860d-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="2860d-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="2860d-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="2860d-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2860d-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2860d-120">參考</span><span class="sxs-lookup"><span data-stu-id="2860d-120">Reference</span></span>

[<span data-ttu-id="2860d-121">EsentTooManyColumnsException 成員</span><span class="sxs-lookup"><span data-stu-id="2860d-121">EsentTooManyColumnsException members</span></span>](./esenttoomanycolumnsexception-members.md)

[<span data-ttu-id="2860d-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="2860d-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
