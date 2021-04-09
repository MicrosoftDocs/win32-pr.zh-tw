---
description: 深入瞭解： EsentRecordDeletedException 類別
title: EsentRecordDeletedException 類別
TOCTitle: EsentRecordDeletedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRecordDeletedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrecorddeletedexception(v=EXCHG.10)
ms:contentKeyID: 55107344
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRecordDeletedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRecordDeletedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 61d09fca2e154f0a5c5e9e64b85b6a855c460593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943872"
---
# <a name="esentrecorddeletedexception-class"></a><span data-ttu-id="77979-103">EsentRecordDeletedException 類別</span><span class="sxs-lookup"><span data-stu-id="77979-103">EsentRecordDeletedException class</span></span>

<span data-ttu-id="77979-104">JET_err 的基類。RecordDeleted 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="77979-104">Base class for JET_err.RecordDeleted exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="77979-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="77979-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="77979-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="77979-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="77979-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="77979-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="77979-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="77979-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="77979-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="77979-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="77979-110">EsentApiException （.）</span><span class="sxs-lookup"><span data-stu-id="77979-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="77979-111">EsentStateException （.）</span><span class="sxs-lookup"><span data-stu-id="77979-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="77979-112">EsentRecordDeletedException （.）</span><span class="sxs-lookup"><span data-stu-id="77979-112">Microsoft.Isam.Esent.Interop.EsentRecordDeletedException</span></span>  

<span data-ttu-id="77979-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="77979-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="77979-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="77979-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="77979-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="77979-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRecordDeletedException _
    Inherits EsentStateException
'Usage
Dim instance As EsentRecordDeletedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRecordDeletedException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="77979-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="77979-116">Thread safety</span></span>

<span data-ttu-id="77979-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="77979-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="77979-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="77979-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="77979-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="77979-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="77979-120">參考</span><span class="sxs-lookup"><span data-stu-id="77979-120">Reference</span></span>

[<span data-ttu-id="77979-121">EsentRecordDeletedException 成員</span><span class="sxs-lookup"><span data-stu-id="77979-121">EsentRecordDeletedException members</span></span>](./esentrecorddeletedexception-members.md)

[<span data-ttu-id="77979-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="77979-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
