---
description: 深入瞭解： JET_DBINFOMISC lgposConsistent 屬性
title: JET_DBINFOMISC lgposConsistent 屬性
TOCTitle: 'lgposConsistent property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.lgposConsistent
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc.lgposconsistent(v=EXCHG.10)
ms:contentKeyID: 39516221
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.lgposConsistent
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.get_lgposConsistent
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.lgposConsistent
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.set_lgposConsistent
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3549e02b99b70f0704cd716410123dd732b1e518
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112120"
---
# <a name="jet_dbinfomisclgposconsistent-property"></a><span data-ttu-id="be731-103">JET_DBINFOMISC lgposConsistent 屬性</span><span class="sxs-lookup"><span data-stu-id="be731-103">JET_DBINFOMISC.lgposConsistent property</span></span>

<span data-ttu-id="be731-104">取得資料庫保持一致時的 lgpo。</span><span class="sxs-lookup"><span data-stu-id="be731-104">Gets the lgpos when the database was made consistent.</span></span> <span data-ttu-id="be731-105">如果資料庫不一致，則此值為 null。</span><span class="sxs-lookup"><span data-stu-id="be731-105">This value is null if the database is inconsistent.</span></span>

<span data-ttu-id="be731-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="be731-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="be731-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="be731-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="be731-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="be731-108">Syntax</span></span>

``` vb
'Declaration
Public Property lgposConsistent As JET_LGPOS
    Get
    Friend Set
'Usage
Dim instance As JET_DBINFOMISC
Dim value As JET_LGPOS

value = instance.lgposConsistent
```

``` csharp
public JET_LGPOS lgposConsistent { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="be731-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="be731-109">Property value</span></span>

<span data-ttu-id="be731-110">類型： [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="be731-110">Type: [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="be731-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="be731-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="be731-112">參考</span><span class="sxs-lookup"><span data-stu-id="be731-112">Reference</span></span>

[<span data-ttu-id="be731-113">JET_DBINFOMISC 類別</span><span class="sxs-lookup"><span data-stu-id="be731-113">JET_DBINFOMISC class</span></span>](./jet-dbinfomisc-class.md)

[<span data-ttu-id="be731-114">JET_DBINFOMISC 成員</span><span class="sxs-lookup"><span data-stu-id="be731-114">JET_DBINFOMISC members</span></span>](./jet-dbinfomisc-members.md)

[<span data-ttu-id="be731-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="be731-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
