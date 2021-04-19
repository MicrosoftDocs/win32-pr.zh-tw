---
description: 深入瞭解： JET_INDEX_RANGE startColumns 屬性
title: StartColumns 屬性 (Windows8) 的 JET_INDEX_RANGE。
TOCTitle: 'startColumns property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_RANGE.startColumns
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_index_range.startcolumns(v=EXCHG.10)
ms:contentKeyID: 55104437
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_RANGE.startColumns
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_RANGE.get_startColumns
- Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_RANGE.set_startColumns
- Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_RANGE.startColumns
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6bbd80d9cec37131d53d6607b9ff17c59eaf73c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997927"
---
# <a name="jet_index_rangestartcolumns-property"></a><span data-ttu-id="fab3d-103">JET_INDEX_RANGE startColumns 屬性</span><span class="sxs-lookup"><span data-stu-id="fab3d-103">JET_INDEX_RANGE.startColumns property</span></span>

<span data-ttu-id="fab3d-104">取得或設定索引開頭的資料行值。</span><span class="sxs-lookup"><span data-stu-id="fab3d-104">Gets or sets the column values for the start of the index.</span></span>

<span data-ttu-id="fab3d-105">**命名空間：**  [Microsoft Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fab3d-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="fab3d-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="fab3d-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fab3d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="fab3d-107">Syntax</span></span>

``` vb
'Declaration
Public Property startColumns As JET_INDEX_COLUMN()
    Get
    Set
'Usage
Dim instance As JET_INDEX_RANGE
Dim value As JET_INDEX_COLUMN()

value = instance.startColumns

instance.startColumns = value
```

``` csharp
public JET_INDEX_COLUMN[] startColumns { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="fab3d-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="fab3d-108">Property value</span></span>

<span data-ttu-id="fab3d-109">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="fab3d-109">Type: \[\]</span></span>  

## <a name="see-also"></a><span data-ttu-id="fab3d-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fab3d-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fab3d-111">參考</span><span class="sxs-lookup"><span data-stu-id="fab3d-111">Reference</span></span>

[<span data-ttu-id="fab3d-112">JET_INDEX_RANGE 類別</span><span class="sxs-lookup"><span data-stu-id="fab3d-112">JET_INDEX_RANGE class</span></span>](./jet-index-range-class.md)

[<span data-ttu-id="fab3d-113">JET_INDEX_RANGE 成員</span><span class="sxs-lookup"><span data-stu-id="fab3d-113">JET_INDEX_RANGE members</span></span>](./jet-index-range-members.md)

[<span data-ttu-id="fab3d-114">Windows8 命名空間。</span><span class="sxs-lookup"><span data-stu-id="fab3d-114">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
