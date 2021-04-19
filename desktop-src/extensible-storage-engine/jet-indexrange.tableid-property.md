---
description: 深入瞭解： JET_INDEXRANGE tableid 屬性
title: JET_INDEXRANGE tableid 屬性
TOCTitle: 'tableid property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXRANGE.tableid
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexrange.tableid(v=EXCHG.10)
ms:contentKeyID: 55103657
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXRANGE.tableid
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXRANGE.tableid
- Microsoft.Isam.Esent.Interop.JET_INDEXRANGE.set_tableid
- Microsoft.Isam.Esent.Interop.JET_INDEXRANGE.get_tableid
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: afd5c9401b3b0284f463aa1dbd6676440fd64b1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979257"
---
# <a name="jet_indexrangetableid-property"></a><span data-ttu-id="4fd0a-103">JET_INDEXRANGE tableid 屬性</span><span class="sxs-lookup"><span data-stu-id="4fd0a-103">JET_INDEXRANGE.tableid property</span></span>

<span data-ttu-id="4fd0a-104">取得或設定包含索引範圍的資料指標。</span><span class="sxs-lookup"><span data-stu-id="4fd0a-104">Gets or sets the cursor containing the index range.</span></span> <span data-ttu-id="4fd0a-105">資料指標的索引範圍應設定為 JetSetIndexRange。</span><span class="sxs-lookup"><span data-stu-id="4fd0a-105">The cursor should have an index range set with JetSetIndexRange.</span></span>

<span data-ttu-id="4fd0a-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4fd0a-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4fd0a-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="4fd0a-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4fd0a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4fd0a-108">Syntax</span></span>

``` vb
'Declaration
Public Property tableid As JET_TABLEID
    Get
    Set
'Usage
Dim instance As JET_INDEXRANGE
Dim value As JET_TABLEID

value = instance.tableid

instance.tableid = value
```

``` csharp
public JET_TABLEID tableid { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="4fd0a-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="4fd0a-109">Property value</span></span>

<span data-ttu-id="4fd0a-110">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4fd0a-110">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="4fd0a-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4fd0a-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4fd0a-112">參考</span><span class="sxs-lookup"><span data-stu-id="4fd0a-112">Reference</span></span>

[<span data-ttu-id="4fd0a-113">JET_INDEXRANGE 類別</span><span class="sxs-lookup"><span data-stu-id="4fd0a-113">JET_INDEXRANGE class</span></span>](./jet-indexrange-class.md)

[<span data-ttu-id="4fd0a-114">JET_INDEXRANGE 成員</span><span class="sxs-lookup"><span data-stu-id="4fd0a-114">JET_INDEXRANGE members</span></span>](./jet-indexrange-members.md)

[<span data-ttu-id="4fd0a-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="4fd0a-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
