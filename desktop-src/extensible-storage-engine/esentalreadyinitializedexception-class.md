---
description: 深入瞭解： EsentAlreadyInitializedException 類別
title: EsentAlreadyInitializedException 類別
TOCTitle: EsentAlreadyInitializedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentAlreadyInitializedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentalreadyinitializedexception(v=EXCHG.10)
ms:contentKeyID: 55101047
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentAlreadyInitializedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentAlreadyInitializedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ffc1cb0a1de8b3e7873ec48fce26507cfc45dd3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996874"
---
# <a name="esentalreadyinitializedexception-class"></a><span data-ttu-id="e3224-103">EsentAlreadyInitializedException 類別</span><span class="sxs-lookup"><span data-stu-id="e3224-103">EsentAlreadyInitializedException class</span></span>

<span data-ttu-id="e3224-104">JET_err 的基類。AlreadyInitialized 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="e3224-104">Base class for JET_err.AlreadyInitialized exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="e3224-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="e3224-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="e3224-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="e3224-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="e3224-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="e3224-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="e3224-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="e3224-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="e3224-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="e3224-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="e3224-110">EsentApiException （.）</span><span class="sxs-lookup"><span data-stu-id="e3224-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="e3224-111">EsentUsageException （.）</span><span class="sxs-lookup"><span data-stu-id="e3224-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="e3224-112">EsentAlreadyInitializedException （.）</span><span class="sxs-lookup"><span data-stu-id="e3224-112">Microsoft.Isam.Esent.Interop.EsentAlreadyInitializedException</span></span>  

<span data-ttu-id="e3224-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e3224-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e3224-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="e3224-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e3224-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3224-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentAlreadyInitializedException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentAlreadyInitializedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentAlreadyInitializedException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="e3224-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="e3224-116">Thread safety</span></span>

<span data-ttu-id="e3224-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="e3224-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="e3224-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="e3224-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="e3224-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e3224-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e3224-120">參考</span><span class="sxs-lookup"><span data-stu-id="e3224-120">Reference</span></span>

[<span data-ttu-id="e3224-121">EsentAlreadyInitializedException 成員</span><span class="sxs-lookup"><span data-stu-id="e3224-121">EsentAlreadyInitializedException members</span></span>](./esentalreadyinitializedexception-members.md)

[<span data-ttu-id="e3224-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="e3224-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
