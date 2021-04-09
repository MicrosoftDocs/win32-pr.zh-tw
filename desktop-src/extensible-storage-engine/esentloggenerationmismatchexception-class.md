---
description: 深入瞭解： EsentLogGenerationMismatchException 類別
title: EsentLogGenerationMismatchException 類別
TOCTitle: EsentLogGenerationMismatchException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLogGenerationMismatchException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentloggenerationmismatchexception(v=EXCHG.10)
ms:contentKeyID: 55102125
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLogGenerationMismatchException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLogGenerationMismatchException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0a878330a00147e1d4f24e7882776ad827d97a50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115700"
---
# <a name="esentloggenerationmismatchexception-class"></a><span data-ttu-id="0c3f1-103">EsentLogGenerationMismatchException 類別</span><span class="sxs-lookup"><span data-stu-id="0c3f1-103">EsentLogGenerationMismatchException class</span></span>

<span data-ttu-id="0c3f1-104">JET_err 的基類。LogGenerationMismatch 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="0c3f1-104">Base class for JET_err.LogGenerationMismatch exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="0c3f1-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="0c3f1-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="0c3f1-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="0c3f1-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="0c3f1-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="0c3f1-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="0c3f1-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="0c3f1-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="0c3f1-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="0c3f1-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="0c3f1-110">EsentDataException （.）</span><span class="sxs-lookup"><span data-stu-id="0c3f1-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="0c3f1-111">EsentInconsistentException （.）</span><span class="sxs-lookup"><span data-stu-id="0c3f1-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  
            <span data-ttu-id="0c3f1-112">EsentLogGenerationMismatchException （.）</span><span class="sxs-lookup"><span data-stu-id="0c3f1-112">Microsoft.Isam.Esent.Interop.EsentLogGenerationMismatchException</span></span>  

<span data-ttu-id="0c3f1-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0c3f1-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0c3f1-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="0c3f1-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0c3f1-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c3f1-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLogGenerationMismatchException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentLogGenerationMismatchException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLogGenerationMismatchException : EsentInconsistentException
```

## <a name="thread-safety"></a><span data-ttu-id="0c3f1-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="0c3f1-116">Thread safety</span></span>

<span data-ttu-id="0c3f1-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="0c3f1-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="0c3f1-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="0c3f1-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="0c3f1-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0c3f1-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0c3f1-120">參考</span><span class="sxs-lookup"><span data-stu-id="0c3f1-120">Reference</span></span>

[<span data-ttu-id="0c3f1-121">EsentLogGenerationMismatchException 成員</span><span class="sxs-lookup"><span data-stu-id="0c3f1-121">EsentLogGenerationMismatchException members</span></span>](./esentloggenerationmismatchexception-members.md)

[<span data-ttu-id="0c3f1-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="0c3f1-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
