---
description: 深入瞭解： EsentDiskException 類別
title: EsentDiskException 類別
TOCTitle: EsentDiskException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDiskException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdiskexception(v=EXCHG.10)
ms:contentKeyID: 55101517
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDiskException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDiskException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 22c2e2e2f829b6fcc6967e6e58692613243549c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104386261"
---
# <a name="esentdiskexception-class"></a><span data-ttu-id="2331a-103">EsentDiskException 類別</span><span class="sxs-lookup"><span data-stu-id="2331a-103">EsentDiskException class</span></span>

<span data-ttu-id="2331a-104">磁片例外狀況的基類。</span><span class="sxs-lookup"><span data-stu-id="2331a-104">Base class for Disk exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="2331a-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="2331a-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="2331a-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="2331a-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="2331a-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="2331a-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="2331a-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="2331a-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="2331a-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="2331a-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="2331a-110">EsentOperationException （.）</span><span class="sxs-lookup"><span data-stu-id="2331a-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="2331a-111">EsentResourceException （.）</span><span class="sxs-lookup"><span data-stu-id="2331a-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            <span data-ttu-id="2331a-112">EsentDiskException （.）</span><span class="sxs-lookup"><span data-stu-id="2331a-112">Microsoft.Isam.Esent.Interop.EsentDiskException</span></span>  
              [<span data-ttu-id="2331a-113">EsentDiskFullException （.）</span><span class="sxs-lookup"><span data-stu-id="2331a-113">Microsoft.Isam.Esent.Interop.EsentDiskFullException</span></span>](./esentdiskfullexception-class.md)  
              [<span data-ttu-id="2331a-114">EsentLogDiskFullException （.）</span><span class="sxs-lookup"><span data-stu-id="2331a-114">Microsoft.Isam.Esent.Interop.EsentLogDiskFullException</span></span>](./esentlogdiskfullexception-class.md)  

<span data-ttu-id="2331a-115">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2331a-115">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2331a-116">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="2331a-116">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2331a-117">Syntax</span><span class="sxs-lookup"><span data-stu-id="2331a-117">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentDiskException _
    Inherits EsentResourceException
'Usage
Dim instance As EsentDiskException
```

``` csharp
[SerializableAttribute]
public abstract class EsentDiskException : EsentResourceException
```

## <a name="thread-safety"></a><span data-ttu-id="2331a-118">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="2331a-118">Thread safety</span></span>

<span data-ttu-id="2331a-119">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="2331a-119">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="2331a-120">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="2331a-120">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="2331a-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2331a-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2331a-122">參考</span><span class="sxs-lookup"><span data-stu-id="2331a-122">Reference</span></span>

[<span data-ttu-id="2331a-123">EsentDiskException 成員</span><span class="sxs-lookup"><span data-stu-id="2331a-123">EsentDiskException members</span></span>](./esentdiskexception-members.md)

[<span data-ttu-id="2331a-124">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="2331a-124">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
