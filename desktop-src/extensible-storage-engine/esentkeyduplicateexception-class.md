---
description: 深入瞭解： EsentKeyDuplicateException 類別
title: EsentKeyDuplicateException 類別
TOCTitle: EsentKeyDuplicateException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentKeyDuplicateException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentkeyduplicateexception(v=EXCHG.10)
ms:contentKeyID: 55102039
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentKeyDuplicateException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentKeyDuplicateException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0d63945d5db3ca97e858e7f02fd2b4e8a9045f86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320779"
---
# <a name="esentkeyduplicateexception-class"></a><span data-ttu-id="afb45-103">EsentKeyDuplicateException 類別</span><span class="sxs-lookup"><span data-stu-id="afb45-103">EsentKeyDuplicateException class</span></span>

<span data-ttu-id="afb45-104">JET_err 的基類。KeyDuplicate 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="afb45-104">Base class for JET_err.KeyDuplicate exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="afb45-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="afb45-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="afb45-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="afb45-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="afb45-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="afb45-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="afb45-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="afb45-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="afb45-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="afb45-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="afb45-110">EsentApiException （.）</span><span class="sxs-lookup"><span data-stu-id="afb45-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="afb45-111">EsentStateException （.）</span><span class="sxs-lookup"><span data-stu-id="afb45-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="afb45-112">EsentKeyDuplicateException （.）</span><span class="sxs-lookup"><span data-stu-id="afb45-112">Microsoft.Isam.Esent.Interop.EsentKeyDuplicateException</span></span>  

<span data-ttu-id="afb45-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="afb45-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="afb45-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="afb45-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="afb45-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="afb45-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentKeyDuplicateException _
    Inherits EsentStateException
'Usage
Dim instance As EsentKeyDuplicateException
```

``` csharp
[SerializableAttribute]
public sealed class EsentKeyDuplicateException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="afb45-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="afb45-116">Thread safety</span></span>

<span data-ttu-id="afb45-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="afb45-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="afb45-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="afb45-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="afb45-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="afb45-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="afb45-120">參考</span><span class="sxs-lookup"><span data-stu-id="afb45-120">Reference</span></span>

[<span data-ttu-id="afb45-121">EsentKeyDuplicateException 成員</span><span class="sxs-lookup"><span data-stu-id="afb45-121">EsentKeyDuplicateException members</span></span>](./esentkeyduplicateexception-members.md)

[<span data-ttu-id="afb45-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="afb45-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
