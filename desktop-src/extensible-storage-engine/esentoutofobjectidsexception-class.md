---
description: 深入瞭解： EsentOutOfObjectIDsException 類別
title: EsentOutOfObjectIDsException 類別
TOCTitle: EsentOutOfObjectIDsException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOutOfObjectIDsException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoutofobjectidsexception(v=EXCHG.10)
ms:contentKeyID: 55102436
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOutOfObjectIDsException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOutOfObjectIDsException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 18cf8d1b7c98db8f855cf970eed7be87185fc9fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979977"
---
# <a name="esentoutofobjectidsexception-class"></a><span data-ttu-id="a2686-103">EsentOutOfObjectIDsException 類別</span><span class="sxs-lookup"><span data-stu-id="a2686-103">EsentOutOfObjectIDsException class</span></span>

<span data-ttu-id="a2686-104">JET_err 的基類。OutOfObjectIDs 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="a2686-104">Base class for JET_err.OutOfObjectIDs exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="a2686-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="a2686-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="a2686-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="a2686-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="a2686-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="a2686-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="a2686-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="a2686-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="a2686-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="a2686-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="a2686-110">EsentDataException （.）</span><span class="sxs-lookup"><span data-stu-id="a2686-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="a2686-111">EsentFragmentationException （.）</span><span class="sxs-lookup"><span data-stu-id="a2686-111">Microsoft.Isam.Esent.Interop.EsentFragmentationException</span></span>](./esentfragmentationexception-class.md)  
            <span data-ttu-id="a2686-112">EsentOutOfObjectIDsException （.）</span><span class="sxs-lookup"><span data-stu-id="a2686-112">Microsoft.Isam.Esent.Interop.EsentOutOfObjectIDsException</span></span>  

<span data-ttu-id="a2686-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a2686-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a2686-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="a2686-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a2686-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2686-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOutOfObjectIDsException _
    Inherits EsentFragmentationException
'Usage
Dim instance As EsentOutOfObjectIDsException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOutOfObjectIDsException : EsentFragmentationException
```

## <a name="thread-safety"></a><span data-ttu-id="a2686-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="a2686-116">Thread safety</span></span>

<span data-ttu-id="a2686-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="a2686-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="a2686-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="a2686-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="a2686-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a2686-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a2686-120">參考</span><span class="sxs-lookup"><span data-stu-id="a2686-120">Reference</span></span>

[<span data-ttu-id="a2686-121">EsentOutOfObjectIDsException 成員</span><span class="sxs-lookup"><span data-stu-id="a2686-121">EsentOutOfObjectIDsException members</span></span>](./esentoutofobjectidsexception-members.md)

[<span data-ttu-id="a2686-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="a2686-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
