---
description: 深入瞭解： EsentLSAlreadySetException 類別
title: EsentLSAlreadySetException 類別
TOCTitle: EsentLSAlreadySetException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLSAlreadySetException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlsalreadysetexception(v=EXCHG.10)
ms:contentKeyID: 55102175
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLSAlreadySetException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLSAlreadySetException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7757740a6c07d6fedaa8b17c7a84755ade4de59b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988363"
---
# <a name="esentlsalreadysetexception-class"></a><span data-ttu-id="b8b45-103">EsentLSAlreadySetException 類別</span><span class="sxs-lookup"><span data-stu-id="b8b45-103">EsentLSAlreadySetException class</span></span>

<span data-ttu-id="b8b45-104">JET_err 的基類。LSAlreadySet 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="b8b45-104">Base class for JET_err.LSAlreadySet exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="b8b45-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="b8b45-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="b8b45-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="b8b45-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="b8b45-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="b8b45-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="b8b45-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="b8b45-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="b8b45-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="b8b45-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="b8b45-110">EsentApiException （.）</span><span class="sxs-lookup"><span data-stu-id="b8b45-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="b8b45-111">EsentUsageException （.）</span><span class="sxs-lookup"><span data-stu-id="b8b45-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="b8b45-112">EsentLSAlreadySetException （.）</span><span class="sxs-lookup"><span data-stu-id="b8b45-112">Microsoft.Isam.Esent.Interop.EsentLSAlreadySetException</span></span>  

<span data-ttu-id="b8b45-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b8b45-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b8b45-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="b8b45-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b8b45-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8b45-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLSAlreadySetException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentLSAlreadySetException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLSAlreadySetException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="b8b45-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="b8b45-116">Thread safety</span></span>

<span data-ttu-id="b8b45-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="b8b45-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="b8b45-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="b8b45-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="b8b45-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b8b45-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b8b45-120">參考</span><span class="sxs-lookup"><span data-stu-id="b8b45-120">Reference</span></span>

[<span data-ttu-id="b8b45-121">EsentLSAlreadySetException 成員</span><span class="sxs-lookup"><span data-stu-id="b8b45-121">EsentLSAlreadySetException members</span></span>](./esentlsalreadysetexception-members.md)

[<span data-ttu-id="b8b45-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="b8b45-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
