---
description: 深入瞭解： JET_THREADSTATS。新增方法
title: 'JET_THREADSTATS。將方法新增 (的 < a0/&gt; < a1/&gt;) '
TOCTitle: 'Add method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Add(Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS,Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.add(v=EXCHG.10)
ms:contentKeyID: 39514259
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Add
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Add
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2a824249fde43de92c65d64d02fbab4097b7dc34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970758"
---
# <a name="jet_threadstatsadd-method"></a><span data-ttu-id="b6df3-103">JET_THREADSTATS。新增方法</span><span class="sxs-lookup"><span data-stu-id="b6df3-103">JET_THREADSTATS.Add method</span></span>

<span data-ttu-id="b6df3-104">將統計資料新增至兩個 JET_THREADSTATS 結構。</span><span class="sxs-lookup"><span data-stu-id="b6df3-104">Add the stats in two JET_THREADSTATS structures.</span></span>

<span data-ttu-id="b6df3-105">**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。  </span><span class="sxs-lookup"><span data-stu-id="b6df3-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="b6df3-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="b6df3-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b6df3-107">語法</span><span class="sxs-lookup"><span data-stu-id="b6df3-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function Add ( _
    t1 As JET_THREADSTATS, _
    t2 As JET_THREADSTATS _
) As JET_THREADSTATS
'Usage
Dim t1 As JET_THREADSTATS
Dim t2 As JET_THREADSTATS
Dim returnValue As JET_THREADSTATS

returnValue = JET_THREADSTATS.Add(t1, t2)
```

``` csharp
public static JET_THREADSTATS Add(
    JET_THREADSTATS t1,
    JET_THREADSTATS t2
)
```

#### <a name="parameters"></a><span data-ttu-id="b6df3-108">參數</span><span class="sxs-lookup"><span data-stu-id="b6df3-108">Parameters</span></span>

  - <span data-ttu-id="b6df3-109">t1</span><span class="sxs-lookup"><span data-stu-id="b6df3-109">t1</span></span>  
    <span data-ttu-id="b6df3-110">類型： [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="b6df3-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="b6df3-111">第一個 JET_THREADSTATS。</span><span class="sxs-lookup"><span data-stu-id="b6df3-111">The first JET_THREADSTATS.</span></span>

<!-- end list -->

  - <span data-ttu-id="b6df3-112">t2</span><span class="sxs-lookup"><span data-stu-id="b6df3-112">t2</span></span>  
    <span data-ttu-id="b6df3-113">類型： [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="b6df3-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="b6df3-114">第二個 JET_THREADSTATS。</span><span class="sxs-lookup"><span data-stu-id="b6df3-114">The second JET_THREADSTATS.</span></span>

#### <a name="return-value"></a><span data-ttu-id="b6df3-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="b6df3-115">Return value</span></span>

<span data-ttu-id="b6df3-116">類型： [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="b6df3-116">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
<span data-ttu-id="b6df3-117">JET_THREADSTATS，其中包含在 t1 和 t2 中新增統計資料的結果。</span><span class="sxs-lookup"><span data-stu-id="b6df3-117">A JET_THREADSTATS containing the result of adding the stats in t1 and t2.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b6df3-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b6df3-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b6df3-119">參考</span><span class="sxs-lookup"><span data-stu-id="b6df3-119">Reference</span></span>

[<span data-ttu-id="b6df3-120">JET_THREADSTATS 結構</span><span class="sxs-lookup"><span data-stu-id="b6df3-120">JET_THREADSTATS structure</span></span>](./jet-threadstats-structure2.md)

[<span data-ttu-id="b6df3-121">JET_THREADSTATS 成員</span><span class="sxs-lookup"><span data-stu-id="b6df3-121">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="b6df3-122">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="b6df3-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
