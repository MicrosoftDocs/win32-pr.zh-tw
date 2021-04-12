---
description: 深入瞭解： JET_RECSIZE cbLongValueDataCompressed 屬性
title: 'JET_RECSIZE. cbLongValueDataCompressed 屬性 (Microsoft. < a0/&gt; < a1/&gt;) '
TOCTitle: 'cbLongValueDataCompressed property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbLongValueDataCompressed
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.cblongvaluedatacompressed(v=EXCHG.10)
ms:contentKeyID: 39515830
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbLongValueDataCompressed
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.get_cbLongValueDataCompressed
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbLongValueDataCompressed
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.set_cbLongValueDataCompressed
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 113bb741287e85ef6f7132cd299202a0b9c2af31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386087"
---
# <a name="jet_recsizecblongvaluedatacompressed-property"></a><span data-ttu-id="15a60-103">JET_RECSIZE cbLongValueDataCompressed 屬性</span><span class="sxs-lookup"><span data-stu-id="15a60-103">JET_RECSIZE.cbLongValueDataCompressed property</span></span>

<span data-ttu-id="15a60-104">取得完整值樹狀結構中使用者資料的壓縮大小。</span><span class="sxs-lookup"><span data-stu-id="15a60-104">Gets the compressed size of user data in the long-value tree.</span></span> <span data-ttu-id="15a60-105">如果沒有壓縮分隔的 long 值，就會與 [cbLongValueData](./jet-recsize.cblongvaluedata-property.md) 相同。</span><span class="sxs-lookup"><span data-stu-id="15a60-105">This is the same as [cbLongValueData](./jet-recsize.cblongvaluedata-property.md) if no separated long values are compressed.</span></span>

<span data-ttu-id="15a60-106">**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。  </span><span class="sxs-lookup"><span data-stu-id="15a60-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="15a60-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="15a60-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="15a60-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="15a60-108">Syntax</span></span>

``` vb
'Declaration
Public Property cbLongValueDataCompressed As Long
    Get
    Friend Set
'Usage
Dim instance As JET_RECSIZE
Dim value As Long

value = instance.cbLongValueDataCompressed
```

``` csharp
public long cbLongValueDataCompressed { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="15a60-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="15a60-109">Property value</span></span>

<span data-ttu-id="15a60-110">類型： [Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="15a60-110">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  

## <a name="see-also"></a><span data-ttu-id="15a60-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="15a60-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="15a60-112">參考</span><span class="sxs-lookup"><span data-stu-id="15a60-112">Reference</span></span>

[<span data-ttu-id="15a60-113">JET_RECSIZE 結構</span><span class="sxs-lookup"><span data-stu-id="15a60-113">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="15a60-114">JET_RECSIZE 成員</span><span class="sxs-lookup"><span data-stu-id="15a60-114">JET_RECSIZE members</span></span>](./jet-recsize-members.md)

[<span data-ttu-id="15a60-115">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="15a60-115">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
