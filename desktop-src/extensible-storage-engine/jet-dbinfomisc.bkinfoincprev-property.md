---
description: 深入瞭解： JET_DBINFOMISC bkinfoIncPrev 屬性
title: JET_DBINFOMISC bkinfoIncPrev 屬性
TOCTitle: 'bkinfoIncPrev property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.bkinfoIncPrev
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc.bkinfoincprev(v=EXCHG.10)
ms:contentKeyID: 39510848
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.bkinfoIncPrev
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.get_bkinfoIncPrev
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.set_bkinfoIncPrev
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.bkinfoIncPrev
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d323c9af95a59895b30c55cc0a2a5b2664a1c043
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106999846"
---
# <a name="jet_dbinfomiscbkinfoincprev-property"></a><span data-ttu-id="283b2-103">JET_DBINFOMISC bkinfoIncPrev 屬性</span><span class="sxs-lookup"><span data-stu-id="283b2-103">JET_DBINFOMISC.bkinfoIncPrev property</span></span>

<span data-ttu-id="283b2-104">取得上一次成功增量備份的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="283b2-104">Gets information about the last successful incremental backup.</span></span> <span data-ttu-id="283b2-105">設定 [bkinfoFullPrev](./jet-dbinfomisc.bkinfofullprev-property.md) 時，會重設此值。</span><span class="sxs-lookup"><span data-stu-id="283b2-105">This value is reset when [bkinfoFullPrev](./jet-dbinfomisc.bkinfofullprev-property.md) is set.</span></span>

<span data-ttu-id="283b2-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="283b2-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="283b2-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="283b2-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="283b2-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="283b2-108">Syntax</span></span>

``` vb
'Declaration
Public Property bkinfoIncPrev As JET_BKINFO
    Get
    Friend Set
'Usage
Dim instance As JET_DBINFOMISC
Dim value As JET_BKINFO

value = instance.bkinfoIncPrev
```

``` csharp
public JET_BKINFO bkinfoIncPrev { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="283b2-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="283b2-109">Property value</span></span>

<span data-ttu-id="283b2-110">類型： [Microsoft.Isam.Esent.Interop.JET_BKINFO](./jet-bkinfo-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="283b2-110">Type: [Microsoft.Isam.Esent.Interop.JET_BKINFO](./jet-bkinfo-structure2.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="283b2-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="283b2-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="283b2-112">參考</span><span class="sxs-lookup"><span data-stu-id="283b2-112">Reference</span></span>

[<span data-ttu-id="283b2-113">JET_DBINFOMISC 類別</span><span class="sxs-lookup"><span data-stu-id="283b2-113">JET_DBINFOMISC class</span></span>](./jet-dbinfomisc-class.md)

[<span data-ttu-id="283b2-114">JET_DBINFOMISC 成員</span><span class="sxs-lookup"><span data-stu-id="283b2-114">JET_DBINFOMISC members</span></span>](./jet-dbinfomisc-members.md)

[<span data-ttu-id="283b2-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="283b2-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
