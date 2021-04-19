---
description: 深入瞭解： EsentInitInProgressException 類別
title: EsentInitInProgressException 類別
TOCTitle: EsentInitInProgressException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInitInProgressException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinitinprogressexception(v=EXCHG.10)
ms:contentKeyID: 55101813
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInitInProgressException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInitInProgressException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b035465e575dd94f68b38cf72f8771c24add49d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001701"
---
# <a name="esentinitinprogressexception-class"></a><span data-ttu-id="c4fa2-103">EsentInitInProgressException 類別</span><span class="sxs-lookup"><span data-stu-id="c4fa2-103">EsentInitInProgressException class</span></span>

<span data-ttu-id="c4fa2-104">JET_err.InitInProgress 例外狀況的基類。</span><span class="sxs-lookup"><span data-stu-id="c4fa2-104">Base class for JET_err.InitInProgress exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="c4fa2-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="c4fa2-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="c4fa2-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="c4fa2-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="c4fa2-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="c4fa2-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="c4fa2-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="c4fa2-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="c4fa2-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="c4fa2-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="c4fa2-110">EsentOperationException （.）</span><span class="sxs-lookup"><span data-stu-id="c4fa2-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          <span data-ttu-id="c4fa2-111">EsentInitInProgressException （.）</span><span class="sxs-lookup"><span data-stu-id="c4fa2-111">Microsoft.Isam.Esent.Interop.EsentInitInProgressException</span></span>  

<span data-ttu-id="c4fa2-112">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c4fa2-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c4fa2-113">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="c4fa2-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c4fa2-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4fa2-114">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInitInProgressException _
    Inherits EsentOperationException
'Usage
Dim instance As EsentInitInProgressException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInitInProgressException : EsentOperationException
```

## <a name="thread-safety"></a><span data-ttu-id="c4fa2-115">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="c4fa2-115">Thread safety</span></span>

<span data-ttu-id="c4fa2-116">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="c4fa2-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="c4fa2-117">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="c4fa2-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="c4fa2-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c4fa2-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c4fa2-119">參考</span><span class="sxs-lookup"><span data-stu-id="c4fa2-119">Reference</span></span>

[<span data-ttu-id="c4fa2-120">EsentInitInProgressException 成員</span><span class="sxs-lookup"><span data-stu-id="c4fa2-120">EsentInitInProgressException members</span></span>](./esentinitinprogressexception-members.md)

[<span data-ttu-id="c4fa2-121">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="c4fa2-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
