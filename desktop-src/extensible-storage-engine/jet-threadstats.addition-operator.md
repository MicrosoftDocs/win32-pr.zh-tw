---
description: 深入瞭解： JET_THREADSTATS。加法運算子
title: JET_THREADSTATS。 (，) 的加法運算子
TOCTitle: 'Addition operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.op_Addition(Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS,Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.op_addition(v=EXCHG.10)
ms:contentKeyID: 39516195
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Addition
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Addition
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.op_Addition
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 829bf96b3c7095b95644db220a5d18c7e987e44b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988490"
---
# <a name="jet_threadstatsaddition-operator"></a><span data-ttu-id="897ae-103">JET_THREADSTATS。加法運算子</span><span class="sxs-lookup"><span data-stu-id="897ae-103">JET_THREADSTATS.Addition operator</span></span>

<span data-ttu-id="897ae-104">將統計資料新增至兩個 JET_THREADSTATS 結構。</span><span class="sxs-lookup"><span data-stu-id="897ae-104">Add the stats in two JET_THREADSTATS structures.</span></span>

<span data-ttu-id="897ae-105">**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。  </span><span class="sxs-lookup"><span data-stu-id="897ae-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="897ae-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="897ae-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="897ae-107">語法</span><span class="sxs-lookup"><span data-stu-id="897ae-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator + ( _
    t1 As JET_THREADSTATS, _
    t2 As JET_THREADSTATS _
) As JET_THREADSTATS
'Usage
Dim t1 As JET_THREADSTATS
Dim t2 As JET_THREADSTATS
Dim returnValue As JET_THREADSTATS

returnValue = (t1 + t2)
```

``` csharp
public static JET_THREADSTATS operator +(
    JET_THREADSTATS t1,
    JET_THREADSTATS t2
)
```

#### <a name="parameters"></a><span data-ttu-id="897ae-108">參數</span><span class="sxs-lookup"><span data-stu-id="897ae-108">Parameters</span></span>

  - <span data-ttu-id="897ae-109">t1</span><span class="sxs-lookup"><span data-stu-id="897ae-109">t1</span></span>  
    <span data-ttu-id="897ae-110">類型： [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="897ae-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="897ae-111">第一個 JET_THREADSTATS。</span><span class="sxs-lookup"><span data-stu-id="897ae-111">The first JET_THREADSTATS.</span></span>

<!-- end list -->

  - <span data-ttu-id="897ae-112">t2</span><span class="sxs-lookup"><span data-stu-id="897ae-112">t2</span></span>  
    <span data-ttu-id="897ae-113">類型： [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="897ae-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="897ae-114">第二個 JET_THREADSTATS。</span><span class="sxs-lookup"><span data-stu-id="897ae-114">The second JET_THREADSTATS.</span></span>

#### <a name="return-value"></a><span data-ttu-id="897ae-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="897ae-115">Return value</span></span>

<span data-ttu-id="897ae-116">類型： [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="897ae-116">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
<span data-ttu-id="897ae-117">JET_THREADSTATS，其中包含在 t1 和 t2 中新增統計資料的結果。</span><span class="sxs-lookup"><span data-stu-id="897ae-117">A JET_THREADSTATS containing the result of adding the stats in t1 and t2.</span></span>  

## <a name="see-also"></a><span data-ttu-id="897ae-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="897ae-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="897ae-119">參考</span><span class="sxs-lookup"><span data-stu-id="897ae-119">Reference</span></span>

[<span data-ttu-id="897ae-120">JET_THREADSTATS 結構</span><span class="sxs-lookup"><span data-stu-id="897ae-120">JET_THREADSTATS structure</span></span>](./jet-threadstats-structure2.md)

[<span data-ttu-id="897ae-121">JET_THREADSTATS 成員</span><span class="sxs-lookup"><span data-stu-id="897ae-121">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="897ae-122">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="897ae-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
