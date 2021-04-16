---
description: 深入瞭解： EsentDiskFullException 類別
title: EsentDiskFullException 類別
TOCTitle: EsentDiskFullException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDiskFullException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdiskfullexception(v=EXCHG.10)
ms:contentKeyID: 55101513
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDiskFullException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDiskFullException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 28c3fb4fa06a6526cf06d0f4822ce3dcb835bad6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320788"
---
# <a name="esentdiskfullexception-class"></a><span data-ttu-id="c5391-103">EsentDiskFullException 類別</span><span class="sxs-lookup"><span data-stu-id="c5391-103">EsentDiskFullException class</span></span>

<span data-ttu-id="c5391-104">JET_err 的基類。DiskFull 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="c5391-104">Base class for JET_err.DiskFull exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="c5391-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="c5391-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="c5391-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="c5391-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="c5391-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="c5391-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="c5391-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="c5391-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="c5391-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="c5391-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="c5391-110">EsentOperationException （.）</span><span class="sxs-lookup"><span data-stu-id="c5391-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="c5391-111">EsentResourceException （.）</span><span class="sxs-lookup"><span data-stu-id="c5391-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="c5391-112">EsentDiskException （.）</span><span class="sxs-lookup"><span data-stu-id="c5391-112">Microsoft.Isam.Esent.Interop.EsentDiskException</span></span>](./esentdiskexception-class.md)  
              <span data-ttu-id="c5391-113">EsentDiskFullException （.）</span><span class="sxs-lookup"><span data-stu-id="c5391-113">Microsoft.Isam.Esent.Interop.EsentDiskFullException</span></span>  

<span data-ttu-id="c5391-114">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c5391-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c5391-115">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="c5391-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c5391-116">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5391-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDiskFullException _
    Inherits EsentDiskException
'Usage
Dim instance As EsentDiskFullException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDiskFullException : EsentDiskException
```

## <a name="thread-safety"></a><span data-ttu-id="c5391-117">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="c5391-117">Thread safety</span></span>

<span data-ttu-id="c5391-118">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="c5391-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="c5391-119">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="c5391-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="c5391-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c5391-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c5391-121">參考</span><span class="sxs-lookup"><span data-stu-id="c5391-121">Reference</span></span>

[<span data-ttu-id="c5391-122">EsentDiskFullException 成員</span><span class="sxs-lookup"><span data-stu-id="c5391-122">EsentDiskFullException members</span></span>](./esentdiskfullexception-members.md)

[<span data-ttu-id="c5391-123">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="c5391-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
