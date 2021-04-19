---
description: 深入瞭解： JET_INDEXLIST columnidgrbitColumn 屬性
title: JET_INDEXLIST columnidgrbitColumn 屬性
TOCTitle: 'columnidgrbitColumn property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidgrbitColumn
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist.columnidgrbitcolumn(v=EXCHG.10)
ms:contentKeyID: 55103665
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidgrbitColumn
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.get_columnidgrbitColumn
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.set_columnidgrbitColumn
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidgrbitColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 18be8455f2618265d77991b7c839f21ff04ef497
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996902"
---
# <a name="jet_indexlistcolumnidgrbitcolumn-property"></a><span data-ttu-id="b53a4-103">JET_INDEXLIST columnidgrbitColumn 屬性</span><span class="sxs-lookup"><span data-stu-id="b53a4-103">JET_INDEXLIST.columnidgrbitColumn property</span></span>

<span data-ttu-id="b53a4-104">取得臨時表中的資料行 columnid，此資料表會儲存套用至索引資料行的 grbit。</span><span class="sxs-lookup"><span data-stu-id="b53a4-104">Gets the columnid of the column in the temporary table which stores the grbit that apply to the indexed column.</span></span> <span data-ttu-id="b53a4-105">請參閱 [IndexKeyGrbit](./indexkeygrbit-enumeration.md)。</span><span class="sxs-lookup"><span data-stu-id="b53a4-105">See [IndexKeyGrbit](./indexkeygrbit-enumeration.md).</span></span> <span data-ttu-id="b53a4-106">資料行的類型為 [Long](./jet-coltyp-enumeration.md)。</span><span class="sxs-lookup"><span data-stu-id="b53a4-106">The column is of type [Long](./jet-coltyp-enumeration.md).</span></span>

<span data-ttu-id="b53a4-107">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b53a4-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b53a4-108">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="b53a4-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b53a4-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b53a4-109">Syntax</span></span>

``` vb
'Declaration
Public Property columnidgrbitColumn As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_INDEXLIST
Dim value As JET_COLUMNID

value = instance.columnidgrbitColumn
```

``` csharp
public JET_COLUMNID columnidgrbitColumn { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="b53a4-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="b53a4-110">Property value</span></span>

<span data-ttu-id="b53a4-111">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b53a4-111">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="b53a4-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b53a4-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b53a4-113">參考</span><span class="sxs-lookup"><span data-stu-id="b53a4-113">Reference</span></span>

[<span data-ttu-id="b53a4-114">JET_INDEXLIST 類別</span><span class="sxs-lookup"><span data-stu-id="b53a4-114">JET_INDEXLIST class</span></span>](./jet-indexlist-class.md)

[<span data-ttu-id="b53a4-115">JET_INDEXLIST 成員</span><span class="sxs-lookup"><span data-stu-id="b53a4-115">JET_INDEXLIST members</span></span>](./jet-indexlist-members.md)

[<span data-ttu-id="b53a4-116">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="b53a4-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
