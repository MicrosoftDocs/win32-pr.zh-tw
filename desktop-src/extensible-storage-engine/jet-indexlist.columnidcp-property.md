---
description: 深入瞭解： JET_INDEXLIST columnidCp 屬性
title: JET_INDEXLIST columnidCp 屬性
TOCTitle: 'columnidCp property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidCp
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist.columnidcp(v=EXCHG.10)
ms:contentKeyID: 55103663
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidCp
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.set_columnidCp
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidCp
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.get_columnidCp
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 80afdce5014edf1678807afd40beff613ca9e4ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193832"
---
# <a name="jet_indexlistcolumnidcp-property"></a><span data-ttu-id="9baba-103">JET_INDEXLIST columnidCp 屬性</span><span class="sxs-lookup"><span data-stu-id="9baba-103">JET_INDEXLIST.columnidCp property</span></span>

<span data-ttu-id="9baba-104">取得臨時表中的資料行 columnid，此資料表會儲存已編制索引之資料行的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="9baba-104">Gets the columnid of the column in the temporary table which stores the code page of the indexed column.</span></span> <span data-ttu-id="9baba-105">資料行的類型為 [Short](./jet-coltyp-enumeration.md)。</span><span class="sxs-lookup"><span data-stu-id="9baba-105">The column is of type [Short](./jet-coltyp-enumeration.md).</span></span>

<span data-ttu-id="9baba-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9baba-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9baba-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="9baba-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9baba-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9baba-108">Syntax</span></span>

``` vb
'Declaration
Public Property columnidCp As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_INDEXLIST
Dim value As JET_COLUMNID

value = instance.columnidCp
```

``` csharp
public JET_COLUMNID columnidCp { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="9baba-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="9baba-109">Property value</span></span>

<span data-ttu-id="9baba-110">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9baba-110">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="9baba-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9baba-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9baba-112">參考</span><span class="sxs-lookup"><span data-stu-id="9baba-112">Reference</span></span>

[<span data-ttu-id="9baba-113">JET_INDEXLIST 類別</span><span class="sxs-lookup"><span data-stu-id="9baba-113">JET_INDEXLIST class</span></span>](./jet-indexlist-class.md)

[<span data-ttu-id="9baba-114">JET_INDEXLIST 成員</span><span class="sxs-lookup"><span data-stu-id="9baba-114">JET_INDEXLIST members</span></span>](./jet-indexlist-members.md)

[<span data-ttu-id="9baba-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="9baba-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
