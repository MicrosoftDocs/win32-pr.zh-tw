---
description: 深入瞭解： EsentVersionStoreEntryTooBigException 類別
title: EsentVersionStoreEntryTooBigException 類別
TOCTitle: EsentVersionStoreEntryTooBigException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentVersionStoreEntryTooBigException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentversionstoreentrytoobigexception(v=EXCHG.10)
ms:contentKeyID: 55103188
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentVersionStoreEntryTooBigException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentVersionStoreEntryTooBigException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9a7e33c748b8d9b53d3c6d2ee6b722a6dd4ae831
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996747"
---
# <a name="esentversionstoreentrytoobigexception-class"></a><span data-ttu-id="ef86f-103">EsentVersionStoreEntryTooBigException 類別</span><span class="sxs-lookup"><span data-stu-id="ef86f-103">EsentVersionStoreEntryTooBigException class</span></span>

<span data-ttu-id="ef86f-104">JET_err 的基類。VersionStoreEntryTooBig 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="ef86f-104">Base class for JET_err.VersionStoreEntryTooBig exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="ef86f-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="ef86f-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="ef86f-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="ef86f-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="ef86f-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="ef86f-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="ef86f-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="ef86f-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="ef86f-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="ef86f-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        <span data-ttu-id="ef86f-110">EsentVersionStoreEntryTooBigException （.）</span><span class="sxs-lookup"><span data-stu-id="ef86f-110">Microsoft.Isam.Esent.Interop.EsentVersionStoreEntryTooBigException</span></span>  

<span data-ttu-id="ef86f-111">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ef86f-111">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ef86f-112">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="ef86f-112">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ef86f-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef86f-113">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentVersionStoreEntryTooBigException _
    Inherits EsentErrorException
'Usage
Dim instance As EsentVersionStoreEntryTooBigException
```

``` csharp
[SerializableAttribute]
public sealed class EsentVersionStoreEntryTooBigException : EsentErrorException
```

## <a name="thread-safety"></a><span data-ttu-id="ef86f-114">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="ef86f-114">Thread safety</span></span>

<span data-ttu-id="ef86f-115">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="ef86f-115">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="ef86f-116">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="ef86f-116">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="ef86f-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ef86f-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ef86f-118">參考</span><span class="sxs-lookup"><span data-stu-id="ef86f-118">Reference</span></span>

[<span data-ttu-id="ef86f-119">EsentVersionStoreEntryTooBigException 成員</span><span class="sxs-lookup"><span data-stu-id="ef86f-119">EsentVersionStoreEntryTooBigException members</span></span>](./esentversionstoreentrytoobigexception-members.md)

[<span data-ttu-id="ef86f-120">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="ef86f-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
