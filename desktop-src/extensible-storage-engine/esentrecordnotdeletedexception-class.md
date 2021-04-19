---
description: 深入瞭解： EsentRecordNotDeletedException 類別
title: EsentRecordNotDeletedException 類別
TOCTitle: EsentRecordNotDeletedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRecordNotDeletedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrecordnotdeletedexception(v=EXCHG.10)
ms:contentKeyID: 55102578
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRecordNotDeletedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRecordNotDeletedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 70eb38e960b127474415c9b7291e4765719fb7bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970640"
---
# <a name="esentrecordnotdeletedexception-class"></a><span data-ttu-id="c17a6-103">EsentRecordNotDeletedException 類別</span><span class="sxs-lookup"><span data-stu-id="c17a6-103">EsentRecordNotDeletedException class</span></span>

<span data-ttu-id="c17a6-104">JET_err 的基類。RecordNotDeleted 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="c17a6-104">Base class for JET_err.RecordNotDeleted exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="c17a6-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="c17a6-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="c17a6-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="c17a6-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="c17a6-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="c17a6-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="c17a6-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="c17a6-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="c17a6-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="c17a6-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="c17a6-110">EsentOperationException （.）</span><span class="sxs-lookup"><span data-stu-id="c17a6-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          <span data-ttu-id="c17a6-111">EsentRecordNotDeletedException （.）</span><span class="sxs-lookup"><span data-stu-id="c17a6-111">Microsoft.Isam.Esent.Interop.EsentRecordNotDeletedException</span></span>  

<span data-ttu-id="c17a6-112">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c17a6-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c17a6-113">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="c17a6-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c17a6-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="c17a6-114">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRecordNotDeletedException _
    Inherits EsentOperationException
'Usage
Dim instance As EsentRecordNotDeletedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRecordNotDeletedException : EsentOperationException
```

## <a name="thread-safety"></a><span data-ttu-id="c17a6-115">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="c17a6-115">Thread safety</span></span>

<span data-ttu-id="c17a6-116">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="c17a6-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="c17a6-117">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="c17a6-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="c17a6-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c17a6-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c17a6-119">參考</span><span class="sxs-lookup"><span data-stu-id="c17a6-119">Reference</span></span>

[<span data-ttu-id="c17a6-120">EsentRecordNotDeletedException 成員</span><span class="sxs-lookup"><span data-stu-id="c17a6-120">EsentRecordNotDeletedException members</span></span>](./esentrecordnotdeletedexception-members.md)

[<span data-ttu-id="c17a6-121">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="c17a6-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
