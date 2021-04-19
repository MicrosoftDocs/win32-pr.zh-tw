---
description: 深入瞭解： EsentDirtyShutdownException 類別
title: EsentDirtyShutdownException 類別
TOCTitle: EsentDirtyShutdownException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDirtyShutdownException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdirtyshutdownexception(v=EXCHG.10)
ms:contentKeyID: 55101504
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDirtyShutdownException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDirtyShutdownException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 72eb3984c034cbbb9c6163e183a5b8680fc49845
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989991"
---
# <a name="esentdirtyshutdownexception-class"></a><span data-ttu-id="051ac-103">EsentDirtyShutdownException 類別</span><span class="sxs-lookup"><span data-stu-id="051ac-103">EsentDirtyShutdownException class</span></span>

<span data-ttu-id="051ac-104">JET_err 的基類。DirtyShutdown 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="051ac-104">Base class for JET_err.DirtyShutdown exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="051ac-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="051ac-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="051ac-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="051ac-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="051ac-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="051ac-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="051ac-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="051ac-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="051ac-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="051ac-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="051ac-110">EsentApiException （.）</span><span class="sxs-lookup"><span data-stu-id="051ac-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="051ac-111">EsentStateException （.）</span><span class="sxs-lookup"><span data-stu-id="051ac-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="051ac-112">EsentDirtyShutdownException （.）</span><span class="sxs-lookup"><span data-stu-id="051ac-112">Microsoft.Isam.Esent.Interop.EsentDirtyShutdownException</span></span>  

<span data-ttu-id="051ac-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="051ac-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="051ac-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="051ac-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="051ac-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="051ac-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDirtyShutdownException _
    Inherits EsentStateException
'Usage
Dim instance As EsentDirtyShutdownException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDirtyShutdownException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="051ac-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="051ac-116">Thread safety</span></span>

<span data-ttu-id="051ac-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="051ac-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="051ac-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="051ac-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="051ac-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="051ac-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="051ac-120">參考</span><span class="sxs-lookup"><span data-stu-id="051ac-120">Reference</span></span>

[<span data-ttu-id="051ac-121">EsentDirtyShutdownException 成員</span><span class="sxs-lookup"><span data-stu-id="051ac-121">EsentDirtyShutdownException members</span></span>](./esentdirtyshutdownexception-members.md)

[<span data-ttu-id="051ac-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="051ac-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
