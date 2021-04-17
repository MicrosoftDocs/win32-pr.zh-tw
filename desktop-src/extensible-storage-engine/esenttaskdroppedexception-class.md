---
description: 深入瞭解： EsentTaskDroppedException 類別
title: EsentTaskDroppedException 類別
TOCTitle: EsentTaskDroppedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTaskDroppedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttaskdroppedexception(v=EXCHG.10)
ms:contentKeyID: 55103022
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTaskDroppedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTaskDroppedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4770f405ff7ca8875e3e2a960dea846e2f34ff6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513452"
---
# <a name="esenttaskdroppedexception-class"></a><span data-ttu-id="6f7eb-103">EsentTaskDroppedException 類別</span><span class="sxs-lookup"><span data-stu-id="6f7eb-103">EsentTaskDroppedException class</span></span>

<span data-ttu-id="6f7eb-104">JET_err 的基類。TaskDropped 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="6f7eb-104">Base class for JET_err.TaskDropped exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="6f7eb-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="6f7eb-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="6f7eb-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="6f7eb-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="6f7eb-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="6f7eb-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="6f7eb-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="6f7eb-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="6f7eb-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="6f7eb-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="6f7eb-110">EsentOperationException （.）</span><span class="sxs-lookup"><span data-stu-id="6f7eb-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="6f7eb-111">EsentResourceException （.）</span><span class="sxs-lookup"><span data-stu-id="6f7eb-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            <span data-ttu-id="6f7eb-112">EsentTaskDroppedException （.）</span><span class="sxs-lookup"><span data-stu-id="6f7eb-112">Microsoft.Isam.Esent.Interop.EsentTaskDroppedException</span></span>  

<span data-ttu-id="6f7eb-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6f7eb-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6f7eb-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="6f7eb-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6f7eb-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f7eb-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTaskDroppedException _
    Inherits EsentResourceException
'Usage
Dim instance As EsentTaskDroppedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTaskDroppedException : EsentResourceException
```

## <a name="thread-safety"></a><span data-ttu-id="6f7eb-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="6f7eb-116">Thread safety</span></span>

<span data-ttu-id="6f7eb-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="6f7eb-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="6f7eb-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="6f7eb-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="6f7eb-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6f7eb-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6f7eb-120">參考</span><span class="sxs-lookup"><span data-stu-id="6f7eb-120">Reference</span></span>

[<span data-ttu-id="6f7eb-121">EsentTaskDroppedException 成員</span><span class="sxs-lookup"><span data-stu-id="6f7eb-121">EsentTaskDroppedException members</span></span>](./esenttaskdroppedexception-members.md)

[<span data-ttu-id="6f7eb-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="6f7eb-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
