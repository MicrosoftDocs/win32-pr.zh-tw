---
description: 深入瞭解： JET_BKLOGTIME。不等比較運算子
title: JET_BKLOGTIME。不等比較運算子
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.op_Inequality(Microsoft.Isam.Esent.Interop.JET_BKLOGTIME,Microsoft.Isam.Esent.Interop.JET_BKLOGTIME)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_bklogtime.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39512908
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.Inequality
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.op_Inequality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 42f13a1068543caaa590015151b523c1a441c806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997192"
---
# <a name="jet_bklogtimeinequality-operator"></a><span data-ttu-id="0a5d7-103">JET_BKLOGTIME。不等比較運算子</span><span class="sxs-lookup"><span data-stu-id="0a5d7-103">JET_BKLOGTIME.Inequality operator</span></span>

<span data-ttu-id="0a5d7-104">判斷 JET_BKLOGTIME 的兩個指定實例是否不相等。</span><span class="sxs-lookup"><span data-stu-id="0a5d7-104">Determines whether two specified instances of JET_BKLOGTIME are not equal.</span></span>

<span data-ttu-id="0a5d7-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0a5d7-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0a5d7-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="0a5d7-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0a5d7-107">語法</span><span class="sxs-lookup"><span data-stu-id="0a5d7-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_BKLOGTIME, _
    rhs As JET_BKLOGTIME _
) As Boolean
'Usage
Dim lhs As JET_BKLOGTIME
Dim rhs As JET_BKLOGTIME
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_BKLOGTIME lhs,
    JET_BKLOGTIME rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="0a5d7-108">參數</span><span class="sxs-lookup"><span data-stu-id="0a5d7-108">Parameters</span></span>

  - <span data-ttu-id="0a5d7-109">lhs</span><span class="sxs-lookup"><span data-stu-id="0a5d7-109">lhs</span></span>  
    <span data-ttu-id="0a5d7-110">類型： [Microsoft.Isam.Esent.Interop.JET_BKLOGTIME](./jet-bklogtime-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="0a5d7-110">Type: [Microsoft.Isam.Esent.Interop.JET_BKLOGTIME](./jet-bklogtime-structure2.md)</span></span>  
    
    <span data-ttu-id="0a5d7-111">要比較的第一個執行個體。</span><span class="sxs-lookup"><span data-stu-id="0a5d7-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="0a5d7-112">rhs</span><span class="sxs-lookup"><span data-stu-id="0a5d7-112">rhs</span></span>  
    <span data-ttu-id="0a5d7-113">類型： [Microsoft.Isam.Esent.Interop.JET_BKLOGTIME](./jet-bklogtime-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="0a5d7-113">Type: [Microsoft.Isam.Esent.Interop.JET_BKLOGTIME](./jet-bklogtime-structure2.md)</span></span>  
    
    <span data-ttu-id="0a5d7-114">要比較的第二個執行個體。</span><span class="sxs-lookup"><span data-stu-id="0a5d7-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="0a5d7-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="0a5d7-115">Return value</span></span>

<span data-ttu-id="0a5d7-116">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="0a5d7-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="0a5d7-117">如果兩個實例不相等，則為 True。</span><span class="sxs-lookup"><span data-stu-id="0a5d7-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0a5d7-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0a5d7-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0a5d7-119">參考</span><span class="sxs-lookup"><span data-stu-id="0a5d7-119">Reference</span></span>

[<span data-ttu-id="0a5d7-120">JET_BKLOGTIME 結構</span><span class="sxs-lookup"><span data-stu-id="0a5d7-120">JET_BKLOGTIME structure</span></span>](./jet-bklogtime-structure2.md)

[<span data-ttu-id="0a5d7-121">JET_BKLOGTIME 成員</span><span class="sxs-lookup"><span data-stu-id="0a5d7-121">JET_BKLOGTIME members</span></span>](./jet-bklogtime-members.md)

[<span data-ttu-id="0a5d7-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="0a5d7-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
