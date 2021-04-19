---
description: 深入瞭解： VistaApi. JetGetThreadStats 方法
title: 'VistaApi. JetGetThreadStats 方法 (< a0/&gt; < a1/&gt;) '
TOCTitle: 'JetGetThreadStats method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetThreadStats(Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetgetthreadstats(v=EXCHG.10)
ms:contentKeyID: 55104192
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetThreadStats
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetThreadStats
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 92572fd538f0c6c2643e7b40a07ac168ae6980d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982329"
---
# <a name="vistaapijetgetthreadstats-method"></a><span data-ttu-id="85341-103">VistaApi. JetGetThreadStats 方法</span><span class="sxs-lookup"><span data-stu-id="85341-103">VistaApi.JetGetThreadStats method</span></span>

<span data-ttu-id="85341-104">從資料庫引擎抓取目前線程的效能資訊。</span><span class="sxs-lookup"><span data-stu-id="85341-104">Retrieves performance information from the database engine for the current thread.</span></span> <span data-ttu-id="85341-105">您可以使用多個呼叫來收集統計資料，以反映這些呼叫之間的資料庫引擎在此執行緒上的活動。</span><span class="sxs-lookup"><span data-stu-id="85341-105">Multiple calls can be used to collect statistics that reflect the activity of the database engine on this thread between those calls.</span></span>

<span data-ttu-id="85341-106">**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。  </span><span class="sxs-lookup"><span data-stu-id="85341-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="85341-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="85341-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="85341-108">語法</span><span class="sxs-lookup"><span data-stu-id="85341-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetThreadStats ( _
    <OutAttribute> ByRef threadstats As JET_THREADSTATS _
)
'Usage
Dim threadstats As JET_THREADSTATSVistaApi.JetGetThreadStats(threadstats)
```

``` csharp
public static void JetGetThreadStats(
    out JET_THREADSTATS threadstats
)
```

#### <a name="parameters"></a><span data-ttu-id="85341-109">參數</span><span class="sxs-lookup"><span data-stu-id="85341-109">Parameters</span></span>

  - <span data-ttu-id="85341-110">threadstats</span><span class="sxs-lookup"><span data-stu-id="85341-110">threadstats</span></span>  
    <span data-ttu-id="85341-111">類型： [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="85341-111">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="85341-112">傳回執行緒統計資料資料。</span><span class="sxs-lookup"><span data-stu-id="85341-112">Returns the thread statistics data.</span></span>

## <a name="see-also"></a><span data-ttu-id="85341-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="85341-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="85341-114">參考</span><span class="sxs-lookup"><span data-stu-id="85341-114">Reference</span></span>

[<span data-ttu-id="85341-115">VistaApi 類別</span><span class="sxs-lookup"><span data-stu-id="85341-115">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="85341-116">VistaApi 成員</span><span class="sxs-lookup"><span data-stu-id="85341-116">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="85341-117">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="85341-117">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
