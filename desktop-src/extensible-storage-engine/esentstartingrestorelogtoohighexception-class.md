---
description: 深入瞭解： EsentStartingRestoreLogTooHighException 類別
title: EsentStartingRestoreLogTooHighException 類別
TOCTitle: EsentStartingRestoreLogTooHighException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentStartingRestoreLogTooHighException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentstartingrestorelogtoohighexception(v=EXCHG.10)
ms:contentKeyID: 55102926
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentStartingRestoreLogTooHighException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentStartingRestoreLogTooHighException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bf3be54b85359f00c94cfc35b960c2d3bf6b202f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319999"
---
# <a name="esentstartingrestorelogtoohighexception-class"></a><span data-ttu-id="a1f39-103">EsentStartingRestoreLogTooHighException 類別</span><span class="sxs-lookup"><span data-stu-id="a1f39-103">EsentStartingRestoreLogTooHighException class</span></span>

<span data-ttu-id="a1f39-104">JET_err 的基類。StartingRestoreLogTooHigh 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="a1f39-104">Base class for JET_err.StartingRestoreLogTooHigh exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="a1f39-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="a1f39-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="a1f39-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="a1f39-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="a1f39-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="a1f39-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="a1f39-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="a1f39-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="a1f39-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="a1f39-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="a1f39-110">EsentDataException （.）</span><span class="sxs-lookup"><span data-stu-id="a1f39-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="a1f39-111">EsentInconsistentException （.）</span><span class="sxs-lookup"><span data-stu-id="a1f39-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  
            <span data-ttu-id="a1f39-112">EsentStartingRestoreLogTooHighException （.）</span><span class="sxs-lookup"><span data-stu-id="a1f39-112">Microsoft.Isam.Esent.Interop.EsentStartingRestoreLogTooHighException</span></span>  

<span data-ttu-id="a1f39-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a1f39-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a1f39-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="a1f39-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a1f39-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1f39-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentStartingRestoreLogTooHighException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentStartingRestoreLogTooHighException
```

``` csharp
[SerializableAttribute]
public sealed class EsentStartingRestoreLogTooHighException : EsentInconsistentException
```

## <a name="thread-safety"></a><span data-ttu-id="a1f39-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="a1f39-116">Thread safety</span></span>

<span data-ttu-id="a1f39-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="a1f39-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="a1f39-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="a1f39-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="a1f39-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a1f39-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a1f39-120">參考</span><span class="sxs-lookup"><span data-stu-id="a1f39-120">Reference</span></span>

[<span data-ttu-id="a1f39-121">EsentStartingRestoreLogTooHighException 成員</span><span class="sxs-lookup"><span data-stu-id="a1f39-121">EsentStartingRestoreLogTooHighException members</span></span>](./esentstartingrestorelogtoohighexception-members.md)

[<span data-ttu-id="a1f39-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="a1f39-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
