---
description: 深入瞭解： EsentDistributedTransactionNotYetPreparedToCommitException 類別
title: EsentDistributedTransactionNotYetPreparedToCommitException 類別
TOCTitle: EsentDistributedTransactionNotYetPreparedToCommitException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDistributedTransactionNotYetPreparedToCommitException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdistributedtransactionnotyetpreparedtocommitexception(v=EXCHG.10)
ms:contentKeyID: 55101626
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDistributedTransactionNotYetPreparedToCommitException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDistributedTransactionNotYetPreparedToCommitException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bc118aa601559677c4b93025b9f39275b12bd89d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849397"
---
# <a name="esentdistributedtransactionnotyetpreparedtocommitexception-class"></a><span data-ttu-id="3d9a8-103">EsentDistributedTransactionNotYetPreparedToCommitException 類別</span><span class="sxs-lookup"><span data-stu-id="3d9a8-103">EsentDistributedTransactionNotYetPreparedToCommitException class</span></span>

<span data-ttu-id="3d9a8-104">JET_err 的基類。DistributedTransactionNotYetPreparedToCommit 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="3d9a8-104">Base class for JET_err.DistributedTransactionNotYetPreparedToCommit exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="3d9a8-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="3d9a8-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="3d9a8-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="3d9a8-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="3d9a8-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="3d9a8-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="3d9a8-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="3d9a8-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="3d9a8-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="3d9a8-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="3d9a8-110">EsentApiException （.）</span><span class="sxs-lookup"><span data-stu-id="3d9a8-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="3d9a8-111">EsentObsoleteException （.）</span><span class="sxs-lookup"><span data-stu-id="3d9a8-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="3d9a8-112">EsentDistributedTransactionNotYetPreparedToCommitException （.）</span><span class="sxs-lookup"><span data-stu-id="3d9a8-112">Microsoft.Isam.Esent.Interop.EsentDistributedTransactionNotYetPreparedToCommitException</span></span>  

<span data-ttu-id="3d9a8-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3d9a8-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3d9a8-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="3d9a8-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3d9a8-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d9a8-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDistributedTransactionNotYetPreparedToCommitException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentDistributedTransactionNotYetPreparedToCommitException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDistributedTransactionNotYetPreparedToCommitException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="3d9a8-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="3d9a8-116">Thread safety</span></span>

<span data-ttu-id="3d9a8-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="3d9a8-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="3d9a8-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="3d9a8-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="3d9a8-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3d9a8-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3d9a8-120">參考</span><span class="sxs-lookup"><span data-stu-id="3d9a8-120">Reference</span></span>

[<span data-ttu-id="3d9a8-121">EsentDistributedTransactionNotYetPreparedToCommitException 成員</span><span class="sxs-lookup"><span data-stu-id="3d9a8-121">EsentDistributedTransactionNotYetPreparedToCommitException members</span></span>](./esentdistributedtransactionnotyetpreparedtocommitexception-members.md)

[<span data-ttu-id="3d9a8-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="3d9a8-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
