---
description: 深入瞭解： EsentInvalidLogDirectoryException 類別
title: EsentInvalidLogDirectoryException 類別
TOCTitle: EsentInvalidLogDirectoryException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidLogDirectoryException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidlogdirectoryexception(v=EXCHG.10)
ms:contentKeyID: 55101985
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidLogDirectoryException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidLogDirectoryException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7ad19107b0fea4b9656db7d7f17b9f6239e478a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851987"
---
# <a name="esentinvalidlogdirectoryexception-class"></a><span data-ttu-id="0a89c-103">EsentInvalidLogDirectoryException 類別</span><span class="sxs-lookup"><span data-stu-id="0a89c-103">EsentInvalidLogDirectoryException class</span></span>

<span data-ttu-id="0a89c-104">JET_err 的基類。InvalidLogDirectory 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="0a89c-104">Base class for JET_err.InvalidLogDirectory exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="0a89c-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="0a89c-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="0a89c-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="0a89c-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="0a89c-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="0a89c-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="0a89c-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="0a89c-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="0a89c-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="0a89c-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="0a89c-110">EsentApiException （.）</span><span class="sxs-lookup"><span data-stu-id="0a89c-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="0a89c-111">EsentObsoleteException （.）</span><span class="sxs-lookup"><span data-stu-id="0a89c-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="0a89c-112">EsentInvalidLogDirectoryException （.）</span><span class="sxs-lookup"><span data-stu-id="0a89c-112">Microsoft.Isam.Esent.Interop.EsentInvalidLogDirectoryException</span></span>  

<span data-ttu-id="0a89c-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0a89c-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0a89c-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="0a89c-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0a89c-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a89c-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidLogDirectoryException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentInvalidLogDirectoryException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidLogDirectoryException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="0a89c-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="0a89c-116">Thread safety</span></span>

<span data-ttu-id="0a89c-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="0a89c-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="0a89c-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="0a89c-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="0a89c-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0a89c-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0a89c-120">參考</span><span class="sxs-lookup"><span data-stu-id="0a89c-120">Reference</span></span>

[<span data-ttu-id="0a89c-121">EsentInvalidLogDirectoryException 成員</span><span class="sxs-lookup"><span data-stu-id="0a89c-121">EsentInvalidLogDirectoryException members</span></span>](./esentinvalidlogdirectoryexception-members.md)

[<span data-ttu-id="0a89c-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="0a89c-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
