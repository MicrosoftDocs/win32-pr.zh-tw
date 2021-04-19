---
description: 深入瞭解： EsentDatabasesNotFromSameSnapshotException 類別
title: EsentDatabasesNotFromSameSnapshotException 類別
TOCTitle: EsentDatabasesNotFromSameSnapshotException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabasesNotFromSameSnapshotException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabasesnotfromsamesnapshotexception(v=EXCHG.10)
ms:contentKeyID: 55101443
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabasesNotFromSameSnapshotException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabasesNotFromSameSnapshotException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e6d26ecdab73517d1634bc6beb79dfc1249a2756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986829"
---
# <a name="esentdatabasesnotfromsamesnapshotexception-class"></a><span data-ttu-id="1cae1-103">EsentDatabasesNotFromSameSnapshotException 類別</span><span class="sxs-lookup"><span data-stu-id="1cae1-103">EsentDatabasesNotFromSameSnapshotException class</span></span>

<span data-ttu-id="1cae1-104">JET_err 的基類。DatabasesNotFromSameSnapshot 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="1cae1-104">Base class for JET_err.DatabasesNotFromSameSnapshot exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="1cae1-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="1cae1-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="1cae1-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="1cae1-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="1cae1-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="1cae1-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="1cae1-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="1cae1-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="1cae1-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="1cae1-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="1cae1-110">EsentApiException （.）</span><span class="sxs-lookup"><span data-stu-id="1cae1-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="1cae1-111">EsentObsoleteException （.）</span><span class="sxs-lookup"><span data-stu-id="1cae1-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="1cae1-112">EsentDatabasesNotFromSameSnapshotException （.）</span><span class="sxs-lookup"><span data-stu-id="1cae1-112">Microsoft.Isam.Esent.Interop.EsentDatabasesNotFromSameSnapshotException</span></span>  

<span data-ttu-id="1cae1-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1cae1-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1cae1-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="1cae1-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1cae1-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="1cae1-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabasesNotFromSameSnapshotException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentDatabasesNotFromSameSnapshotException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabasesNotFromSameSnapshotException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="1cae1-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="1cae1-116">Thread safety</span></span>

<span data-ttu-id="1cae1-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="1cae1-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="1cae1-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="1cae1-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="1cae1-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1cae1-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1cae1-120">參考</span><span class="sxs-lookup"><span data-stu-id="1cae1-120">Reference</span></span>

[<span data-ttu-id="1cae1-121">EsentDatabasesNotFromSameSnapshotException 成員</span><span class="sxs-lookup"><span data-stu-id="1cae1-121">EsentDatabasesNotFromSameSnapshotException members</span></span>](./esentdatabasesnotfromsamesnapshotexception-members.md)

[<span data-ttu-id="1cae1-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="1cae1-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
