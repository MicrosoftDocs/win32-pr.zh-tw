---
description: 深入瞭解： EsentErrorException 類別
title: EsentErrorException 類別
TOCTitle: EsentErrorException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentErrorException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenterrorexception(v=EXCHG.10)
ms:contentKeyID: 55101648
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentErrorException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentErrorException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: eb05197392c1d5c8798968254b24d2d0ae677bbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026960"
---
# <a name="esenterrorexception-class"></a><span data-ttu-id="98895-103">EsentErrorException 類別</span><span class="sxs-lookup"><span data-stu-id="98895-103">EsentErrorException class</span></span>

<span data-ttu-id="98895-104">ESENT 錯誤例外狀況的基類。</span><span class="sxs-lookup"><span data-stu-id="98895-104">Base class for ESENT error exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="98895-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="98895-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="98895-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="98895-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="98895-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="98895-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="98895-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="98895-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      <span data-ttu-id="98895-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="98895-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>  
        [<span data-ttu-id="98895-110">EsentApiException （.）</span><span class="sxs-lookup"><span data-stu-id="98895-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
        [<span data-ttu-id="98895-111">EsentCannotLogDuringRecoveryRedoException （.）</span><span class="sxs-lookup"><span data-stu-id="98895-111">Microsoft.Isam.Esent.Interop.EsentCannotLogDuringRecoveryRedoException</span></span>](./esentcannotlogduringrecoveryredoexception-class.md)  
        [<span data-ttu-id="98895-112">EsentDataException （.）</span><span class="sxs-lookup"><span data-stu-id="98895-112">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
        [<span data-ttu-id="98895-113">EsentOperationException （.）</span><span class="sxs-lookup"><span data-stu-id="98895-113">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
        [<span data-ttu-id="98895-114">EsentPreviousVersionException （.）</span><span class="sxs-lookup"><span data-stu-id="98895-114">Microsoft.Isam.Esent.Interop.EsentPreviousVersionException</span></span>](./esentpreviousversionexception-class.md)  
        [<span data-ttu-id="98895-115">EsentVersionStoreEntryTooBigException （.）</span><span class="sxs-lookup"><span data-stu-id="98895-115">Microsoft.Isam.Esent.Interop.EsentVersionStoreEntryTooBigException</span></span>](./esentversionstoreentrytoobigexception-class.md)  

<span data-ttu-id="98895-116">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="98895-116">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="98895-117">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="98895-117">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="98895-118">Syntax</span><span class="sxs-lookup"><span data-stu-id="98895-118">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public Class EsentErrorException _
    Inherits EsentException
'Usage
Dim instance As EsentErrorException
```

``` csharp
[SerializableAttribute]
public class EsentErrorException : EsentException
```

## <a name="thread-safety"></a><span data-ttu-id="98895-119">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="98895-119">Thread safety</span></span>

<span data-ttu-id="98895-120">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="98895-120">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="98895-121">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="98895-121">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="98895-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="98895-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="98895-123">參考</span><span class="sxs-lookup"><span data-stu-id="98895-123">Reference</span></span>

[<span data-ttu-id="98895-124">EsentErrorException 成員</span><span class="sxs-lookup"><span data-stu-id="98895-124">EsentErrorException members</span></span>](./esenterrorexception-members.md)

[<span data-ttu-id="98895-125">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="98895-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
