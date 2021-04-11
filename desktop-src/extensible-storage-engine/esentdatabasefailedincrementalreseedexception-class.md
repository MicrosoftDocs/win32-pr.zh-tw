---
description: 深入瞭解： EsentDatabaseFailedIncrementalReseedException 類別
title: EsentDatabaseFailedIncrementalReseedException 類別
TOCTitle: EsentDatabaseFailedIncrementalReseedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseFailedIncrementalReseedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabasefailedincrementalreseedexception(v=EXCHG.10)
ms:contentKeyID: 55101465
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseFailedIncrementalReseedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseFailedIncrementalReseedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cfa0f4a82e3a8936ee3e7a262f8079396b95a54a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113480"
---
# <a name="esentdatabasefailedincrementalreseedexception-class"></a><span data-ttu-id="0656e-103">EsentDatabaseFailedIncrementalReseedException 類別</span><span class="sxs-lookup"><span data-stu-id="0656e-103">EsentDatabaseFailedIncrementalReseedException class</span></span>

<span data-ttu-id="0656e-104">JET_err 的基類。DatabaseFailedIncrementalReseed 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="0656e-104">Base class for JET_err.DatabaseFailedIncrementalReseed exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="0656e-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="0656e-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="0656e-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="0656e-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="0656e-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="0656e-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="0656e-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="0656e-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="0656e-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="0656e-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="0656e-110">EsentApiException （.）</span><span class="sxs-lookup"><span data-stu-id="0656e-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="0656e-111">EsentStateException （.）</span><span class="sxs-lookup"><span data-stu-id="0656e-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="0656e-112">EsentDatabaseFailedIncrementalReseedException （.）</span><span class="sxs-lookup"><span data-stu-id="0656e-112">Microsoft.Isam.Esent.Interop.EsentDatabaseFailedIncrementalReseedException</span></span>  

<span data-ttu-id="0656e-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0656e-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0656e-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="0656e-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0656e-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="0656e-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseFailedIncrementalReseedException _
    Inherits EsentStateException
'Usage
Dim instance As EsentDatabaseFailedIncrementalReseedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseFailedIncrementalReseedException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="0656e-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="0656e-116">Thread safety</span></span>

<span data-ttu-id="0656e-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="0656e-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="0656e-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="0656e-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="0656e-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0656e-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0656e-120">參考</span><span class="sxs-lookup"><span data-stu-id="0656e-120">Reference</span></span>

[<span data-ttu-id="0656e-121">EsentDatabaseFailedIncrementalReseedException 成員</span><span class="sxs-lookup"><span data-stu-id="0656e-121">EsentDatabaseFailedIncrementalReseedException members</span></span>](./esentdatabasefailedincrementalreseedexception-members.md)

[<span data-ttu-id="0656e-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="0656e-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
