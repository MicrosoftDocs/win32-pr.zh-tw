---
description: 深入瞭解： JET_OBJECTLIST columnidflags 屬性
title: JET_OBJECTLIST columnidflags 屬性
TOCTitle: 'columnidflags property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.columnidflags
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_objectlist.columnidflags(v=EXCHG.10)
ms:contentKeyID: 55103772
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.columnidflags
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.columnidflags
- Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.get_columnidflags
- Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.set_columnidflags
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ca7e2be41262578b2c4224ebcc97050b8e27bcec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990492"
---
# <a name="jet_objectlistcolumnidflags-property"></a><span data-ttu-id="8148a-103">JET_OBJECTLIST columnidflags 屬性</span><span class="sxs-lookup"><span data-stu-id="8148a-103">JET_OBJECTLIST.columnidflags property</span></span>

<span data-ttu-id="8148a-104">取得臨時表中的資料行 columnid，其中儲存資料表旗標 (例如系統資料表旗標) 。</span><span class="sxs-lookup"><span data-stu-id="8148a-104">Gets the columnid of the column in the temporary table which stores the table flags (e.g. the system table flag).</span></span>

<span data-ttu-id="8148a-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8148a-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8148a-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="8148a-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8148a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8148a-107">Syntax</span></span>

``` vb
'Declaration
Public Property columnidflags As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_OBJECTLIST
Dim value As JET_COLUMNID

value = instance.columnidflags
```

``` csharp
public JET_COLUMNID columnidflags { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="8148a-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="8148a-108">Property value</span></span>

<span data-ttu-id="8148a-109">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8148a-109">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="8148a-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8148a-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8148a-111">參考</span><span class="sxs-lookup"><span data-stu-id="8148a-111">Reference</span></span>

[<span data-ttu-id="8148a-112">JET_OBJECTLIST 類別</span><span class="sxs-lookup"><span data-stu-id="8148a-112">JET_OBJECTLIST class</span></span>](./jet-objectlist-class.md)

[<span data-ttu-id="8148a-113">JET_OBJECTLIST 成員</span><span class="sxs-lookup"><span data-stu-id="8148a-113">JET_OBJECTLIST members</span></span>](./jet-objectlist-members.md)

[<span data-ttu-id="8148a-114">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="8148a-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
