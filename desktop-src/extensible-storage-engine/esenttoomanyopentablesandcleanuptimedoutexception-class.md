---
description: 深入瞭解： EsentTooManyOpenTablesAndCleanupTimedOutException 類別
title: EsentTooManyOpenTablesAndCleanupTimedOutException 類別
TOCTitle: EsentTooManyOpenTablesAndCleanupTimedOutException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTooManyOpenTablesAndCleanupTimedOutException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttoomanyopentablesandcleanuptimedoutexception(v=EXCHG.10)
ms:contentKeyID: 55103109
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTooManyOpenTablesAndCleanupTimedOutException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTooManyOpenTablesAndCleanupTimedOutException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ddfcf7f09a98e62b44265c263fd835cace699e8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997976"
---
# <a name="esenttoomanyopentablesandcleanuptimedoutexception-class"></a><span data-ttu-id="65418-103">EsentTooManyOpenTablesAndCleanupTimedOutException 類別</span><span class="sxs-lookup"><span data-stu-id="65418-103">EsentTooManyOpenTablesAndCleanupTimedOutException class</span></span>

<span data-ttu-id="65418-104">JET_err 的基類。TooManyOpenTablesAndCleanupTimedOut 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="65418-104">Base class for JET_err.TooManyOpenTablesAndCleanupTimedOut exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="65418-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="65418-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="65418-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="65418-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="65418-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="65418-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="65418-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="65418-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="65418-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="65418-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="65418-110">EsentApiException （.）</span><span class="sxs-lookup"><span data-stu-id="65418-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="65418-111">EsentUsageException （.）</span><span class="sxs-lookup"><span data-stu-id="65418-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="65418-112">EsentTooManyOpenTablesAndCleanupTimedOutException （.）</span><span class="sxs-lookup"><span data-stu-id="65418-112">Microsoft.Isam.Esent.Interop.EsentTooManyOpenTablesAndCleanupTimedOutException</span></span>  

<span data-ttu-id="65418-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="65418-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="65418-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="65418-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="65418-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="65418-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTooManyOpenTablesAndCleanupTimedOutException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentTooManyOpenTablesAndCleanupTimedOutException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTooManyOpenTablesAndCleanupTimedOutException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="65418-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="65418-116">Thread safety</span></span>

<span data-ttu-id="65418-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="65418-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="65418-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="65418-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="65418-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="65418-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="65418-120">參考</span><span class="sxs-lookup"><span data-stu-id="65418-120">Reference</span></span>

[<span data-ttu-id="65418-121">EsentTooManyOpenTablesAndCleanupTimedOutException 成員</span><span class="sxs-lookup"><span data-stu-id="65418-121">EsentTooManyOpenTablesAndCleanupTimedOutException members</span></span>](./esenttoomanyopentablesandcleanuptimedoutexception-members.md)

[<span data-ttu-id="65418-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="65418-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
