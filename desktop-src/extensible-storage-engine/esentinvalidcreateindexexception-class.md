---
description: 深入瞭解： EsentInvalidCreateIndexException 類別
title: EsentInvalidCreateIndexException 類別
TOCTitle: EsentInvalidCreateIndexException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidCreateIndexException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidcreateindexexception(v=EXCHG.10)
ms:contentKeyID: 55101944
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidCreateIndexException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidCreateIndexException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1294d858d649bcde551e151919db8a04ef793e43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192002"
---
# <a name="esentinvalidcreateindexexception-class"></a><span data-ttu-id="b61ea-103">EsentInvalidCreateIndexException 類別</span><span class="sxs-lookup"><span data-stu-id="b61ea-103">EsentInvalidCreateIndexException class</span></span>

<span data-ttu-id="b61ea-104">JET_err 的基類。InvalidCreateIndex 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="b61ea-104">Base class for JET_err.InvalidCreateIndex exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="b61ea-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="b61ea-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="b61ea-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="b61ea-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="b61ea-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="b61ea-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="b61ea-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="b61ea-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="b61ea-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="b61ea-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="b61ea-110">EsentApiException （.）</span><span class="sxs-lookup"><span data-stu-id="b61ea-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="b61ea-111">EsentUsageException （.）</span><span class="sxs-lookup"><span data-stu-id="b61ea-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="b61ea-112">EsentInvalidCreateIndexException （.）</span><span class="sxs-lookup"><span data-stu-id="b61ea-112">Microsoft.Isam.Esent.Interop.EsentInvalidCreateIndexException</span></span>  

<span data-ttu-id="b61ea-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b61ea-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b61ea-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="b61ea-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b61ea-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="b61ea-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidCreateIndexException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentInvalidCreateIndexException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidCreateIndexException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="b61ea-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="b61ea-116">Thread safety</span></span>

<span data-ttu-id="b61ea-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="b61ea-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="b61ea-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="b61ea-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="b61ea-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b61ea-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b61ea-120">參考</span><span class="sxs-lookup"><span data-stu-id="b61ea-120">Reference</span></span>

[<span data-ttu-id="b61ea-121">EsentInvalidCreateIndexException 成員</span><span class="sxs-lookup"><span data-stu-id="b61ea-121">EsentInvalidCreateIndexException members</span></span>](./esentinvalidcreateindexexception-members.md)

[<span data-ttu-id="b61ea-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="b61ea-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
