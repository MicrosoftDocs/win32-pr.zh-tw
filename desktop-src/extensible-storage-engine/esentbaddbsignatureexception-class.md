---
description: 深入瞭解： EsentBadDbSignatureException 類別
title: EsentBadDbSignatureException 類別
TOCTitle: EsentBadDbSignatureException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentBadDbSignatureException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentbaddbsignatureexception(v=EXCHG.10)
ms:contentKeyID: 55107255
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentBadDbSignatureException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentBadDbSignatureException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5c0adf077cf0665c6bee2246c66af882a397c46b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987647"
---
# <a name="esentbaddbsignatureexception-class"></a><span data-ttu-id="28dce-103">EsentBadDbSignatureException 類別</span><span class="sxs-lookup"><span data-stu-id="28dce-103">EsentBadDbSignatureException class</span></span>

<span data-ttu-id="28dce-104">JET_err 的基類。BadDbSignature 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="28dce-104">Base class for JET_err.BadDbSignature exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="28dce-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="28dce-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="28dce-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="28dce-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="28dce-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="28dce-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="28dce-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="28dce-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="28dce-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="28dce-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="28dce-110">EsentApiException （.）</span><span class="sxs-lookup"><span data-stu-id="28dce-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="28dce-111">EsentObsoleteException （.）</span><span class="sxs-lookup"><span data-stu-id="28dce-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="28dce-112">EsentBadDbSignatureException （.）</span><span class="sxs-lookup"><span data-stu-id="28dce-112">Microsoft.Isam.Esent.Interop.EsentBadDbSignatureException</span></span>  

<span data-ttu-id="28dce-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="28dce-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="28dce-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="28dce-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="28dce-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="28dce-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentBadDbSignatureException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentBadDbSignatureException
```

``` csharp
[SerializableAttribute]
public sealed class EsentBadDbSignatureException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="28dce-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="28dce-116">Thread safety</span></span>

<span data-ttu-id="28dce-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="28dce-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="28dce-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="28dce-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="28dce-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="28dce-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="28dce-120">參考</span><span class="sxs-lookup"><span data-stu-id="28dce-120">Reference</span></span>

[<span data-ttu-id="28dce-121">EsentBadDbSignatureException 成員</span><span class="sxs-lookup"><span data-stu-id="28dce-121">EsentBadDbSignatureException members</span></span>](./esentbaddbsignatureexception-members.md)

[<span data-ttu-id="28dce-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="28dce-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
