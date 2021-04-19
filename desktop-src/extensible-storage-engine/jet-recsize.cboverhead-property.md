---
description: 深入瞭解： JET_RECSIZE cbOverhead 屬性
title: 'JET_RECSIZE. cbOverhead 屬性 (Microsoft. < a0/&gt; < a1/&gt;) '
TOCTitle: 'cbOverhead property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbOverhead
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.cboverhead(v=EXCHG.10)
ms:contentKeyID: 39514763
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbOverhead
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.get_cbOverhead
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbOverhead
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.set_cbOverhead
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2e7318428ef4b50a08a05f5021d293ad1d8d78cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106984160"
---
# <a name="jet_recsizecboverhead-property"></a><span data-ttu-id="e547c-103">JET_RECSIZE cbOverhead 屬性</span><span class="sxs-lookup"><span data-stu-id="e547c-103">JET_RECSIZE.cbOverhead property</span></span>

<span data-ttu-id="e547c-104">取得此記錄之 ESENT 記錄結構的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="e547c-104">Gets the overhead of the ESENT record structure for this record.</span></span> <span data-ttu-id="e547c-105">這包括記錄的金鑰大小。</span><span class="sxs-lookup"><span data-stu-id="e547c-105">This includes the record's key size.</span></span>

<span data-ttu-id="e547c-106">**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。  </span><span class="sxs-lookup"><span data-stu-id="e547c-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="e547c-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="e547c-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e547c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e547c-108">Syntax</span></span>

``` vb
'Declaration
Public Property cbOverhead As Long
    Get
    Friend Set
'Usage
Dim instance As JET_RECSIZE
Dim value As Long

value = instance.cbOverhead
```

``` csharp
public long cbOverhead { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="e547c-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="e547c-109">Property value</span></span>

<span data-ttu-id="e547c-110">類型： [Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="e547c-110">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  

## <a name="see-also"></a><span data-ttu-id="e547c-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e547c-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e547c-112">參考</span><span class="sxs-lookup"><span data-stu-id="e547c-112">Reference</span></span>

[<span data-ttu-id="e547c-113">JET_RECSIZE 結構</span><span class="sxs-lookup"><span data-stu-id="e547c-113">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="e547c-114">JET_RECSIZE 成員</span><span class="sxs-lookup"><span data-stu-id="e547c-114">JET_RECSIZE members</span></span>](./jet-recsize-members.md)

[<span data-ttu-id="e547c-115">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="e547c-115">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
