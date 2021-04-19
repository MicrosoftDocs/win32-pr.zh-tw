---
description: 深入瞭解： EsentVersionStoreOutOfMemoryAndCleanupTimedOutException 類別
title: EsentVersionStoreOutOfMemoryAndCleanupTimedOutException 類別
TOCTitle: EsentVersionStoreOutOfMemoryAndCleanupTimedOutException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentVersionStoreOutOfMemoryAndCleanupTimedOutException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentversionstoreoutofmemoryandcleanuptimedoutexception(v=EXCHG.10)
ms:contentKeyID: 55103240
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentVersionStoreOutOfMemoryAndCleanupTimedOutException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentVersionStoreOutOfMemoryAndCleanupTimedOutException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 58cfb5343bd4de471dc73cb0fa5a57729dde5b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983695"
---
# <a name="esentversionstoreoutofmemoryandcleanuptimedoutexception-class"></a><span data-ttu-id="e5e92-103">EsentVersionStoreOutOfMemoryAndCleanupTimedOutException 類別</span><span class="sxs-lookup"><span data-stu-id="e5e92-103">EsentVersionStoreOutOfMemoryAndCleanupTimedOutException class</span></span>

<span data-ttu-id="e5e92-104">JET_err 的基類。VersionStoreOutOfMemoryAndCleanupTimedOut 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="e5e92-104">Base class for JET_err.VersionStoreOutOfMemoryAndCleanupTimedOut exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="e5e92-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="e5e92-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="e5e92-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="e5e92-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="e5e92-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="e5e92-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="e5e92-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="e5e92-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="e5e92-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="e5e92-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="e5e92-110">EsentApiException （.）</span><span class="sxs-lookup"><span data-stu-id="e5e92-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="e5e92-111">EsentUsageException （.）</span><span class="sxs-lookup"><span data-stu-id="e5e92-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="e5e92-112">EsentVersionStoreOutOfMemoryAndCleanupTimedOutException （.）</span><span class="sxs-lookup"><span data-stu-id="e5e92-112">Microsoft.Isam.Esent.Interop.EsentVersionStoreOutOfMemoryAndCleanupTimedOutException</span></span>  

<span data-ttu-id="e5e92-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e5e92-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e5e92-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="e5e92-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e5e92-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5e92-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentVersionStoreOutOfMemoryAndCleanupTimedOutException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentVersionStoreOutOfMemoryAndCleanupTimedOutException
```

``` csharp
[SerializableAttribute]
public sealed class EsentVersionStoreOutOfMemoryAndCleanupTimedOutException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="e5e92-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="e5e92-116">Thread safety</span></span>

<span data-ttu-id="e5e92-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="e5e92-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="e5e92-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="e5e92-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="e5e92-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e5e92-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e5e92-120">參考</span><span class="sxs-lookup"><span data-stu-id="e5e92-120">Reference</span></span>

[<span data-ttu-id="e5e92-121">EsentVersionStoreOutOfMemoryAndCleanupTimedOutException 成員</span><span class="sxs-lookup"><span data-stu-id="e5e92-121">EsentVersionStoreOutOfMemoryAndCleanupTimedOutException members</span></span>](./esentversionstoreoutofmemoryandcleanuptimedoutexception-members.md)

[<span data-ttu-id="e5e92-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="e5e92-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
