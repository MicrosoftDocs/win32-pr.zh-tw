---
description: 深入瞭解： EsentRecoveredWithoutUndoDatabasesConsistentException 類別
title: EsentRecoveredWithoutUndoDatabasesConsistentException 類別
TOCTitle: EsentRecoveredWithoutUndoDatabasesConsistentException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRecoveredWithoutUndoDatabasesConsistentException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrecoveredwithoutundodatabasesconsistentexception(v=EXCHG.10)
ms:contentKeyID: 55102610
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRecoveredWithoutUndoDatabasesConsistentException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRecoveredWithoutUndoDatabasesConsistentException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6e874fb436ae30fe8e393b21d48c560a8ad6e92f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191231"
---
# <a name="esentrecoveredwithoutundodatabasesconsistentexception-class"></a><span data-ttu-id="6e132-103">EsentRecoveredWithoutUndoDatabasesConsistentException 類別</span><span class="sxs-lookup"><span data-stu-id="6e132-103">EsentRecoveredWithoutUndoDatabasesConsistentException class</span></span>

<span data-ttu-id="6e132-104">JET_err 的基類。RecoveredWithoutUndoDatabasesConsistent 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="6e132-104">Base class for JET_err.RecoveredWithoutUndoDatabasesConsistent exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="6e132-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="6e132-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="6e132-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="6e132-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="6e132-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="6e132-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="6e132-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="6e132-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="6e132-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="6e132-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="6e132-110">EsentApiException （.）</span><span class="sxs-lookup"><span data-stu-id="6e132-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="6e132-111">EsentStateException （.）</span><span class="sxs-lookup"><span data-stu-id="6e132-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="6e132-112">EsentRecoveredWithoutUndoDatabasesConsistentException （.）</span><span class="sxs-lookup"><span data-stu-id="6e132-112">Microsoft.Isam.Esent.Interop.EsentRecoveredWithoutUndoDatabasesConsistentException</span></span>  

<span data-ttu-id="6e132-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6e132-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6e132-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="6e132-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6e132-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e132-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRecoveredWithoutUndoDatabasesConsistentException _
    Inherits EsentStateException
'Usage
Dim instance As EsentRecoveredWithoutUndoDatabasesConsistentException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRecoveredWithoutUndoDatabasesConsistentException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="6e132-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="6e132-116">Thread safety</span></span>

<span data-ttu-id="6e132-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="6e132-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="6e132-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="6e132-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="6e132-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6e132-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6e132-120">參考</span><span class="sxs-lookup"><span data-stu-id="6e132-120">Reference</span></span>

[<span data-ttu-id="6e132-121">EsentRecoveredWithoutUndoDatabasesConsistentException 成員</span><span class="sxs-lookup"><span data-stu-id="6e132-121">EsentRecoveredWithoutUndoDatabasesConsistentException members</span></span>](./esentrecoveredwithoutundodatabasesconsistentexception-members.md)

[<span data-ttu-id="6e132-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="6e132-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
