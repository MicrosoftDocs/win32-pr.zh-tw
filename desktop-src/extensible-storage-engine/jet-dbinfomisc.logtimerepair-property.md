---
description: 深入瞭解： JET_DBINFOMISC logtimeRepair 屬性
title: JET_DBINFOMISC logtimeRepair 屬性
TOCTitle: 'logtimeRepair property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.logtimeRepair
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc.logtimerepair(v=EXCHG.10)
ms:contentKeyID: 39514541
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.logtimeRepair
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.set_logtimeRepair
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.get_logtimeRepair
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.logtimeRepair
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cb5b890ce082b27ca76842540113c0560c5e122c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106967119"
---
# <a name="jet_dbinfomisclogtimerepair-property"></a><span data-ttu-id="35e3e-103">JET_DBINFOMISC logtimeRepair 屬性</span><span class="sxs-lookup"><span data-stu-id="35e3e-103">JET_DBINFOMISC.logtimeRepair property</span></span>

<span data-ttu-id="35e3e-104">取得上次對此資料庫執行修復的時間。</span><span class="sxs-lookup"><span data-stu-id="35e3e-104">Gets the last time that repair was run against this database.</span></span>

<span data-ttu-id="35e3e-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="35e3e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="35e3e-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="35e3e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="35e3e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="35e3e-107">Syntax</span></span>

``` vb
'Declaration
Public Property logtimeRepair As JET_LOGTIME
    Get
    Friend Set
'Usage
Dim instance As JET_DBINFOMISC
Dim value As JET_LOGTIME

value = instance.logtimeRepair
```

``` csharp
public JET_LOGTIME logtimeRepair { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="35e3e-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="35e3e-108">Property value</span></span>

<span data-ttu-id="35e3e-109">類型： [Microsoft.Isam.Esent.Interop.JET_LOGTIME](./jet-logtime-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="35e3e-109">Type: [Microsoft.Isam.Esent.Interop.JET_LOGTIME](./jet-logtime-structure2.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="35e3e-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="35e3e-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="35e3e-111">參考</span><span class="sxs-lookup"><span data-stu-id="35e3e-111">Reference</span></span>

[<span data-ttu-id="35e3e-112">JET_DBINFOMISC 類別</span><span class="sxs-lookup"><span data-stu-id="35e3e-112">JET_DBINFOMISC class</span></span>](./jet-dbinfomisc-class.md)

[<span data-ttu-id="35e3e-113">JET_DBINFOMISC 成員</span><span class="sxs-lookup"><span data-stu-id="35e3e-113">JET_DBINFOMISC members</span></span>](./jet-dbinfomisc-members.md)

[<span data-ttu-id="35e3e-114">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="35e3e-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
