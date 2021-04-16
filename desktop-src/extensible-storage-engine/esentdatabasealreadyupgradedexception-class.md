---
description: 深入瞭解： EsentDatabaseAlreadyUpgradedException 類別
title: EsentDatabaseAlreadyUpgradedException 類別
TOCTitle: EsentDatabaseAlreadyUpgradedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseAlreadyUpgradedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabasealreadyupgradedexception(v=EXCHG.10)
ms:contentKeyID: 55101322
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseAlreadyUpgradedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseAlreadyUpgradedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 27ad5a37676ef0b8e4a450619c19a45f3bdee1b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514236"
---
# <a name="esentdatabasealreadyupgradedexception-class"></a><span data-ttu-id="12e0e-103">EsentDatabaseAlreadyUpgradedException 類別</span><span class="sxs-lookup"><span data-stu-id="12e0e-103">EsentDatabaseAlreadyUpgradedException class</span></span>

<span data-ttu-id="12e0e-104">JET_err 的基類。DatabaseAlreadyUpgraded 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="12e0e-104">Base class for JET_err.DatabaseAlreadyUpgraded exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="12e0e-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="12e0e-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="12e0e-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="12e0e-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="12e0e-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="12e0e-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="12e0e-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="12e0e-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="12e0e-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="12e0e-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="12e0e-110">EsentApiException （.）</span><span class="sxs-lookup"><span data-stu-id="12e0e-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="12e0e-111">EsentStateException （.）</span><span class="sxs-lookup"><span data-stu-id="12e0e-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="12e0e-112">EsentDatabaseAlreadyUpgradedException （.）</span><span class="sxs-lookup"><span data-stu-id="12e0e-112">Microsoft.Isam.Esent.Interop.EsentDatabaseAlreadyUpgradedException</span></span>  

<span data-ttu-id="12e0e-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="12e0e-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="12e0e-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="12e0e-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="12e0e-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="12e0e-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseAlreadyUpgradedException _
    Inherits EsentStateException
'Usage
Dim instance As EsentDatabaseAlreadyUpgradedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseAlreadyUpgradedException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="12e0e-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="12e0e-116">Thread safety</span></span>

<span data-ttu-id="12e0e-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="12e0e-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="12e0e-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="12e0e-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="12e0e-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="12e0e-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="12e0e-120">參考</span><span class="sxs-lookup"><span data-stu-id="12e0e-120">Reference</span></span>

[<span data-ttu-id="12e0e-121">EsentDatabaseAlreadyUpgradedException 成員</span><span class="sxs-lookup"><span data-stu-id="12e0e-121">EsentDatabaseAlreadyUpgradedException members</span></span>](./esentdatabasealreadyupgradedexception-members.md)

[<span data-ttu-id="12e0e-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="12e0e-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
