---
description: 深入瞭解： EsentGivenLogFileIsNotContiguousException 類別
title: EsentGivenLogFileIsNotContiguousException 類別
TOCTitle: EsentGivenLogFileIsNotContiguousException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentGivenLogFileIsNotContiguousException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentgivenlogfileisnotcontiguousexception(v=EXCHG.10)
ms:contentKeyID: 55101788
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentGivenLogFileIsNotContiguousException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentGivenLogFileIsNotContiguousException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d6cbba7d6bf7f5fb30ac77cc92232507cc2a15d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974530"
---
# <a name="esentgivenlogfileisnotcontiguousexception-class"></a><span data-ttu-id="6a592-103">EsentGivenLogFileIsNotContiguousException 類別</span><span class="sxs-lookup"><span data-stu-id="6a592-103">EsentGivenLogFileIsNotContiguousException class</span></span>

<span data-ttu-id="6a592-104">JET_err 的基類。GivenLogFileIsNotContiguous 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="6a592-104">Base class for JET_err.GivenLogFileIsNotContiguous exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="6a592-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="6a592-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="6a592-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="6a592-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="6a592-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="6a592-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="6a592-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="6a592-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="6a592-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="6a592-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="6a592-110">EsentDataException （.）</span><span class="sxs-lookup"><span data-stu-id="6a592-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="6a592-111">EsentInconsistentException （.）</span><span class="sxs-lookup"><span data-stu-id="6a592-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  
            <span data-ttu-id="6a592-112">EsentGivenLogFileIsNotContiguousException （.）</span><span class="sxs-lookup"><span data-stu-id="6a592-112">Microsoft.Isam.Esent.Interop.EsentGivenLogFileIsNotContiguousException</span></span>  

<span data-ttu-id="6a592-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6a592-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6a592-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="6a592-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6a592-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="6a592-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentGivenLogFileIsNotContiguousException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentGivenLogFileIsNotContiguousException
```

``` csharp
[SerializableAttribute]
public sealed class EsentGivenLogFileIsNotContiguousException : EsentInconsistentException
```

## <a name="thread-safety"></a><span data-ttu-id="6a592-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="6a592-116">Thread safety</span></span>

<span data-ttu-id="6a592-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="6a592-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="6a592-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="6a592-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="6a592-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6a592-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6a592-120">參考</span><span class="sxs-lookup"><span data-stu-id="6a592-120">Reference</span></span>

[<span data-ttu-id="6a592-121">EsentGivenLogFileIsNotContiguousException 成員</span><span class="sxs-lookup"><span data-stu-id="6a592-121">EsentGivenLogFileIsNotContiguousException members</span></span>](./esentgivenlogfileisnotcontiguousexception-members.md)

[<span data-ttu-id="6a592-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="6a592-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
