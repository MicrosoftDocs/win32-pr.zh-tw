---
description: 深入瞭解： JET_SNPROG cunitTotal 屬性
title: JET_SNPROG cunitTotal 屬性
TOCTitle: 'cunitTotal property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_SNPROG.cunitTotal
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_snprog.cunittotal(v=EXCHG.10)
ms:contentKeyID: 55103955
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SNPROG.cunitTotal
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SNPROG.set_cunitTotal
- Microsoft.Isam.Esent.Interop.JET_SNPROG.cunitTotal
- Microsoft.Isam.Esent.Interop.JET_SNPROG.get_cunitTotal
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 983e07dd56dd75b374a6e869f5614662ad92d5a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973607"
---
# <a name="jet_snprogcunittotal-property"></a><span data-ttu-id="3303f-103">JET_SNPROG cunitTotal 屬性</span><span class="sxs-lookup"><span data-stu-id="3303f-103">JET_SNPROG.cunitTotal property</span></span>

<span data-ttu-id="3303f-104">取得需要完成的工作單位數目。</span><span class="sxs-lookup"><span data-stu-id="3303f-104">Gets the number of work units that need to be completed.</span></span> <span data-ttu-id="3303f-105">此值一律會大於或等於 cunitDone。</span><span class="sxs-lookup"><span data-stu-id="3303f-105">This value will always be bigger than or equal to cunitDone.</span></span>

<span data-ttu-id="3303f-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3303f-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3303f-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="3303f-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3303f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3303f-108">Syntax</span></span>

``` vb
'Declaration
Public Property cunitTotal As Integer
    Get
    Friend Set
'Usage
Dim instance As JET_SNPROG
Dim value As Integer

value = instance.cunitTotal
```

``` csharp
public int cunitTotal { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="3303f-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="3303f-109">Property value</span></span>

<span data-ttu-id="3303f-110">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="3303f-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="3303f-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3303f-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3303f-112">參考</span><span class="sxs-lookup"><span data-stu-id="3303f-112">Reference</span></span>

[<span data-ttu-id="3303f-113">JET_SNPROG 類別</span><span class="sxs-lookup"><span data-stu-id="3303f-113">JET_SNPROG class</span></span>](./jet-snprog-class.md)

[<span data-ttu-id="3303f-114">JET_SNPROG 成員</span><span class="sxs-lookup"><span data-stu-id="3303f-114">JET_SNPROG members</span></span>](./jet-snprog-members.md)

[<span data-ttu-id="3303f-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="3303f-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
