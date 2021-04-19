---
description: 深入瞭解： JET_INDEXLIST columnidcolumnid 屬性
title: JET_INDEXLIST columnidcolumnid 屬性
TOCTitle: 'columnidcolumnid property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidcolumnid
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist.columnidcolumnid(v=EXCHG.10)
ms:contentKeyID: 55103608
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidcolumnid
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.get_columnidcolumnid
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.set_columnidcolumnid
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidcolumnid
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 53d31fa7e981fce92de8c0c89c77d69acd8fa996
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989074"
---
# <a name="jet_indexlistcolumnidcolumnid-property"></a><span data-ttu-id="9f80c-103">JET_INDEXLIST columnidcolumnid 屬性</span><span class="sxs-lookup"><span data-stu-id="9f80c-103">JET_INDEXLIST.columnidcolumnid property</span></span>

<span data-ttu-id="9f80c-104">取得臨時表中的資料行 columnid，此資料表會儲存正在編制索引之資料行的 columnid。</span><span class="sxs-lookup"><span data-stu-id="9f80c-104">Gets the columnid of the column in the temporary table which stores the columnid of the column being indexed.</span></span> <span data-ttu-id="9f80c-105">資料行的類型為 [Long](./jet-coltyp-enumeration.md)。</span><span class="sxs-lookup"><span data-stu-id="9f80c-105">The column is of type [Long](./jet-coltyp-enumeration.md).</span></span>

<span data-ttu-id="9f80c-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9f80c-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9f80c-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="9f80c-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9f80c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f80c-108">Syntax</span></span>

``` vb
'Declaration
Public Property columnidcolumnid As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_INDEXLIST
Dim value As JET_COLUMNID

value = instance.columnidcolumnid
```

``` csharp
public JET_COLUMNID columnidcolumnid { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="9f80c-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="9f80c-109">Property value</span></span>

<span data-ttu-id="9f80c-110">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9f80c-110">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="9f80c-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9f80c-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9f80c-112">參考</span><span class="sxs-lookup"><span data-stu-id="9f80c-112">Reference</span></span>

[<span data-ttu-id="9f80c-113">JET_INDEXLIST 類別</span><span class="sxs-lookup"><span data-stu-id="9f80c-113">JET_INDEXLIST class</span></span>](./jet-indexlist-class.md)

[<span data-ttu-id="9f80c-114">JET_INDEXLIST 成員</span><span class="sxs-lookup"><span data-stu-id="9f80c-114">JET_INDEXLIST members</span></span>](./jet-indexlist-members.md)

[<span data-ttu-id="9f80c-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="9f80c-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
