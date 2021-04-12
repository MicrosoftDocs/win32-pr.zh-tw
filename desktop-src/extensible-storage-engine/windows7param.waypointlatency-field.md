---
description: 深入瞭解： Windows7Param. WaypointLatency 欄位
title: 'Windows7Param. WaypointLatency 欄位 (欄位，最為理想) '
TOCTitle: WaypointLatency field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Windows7.Windows7Param.WaypointLatency
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows7.windows7param.waypointlatency(v=EXCHG.10)
ms:contentKeyID: 55104440
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows7.Windows7Param.WaypointLatency
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows7.Windows7Param.WaypointLatency
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4c999c288e2eb3ee2eed61795cd446b25ea0fb48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318703"
---
# <a name="windows7paramwaypointlatency-field"></a><span data-ttu-id="d6ae4-103">Windows7Param. WaypointLatency 欄位</span><span class="sxs-lookup"><span data-stu-id="d6ae4-103">Windows7Param.WaypointLatency field</span></span>

<span data-ttu-id="d6ae4-104">此參數會設定 esent 將延遲資料庫排清的記錄檔數目。</span><span class="sxs-lookup"><span data-stu-id="d6ae4-104">This parameter sets the number of logs that esent will defer database flushes for.</span></span> <span data-ttu-id="d6ae4-105">如果失敗導致記錄檔遺失，這可以用來提高資料庫復原能力。</span><span class="sxs-lookup"><span data-stu-id="d6ae4-105">This can be used to increase database recoverability if failures cause logfiles to be lost.</span></span>

<span data-ttu-id="d6ae4-106">**命名空間：**  [Microsoft 最為理想](./microsoft.isam.esent.interop.windows7-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d6ae4-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows7](./microsoft.isam.esent.interop.windows7-namespace.md)</span></span>  
<span data-ttu-id="d6ae4-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="d6ae4-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d6ae4-108">語法</span><span class="sxs-lookup"><span data-stu-id="d6ae4-108">Syntax</span></span>

``` vb
'Declaration
Public Const WaypointLatency As JET_param
'Usage
Dim value As JET_param

value = Windows7Param.WaypointLatency
```

``` csharp
public const JET_param WaypointLatency
```

## <a name="see-also"></a><span data-ttu-id="d6ae4-109">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d6ae4-109">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d6ae4-110">參考</span><span class="sxs-lookup"><span data-stu-id="d6ae4-110">Reference</span></span>

[<span data-ttu-id="d6ae4-111">Windows7Param 類別</span><span class="sxs-lookup"><span data-stu-id="d6ae4-111">Windows7Param class</span></span>](./windows7param-class.md)

[<span data-ttu-id="d6ae4-112">Windows7Param 成員</span><span class="sxs-lookup"><span data-stu-id="d6ae4-112">Windows7Param members</span></span>](./windows7param-members.md)

[<span data-ttu-id="d6ae4-113">最為理想命名空間。</span><span class="sxs-lookup"><span data-stu-id="d6ae4-113">Microsoft.Isam.Esent.Interop.Windows7 namespace</span></span>](./microsoft.isam.esent.interop.windows7-namespace.md)
