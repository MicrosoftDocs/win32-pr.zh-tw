---
description: 深入瞭解： EsentIndexBuildCorruptedException 類別
title: EsentIndexBuildCorruptedException 類別
TOCTitle: EsentIndexBuildCorruptedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentIndexBuildCorruptedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentindexbuildcorruptedexception(v=EXCHG.10)
ms:contentKeyID: 55101803
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentIndexBuildCorruptedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentIndexBuildCorruptedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a4dc01c34f1e40d1f822ca21d3792984a07d0b62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103853055"
---
# <a name="esentindexbuildcorruptedexception-class"></a><span data-ttu-id="88673-103">EsentIndexBuildCorruptedException 類別</span><span class="sxs-lookup"><span data-stu-id="88673-103">EsentIndexBuildCorruptedException class</span></span>

<span data-ttu-id="88673-104">JET_err 的基類。IndexBuildCorrupted 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="88673-104">Base class for JET_err.IndexBuildCorrupted exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="88673-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="88673-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="88673-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="88673-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="88673-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="88673-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="88673-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="88673-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="88673-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="88673-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="88673-110">EsentDataException （.）</span><span class="sxs-lookup"><span data-stu-id="88673-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="88673-111">EsentCorruptionException （.）</span><span class="sxs-lookup"><span data-stu-id="88673-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="88673-112">EsentIndexBuildCorruptedException （.）</span><span class="sxs-lookup"><span data-stu-id="88673-112">Microsoft.Isam.Esent.Interop.EsentIndexBuildCorruptedException</span></span>  

<span data-ttu-id="88673-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="88673-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="88673-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="88673-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="88673-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="88673-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentIndexBuildCorruptedException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentIndexBuildCorruptedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentIndexBuildCorruptedException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="88673-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="88673-116">Thread safety</span></span>

<span data-ttu-id="88673-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="88673-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="88673-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="88673-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="88673-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="88673-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="88673-120">參考</span><span class="sxs-lookup"><span data-stu-id="88673-120">Reference</span></span>

[<span data-ttu-id="88673-121">EsentIndexBuildCorruptedException 成員</span><span class="sxs-lookup"><span data-stu-id="88673-121">EsentIndexBuildCorruptedException members</span></span>](./esentindexbuildcorruptedexception-members.md)

[<span data-ttu-id="88673-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="88673-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
