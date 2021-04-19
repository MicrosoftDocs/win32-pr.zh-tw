---
description: 深入瞭解： JET_THREADSTATS。等號比較運算子
title: 'JET_THREADSTATS。等號比較運算子 (的) '
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.op_Equality(Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS,Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.op_equality(v=EXCHG.10)
ms:contentKeyID: 39515069
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Equality
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.op_Equality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 076ae2cfa25f446d8d6200fbee7f53ecf0edea5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989977"
---
# <a name="jet_threadstatsequality-operator"></a><span data-ttu-id="622c8-103">JET_THREADSTATS。等號比較運算子</span><span class="sxs-lookup"><span data-stu-id="622c8-103">JET_THREADSTATS.Equality operator</span></span>

<span data-ttu-id="622c8-104">判斷 JET_THREADSTATS 的兩個指定實例是否相等。</span><span class="sxs-lookup"><span data-stu-id="622c8-104">Determines whether two specified instances of JET_THREADSTATS are equal.</span></span>

<span data-ttu-id="622c8-105">**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。  </span><span class="sxs-lookup"><span data-stu-id="622c8-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="622c8-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="622c8-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="622c8-107">語法</span><span class="sxs-lookup"><span data-stu-id="622c8-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_THREADSTATS, _
    rhs As JET_THREADSTATS _
) As Boolean
'Usage
Dim lhs As JET_THREADSTATS
Dim rhs As JET_THREADSTATS
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_THREADSTATS lhs,
    JET_THREADSTATS rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="622c8-108">參數</span><span class="sxs-lookup"><span data-stu-id="622c8-108">Parameters</span></span>

  - <span data-ttu-id="622c8-109">lhs</span><span class="sxs-lookup"><span data-stu-id="622c8-109">lhs</span></span>  
    <span data-ttu-id="622c8-110">類型： [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="622c8-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="622c8-111">要比較的第一個執行個體。</span><span class="sxs-lookup"><span data-stu-id="622c8-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="622c8-112">rhs</span><span class="sxs-lookup"><span data-stu-id="622c8-112">rhs</span></span>  
    <span data-ttu-id="622c8-113">類型： [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="622c8-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="622c8-114">要比較的第二個執行個體。</span><span class="sxs-lookup"><span data-stu-id="622c8-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622c8-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="622c8-115">Return value</span></span>

<span data-ttu-id="622c8-116">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="622c8-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="622c8-117">如果兩個實例相等，則為 True。</span><span class="sxs-lookup"><span data-stu-id="622c8-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="622c8-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="622c8-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="622c8-119">參考</span><span class="sxs-lookup"><span data-stu-id="622c8-119">Reference</span></span>

[<span data-ttu-id="622c8-120">JET_THREADSTATS 結構</span><span class="sxs-lookup"><span data-stu-id="622c8-120">JET_THREADSTATS structure</span></span>](./jet-threadstats-structure2.md)

[<span data-ttu-id="622c8-121">JET_THREADSTATS 成員</span><span class="sxs-lookup"><span data-stu-id="622c8-121">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="622c8-122">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="622c8-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
