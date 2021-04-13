---
description: 深入瞭解： EsentPreviousVersionException 類別
title: EsentPreviousVersionException 類別
TOCTitle: EsentPreviousVersionException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentPreviousVersionException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentpreviousversionexception(v=EXCHG.10)
ms:contentKeyID: 55102535
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentPreviousVersionException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentPreviousVersionException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 75392fda39bc13e26c0667378021989e138dd893
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104386274"
---
# <a name="esentpreviousversionexception-class"></a><span data-ttu-id="b22a7-103">EsentPreviousVersionException 類別</span><span class="sxs-lookup"><span data-stu-id="b22a7-103">EsentPreviousVersionException class</span></span>

<span data-ttu-id="b22a7-104">JET_err 的基類。PreviousVersion 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="b22a7-104">Base class for JET_err.PreviousVersion exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="b22a7-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="b22a7-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="b22a7-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="b22a7-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="b22a7-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="b22a7-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="b22a7-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="b22a7-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="b22a7-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="b22a7-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        <span data-ttu-id="b22a7-110">EsentPreviousVersionException （.）</span><span class="sxs-lookup"><span data-stu-id="b22a7-110">Microsoft.Isam.Esent.Interop.EsentPreviousVersionException</span></span>  

<span data-ttu-id="b22a7-111">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b22a7-111">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b22a7-112">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="b22a7-112">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b22a7-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="b22a7-113">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentPreviousVersionException _
    Inherits EsentErrorException
'Usage
Dim instance As EsentPreviousVersionException
```

``` csharp
[SerializableAttribute]
public sealed class EsentPreviousVersionException : EsentErrorException
```

## <a name="thread-safety"></a><span data-ttu-id="b22a7-114">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="b22a7-114">Thread safety</span></span>

<span data-ttu-id="b22a7-115">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="b22a7-115">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="b22a7-116">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="b22a7-116">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="b22a7-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b22a7-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b22a7-118">參考</span><span class="sxs-lookup"><span data-stu-id="b22a7-118">Reference</span></span>

[<span data-ttu-id="b22a7-119">EsentPreviousVersionException 成員</span><span class="sxs-lookup"><span data-stu-id="b22a7-119">EsentPreviousVersionException members</span></span>](./esentpreviousversionexception-members.md)

[<span data-ttu-id="b22a7-120">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="b22a7-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
