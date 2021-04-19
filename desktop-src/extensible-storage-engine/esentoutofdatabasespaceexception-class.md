---
description: 深入瞭解： EsentOutOfDatabaseSpaceException 類別
title: EsentOutOfDatabaseSpaceException 類別
TOCTitle: EsentOutOfDatabaseSpaceException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOutOfDatabaseSpaceException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoutofdatabasespaceexception(v=EXCHG.10)
ms:contentKeyID: 55102410
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOutOfDatabaseSpaceException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOutOfDatabaseSpaceException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ece3a81fa0687299edba0857b15f4c0abc50e403
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969325"
---
# <a name="esentoutofdatabasespaceexception-class"></a><span data-ttu-id="93ec5-103">EsentOutOfDatabaseSpaceException 類別</span><span class="sxs-lookup"><span data-stu-id="93ec5-103">EsentOutOfDatabaseSpaceException class</span></span>

<span data-ttu-id="93ec5-104">JET_err 的基類。OutOfDatabaseSpace 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="93ec5-104">Base class for JET_err.OutOfDatabaseSpace exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="93ec5-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="93ec5-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="93ec5-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="93ec5-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="93ec5-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="93ec5-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="93ec5-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="93ec5-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="93ec5-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="93ec5-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="93ec5-110">EsentOperationException （.）</span><span class="sxs-lookup"><span data-stu-id="93ec5-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="93ec5-111">EsentResourceException （.）</span><span class="sxs-lookup"><span data-stu-id="93ec5-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="93ec5-112">EsentQuotaException （.）</span><span class="sxs-lookup"><span data-stu-id="93ec5-112">Microsoft.Isam.Esent.Interop.EsentQuotaException</span></span>](./esentquotaexception-class.md)  
              <span data-ttu-id="93ec5-113">EsentOutOfDatabaseSpaceException （.）</span><span class="sxs-lookup"><span data-stu-id="93ec5-113">Microsoft.Isam.Esent.Interop.EsentOutOfDatabaseSpaceException</span></span>  

<span data-ttu-id="93ec5-114">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="93ec5-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="93ec5-115">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="93ec5-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="93ec5-116">Syntax</span><span class="sxs-lookup"><span data-stu-id="93ec5-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOutOfDatabaseSpaceException _
    Inherits EsentQuotaException
'Usage
Dim instance As EsentOutOfDatabaseSpaceException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOutOfDatabaseSpaceException : EsentQuotaException
```

## <a name="thread-safety"></a><span data-ttu-id="93ec5-117">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="93ec5-117">Thread safety</span></span>

<span data-ttu-id="93ec5-118">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="93ec5-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="93ec5-119">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="93ec5-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="93ec5-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="93ec5-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="93ec5-121">參考</span><span class="sxs-lookup"><span data-stu-id="93ec5-121">Reference</span></span>

[<span data-ttu-id="93ec5-122">EsentOutOfDatabaseSpaceException 成員</span><span class="sxs-lookup"><span data-stu-id="93ec5-122">EsentOutOfDatabaseSpaceException members</span></span>](./esentoutofdatabasespaceexception-members.md)

[<span data-ttu-id="93ec5-123">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="93ec5-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
