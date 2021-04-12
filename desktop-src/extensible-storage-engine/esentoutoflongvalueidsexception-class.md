---
description: 深入瞭解： EsentOutOfLongValueIDsException 類別
title: EsentOutOfLongValueIDsException 類別
TOCTitle: EsentOutOfLongValueIDsException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOutOfLongValueIDsException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoutoflongvalueidsexception(v=EXCHG.10)
ms:contentKeyID: 55102476
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOutOfLongValueIDsException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOutOfLongValueIDsException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: aada406390da086bc209094641a5ceca546d4932
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191544"
---
# <a name="esentoutoflongvalueidsexception-class"></a><span data-ttu-id="c5d85-103">EsentOutOfLongValueIDsException 類別</span><span class="sxs-lookup"><span data-stu-id="c5d85-103">EsentOutOfLongValueIDsException class</span></span>

<span data-ttu-id="c5d85-104">JET_err 的基類。OutOfLongValueIDs 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="c5d85-104">Base class for JET_err.OutOfLongValueIDs exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="c5d85-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="c5d85-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="c5d85-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="c5d85-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="c5d85-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="c5d85-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="c5d85-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="c5d85-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="c5d85-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="c5d85-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="c5d85-110">EsentDataException （.）</span><span class="sxs-lookup"><span data-stu-id="c5d85-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="c5d85-111">EsentFragmentationException （.）</span><span class="sxs-lookup"><span data-stu-id="c5d85-111">Microsoft.Isam.Esent.Interop.EsentFragmentationException</span></span>](./esentfragmentationexception-class.md)  
            <span data-ttu-id="c5d85-112">EsentOutOfLongValueIDsException （.）</span><span class="sxs-lookup"><span data-stu-id="c5d85-112">Microsoft.Isam.Esent.Interop.EsentOutOfLongValueIDsException</span></span>  

<span data-ttu-id="c5d85-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c5d85-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c5d85-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="c5d85-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c5d85-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5d85-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOutOfLongValueIDsException _
    Inherits EsentFragmentationException
'Usage
Dim instance As EsentOutOfLongValueIDsException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOutOfLongValueIDsException : EsentFragmentationException
```

## <a name="thread-safety"></a><span data-ttu-id="c5d85-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="c5d85-116">Thread safety</span></span>

<span data-ttu-id="c5d85-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="c5d85-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="c5d85-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="c5d85-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="c5d85-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c5d85-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c5d85-120">參考</span><span class="sxs-lookup"><span data-stu-id="c5d85-120">Reference</span></span>

[<span data-ttu-id="c5d85-121">EsentOutOfLongValueIDsException 成員</span><span class="sxs-lookup"><span data-stu-id="c5d85-121">EsentOutOfLongValueIDsException members</span></span>](./esentoutoflongvalueidsexception-members.md)

[<span data-ttu-id="c5d85-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="c5d85-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
