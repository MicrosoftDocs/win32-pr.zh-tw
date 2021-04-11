---
description: 深入瞭解： Instance 類別
title: Instance 類別
TOCTitle: Instance class
ms:assetid: T:Microsoft.Isam.Esent.Interop.Instance
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance(v=EXCHG.10)
ms:contentKeyID: 55103260
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Instance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Instance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7b717286a9d07b7eb17b87354cbe0896cf182f5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691335"
---
# <a name="instance-class"></a><span data-ttu-id="a0eff-103">Instance 類別</span><span class="sxs-lookup"><span data-stu-id="a0eff-103">Instance class</span></span>

<span data-ttu-id="a0eff-104">封裝可處置物件中之 [JET_INSTANCE](./jet-instance-structure.md) 的類別。</span><span class="sxs-lookup"><span data-stu-id="a0eff-104">A class that encapsulates a [JET_INSTANCE](./jet-instance-structure.md) in a disposable object.</span></span> <span data-ttu-id="a0eff-105">實例必須最後關閉，且關閉實例會釋放實例的所有其他資源。</span><span class="sxs-lookup"><span data-stu-id="a0eff-105">The instance must be closed last and closing the instance releases all other resources for the instance.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="a0eff-106">繼承階層</span><span class="sxs-lookup"><span data-stu-id="a0eff-106">Inheritance hierarchy</span></span>

[<span data-ttu-id="a0eff-107">System.Object</span><span class="sxs-lookup"><span data-stu-id="a0eff-107">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="a0eff-108">System.runtime.constrainedexecution. CriticalFinalizerObject</span><span class="sxs-lookup"><span data-stu-id="a0eff-108">System.Runtime.ConstrainedExecution.CriticalFinalizerObject</span></span>](/dotnet/api/system.runtime.constrainedexecution.criticalfinalizerobject)  
    [<span data-ttu-id="a0eff-109">System.Runtime.InteropServices.SafeHandle</span><span class="sxs-lookup"><span data-stu-id="a0eff-109">System.Runtime.InteropServices.SafeHandle</span></span>](/dotnet/api/system.runtime.interopservices.safehandle)  
      [<span data-ttu-id="a0eff-110">Safehandle. SafeHandleZeroOrMinusOneIsInvalid</span><span class="sxs-lookup"><span data-stu-id="a0eff-110">Microsoft.Win32.SafeHandles.SafeHandleZeroOrMinusOneIsInvalid</span></span>](/dotnet/api/microsoft.win32.safehandles.safehandlezeroorminusoneisinvalid)  
        <span data-ttu-id="a0eff-111">Microsoft. Esent 實例</span><span class="sxs-lookup"><span data-stu-id="a0eff-111">Microsoft.Isam.Esent.Interop.Instance</span></span>  

<span data-ttu-id="a0eff-112">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a0eff-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a0eff-113">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="a0eff-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a0eff-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0eff-114">Syntax</span></span>

``` vb
'Declaration
Public Class Instance _
    Inherits SafeHandleZeroOrMinusOneIsInvalid
'Usage
Dim instance As Instance
```

``` csharp
public class Instance : SafeHandleZeroOrMinusOneIsInvalid
```

## <a name="thread-safety"></a><span data-ttu-id="a0eff-115">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="a0eff-115">Thread safety</span></span>

<span data-ttu-id="a0eff-116">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="a0eff-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="a0eff-117">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="a0eff-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="a0eff-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a0eff-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a0eff-119">參考</span><span class="sxs-lookup"><span data-stu-id="a0eff-119">Reference</span></span>

[<span data-ttu-id="a0eff-120">實例成員</span><span class="sxs-lookup"><span data-stu-id="a0eff-120">Instance members</span></span>](./instance-members.md)

[<span data-ttu-id="a0eff-121">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="a0eff-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
