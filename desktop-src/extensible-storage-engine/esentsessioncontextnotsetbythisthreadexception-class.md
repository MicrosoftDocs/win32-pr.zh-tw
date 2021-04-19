---
description: 深入瞭解： EsentSessionCoNtextNotSetByThisThreadException 類別
title: EsentSessionCoNtextNotSetByThisThreadException 類別
TOCTitle: EsentSessionContextNotSetByThisThreadException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentSessionContextNotSetByThisThreadException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentsessioncontextnotsetbythisthreadexception(v=EXCHG.10)
ms:contentKeyID: 55102698
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentSessionContextNotSetByThisThreadException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentSessionContextNotSetByThisThreadException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 097712353336a9a412dd4255781a42c74eac1782
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980012"
---
# <a name="esentsessioncontextnotsetbythisthreadexception-class"></a><span data-ttu-id="c15c4-103">EsentSessionCoNtextNotSetByThisThreadException 類別</span><span class="sxs-lookup"><span data-stu-id="c15c4-103">EsentSessionContextNotSetByThisThreadException class</span></span>

<span data-ttu-id="c15c4-104">JET_err 的基類。SessionCoNtextNotSetByThisThread 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="c15c4-104">Base class for JET_err.SessionContextNotSetByThisThread exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="c15c4-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="c15c4-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="c15c4-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="c15c4-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="c15c4-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="c15c4-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="c15c4-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="c15c4-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="c15c4-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="c15c4-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="c15c4-110">EsentApiException （.）</span><span class="sxs-lookup"><span data-stu-id="c15c4-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="c15c4-111">EsentUsageException （.）</span><span class="sxs-lookup"><span data-stu-id="c15c4-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="c15c4-112">EsentSessionCoNtextNotSetByThisThreadException （.）</span><span class="sxs-lookup"><span data-stu-id="c15c4-112">Microsoft.Isam.Esent.Interop.EsentSessionContextNotSetByThisThreadException</span></span>  

<span data-ttu-id="c15c4-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c15c4-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c15c4-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="c15c4-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c15c4-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="c15c4-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentSessionContextNotSetByThisThreadException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentSessionContextNotSetByThisThreadException
```

``` csharp
[SerializableAttribute]
public sealed class EsentSessionContextNotSetByThisThreadException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="c15c4-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="c15c4-116">Thread safety</span></span>

<span data-ttu-id="c15c4-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="c15c4-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="c15c4-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="c15c4-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="c15c4-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c15c4-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c15c4-120">參考</span><span class="sxs-lookup"><span data-stu-id="c15c4-120">Reference</span></span>

[<span data-ttu-id="c15c4-121">EsentSessionCoNtextNotSetByThisThreadException 成員</span><span class="sxs-lookup"><span data-stu-id="c15c4-121">EsentSessionContextNotSetByThisThreadException members</span></span>](./esentsessioncontextnotsetbythisthreadexception-members.md)

[<span data-ttu-id="c15c4-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="c15c4-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
