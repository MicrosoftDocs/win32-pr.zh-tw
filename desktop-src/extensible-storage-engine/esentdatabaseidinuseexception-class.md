---
description: 深入瞭解： EsentDatabaseIdInUseException 類別
title: EsentDatabaseIdInUseException 類別
TOCTitle: EsentDatabaseIdInUseException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseIdInUseException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabaseidinuseexception(v=EXCHG.10)
ms:contentKeyID: 55101458
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseIdInUseException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseIdInUseException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 26788132dc36cbddbd2d891746c86045182a1e80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970628"
---
# <a name="esentdatabaseidinuseexception-class"></a><span data-ttu-id="a0761-103">EsentDatabaseIdInUseException 類別</span><span class="sxs-lookup"><span data-stu-id="a0761-103">EsentDatabaseIdInUseException class</span></span>

<span data-ttu-id="a0761-104">JET_err 的基類。DatabaseIdInUse 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="a0761-104">Base class for JET_err.DatabaseIdInUse exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="a0761-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="a0761-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="a0761-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="a0761-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="a0761-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="a0761-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="a0761-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="a0761-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="a0761-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="a0761-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="a0761-110">EsentApiException （.）</span><span class="sxs-lookup"><span data-stu-id="a0761-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="a0761-111">EsentObsoleteException （.）</span><span class="sxs-lookup"><span data-stu-id="a0761-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="a0761-112">EsentDatabaseIdInUseException （.）</span><span class="sxs-lookup"><span data-stu-id="a0761-112">Microsoft.Isam.Esent.Interop.EsentDatabaseIdInUseException</span></span>  

<span data-ttu-id="a0761-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a0761-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a0761-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="a0761-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a0761-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0761-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseIdInUseException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentDatabaseIdInUseException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseIdInUseException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="a0761-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="a0761-116">Thread safety</span></span>

<span data-ttu-id="a0761-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="a0761-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="a0761-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="a0761-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="a0761-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a0761-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a0761-120">參考</span><span class="sxs-lookup"><span data-stu-id="a0761-120">Reference</span></span>

[<span data-ttu-id="a0761-121">EsentDatabaseIdInUseException 成員</span><span class="sxs-lookup"><span data-stu-id="a0761-121">EsentDatabaseIdInUseException members</span></span>](./esentdatabaseidinuseexception-members.md)

[<span data-ttu-id="a0761-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="a0761-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
