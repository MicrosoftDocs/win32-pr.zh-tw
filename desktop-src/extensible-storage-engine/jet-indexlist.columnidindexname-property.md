---
description: 深入瞭解： JET_INDEXLIST columnidindexname 屬性
title: JET_INDEXLIST columnidindexname 屬性
TOCTitle: 'columnidindexname property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidindexname
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist.columnidindexname(v=EXCHG.10)
ms:contentKeyID: 55103619
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidindexname
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.get_columnidindexname
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidindexname
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.set_columnidindexname
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ebda018b294ba87f48b7cc6b0e48b7c3d9ac39b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115849"
---
# <a name="jet_indexlistcolumnidindexname-property"></a><span data-ttu-id="eee9d-103">JET_INDEXLIST columnidindexname 屬性</span><span class="sxs-lookup"><span data-stu-id="eee9d-103">JET_INDEXLIST.columnidindexname property</span></span>

<span data-ttu-id="eee9d-104">取得臨時表中儲存索引名稱之資料行的 columnid。</span><span class="sxs-lookup"><span data-stu-id="eee9d-104">Gets the columnid of the column in the temporary table which stores the name of the index.</span></span> <span data-ttu-id="eee9d-105">資料行的類型為 [Text](./jet-coltyp-enumeration.md)。</span><span class="sxs-lookup"><span data-stu-id="eee9d-105">The column is of type [Text](./jet-coltyp-enumeration.md).</span></span>

<span data-ttu-id="eee9d-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="eee9d-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="eee9d-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="eee9d-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="eee9d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="eee9d-108">Syntax</span></span>

``` vb
'Declaration
Public Property columnidindexname As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_INDEXLIST
Dim value As JET_COLUMNID

value = instance.columnidindexname
```

``` csharp
public JET_COLUMNID columnidindexname { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="eee9d-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="eee9d-109">Property value</span></span>

<span data-ttu-id="eee9d-110">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="eee9d-110">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="eee9d-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eee9d-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="eee9d-112">參考</span><span class="sxs-lookup"><span data-stu-id="eee9d-112">Reference</span></span>

[<span data-ttu-id="eee9d-113">JET_INDEXLIST 類別</span><span class="sxs-lookup"><span data-stu-id="eee9d-113">JET_INDEXLIST class</span></span>](./jet-indexlist-class.md)

[<span data-ttu-id="eee9d-114">JET_INDEXLIST 成員</span><span class="sxs-lookup"><span data-stu-id="eee9d-114">JET_INDEXLIST members</span></span>](./jet-indexlist-members.md)

[<span data-ttu-id="eee9d-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="eee9d-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
