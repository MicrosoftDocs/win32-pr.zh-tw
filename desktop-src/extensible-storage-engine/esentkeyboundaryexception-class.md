---
description: 深入瞭解： EsentKeyBoundaryException 類別
title: EsentKeyBoundaryException 類別
TOCTitle: EsentKeyBoundaryException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentKeyBoundaryException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentkeyboundaryexception(v=EXCHG.10)
ms:contentKeyID: 55107283
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentKeyBoundaryException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentKeyBoundaryException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 959c410f9f2f38b722b7517c5324f8d4f98affa1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988495"
---
# <a name="esentkeyboundaryexception-class"></a><span data-ttu-id="db68b-103">EsentKeyBoundaryException 類別</span><span class="sxs-lookup"><span data-stu-id="db68b-103">EsentKeyBoundaryException class</span></span>

<span data-ttu-id="db68b-104">JET_err 的基類。KeyBoundary 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="db68b-104">Base class for JET_err.KeyBoundary exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="db68b-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="db68b-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="db68b-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="db68b-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="db68b-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="db68b-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="db68b-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="db68b-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="db68b-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="db68b-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="db68b-110">EsentApiException （.）</span><span class="sxs-lookup"><span data-stu-id="db68b-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="db68b-111">EsentObsoleteException （.）</span><span class="sxs-lookup"><span data-stu-id="db68b-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="db68b-112">EsentKeyBoundaryException （.）</span><span class="sxs-lookup"><span data-stu-id="db68b-112">Microsoft.Isam.Esent.Interop.EsentKeyBoundaryException</span></span>  

<span data-ttu-id="db68b-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="db68b-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="db68b-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="db68b-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="db68b-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="db68b-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentKeyBoundaryException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentKeyBoundaryException
```

``` csharp
[SerializableAttribute]
public sealed class EsentKeyBoundaryException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="db68b-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="db68b-116">Thread safety</span></span>

<span data-ttu-id="db68b-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="db68b-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="db68b-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="db68b-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="db68b-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="db68b-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="db68b-120">參考</span><span class="sxs-lookup"><span data-stu-id="db68b-120">Reference</span></span>

[<span data-ttu-id="db68b-121">EsentKeyBoundaryException 成員</span><span class="sxs-lookup"><span data-stu-id="db68b-121">EsentKeyBoundaryException members</span></span>](./esentkeyboundaryexception-members.md)

[<span data-ttu-id="db68b-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="db68b-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
