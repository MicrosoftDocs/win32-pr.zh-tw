---
description: 深入瞭解： JET_THREADSTATS。減法方法
title: JET_THREADSTATS。 (的 < a0/&gt; < a1/&gt;) 減去方法
TOCTitle: 'Subtract method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Subtract(Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS,Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.subtract(v=EXCHG.10)
ms:contentKeyID: 39514465
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Subtract
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Subtract
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cf1f47258fe965c41b0a02ccbb32712b0a54c97b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985298"
---
# <a name="jet_threadstatssubtract-method"></a><span data-ttu-id="6eabb-103">JET_THREADSTATS。減法方法</span><span class="sxs-lookup"><span data-stu-id="6eabb-103">JET_THREADSTATS.Subtract method</span></span>

<span data-ttu-id="6eabb-104">計算兩個 JET_THREADSTATS 結構之間的統計差異。</span><span class="sxs-lookup"><span data-stu-id="6eabb-104">Calculate the difference in stats between two JET_THREADSTATS structures.</span></span>

<span data-ttu-id="6eabb-105">**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。  </span><span class="sxs-lookup"><span data-stu-id="6eabb-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="6eabb-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="6eabb-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6eabb-107">語法</span><span class="sxs-lookup"><span data-stu-id="6eabb-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function Subtract ( _
    t1 As JET_THREADSTATS, _
    t2 As JET_THREADSTATS _
) As JET_THREADSTATS
'Usage
Dim t1 As JET_THREADSTATS
Dim t2 As JET_THREADSTATS
Dim returnValue As JET_THREADSTATS

returnValue = JET_THREADSTATS.Subtract(t1, t2)
```

``` csharp
public static JET_THREADSTATS Subtract(
    JET_THREADSTATS t1,
    JET_THREADSTATS t2
)
```

#### <a name="parameters"></a><span data-ttu-id="6eabb-108">參數</span><span class="sxs-lookup"><span data-stu-id="6eabb-108">Parameters</span></span>

  - <span data-ttu-id="6eabb-109">t1</span><span class="sxs-lookup"><span data-stu-id="6eabb-109">t1</span></span>  
    <span data-ttu-id="6eabb-110">類型： [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="6eabb-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="6eabb-111">第一個 JET_THREADSTATS。</span><span class="sxs-lookup"><span data-stu-id="6eabb-111">The first JET_THREADSTATS.</span></span>

<!-- end list -->

  - <span data-ttu-id="6eabb-112">t2</span><span class="sxs-lookup"><span data-stu-id="6eabb-112">t2</span></span>  
    <span data-ttu-id="6eabb-113">類型： [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="6eabb-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="6eabb-114">第二個 JET_THREADSTATS。</span><span class="sxs-lookup"><span data-stu-id="6eabb-114">The second JET_THREADSTATS.</span></span>

#### <a name="return-value"></a><span data-ttu-id="6eabb-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="6eabb-115">Return value</span></span>

<span data-ttu-id="6eabb-116">類型： [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="6eabb-116">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
<span data-ttu-id="6eabb-117">JET_THREADSTATS，其中包含 t1 和 t2 之間的統計資料差異。</span><span class="sxs-lookup"><span data-stu-id="6eabb-117">A JET_THREADSTATS containing the difference in stats between t1 and t2.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6eabb-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6eabb-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6eabb-119">參考</span><span class="sxs-lookup"><span data-stu-id="6eabb-119">Reference</span></span>

[<span data-ttu-id="6eabb-120">JET_THREADSTATS 結構</span><span class="sxs-lookup"><span data-stu-id="6eabb-120">JET_THREADSTATS structure</span></span>](./jet-threadstats-structure2.md)

[<span data-ttu-id="6eabb-121">JET_THREADSTATS 成員</span><span class="sxs-lookup"><span data-stu-id="6eabb-121">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="6eabb-122">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="6eabb-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
