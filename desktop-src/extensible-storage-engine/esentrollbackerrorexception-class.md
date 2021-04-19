---
description: 深入瞭解： EsentRollbackErrorException 類別
title: EsentRollbackErrorException 類別
TOCTitle: EsentRollbackErrorException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRollbackErrorException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrollbackerrorexception(v=EXCHG.10)
ms:contentKeyID: 55102663
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRollbackErrorException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRollbackErrorException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6e56e3e829b8c44ff6325ed877606fb44471f6a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974592"
---
# <a name="esentrollbackerrorexception-class"></a><span data-ttu-id="f7228-103">EsentRollbackErrorException 類別</span><span class="sxs-lookup"><span data-stu-id="f7228-103">EsentRollbackErrorException class</span></span>

<span data-ttu-id="f7228-104">JET_err 的基類。RollbackError 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="f7228-104">Base class for JET_err.RollbackError exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="f7228-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="f7228-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="f7228-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="f7228-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="f7228-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="f7228-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="f7228-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="f7228-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="f7228-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="f7228-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="f7228-110">EsentOperationException （.）</span><span class="sxs-lookup"><span data-stu-id="f7228-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="f7228-111">EsentFatalException （.）</span><span class="sxs-lookup"><span data-stu-id="f7228-111">Microsoft.Isam.Esent.Interop.EsentFatalException</span></span>](./esentfatalexception-class.md)  
            <span data-ttu-id="f7228-112">EsentRollbackErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="f7228-112">Microsoft.Isam.Esent.Interop.EsentRollbackErrorException</span></span>  

<span data-ttu-id="f7228-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f7228-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f7228-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="f7228-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f7228-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7228-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRollbackErrorException _
    Inherits EsentFatalException
'Usage
Dim instance As EsentRollbackErrorException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRollbackErrorException : EsentFatalException
```

## <a name="thread-safety"></a><span data-ttu-id="f7228-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="f7228-116">Thread safety</span></span>

<span data-ttu-id="f7228-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="f7228-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="f7228-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="f7228-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="f7228-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f7228-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f7228-120">參考</span><span class="sxs-lookup"><span data-stu-id="f7228-120">Reference</span></span>

[<span data-ttu-id="f7228-121">EsentRollbackErrorException 成員</span><span class="sxs-lookup"><span data-stu-id="f7228-121">EsentRollbackErrorException members</span></span>](./esentrollbackerrorexception-members.md)

[<span data-ttu-id="f7228-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="f7228-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
