---
description: 深入瞭解： JET_OSSNAPID。等號比較運算子
title: JET_OSSNAPID。等號比較運算子
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_OSSNAPID.op_Equality(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.JET_OSSNAPID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_ossnapid.op_equality(v=EXCHG.10)
ms:contentKeyID: 39513985
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_OSSNAPID.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_OSSNAPID.op_Equality
- Microsoft.Isam.Esent.Interop.JET_OSSNAPID.Equality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9a0fcd5d1edba1a0c3d05fe2b1778741626832d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194296"
---
# <a name="jet_ossnapidequality-operator"></a><span data-ttu-id="3494c-103">JET_OSSNAPID。等號比較運算子</span><span class="sxs-lookup"><span data-stu-id="3494c-103">JET_OSSNAPID.Equality operator</span></span>

<span data-ttu-id="3494c-104">判斷 JET_OSSNAPID 的兩個指定實例是否相等。</span><span class="sxs-lookup"><span data-stu-id="3494c-104">Determines whether two specified instances of JET_OSSNAPID are equal.</span></span>

<span data-ttu-id="3494c-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3494c-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3494c-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="3494c-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3494c-107">語法</span><span class="sxs-lookup"><span data-stu-id="3494c-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_OSSNAPID, _
    rhs As JET_OSSNAPID _
) As Boolean
'Usage
Dim lhs As JET_OSSNAPID
Dim rhs As JET_OSSNAPID
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_OSSNAPID lhs,
    JET_OSSNAPID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="3494c-108">參數</span><span class="sxs-lookup"><span data-stu-id="3494c-108">Parameters</span></span>

  - <span data-ttu-id="3494c-109">lhs</span><span class="sxs-lookup"><span data-stu-id="3494c-109">lhs</span></span>  
    <span data-ttu-id="3494c-110">類型： [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3494c-110">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="3494c-111">要比較的第一個執行個體。</span><span class="sxs-lookup"><span data-stu-id="3494c-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="3494c-112">rhs</span><span class="sxs-lookup"><span data-stu-id="3494c-112">rhs</span></span>  
    <span data-ttu-id="3494c-113">類型： [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3494c-113">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="3494c-114">要比較的第二個執行個體。</span><span class="sxs-lookup"><span data-stu-id="3494c-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="3494c-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="3494c-115">Return value</span></span>

<span data-ttu-id="3494c-116">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="3494c-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="3494c-117">如果兩個實例相等，則為 True。</span><span class="sxs-lookup"><span data-stu-id="3494c-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="3494c-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3494c-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3494c-119">參考</span><span class="sxs-lookup"><span data-stu-id="3494c-119">Reference</span></span>

[<span data-ttu-id="3494c-120">JET_OSSNAPID 結構</span><span class="sxs-lookup"><span data-stu-id="3494c-120">JET_OSSNAPID structure</span></span>](./jet-ossnapid-structure.md)

[<span data-ttu-id="3494c-121">JET_OSSNAPID 成員</span><span class="sxs-lookup"><span data-stu-id="3494c-121">JET_OSSNAPID members</span></span>](./jet-ossnapid-members.md)

[<span data-ttu-id="3494c-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="3494c-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
