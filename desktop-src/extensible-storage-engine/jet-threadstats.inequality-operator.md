---
description: 深入瞭解： JET_THREADSTATS。不等比較運算子
title: 'JET_THREADSTATS。不等比較運算子 (的 < a0/&gt; < a1/&gt;) '
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.op_Inequality(Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS,Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39510396
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Inequality
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.op_Inequality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9dd3bc0f56b5fbbc47928387f999664df7bcc7a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851440"
---
# <a name="jet_threadstatsinequality-operator"></a><span data-ttu-id="da101-103">JET_THREADSTATS。不等比較運算子</span><span class="sxs-lookup"><span data-stu-id="da101-103">JET_THREADSTATS.Inequality operator</span></span>

<span data-ttu-id="da101-104">判斷 JET_THREADSTATS 的兩個指定實例是否不相等。</span><span class="sxs-lookup"><span data-stu-id="da101-104">Determines whether two specified instances of JET_THREADSTATS are not equal.</span></span>

<span data-ttu-id="da101-105">**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。  </span><span class="sxs-lookup"><span data-stu-id="da101-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="da101-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="da101-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="da101-107">語法</span><span class="sxs-lookup"><span data-stu-id="da101-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_THREADSTATS, _
    rhs As JET_THREADSTATS _
) As Boolean
'Usage
Dim lhs As JET_THREADSTATS
Dim rhs As JET_THREADSTATS
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_THREADSTATS lhs,
    JET_THREADSTATS rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="da101-108">參數</span><span class="sxs-lookup"><span data-stu-id="da101-108">Parameters</span></span>

  - <span data-ttu-id="da101-109">lhs</span><span class="sxs-lookup"><span data-stu-id="da101-109">lhs</span></span>  
    <span data-ttu-id="da101-110">類型： [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="da101-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="da101-111">要比較的第一個執行個體。</span><span class="sxs-lookup"><span data-stu-id="da101-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="da101-112">rhs</span><span class="sxs-lookup"><span data-stu-id="da101-112">rhs</span></span>  
    <span data-ttu-id="da101-113">類型： [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="da101-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="da101-114">要比較的第二個執行個體。</span><span class="sxs-lookup"><span data-stu-id="da101-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="da101-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="da101-115">Return value</span></span>

<span data-ttu-id="da101-116">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="da101-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="da101-117">如果兩個實例不相等，則為 True。</span><span class="sxs-lookup"><span data-stu-id="da101-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="da101-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="da101-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="da101-119">參考</span><span class="sxs-lookup"><span data-stu-id="da101-119">Reference</span></span>

[<span data-ttu-id="da101-120">JET_THREADSTATS 結構</span><span class="sxs-lookup"><span data-stu-id="da101-120">JET_THREADSTATS structure</span></span>](./jet-threadstats-structure2.md)

[<span data-ttu-id="da101-121">JET_THREADSTATS 成員</span><span class="sxs-lookup"><span data-stu-id="da101-121">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="da101-122">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="da101-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
