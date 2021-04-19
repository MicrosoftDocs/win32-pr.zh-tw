---
description: 深入瞭解： EsentLogWriteFailException 類別
title: EsentLogWriteFailException 類別
TOCTitle: EsentLogWriteFailException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLogWriteFailException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlogwritefailexception(v=EXCHG.10)
ms:contentKeyID: 55102169
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLogWriteFailException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLogWriteFailException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9cd3fe6b541a58b7498ca4117f7ba2af7662d5a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980332"
---
# <a name="esentlogwritefailexception-class"></a><span data-ttu-id="97c20-103">EsentLogWriteFailException 類別</span><span class="sxs-lookup"><span data-stu-id="97c20-103">EsentLogWriteFailException class</span></span>

<span data-ttu-id="97c20-104">JET_err 的基類。LogWriteFail 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="97c20-104">Base class for JET_err.LogWriteFail exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="97c20-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="97c20-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="97c20-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="97c20-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="97c20-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="97c20-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="97c20-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="97c20-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="97c20-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="97c20-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="97c20-110">EsentOperationException （.）</span><span class="sxs-lookup"><span data-stu-id="97c20-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="97c20-111">EsentIOException （.）</span><span class="sxs-lookup"><span data-stu-id="97c20-111">Microsoft.Isam.Esent.Interop.EsentIOException</span></span>](./esentioexception-class.md)  
            <span data-ttu-id="97c20-112">EsentLogWriteFailException （.）</span><span class="sxs-lookup"><span data-stu-id="97c20-112">Microsoft.Isam.Esent.Interop.EsentLogWriteFailException</span></span>  

<span data-ttu-id="97c20-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="97c20-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="97c20-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="97c20-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="97c20-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="97c20-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLogWriteFailException _
    Inherits EsentIOException
'Usage
Dim instance As EsentLogWriteFailException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLogWriteFailException : EsentIOException
```

## <a name="thread-safety"></a><span data-ttu-id="97c20-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="97c20-116">Thread safety</span></span>

<span data-ttu-id="97c20-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="97c20-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="97c20-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="97c20-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="97c20-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="97c20-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="97c20-120">參考</span><span class="sxs-lookup"><span data-stu-id="97c20-120">Reference</span></span>

[<span data-ttu-id="97c20-121">EsentLogWriteFailException 成員</span><span class="sxs-lookup"><span data-stu-id="97c20-121">EsentLogWriteFailException members</span></span>](./esentlogwritefailexception-members.md)

[<span data-ttu-id="97c20-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="97c20-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
