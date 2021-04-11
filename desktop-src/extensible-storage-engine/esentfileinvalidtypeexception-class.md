---
description: 深入瞭解： EsentFileInvalidTypeException 類別
title: EsentFileInvalidTypeException 類別
TOCTitle: EsentFileInvalidTypeException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFileInvalidTypeException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfileinvalidtypeexception(v=EXCHG.10)
ms:contentKeyID: 55107272
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFileInvalidTypeException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFileInvalidTypeException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d2c2bf5cf30cb45734613fcabc446834085d5bc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320640"
---
# <a name="esentfileinvalidtypeexception-class"></a><span data-ttu-id="05e09-103">EsentFileInvalidTypeException 類別</span><span class="sxs-lookup"><span data-stu-id="05e09-103">EsentFileInvalidTypeException class</span></span>

<span data-ttu-id="05e09-104">JET_err 的基類。FileInvalidType 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="05e09-104">Base class for JET_err.FileInvalidType exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="05e09-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="05e09-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="05e09-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="05e09-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="05e09-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="05e09-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="05e09-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="05e09-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="05e09-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="05e09-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="05e09-110">EsentDataException （.）</span><span class="sxs-lookup"><span data-stu-id="05e09-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="05e09-111">EsentInconsistentException （.）</span><span class="sxs-lookup"><span data-stu-id="05e09-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  
            <span data-ttu-id="05e09-112">EsentFileInvalidTypeException （.）</span><span class="sxs-lookup"><span data-stu-id="05e09-112">Microsoft.Isam.Esent.Interop.EsentFileInvalidTypeException</span></span>  

<span data-ttu-id="05e09-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="05e09-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="05e09-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="05e09-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="05e09-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="05e09-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentFileInvalidTypeException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentFileInvalidTypeException
```

``` csharp
[SerializableAttribute]
public sealed class EsentFileInvalidTypeException : EsentInconsistentException
```

## <a name="thread-safety"></a><span data-ttu-id="05e09-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="05e09-116">Thread safety</span></span>

<span data-ttu-id="05e09-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="05e09-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="05e09-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="05e09-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="05e09-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="05e09-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="05e09-120">參考</span><span class="sxs-lookup"><span data-stu-id="05e09-120">Reference</span></span>

[<span data-ttu-id="05e09-121">EsentFileInvalidTypeException 成員</span><span class="sxs-lookup"><span data-stu-id="05e09-121">EsentFileInvalidTypeException members</span></span>](./esentfileinvalidtypeexception-members.md)

[<span data-ttu-id="05e09-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="05e09-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
