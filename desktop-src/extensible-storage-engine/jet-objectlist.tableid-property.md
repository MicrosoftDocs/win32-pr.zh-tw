---
description: 深入瞭解： JET_OBJECTLIST tableid 屬性
title: JET_OBJECTLIST tableid 屬性
TOCTitle: 'tableid property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.tableid
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_objectlist.tableid(v=EXCHG.10)
ms:contentKeyID: 55103778
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.tableid
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.set_tableid
- Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.tableid
- Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.get_tableid
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 080d6bd1c46f86d0bb1ab780da2e44a7eb8ae6f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106974307"
---
# <a name="jet_objectlisttableid-property"></a><span data-ttu-id="8c4eb-103">JET_OBJECTLIST tableid 屬性</span><span class="sxs-lookup"><span data-stu-id="8c4eb-103">JET_OBJECTLIST.tableid property</span></span>

<span data-ttu-id="8c4eb-104">取得臨時表的 tableid。</span><span class="sxs-lookup"><span data-stu-id="8c4eb-104">Gets tableid of the temporary table.</span></span> <span data-ttu-id="8c4eb-105">當不再需要資料表時，這應該會關閉。</span><span class="sxs-lookup"><span data-stu-id="8c4eb-105">This should be closed when the table is no longer needed.</span></span>

<span data-ttu-id="8c4eb-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8c4eb-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8c4eb-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="8c4eb-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8c4eb-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c4eb-108">Syntax</span></span>

``` vb
'Declaration
Public Property tableid As JET_TABLEID
    Get
    Friend Set
'Usage
Dim instance As JET_OBJECTLIST
Dim value As JET_TABLEID

value = instance.tableid
```

``` csharp
public JET_TABLEID tableid { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="8c4eb-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="8c4eb-109">Property value</span></span>

<span data-ttu-id="8c4eb-110">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8c4eb-110">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="8c4eb-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8c4eb-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8c4eb-112">參考</span><span class="sxs-lookup"><span data-stu-id="8c4eb-112">Reference</span></span>

[<span data-ttu-id="8c4eb-113">JET_OBJECTLIST 類別</span><span class="sxs-lookup"><span data-stu-id="8c4eb-113">JET_OBJECTLIST class</span></span>](./jet-objectlist-class.md)

[<span data-ttu-id="8c4eb-114">JET_OBJECTLIST 成員</span><span class="sxs-lookup"><span data-stu-id="8c4eb-114">JET_OBJECTLIST members</span></span>](./jet-objectlist-members.md)

[<span data-ttu-id="8c4eb-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="8c4eb-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
