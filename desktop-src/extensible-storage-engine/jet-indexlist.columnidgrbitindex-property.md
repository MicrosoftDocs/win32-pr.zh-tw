---
description: 深入瞭解： JET_INDEXLIST columnidgrbitIndex 屬性
title: JET_INDEXLIST columnidgrbitIndex 屬性
TOCTitle: 'columnidgrbitIndex property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidgrbitIndex
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist.columnidgrbitindex(v=EXCHG.10)
ms:contentKeyID: 55103615
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidgrbitIndex
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidgrbitIndex
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.set_columnidgrbitIndex
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.get_columnidgrbitIndex
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ae8d31661451a2bd1c7c5f942141c27ae552c578
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851028"
---
# <a name="jet_indexlistcolumnidgrbitindex-property"></a><span data-ttu-id="13f76-103">JET_INDEXLIST columnidgrbitIndex 屬性</span><span class="sxs-lookup"><span data-stu-id="13f76-103">JET_INDEXLIST.columnidgrbitIndex property</span></span>

<span data-ttu-id="13f76-104">取得臨時表中的資料行 columnid，此資料表會儲存用於索引的 grbits。</span><span class="sxs-lookup"><span data-stu-id="13f76-104">Gets the columnid of the column in the temporary table which stores the grbits used on the index.</span></span> <span data-ttu-id="13f76-105">請參閱 [CreateIndexGrbit](./createindexgrbit-enumeration.md)。</span><span class="sxs-lookup"><span data-stu-id="13f76-105">See [CreateIndexGrbit](./createindexgrbit-enumeration.md).</span></span> <span data-ttu-id="13f76-106">資料行的類型為 [Long](./jet-coltyp-enumeration.md)。</span><span class="sxs-lookup"><span data-stu-id="13f76-106">The column is of type [Long](./jet-coltyp-enumeration.md).</span></span>

<span data-ttu-id="13f76-107">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="13f76-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="13f76-108">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="13f76-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="13f76-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="13f76-109">Syntax</span></span>

``` vb
'Declaration
Public Property columnidgrbitIndex As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_INDEXLIST
Dim value As JET_COLUMNID

value = instance.columnidgrbitIndex
```

``` csharp
public JET_COLUMNID columnidgrbitIndex { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="13f76-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="13f76-110">Property value</span></span>

<span data-ttu-id="13f76-111">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="13f76-111">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="13f76-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="13f76-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="13f76-113">參考</span><span class="sxs-lookup"><span data-stu-id="13f76-113">Reference</span></span>

[<span data-ttu-id="13f76-114">JET_INDEXLIST 類別</span><span class="sxs-lookup"><span data-stu-id="13f76-114">JET_INDEXLIST class</span></span>](./jet-indexlist-class.md)

[<span data-ttu-id="13f76-115">JET_INDEXLIST 成員</span><span class="sxs-lookup"><span data-stu-id="13f76-115">JET_INDEXLIST members</span></span>](./jet-indexlist-members.md)

[<span data-ttu-id="13f76-116">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="13f76-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
