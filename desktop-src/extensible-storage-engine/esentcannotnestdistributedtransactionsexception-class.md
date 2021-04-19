---
description: 深入瞭解： EsentCannotNestDistributedTransactionsException 類別
title: EsentCannotNestDistributedTransactionsException 類別
TOCTitle: EsentCannotNestDistributedTransactionsException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentCannotNestDistributedTransactionsException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcannotnestdistributedtransactionsexception(v=EXCHG.10)
ms:contentKeyID: 55101211
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentCannotNestDistributedTransactionsException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentCannotNestDistributedTransactionsException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 732b0995f75bb02174325489554aff2ece18a7f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106995849"
---
# <a name="esentcannotnestdistributedtransactionsexception-class"></a><span data-ttu-id="b32fc-103">EsentCannotNestDistributedTransactionsException 類別</span><span class="sxs-lookup"><span data-stu-id="b32fc-103">EsentCannotNestDistributedTransactionsException class</span></span>

<span data-ttu-id="b32fc-104">JET_err 的基類。CannotNestDistributedTransactions 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="b32fc-104">Base class for JET_err.CannotNestDistributedTransactions exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="b32fc-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="b32fc-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="b32fc-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="b32fc-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="b32fc-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="b32fc-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="b32fc-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="b32fc-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="b32fc-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="b32fc-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="b32fc-110">EsentApiException （.）</span><span class="sxs-lookup"><span data-stu-id="b32fc-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="b32fc-111">EsentObsoleteException （.）</span><span class="sxs-lookup"><span data-stu-id="b32fc-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="b32fc-112">EsentCannotNestDistributedTransactionsException （.）</span><span class="sxs-lookup"><span data-stu-id="b32fc-112">Microsoft.Isam.Esent.Interop.EsentCannotNestDistributedTransactionsException</span></span>  

<span data-ttu-id="b32fc-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b32fc-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b32fc-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="b32fc-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b32fc-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="b32fc-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentCannotNestDistributedTransactionsException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentCannotNestDistributedTransactionsException
```

``` csharp
[SerializableAttribute]
public sealed class EsentCannotNestDistributedTransactionsException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="b32fc-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="b32fc-116">Thread safety</span></span>

<span data-ttu-id="b32fc-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="b32fc-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="b32fc-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="b32fc-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="b32fc-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b32fc-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b32fc-120">參考</span><span class="sxs-lookup"><span data-stu-id="b32fc-120">Reference</span></span>

[<span data-ttu-id="b32fc-121">EsentCannotNestDistributedTransactionsException 成員</span><span class="sxs-lookup"><span data-stu-id="b32fc-121">EsentCannotNestDistributedTransactionsException members</span></span>](./esentcannotnestdistributedtransactionsexception-members.md)

[<span data-ttu-id="b32fc-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="b32fc-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
