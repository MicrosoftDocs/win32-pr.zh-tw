---
description: 深入瞭解： JET_DBINFOMISC logtimeConsistent 屬性
title: JET_DBINFOMISC logtimeConsistent 屬性
TOCTitle: 'logtimeConsistent property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.logtimeConsistent
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc.logtimeconsistent(v=EXCHG.10)
ms:contentKeyID: 39513228
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.logtimeConsistent
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.logtimeConsistent
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.get_logtimeConsistent
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.set_logtimeConsistent
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d46302373df17e147095c5ac5c37f02ffef1eb4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112117"
---
# <a name="jet_dbinfomisclogtimeconsistent-property"></a><span data-ttu-id="3f573-103">JET_DBINFOMISC logtimeConsistent 屬性</span><span class="sxs-lookup"><span data-stu-id="3f573-103">JET_DBINFOMISC.logtimeConsistent property</span></span>

<span data-ttu-id="3f573-104">取得資料庫建立一致的時間。</span><span class="sxs-lookup"><span data-stu-id="3f573-104">Gets the time when the database was made consistent.</span></span> <span data-ttu-id="3f573-105">如果資料庫不一致，則此值為 null。</span><span class="sxs-lookup"><span data-stu-id="3f573-105">This value is null if the database is inconsistent.</span></span>

<span data-ttu-id="3f573-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3f573-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3f573-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="3f573-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3f573-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f573-108">Syntax</span></span>

``` vb
'Declaration
Public Property logtimeConsistent As JET_LOGTIME
    Get
    Friend Set
'Usage
Dim instance As JET_DBINFOMISC
Dim value As JET_LOGTIME

value = instance.logtimeConsistent
```

``` csharp
public JET_LOGTIME logtimeConsistent { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="3f573-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="3f573-109">Property value</span></span>

<span data-ttu-id="3f573-110">類型： [Microsoft.Isam.Esent.Interop.JET_LOGTIME](./jet-logtime-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="3f573-110">Type: [Microsoft.Isam.Esent.Interop.JET_LOGTIME](./jet-logtime-structure2.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="3f573-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3f573-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3f573-112">參考</span><span class="sxs-lookup"><span data-stu-id="3f573-112">Reference</span></span>

[<span data-ttu-id="3f573-113">JET_DBINFOMISC 類別</span><span class="sxs-lookup"><span data-stu-id="3f573-113">JET_DBINFOMISC class</span></span>](./jet-dbinfomisc-class.md)

[<span data-ttu-id="3f573-114">JET_DBINFOMISC 成員</span><span class="sxs-lookup"><span data-stu-id="3f573-114">JET_DBINFOMISC members</span></span>](./jet-dbinfomisc-members.md)

[<span data-ttu-id="3f573-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="3f573-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
