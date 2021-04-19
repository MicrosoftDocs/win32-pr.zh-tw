---
description: 深入瞭解： JET_INDEXLIST columnidiColumn 屬性
title: JET_INDEXLIST columnidiColumn 屬性
TOCTitle: 'columnidiColumn property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidiColumn
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist.columnidicolumn(v=EXCHG.10)
ms:contentKeyID: 55103664
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidiColumn
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.get_columnidiColumn
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidiColumn
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.set_columnidiColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2759c04b60c15d5786306ec536c7eddb89b02172
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983802"
---
# <a name="jet_indexlistcolumnidicolumn-property"></a><span data-ttu-id="36d57-103">JET_INDEXLIST columnidiColumn 屬性</span><span class="sxs-lookup"><span data-stu-id="36d57-103">JET_INDEXLIST.columnidiColumn property</span></span>

<span data-ttu-id="36d57-104">取得臨時表中的資料行 columnid，此資料表會將此資料行的索引儲存在索引鍵中。</span><span class="sxs-lookup"><span data-stu-id="36d57-104">Gets the columnid of the column in the temporary table which stores the index of of this column in the index key.</span></span> <span data-ttu-id="36d57-105">資料行的類型為 [Long](./jet-coltyp-enumeration.md)。</span><span class="sxs-lookup"><span data-stu-id="36d57-105">The column is of type [Long](./jet-coltyp-enumeration.md).</span></span>

<span data-ttu-id="36d57-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="36d57-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="36d57-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="36d57-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="36d57-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="36d57-108">Syntax</span></span>

``` vb
'Declaration
Public Property columnidiColumn As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_INDEXLIST
Dim value As JET_COLUMNID

value = instance.columnidiColumn
```

``` csharp
public JET_COLUMNID columnidiColumn { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="36d57-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="36d57-109">Property value</span></span>

<span data-ttu-id="36d57-110">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="36d57-110">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="36d57-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="36d57-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="36d57-112">參考</span><span class="sxs-lookup"><span data-stu-id="36d57-112">Reference</span></span>

[<span data-ttu-id="36d57-113">JET_INDEXLIST 類別</span><span class="sxs-lookup"><span data-stu-id="36d57-113">JET_INDEXLIST class</span></span>](./jet-indexlist-class.md)

[<span data-ttu-id="36d57-114">JET_INDEXLIST 成員</span><span class="sxs-lookup"><span data-stu-id="36d57-114">JET_INDEXLIST members</span></span>](./jet-indexlist-members.md)

[<span data-ttu-id="36d57-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="36d57-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
