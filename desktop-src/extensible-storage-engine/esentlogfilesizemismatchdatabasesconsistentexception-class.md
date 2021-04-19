---
description: 深入瞭解： EsentLogFileSizeMismatchDatabasesConsistentException 類別
title: EsentLogFileSizeMismatchDatabasesConsistentException 類別
TOCTitle: EsentLogFileSizeMismatchDatabasesConsistentException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLogFileSizeMismatchDatabasesConsistentException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlogfilesizemismatchdatabasesconsistentexception(v=EXCHG.10)
ms:contentKeyID: 55102114
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLogFileSizeMismatchDatabasesConsistentException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLogFileSizeMismatchDatabasesConsistentException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: be10e9d818953c0f2ffcbe2ab5d4b4bc8bcf5c14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984747"
---
# <a name="esentlogfilesizemismatchdatabasesconsistentexception-class"></a><span data-ttu-id="04103-103">EsentLogFileSizeMismatchDatabasesConsistentException 類別</span><span class="sxs-lookup"><span data-stu-id="04103-103">EsentLogFileSizeMismatchDatabasesConsistentException class</span></span>

<span data-ttu-id="04103-104">JET_err 的基類。LogFileSizeMismatchDatabasesConsistent 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="04103-104">Base class for JET_err.LogFileSizeMismatchDatabasesConsistent exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="04103-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="04103-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="04103-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="04103-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="04103-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="04103-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="04103-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="04103-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="04103-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="04103-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="04103-110">EsentApiException （.）</span><span class="sxs-lookup"><span data-stu-id="04103-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="04103-111">EsentStateException （.）</span><span class="sxs-lookup"><span data-stu-id="04103-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="04103-112">EsentLogFileSizeMismatchDatabasesConsistentException （.）</span><span class="sxs-lookup"><span data-stu-id="04103-112">Microsoft.Isam.Esent.Interop.EsentLogFileSizeMismatchDatabasesConsistentException</span></span>  

<span data-ttu-id="04103-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="04103-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="04103-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="04103-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="04103-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="04103-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLogFileSizeMismatchDatabasesConsistentException _
    Inherits EsentStateException
'Usage
Dim instance As EsentLogFileSizeMismatchDatabasesConsistentException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLogFileSizeMismatchDatabasesConsistentException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="04103-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="04103-116">Thread safety</span></span>

<span data-ttu-id="04103-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="04103-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="04103-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="04103-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="04103-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="04103-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="04103-120">參考</span><span class="sxs-lookup"><span data-stu-id="04103-120">Reference</span></span>

[<span data-ttu-id="04103-121">EsentLogFileSizeMismatchDatabasesConsistentException 成員</span><span class="sxs-lookup"><span data-stu-id="04103-121">EsentLogFileSizeMismatchDatabasesConsistentException members</span></span>](./esentlogfilesizemismatchdatabasesconsistentexception-members.md)

[<span data-ttu-id="04103-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="04103-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
