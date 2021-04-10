---
description: 深入瞭解： EsentSessionSharingViolationException 類別
title: EsentSessionSharingViolationException 類別
TOCTitle: EsentSessionSharingViolationException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentSessionSharingViolationException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentsessionsharingviolationexception(v=EXCHG.10)
ms:contentKeyID: 55102713
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentSessionSharingViolationException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentSessionSharingViolationException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1303792b8d45ec169211c1e176d913db682c850b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945473"
---
# <a name="esentsessionsharingviolationexception-class"></a><span data-ttu-id="61a5e-103">EsentSessionSharingViolationException 類別</span><span class="sxs-lookup"><span data-stu-id="61a5e-103">EsentSessionSharingViolationException class</span></span>

<span data-ttu-id="61a5e-104">JET_err 的基類。SessionSharingViolation 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="61a5e-104">Base class for JET_err.SessionSharingViolation exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="61a5e-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="61a5e-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="61a5e-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="61a5e-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="61a5e-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="61a5e-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="61a5e-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="61a5e-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="61a5e-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="61a5e-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="61a5e-110">EsentApiException （.）</span><span class="sxs-lookup"><span data-stu-id="61a5e-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="61a5e-111">EsentUsageException （.）</span><span class="sxs-lookup"><span data-stu-id="61a5e-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="61a5e-112">EsentSessionSharingViolationException （.）</span><span class="sxs-lookup"><span data-stu-id="61a5e-112">Microsoft.Isam.Esent.Interop.EsentSessionSharingViolationException</span></span>  

<span data-ttu-id="61a5e-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="61a5e-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="61a5e-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="61a5e-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="61a5e-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="61a5e-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentSessionSharingViolationException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentSessionSharingViolationException
```

``` csharp
[SerializableAttribute]
public sealed class EsentSessionSharingViolationException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="61a5e-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="61a5e-116">Thread safety</span></span>

<span data-ttu-id="61a5e-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="61a5e-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="61a5e-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="61a5e-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="61a5e-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="61a5e-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="61a5e-120">參考</span><span class="sxs-lookup"><span data-stu-id="61a5e-120">Reference</span></span>

[<span data-ttu-id="61a5e-121">EsentSessionSharingViolationException 成員</span><span class="sxs-lookup"><span data-stu-id="61a5e-121">EsentSessionSharingViolationException members</span></span>](./esentsessionsharingviolationexception-members.md)

[<span data-ttu-id="61a5e-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="61a5e-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
