---
description: 深入瞭解： JET_OBJECTLIST columnidgrbit 屬性
title: JET_OBJECTLIST columnidgrbit 屬性
TOCTitle: 'columnidgrbit property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.columnidgrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_objectlist.columnidgrbit(v=EXCHG.10)
ms:contentKeyID: 55103774
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.columnidgrbit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.get_columnidgrbit
- Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.columnidgrbit
- Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.set_columnidgrbit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5019e2066c87960db1cf5375e1cfb69575a44528
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978344"
---
# <a name="jet_objectlistcolumnidgrbit-property"></a><span data-ttu-id="f67a2-103">JET_OBJECTLIST columnidgrbit 屬性</span><span class="sxs-lookup"><span data-stu-id="f67a2-103">JET_OBJECTLIST.columnidgrbit property</span></span>

<span data-ttu-id="f67a2-104">取得臨時表中的資料行 columnid，此資料表會儲存建立資料表時所使用的 grbits。</span><span class="sxs-lookup"><span data-stu-id="f67a2-104">Gets the columnid of the column in the temporary table which stores the grbits used when the table was created.</span></span>

<span data-ttu-id="f67a2-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f67a2-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f67a2-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="f67a2-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f67a2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f67a2-107">Syntax</span></span>

``` vb
'Declaration
Public Property columnidgrbit As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_OBJECTLIST
Dim value As JET_COLUMNID

value = instance.columnidgrbit
```

``` csharp
public JET_COLUMNID columnidgrbit { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="f67a2-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="f67a2-108">Property value</span></span>

<span data-ttu-id="f67a2-109">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f67a2-109">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="f67a2-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f67a2-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f67a2-111">參考</span><span class="sxs-lookup"><span data-stu-id="f67a2-111">Reference</span></span>

[<span data-ttu-id="f67a2-112">JET_OBJECTLIST 類別</span><span class="sxs-lookup"><span data-stu-id="f67a2-112">JET_OBJECTLIST class</span></span>](./jet-objectlist-class.md)

[<span data-ttu-id="f67a2-113">JET_OBJECTLIST 成員</span><span class="sxs-lookup"><span data-stu-id="f67a2-113">JET_OBJECTLIST members</span></span>](./jet-objectlist-members.md)

[<span data-ttu-id="f67a2-114">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="f67a2-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
