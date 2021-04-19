---
description: 深入瞭解： JET_RECSIZE cLongValues 屬性
title: 'JET_RECSIZE. cLongValues 屬性 (Microsoft. < a0/&gt; < a1/&gt;) '
TOCTitle: 'cLongValues property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cLongValues
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.clongvalues(v=EXCHG.10)
ms:contentKeyID: 39515366
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cLongValues
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.get_cLongValues
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.set_cLongValues
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cLongValues
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2ba70428ccc6ceb1d03fe5109d6bf5c0d17e7831
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973412"
---
# <a name="jet_recsizeclongvalues-property"></a><span data-ttu-id="a26d3-103">JET_RECSIZE cLongValues 屬性</span><span class="sxs-lookup"><span data-stu-id="a26d3-103">JET_RECSIZE.cLongValues property</span></span>

<span data-ttu-id="a26d3-104">取得儲存在此記錄之完整值樹狀結構中的完整值總數。</span><span class="sxs-lookup"><span data-stu-id="a26d3-104">Gets the total number of long values stored in the long-value tree for this record.</span></span> <span data-ttu-id="a26d3-105">這不包含內建的 long 值。</span><span class="sxs-lookup"><span data-stu-id="a26d3-105">This does not include intrinsic long values.</span></span>

<span data-ttu-id="a26d3-106">**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。  </span><span class="sxs-lookup"><span data-stu-id="a26d3-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="a26d3-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="a26d3-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a26d3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a26d3-108">Syntax</span></span>

``` vb
'Declaration
Public Property cLongValues As Long
    Get
    Friend Set
'Usage
Dim instance As JET_RECSIZE
Dim value As Long

value = instance.cLongValues
```

``` csharp
public long cLongValues { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="a26d3-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="a26d3-109">Property value</span></span>

<span data-ttu-id="a26d3-110">類型： [Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="a26d3-110">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  

## <a name="see-also"></a><span data-ttu-id="a26d3-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a26d3-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a26d3-112">參考</span><span class="sxs-lookup"><span data-stu-id="a26d3-112">Reference</span></span>

[<span data-ttu-id="a26d3-113">JET_RECSIZE 結構</span><span class="sxs-lookup"><span data-stu-id="a26d3-113">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="a26d3-114">JET_RECSIZE 成員</span><span class="sxs-lookup"><span data-stu-id="a26d3-114">JET_RECSIZE members</span></span>](./jet-recsize-members.md)

[<span data-ttu-id="a26d3-115">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="a26d3-115">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
