---
description: 深入瞭解： EsentDataException 類別
title: EsentDataException 類別
TOCTitle: EsentDataException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDataException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdataexception(v=EXCHG.10)
ms:contentKeyID: 55101456
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDataException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDataException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 996839740d1b008ffae12cf823b9664bf8ca4273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986828"
---
# <a name="esentdataexception-class"></a><span data-ttu-id="42ae1-103">EsentDataException 類別</span><span class="sxs-lookup"><span data-stu-id="42ae1-103">EsentDataException class</span></span>

<span data-ttu-id="42ae1-104">資料例外狀況的基類。</span><span class="sxs-lookup"><span data-stu-id="42ae1-104">Base class for Data exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="42ae1-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="42ae1-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="42ae1-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="42ae1-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="42ae1-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="42ae1-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="42ae1-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="42ae1-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="42ae1-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="42ae1-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        <span data-ttu-id="42ae1-110">EsentDataException （.）</span><span class="sxs-lookup"><span data-stu-id="42ae1-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>  
          [<span data-ttu-id="42ae1-111">EsentCorruptionException （.）</span><span class="sxs-lookup"><span data-stu-id="42ae1-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
          [<span data-ttu-id="42ae1-112">EsentFragmentationException （.）</span><span class="sxs-lookup"><span data-stu-id="42ae1-112">Microsoft.Isam.Esent.Interop.EsentFragmentationException</span></span>](./esentfragmentationexception-class.md)  
          [<span data-ttu-id="42ae1-113">EsentInconsistentException （.）</span><span class="sxs-lookup"><span data-stu-id="42ae1-113">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  

<span data-ttu-id="42ae1-114">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="42ae1-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="42ae1-115">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="42ae1-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="42ae1-116">Syntax</span><span class="sxs-lookup"><span data-stu-id="42ae1-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentDataException _
    Inherits EsentErrorException
'Usage
Dim instance As EsentDataException
```

``` csharp
[SerializableAttribute]
public abstract class EsentDataException : EsentErrorException
```

## <a name="thread-safety"></a><span data-ttu-id="42ae1-117">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="42ae1-117">Thread safety</span></span>

<span data-ttu-id="42ae1-118">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="42ae1-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="42ae1-119">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="42ae1-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="42ae1-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="42ae1-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="42ae1-121">參考</span><span class="sxs-lookup"><span data-stu-id="42ae1-121">Reference</span></span>

[<span data-ttu-id="42ae1-122">EsentDataException 成員</span><span class="sxs-lookup"><span data-stu-id="42ae1-122">EsentDataException members</span></span>](./esentdataexception-members.md)

[<span data-ttu-id="42ae1-123">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="42ae1-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
