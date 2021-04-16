---
description: 深入瞭解： EsentLinkNotSupportedException 類別
title: EsentLinkNotSupportedException 類別
TOCTitle: EsentLinkNotSupportedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLinkNotSupportedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlinknotsupportedexception(v=EXCHG.10)
ms:contentKeyID: 55102133
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLinkNotSupportedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLinkNotSupportedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a72a8f516e3c3a9c3e2a78f0397442bad9236a6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513456"
---
# <a name="esentlinknotsupportedexception-class"></a><span data-ttu-id="cecbb-103">EsentLinkNotSupportedException 類別</span><span class="sxs-lookup"><span data-stu-id="cecbb-103">EsentLinkNotSupportedException class</span></span>

<span data-ttu-id="cecbb-104">JET_err 的基類。LinkNotSupported 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="cecbb-104">Base class for JET_err.LinkNotSupported exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="cecbb-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="cecbb-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="cecbb-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="cecbb-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="cecbb-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="cecbb-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="cecbb-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="cecbb-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="cecbb-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="cecbb-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="cecbb-110">EsentApiException （.）</span><span class="sxs-lookup"><span data-stu-id="cecbb-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="cecbb-111">EsentObsoleteException （.）</span><span class="sxs-lookup"><span data-stu-id="cecbb-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="cecbb-112">EsentLinkNotSupportedException （.）</span><span class="sxs-lookup"><span data-stu-id="cecbb-112">Microsoft.Isam.Esent.Interop.EsentLinkNotSupportedException</span></span>  

<span data-ttu-id="cecbb-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="cecbb-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="cecbb-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="cecbb-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="cecbb-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="cecbb-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLinkNotSupportedException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentLinkNotSupportedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLinkNotSupportedException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="cecbb-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="cecbb-116">Thread safety</span></span>

<span data-ttu-id="cecbb-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="cecbb-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="cecbb-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="cecbb-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="cecbb-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cecbb-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="cecbb-120">參考</span><span class="sxs-lookup"><span data-stu-id="cecbb-120">Reference</span></span>

[<span data-ttu-id="cecbb-121">EsentLinkNotSupportedException 成員</span><span class="sxs-lookup"><span data-stu-id="cecbb-121">EsentLinkNotSupportedException members</span></span>](./esentlinknotsupportedexception-members.md)

[<span data-ttu-id="cecbb-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="cecbb-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
