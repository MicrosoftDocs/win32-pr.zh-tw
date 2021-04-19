---
description: 深入瞭解： EsentAttachedDatabaseMismatchException 類別
title: EsentAttachedDatabaseMismatchException 類別
TOCTitle: EsentAttachedDatabaseMismatchException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentAttachedDatabaseMismatchException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentattacheddatabasemismatchexception(v=EXCHG.10)
ms:contentKeyID: 55101019
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentAttachedDatabaseMismatchException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentAttachedDatabaseMismatchException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8fca9c0dcb7526df0373cbf26099a8ca810ab3eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971156"
---
# <a name="esentattacheddatabasemismatchexception-class"></a><span data-ttu-id="10a88-103">EsentAttachedDatabaseMismatchException 類別</span><span class="sxs-lookup"><span data-stu-id="10a88-103">EsentAttachedDatabaseMismatchException class</span></span>

<span data-ttu-id="10a88-104">JET_err 的基類。AttachedDatabaseMismatch 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="10a88-104">Base class for JET_err.AttachedDatabaseMismatch exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="10a88-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="10a88-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="10a88-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="10a88-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="10a88-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="10a88-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="10a88-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="10a88-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="10a88-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="10a88-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="10a88-110">EsentDataException （.）</span><span class="sxs-lookup"><span data-stu-id="10a88-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="10a88-111">EsentInconsistentException （.）</span><span class="sxs-lookup"><span data-stu-id="10a88-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  
            <span data-ttu-id="10a88-112">EsentAttachedDatabaseMismatchException （.）</span><span class="sxs-lookup"><span data-stu-id="10a88-112">Microsoft.Isam.Esent.Interop.EsentAttachedDatabaseMismatchException</span></span>  

<span data-ttu-id="10a88-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="10a88-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="10a88-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="10a88-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="10a88-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="10a88-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentAttachedDatabaseMismatchException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentAttachedDatabaseMismatchException
```

``` csharp
[SerializableAttribute]
public sealed class EsentAttachedDatabaseMismatchException : EsentInconsistentException
```

## <a name="thread-safety"></a><span data-ttu-id="10a88-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="10a88-116">Thread safety</span></span>

<span data-ttu-id="10a88-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="10a88-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="10a88-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="10a88-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="10a88-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10a88-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="10a88-120">參考</span><span class="sxs-lookup"><span data-stu-id="10a88-120">Reference</span></span>

[<span data-ttu-id="10a88-121">EsentAttachedDatabaseMismatchException 成員</span><span class="sxs-lookup"><span data-stu-id="10a88-121">EsentAttachedDatabaseMismatchException members</span></span>](./esentattacheddatabasemismatchexception-members.md)

[<span data-ttu-id="10a88-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="10a88-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
