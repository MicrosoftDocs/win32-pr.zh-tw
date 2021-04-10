---
description: 深入瞭解： JET_INDEX_RANGE endColumns 屬性
title: EndColumns 屬性 (Windows8) 的 JET_INDEX_RANGE。
TOCTitle: 'endColumns property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_RANGE.endColumns
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_index_range.endcolumns(v=EXCHG.10)
ms:contentKeyID: 55107824
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_RANGE.endColumns
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_RANGE.set_endColumns
- Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_RANGE.endColumns
- Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_RANGE.get_endColumns
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3053221089c68463db1e3f6268b8aa0dc03902a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194607"
---
# <a name="jet_index_rangeendcolumns-property"></a><span data-ttu-id="5eb03-103">JET_INDEX_RANGE endColumns 屬性</span><span class="sxs-lookup"><span data-stu-id="5eb03-103">JET_INDEX_RANGE.endColumns property</span></span>

<span data-ttu-id="5eb03-104">取得或設定索引結尾的資料行值。</span><span class="sxs-lookup"><span data-stu-id="5eb03-104">Gets or sets the column values for the end of the index.</span></span>

<span data-ttu-id="5eb03-105">**命名空間：**  [Microsoft Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5eb03-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="5eb03-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="5eb03-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5eb03-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5eb03-107">Syntax</span></span>

``` vb
'Declaration
Public Property endColumns As JET_INDEX_COLUMN()
    Get
    Set
'Usage
Dim instance As JET_INDEX_RANGE
Dim value As JET_INDEX_COLUMN()

value = instance.endColumns

instance.endColumns = value
```

``` csharp
public JET_INDEX_COLUMN[] endColumns { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="5eb03-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="5eb03-108">Property value</span></span>

<span data-ttu-id="5eb03-109">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="5eb03-109">Type: \[\]</span></span>  

## <a name="see-also"></a><span data-ttu-id="5eb03-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5eb03-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5eb03-111">參考</span><span class="sxs-lookup"><span data-stu-id="5eb03-111">Reference</span></span>

[<span data-ttu-id="5eb03-112">JET_INDEX_RANGE 類別</span><span class="sxs-lookup"><span data-stu-id="5eb03-112">JET_INDEX_RANGE class</span></span>](./jet-index-range-class.md)

[<span data-ttu-id="5eb03-113">JET_INDEX_RANGE 成員</span><span class="sxs-lookup"><span data-stu-id="5eb03-113">JET_INDEX_RANGE members</span></span>](./jet-index-range-members.md)

[<span data-ttu-id="5eb03-114">Windows8 命名空間。</span><span class="sxs-lookup"><span data-stu-id="5eb03-114">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
