---
description: 深入瞭解： EsentDbTimeTooOldException 類別
title: EsentDbTimeTooOldException 類別
TOCTitle: EsentDbTimeTooOldException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDbTimeTooOldException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdbtimetoooldexception(v=EXCHG.10)
ms:contentKeyID: 55101581
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDbTimeTooOldException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDbTimeTooOldException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 12dfb0b661d1bcc1469470c2cc4476f41499e6cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192016"
---
# <a name="esentdbtimetoooldexception-class"></a><span data-ttu-id="ae23f-103">EsentDbTimeTooOldException 類別</span><span class="sxs-lookup"><span data-stu-id="ae23f-103">EsentDbTimeTooOldException class</span></span>

<span data-ttu-id="ae23f-104">JET_err 的基類。DbTimeTooOld 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="ae23f-104">Base class for JET_err.DbTimeTooOld exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="ae23f-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="ae23f-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="ae23f-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="ae23f-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="ae23f-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="ae23f-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="ae23f-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="ae23f-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="ae23f-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="ae23f-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="ae23f-110">EsentDataException （.）</span><span class="sxs-lookup"><span data-stu-id="ae23f-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="ae23f-111">EsentInconsistentException （.）</span><span class="sxs-lookup"><span data-stu-id="ae23f-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  
            <span data-ttu-id="ae23f-112">EsentDbTimeTooOldException （.）</span><span class="sxs-lookup"><span data-stu-id="ae23f-112">Microsoft.Isam.Esent.Interop.EsentDbTimeTooOldException</span></span>  

<span data-ttu-id="ae23f-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ae23f-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ae23f-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="ae23f-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ae23f-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae23f-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDbTimeTooOldException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentDbTimeTooOldException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDbTimeTooOldException : EsentInconsistentException
```

## <a name="thread-safety"></a><span data-ttu-id="ae23f-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="ae23f-116">Thread safety</span></span>

<span data-ttu-id="ae23f-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="ae23f-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="ae23f-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="ae23f-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="ae23f-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ae23f-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ae23f-120">參考</span><span class="sxs-lookup"><span data-stu-id="ae23f-120">Reference</span></span>

[<span data-ttu-id="ae23f-121">EsentDbTimeTooOldException 成員</span><span class="sxs-lookup"><span data-stu-id="ae23f-121">EsentDbTimeTooOldException members</span></span>](./esentdbtimetoooldexception-members.md)

[<span data-ttu-id="ae23f-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="ae23f-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
