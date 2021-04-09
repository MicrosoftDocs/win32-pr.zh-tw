---
description: 深入瞭解： EsentDiskIOException 類別
title: EsentDiskIOException 類別
TOCTitle: EsentDiskIOException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDiskIOException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdiskioexception(v=EXCHG.10)
ms:contentKeyID: 55101660
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDiskIOException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDiskIOException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b9810c7cd54afd9649530c1bea6db93161911efb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945221"
---
# <a name="esentdiskioexception-class"></a><span data-ttu-id="4cb43-103">EsentDiskIOException 類別</span><span class="sxs-lookup"><span data-stu-id="4cb43-103">EsentDiskIOException class</span></span>

<span data-ttu-id="4cb43-104">JET_err 的基類。DiskIO 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="4cb43-104">Base class for JET_err.DiskIO exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="4cb43-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="4cb43-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="4cb43-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="4cb43-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="4cb43-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="4cb43-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="4cb43-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="4cb43-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="4cb43-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="4cb43-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="4cb43-110">EsentOperationException （.）</span><span class="sxs-lookup"><span data-stu-id="4cb43-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="4cb43-111">EsentIOException （.）</span><span class="sxs-lookup"><span data-stu-id="4cb43-111">Microsoft.Isam.Esent.Interop.EsentIOException</span></span>](./esentioexception-class.md)  
            <span data-ttu-id="4cb43-112">EsentDiskIOException （.）</span><span class="sxs-lookup"><span data-stu-id="4cb43-112">Microsoft.Isam.Esent.Interop.EsentDiskIOException</span></span>  

<span data-ttu-id="4cb43-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4cb43-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4cb43-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="4cb43-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4cb43-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="4cb43-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDiskIOException _
    Inherits EsentIOException
'Usage
Dim instance As EsentDiskIOException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDiskIOException : EsentIOException
```

## <a name="thread-safety"></a><span data-ttu-id="4cb43-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="4cb43-116">Thread safety</span></span>

<span data-ttu-id="4cb43-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="4cb43-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="4cb43-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="4cb43-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="4cb43-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4cb43-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4cb43-120">參考</span><span class="sxs-lookup"><span data-stu-id="4cb43-120">Reference</span></span>

[<span data-ttu-id="4cb43-121">EsentDiskIOException 成員</span><span class="sxs-lookup"><span data-stu-id="4cb43-121">EsentDiskIOException members</span></span>](./esentdiskioexception-members.md)

[<span data-ttu-id="4cb43-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="4cb43-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
