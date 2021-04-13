---
description: 深入瞭解： EsentPageNotInitializedException 類別
title: EsentPageNotInitializedException 類別
TOCTitle: EsentPageNotInitializedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentPageNotInitializedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentpagenotinitializedexception(v=EXCHG.10)
ms:contentKeyID: 55107308
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentPageNotInitializedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentPageNotInitializedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c349560498993d0920f344ef716835afa8fb62c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320015"
---
# <a name="esentpagenotinitializedexception-class"></a><span data-ttu-id="0741b-103">EsentPageNotInitializedException 類別</span><span class="sxs-lookup"><span data-stu-id="0741b-103">EsentPageNotInitializedException class</span></span>

<span data-ttu-id="0741b-104">JET_err 的基類。PageNotInitialized 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="0741b-104">Base class for JET_err.PageNotInitialized exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="0741b-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="0741b-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="0741b-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="0741b-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="0741b-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="0741b-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="0741b-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="0741b-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="0741b-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="0741b-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="0741b-110">EsentDataException （.）</span><span class="sxs-lookup"><span data-stu-id="0741b-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="0741b-111">EsentCorruptionException （.）</span><span class="sxs-lookup"><span data-stu-id="0741b-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="0741b-112">EsentPageNotInitializedException （.）</span><span class="sxs-lookup"><span data-stu-id="0741b-112">Microsoft.Isam.Esent.Interop.EsentPageNotInitializedException</span></span>  

<span data-ttu-id="0741b-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0741b-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0741b-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="0741b-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0741b-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="0741b-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentPageNotInitializedException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentPageNotInitializedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentPageNotInitializedException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="0741b-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="0741b-116">Thread safety</span></span>

<span data-ttu-id="0741b-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="0741b-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="0741b-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="0741b-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="0741b-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0741b-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0741b-120">參考</span><span class="sxs-lookup"><span data-stu-id="0741b-120">Reference</span></span>

[<span data-ttu-id="0741b-121">EsentPageNotInitializedException 成員</span><span class="sxs-lookup"><span data-stu-id="0741b-121">EsentPageNotInitializedException members</span></span>](./esentpagenotinitializedexception-members.md)

[<span data-ttu-id="0741b-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="0741b-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
