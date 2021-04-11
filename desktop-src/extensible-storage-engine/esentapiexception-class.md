---
description: 深入瞭解： EsentApiException 類別
title: EsentApiException 類別
TOCTitle: EsentApiException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentApiException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentapiexception(v=EXCHG.10)
ms:contentKeyID: 55101032
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentApiException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentApiException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b01747d2ecb197ce99617b8c9206d4fada8c2a81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195013"
---
# <a name="esentapiexception-class"></a><span data-ttu-id="e119f-103">EsentApiException 類別</span><span class="sxs-lookup"><span data-stu-id="e119f-103">EsentApiException class</span></span>

<span data-ttu-id="e119f-104">API 例外狀況的基類。</span><span class="sxs-lookup"><span data-stu-id="e119f-104">Base class for API exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="e119f-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="e119f-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="e119f-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="e119f-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="e119f-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="e119f-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="e119f-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="e119f-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="e119f-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="e119f-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        <span data-ttu-id="e119f-110">EsentApiException （.）</span><span class="sxs-lookup"><span data-stu-id="e119f-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>  
          [<span data-ttu-id="e119f-111">EsentObsoleteException （.）</span><span class="sxs-lookup"><span data-stu-id="e119f-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
          [<span data-ttu-id="e119f-112">EsentStateException （.）</span><span class="sxs-lookup"><span data-stu-id="e119f-112">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
          [<span data-ttu-id="e119f-113">EsentUsageException （.）</span><span class="sxs-lookup"><span data-stu-id="e119f-113">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  

<span data-ttu-id="e119f-114">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e119f-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e119f-115">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="e119f-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e119f-116">Syntax</span><span class="sxs-lookup"><span data-stu-id="e119f-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentApiException _
    Inherits EsentErrorException
'Usage
Dim instance As EsentApiException
```

``` csharp
[SerializableAttribute]
public abstract class EsentApiException : EsentErrorException
```

## <a name="thread-safety"></a><span data-ttu-id="e119f-117">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="e119f-117">Thread safety</span></span>

<span data-ttu-id="e119f-118">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="e119f-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="e119f-119">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="e119f-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="e119f-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e119f-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e119f-121">參考</span><span class="sxs-lookup"><span data-stu-id="e119f-121">Reference</span></span>

[<span data-ttu-id="e119f-122">EsentApiException 成員</span><span class="sxs-lookup"><span data-stu-id="e119f-122">EsentApiException members</span></span>](./esentapiexception-members.md)

[<span data-ttu-id="e119f-123">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="e119f-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
