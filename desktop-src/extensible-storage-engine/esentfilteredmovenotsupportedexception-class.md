---
description: 深入瞭解： EsentFilteredMoveNotSupportedException 類別
title: EsentFilteredMoveNotSupportedException 類別
TOCTitle: EsentFilteredMoveNotSupportedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFilteredMoveNotSupportedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfilteredmovenotsupportedexception(v=EXCHG.10)
ms:contentKeyID: 55107268
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFilteredMoveNotSupportedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFilteredMoveNotSupportedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d40bb0fdcccb5d630ad9d9011c3c0ed414d93f9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026309"
---
# <a name="esentfilteredmovenotsupportedexception-class"></a><span data-ttu-id="b96e7-103">EsentFilteredMoveNotSupportedException 類別</span><span class="sxs-lookup"><span data-stu-id="b96e7-103">EsentFilteredMoveNotSupportedException class</span></span>

<span data-ttu-id="b96e7-104">JET_err 的基類。FilteredMoveNotSupported 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="b96e7-104">Base class for JET_err.FilteredMoveNotSupported exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="b96e7-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="b96e7-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="b96e7-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="b96e7-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="b96e7-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="b96e7-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="b96e7-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="b96e7-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="b96e7-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="b96e7-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="b96e7-110">EsentApiException （.）</span><span class="sxs-lookup"><span data-stu-id="b96e7-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="b96e7-111">EsentUsageException （.）</span><span class="sxs-lookup"><span data-stu-id="b96e7-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="b96e7-112">EsentFilteredMoveNotSupportedException （.）</span><span class="sxs-lookup"><span data-stu-id="b96e7-112">Microsoft.Isam.Esent.Interop.EsentFilteredMoveNotSupportedException</span></span>  

<span data-ttu-id="b96e7-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b96e7-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b96e7-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="b96e7-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b96e7-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="b96e7-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentFilteredMoveNotSupportedException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentFilteredMoveNotSupportedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentFilteredMoveNotSupportedException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="b96e7-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="b96e7-116">Thread safety</span></span>

<span data-ttu-id="b96e7-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="b96e7-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="b96e7-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="b96e7-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="b96e7-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b96e7-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b96e7-120">參考</span><span class="sxs-lookup"><span data-stu-id="b96e7-120">Reference</span></span>

[<span data-ttu-id="b96e7-121">EsentFilteredMoveNotSupportedException 成員</span><span class="sxs-lookup"><span data-stu-id="b96e7-121">EsentFilteredMoveNotSupportedException members</span></span>](./esentfilteredmovenotsupportedexception-members.md)

[<span data-ttu-id="b96e7-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="b96e7-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
