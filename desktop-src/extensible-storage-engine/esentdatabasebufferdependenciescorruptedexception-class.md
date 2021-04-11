---
description: 深入瞭解： EsentDatabaseBufferDependenciesCorruptedException 類別
title: EsentDatabaseBufferDependenciesCorruptedException 類別
TOCTitle: EsentDatabaseBufferDependenciesCorruptedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseBufferDependenciesCorruptedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabasebufferdependenciescorruptedexception(v=EXCHG.10)
ms:contentKeyID: 55101428
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseBufferDependenciesCorruptedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseBufferDependenciesCorruptedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ace9bfb553aaa04d853addd21e23df487fedd8cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944203"
---
# <a name="esentdatabasebufferdependenciescorruptedexception-class"></a><span data-ttu-id="4927e-103">EsentDatabaseBufferDependenciesCorruptedException 類別</span><span class="sxs-lookup"><span data-stu-id="4927e-103">EsentDatabaseBufferDependenciesCorruptedException class</span></span>

<span data-ttu-id="4927e-104">JET_err 的基類。DatabaseBufferDependenciesCorrupted 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="4927e-104">Base class for JET_err.DatabaseBufferDependenciesCorrupted exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="4927e-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="4927e-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="4927e-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="4927e-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="4927e-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="4927e-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="4927e-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="4927e-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="4927e-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="4927e-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="4927e-110">EsentDataException （.）</span><span class="sxs-lookup"><span data-stu-id="4927e-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="4927e-111">EsentCorruptionException （.）</span><span class="sxs-lookup"><span data-stu-id="4927e-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="4927e-112">EsentDatabaseBufferDependenciesCorruptedException （.）</span><span class="sxs-lookup"><span data-stu-id="4927e-112">Microsoft.Isam.Esent.Interop.EsentDatabaseBufferDependenciesCorruptedException</span></span>  

<span data-ttu-id="4927e-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4927e-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4927e-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="4927e-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4927e-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="4927e-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseBufferDependenciesCorruptedException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentDatabaseBufferDependenciesCorruptedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseBufferDependenciesCorruptedException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="4927e-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="4927e-116">Thread safety</span></span>

<span data-ttu-id="4927e-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="4927e-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="4927e-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="4927e-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="4927e-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4927e-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4927e-120">參考</span><span class="sxs-lookup"><span data-stu-id="4927e-120">Reference</span></span>

[<span data-ttu-id="4927e-121">EsentDatabaseBufferDependenciesCorruptedException 成員</span><span class="sxs-lookup"><span data-stu-id="4927e-121">EsentDatabaseBufferDependenciesCorruptedException members</span></span>](./esentdatabasebufferdependenciescorruptedexception-members.md)

[<span data-ttu-id="4927e-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="4927e-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
