---
description: 深入瞭解： EsentInvalidBufferSizeException 類別
title: EsentInvalidBufferSizeException 類別
TOCTitle: EsentInvalidBufferSizeException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidBufferSizeException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidbuffersizeexception(v=EXCHG.10)
ms:contentKeyID: 55101912
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidBufferSizeException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidBufferSizeException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0dc693135124ba5d2979fa0f1a7ff80fcca27600
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849836"
---
# <a name="esentinvalidbuffersizeexception-class"></a><span data-ttu-id="3f3fe-103">EsentInvalidBufferSizeException 類別</span><span class="sxs-lookup"><span data-stu-id="3f3fe-103">EsentInvalidBufferSizeException class</span></span>

<span data-ttu-id="3f3fe-104">JET_err 的基類。InvalidBufferSize 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="3f3fe-104">Base class for JET_err.InvalidBufferSize exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="3f3fe-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="3f3fe-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="3f3fe-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="3f3fe-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="3f3fe-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="3f3fe-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="3f3fe-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="3f3fe-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="3f3fe-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="3f3fe-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="3f3fe-110">EsentApiException （.）</span><span class="sxs-lookup"><span data-stu-id="3f3fe-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="3f3fe-111">EsentStateException （.）</span><span class="sxs-lookup"><span data-stu-id="3f3fe-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="3f3fe-112">EsentInvalidBufferSizeException （.）</span><span class="sxs-lookup"><span data-stu-id="3f3fe-112">Microsoft.Isam.Esent.Interop.EsentInvalidBufferSizeException</span></span>  

<span data-ttu-id="3f3fe-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3f3fe-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3f3fe-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="3f3fe-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3f3fe-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f3fe-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidBufferSizeException _
    Inherits EsentStateException
'Usage
Dim instance As EsentInvalidBufferSizeException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidBufferSizeException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="3f3fe-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="3f3fe-116">Thread safety</span></span>

<span data-ttu-id="3f3fe-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="3f3fe-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="3f3fe-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="3f3fe-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="3f3fe-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3f3fe-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3f3fe-120">參考</span><span class="sxs-lookup"><span data-stu-id="3f3fe-120">Reference</span></span>

[<span data-ttu-id="3f3fe-121">EsentInvalidBufferSizeException 成員</span><span class="sxs-lookup"><span data-stu-id="3f3fe-121">EsentInvalidBufferSizeException members</span></span>](./esentinvalidbuffersizeexception-members.md)

[<span data-ttu-id="3f3fe-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="3f3fe-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
