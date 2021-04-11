---
description: 深入瞭解： JET_THREADSTATS。減法運算子
title: 'JET_THREADSTATS。減法運算子 (的 < a0/&gt; < a1/&gt;) '
TOCTitle: 'Subtraction operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.op_Subtraction(Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS,Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.op_subtraction(v=EXCHG.10)
ms:contentKeyID: 39512217
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Subtraction
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.op_Subtraction
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Subtraction
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5a41455f05b91a582a1d8aae824ca5b426628cf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191131"
---
# <a name="jet_threadstatssubtraction-operator"></a><span data-ttu-id="c73e4-103">JET_THREADSTATS。減法運算子</span><span class="sxs-lookup"><span data-stu-id="c73e4-103">JET_THREADSTATS.Subtraction operator</span></span>

<span data-ttu-id="c73e4-104">計算兩個 JET_THREADSTATS 結構之間的統計差異。</span><span class="sxs-lookup"><span data-stu-id="c73e4-104">Calculate the difference in stats between two JET_THREADSTATS structures.</span></span>

<span data-ttu-id="c73e4-105">**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。  </span><span class="sxs-lookup"><span data-stu-id="c73e4-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="c73e4-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="c73e4-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c73e4-107">語法</span><span class="sxs-lookup"><span data-stu-id="c73e4-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator - ( _
    t1 As JET_THREADSTATS, _
    t2 As JET_THREADSTATS _
) As JET_THREADSTATS
'Usage
Dim t1 As JET_THREADSTATS
Dim t2 As JET_THREADSTATS
Dim returnValue As JET_THREADSTATS

returnValue = (t1 - t2)
```

``` csharp
public static JET_THREADSTATS operator -(
    JET_THREADSTATS t1,
    JET_THREADSTATS t2
)
```

#### <a name="parameters"></a><span data-ttu-id="c73e4-108">參數</span><span class="sxs-lookup"><span data-stu-id="c73e4-108">Parameters</span></span>

  - <span data-ttu-id="c73e4-109">t1</span><span class="sxs-lookup"><span data-stu-id="c73e4-109">t1</span></span>  
    <span data-ttu-id="c73e4-110">類型： [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="c73e4-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="c73e4-111">第一個 JET_THREADSTATS。</span><span class="sxs-lookup"><span data-stu-id="c73e4-111">The first JET_THREADSTATS.</span></span>

<!-- end list -->

  - <span data-ttu-id="c73e4-112">t2</span><span class="sxs-lookup"><span data-stu-id="c73e4-112">t2</span></span>  
    <span data-ttu-id="c73e4-113">類型： [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="c73e4-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="c73e4-114">第二個 JET_THREADSTATS。</span><span class="sxs-lookup"><span data-stu-id="c73e4-114">The second JET_THREADSTATS.</span></span>

#### <a name="return-value"></a><span data-ttu-id="c73e4-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="c73e4-115">Return value</span></span>

<span data-ttu-id="c73e4-116">類型： [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="c73e4-116">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
<span data-ttu-id="c73e4-117">JET_THREADSTATS，其中包含 t1 和 t2 之間的統計資料差異。</span><span class="sxs-lookup"><span data-stu-id="c73e4-117">A JET_THREADSTATS containing the difference in stats between t1 and t2.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c73e4-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c73e4-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c73e4-119">參考</span><span class="sxs-lookup"><span data-stu-id="c73e4-119">Reference</span></span>

[<span data-ttu-id="c73e4-120">JET_THREADSTATS 結構</span><span class="sxs-lookup"><span data-stu-id="c73e4-120">JET_THREADSTATS structure</span></span>](./jet-threadstats-structure2.md)

[<span data-ttu-id="c73e4-121">JET_THREADSTATS 成員</span><span class="sxs-lookup"><span data-stu-id="c73e4-121">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="c73e4-122">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="c73e4-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
