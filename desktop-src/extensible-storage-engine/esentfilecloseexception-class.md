---
description: 深入瞭解： EsentFileCloseException 類別
title: EsentFileCloseException 類別
TOCTitle: EsentFileCloseException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFileCloseException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfilecloseexception(v=EXCHG.10)
ms:contentKeyID: 55101667
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFileCloseException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFileCloseException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 357237cd6ed2210f298eccb3e76d7684ec52c0f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979213"
---
# <a name="esentfilecloseexception-class"></a><span data-ttu-id="5f159-103">EsentFileCloseException 類別</span><span class="sxs-lookup"><span data-stu-id="5f159-103">EsentFileCloseException class</span></span>

<span data-ttu-id="5f159-104">JET_err 的基類。FileClose 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="5f159-104">Base class for JET_err.FileClose exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="5f159-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="5f159-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="5f159-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="5f159-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="5f159-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="5f159-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="5f159-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="5f159-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="5f159-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="5f159-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="5f159-110">EsentApiException （.）</span><span class="sxs-lookup"><span data-stu-id="5f159-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="5f159-111">EsentObsoleteException （.）</span><span class="sxs-lookup"><span data-stu-id="5f159-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="5f159-112">EsentFileCloseException （.）</span><span class="sxs-lookup"><span data-stu-id="5f159-112">Microsoft.Isam.Esent.Interop.EsentFileCloseException</span></span>  

<span data-ttu-id="5f159-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5f159-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5f159-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="5f159-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5f159-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f159-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentFileCloseException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentFileCloseException
```

``` csharp
[SerializableAttribute]
public sealed class EsentFileCloseException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="5f159-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="5f159-116">Thread safety</span></span>

<span data-ttu-id="5f159-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="5f159-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="5f159-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="5f159-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="5f159-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5f159-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5f159-120">參考</span><span class="sxs-lookup"><span data-stu-id="5f159-120">Reference</span></span>

[<span data-ttu-id="5f159-121">EsentFileCloseException 成員</span><span class="sxs-lookup"><span data-stu-id="5f159-121">EsentFileCloseException members</span></span>](./esentfilecloseexception-members.md)

[<span data-ttu-id="5f159-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="5f159-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
