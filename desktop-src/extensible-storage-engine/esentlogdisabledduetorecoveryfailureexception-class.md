---
description: 深入瞭解： EsentLogDisabledDueToRecoveryFailureException 類別
title: EsentLogDisabledDueToRecoveryFailureException 類別
TOCTitle: EsentLogDisabledDueToRecoveryFailureException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLogDisabledDueToRecoveryFailureException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlogdisabledduetorecoveryfailureexception(v=EXCHG.10)
ms:contentKeyID: 55102151
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLogDisabledDueToRecoveryFailureException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLogDisabledDueToRecoveryFailureException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b1a631dc6e0495a958555547f8e7c540263dfc53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945477"
---
# <a name="esentlogdisabledduetorecoveryfailureexception-class"></a><span data-ttu-id="b86b6-103">EsentLogDisabledDueToRecoveryFailureException 類別</span><span class="sxs-lookup"><span data-stu-id="b86b6-103">EsentLogDisabledDueToRecoveryFailureException class</span></span>

<span data-ttu-id="b86b6-104">JET_err 的基類。LogDisabledDueToRecoveryFailure 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="b86b6-104">Base class for JET_err.LogDisabledDueToRecoveryFailure exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="b86b6-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="b86b6-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="b86b6-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="b86b6-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="b86b6-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="b86b6-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="b86b6-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="b86b6-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="b86b6-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="b86b6-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="b86b6-110">EsentOperationException （.）</span><span class="sxs-lookup"><span data-stu-id="b86b6-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="b86b6-111">EsentFatalException （.）</span><span class="sxs-lookup"><span data-stu-id="b86b6-111">Microsoft.Isam.Esent.Interop.EsentFatalException</span></span>](./esentfatalexception-class.md)  
            <span data-ttu-id="b86b6-112">EsentLogDisabledDueToRecoveryFailureException （.）</span><span class="sxs-lookup"><span data-stu-id="b86b6-112">Microsoft.Isam.Esent.Interop.EsentLogDisabledDueToRecoveryFailureException</span></span>  

<span data-ttu-id="b86b6-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b86b6-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b86b6-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="b86b6-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b86b6-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="b86b6-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLogDisabledDueToRecoveryFailureException _
    Inherits EsentFatalException
'Usage
Dim instance As EsentLogDisabledDueToRecoveryFailureException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLogDisabledDueToRecoveryFailureException : EsentFatalException
```

## <a name="thread-safety"></a><span data-ttu-id="b86b6-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="b86b6-116">Thread safety</span></span>

<span data-ttu-id="b86b6-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="b86b6-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="b86b6-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="b86b6-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="b86b6-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b86b6-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b86b6-120">參考</span><span class="sxs-lookup"><span data-stu-id="b86b6-120">Reference</span></span>

[<span data-ttu-id="b86b6-121">EsentLogDisabledDueToRecoveryFailureException 成員</span><span class="sxs-lookup"><span data-stu-id="b86b6-121">EsentLogDisabledDueToRecoveryFailureException members</span></span>](./esentlogdisabledduetorecoveryfailureexception-members.md)

[<span data-ttu-id="b86b6-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="b86b6-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
