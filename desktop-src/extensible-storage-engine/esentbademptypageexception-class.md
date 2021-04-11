---
description: 深入瞭解： EsentBadEmptyPageException 類別
title: EsentBadEmptyPageException 類別
TOCTitle: EsentBadEmptyPageException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentBadEmptyPageException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentbademptypageexception(v=EXCHG.10)
ms:contentKeyID: 55101115
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentBadEmptyPageException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentBadEmptyPageException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 144f42c42eaf3ccb804344214d396cd8ac2f8aa3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194019"
---
# <a name="esentbademptypageexception-class"></a><span data-ttu-id="ad002-103">EsentBadEmptyPageException 類別</span><span class="sxs-lookup"><span data-stu-id="ad002-103">EsentBadEmptyPageException class</span></span>

<span data-ttu-id="ad002-104">JET_err 的基類。BadEmptyPage 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="ad002-104">Base class for JET_err.BadEmptyPage exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="ad002-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="ad002-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="ad002-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="ad002-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="ad002-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="ad002-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="ad002-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="ad002-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="ad002-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="ad002-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="ad002-110">EsentDataException （.）</span><span class="sxs-lookup"><span data-stu-id="ad002-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="ad002-111">EsentCorruptionException （.）</span><span class="sxs-lookup"><span data-stu-id="ad002-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="ad002-112">EsentBadEmptyPageException （.）</span><span class="sxs-lookup"><span data-stu-id="ad002-112">Microsoft.Isam.Esent.Interop.EsentBadEmptyPageException</span></span>  

<span data-ttu-id="ad002-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ad002-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ad002-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="ad002-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ad002-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad002-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentBadEmptyPageException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentBadEmptyPageException
```

``` csharp
[SerializableAttribute]
public sealed class EsentBadEmptyPageException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="ad002-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="ad002-116">Thread safety</span></span>

<span data-ttu-id="ad002-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="ad002-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="ad002-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="ad002-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="ad002-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ad002-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ad002-120">參考</span><span class="sxs-lookup"><span data-stu-id="ad002-120">Reference</span></span>

[<span data-ttu-id="ad002-121">EsentBadEmptyPageException 成員</span><span class="sxs-lookup"><span data-stu-id="ad002-121">EsentBadEmptyPageException members</span></span>](./esentbademptypageexception-members.md)

[<span data-ttu-id="ad002-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="ad002-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
