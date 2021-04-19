---
description: 深入瞭解： JET_LGPOS。等號比較運算子
title: JET_LGPOS。等號比較運算子
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LGPOS.op_Equality(Microsoft.Isam.Esent.Interop.JET_LGPOS,Microsoft.Isam.Esent.Interop.JET_LGPOS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_lgpos.op_equality(v=EXCHG.10)
ms:contentKeyID: 39510144
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.Equality
- Microsoft.Isam.Esent.Interop.JET_LGPOS.op_Equality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ffdde1ee34cb60761d55dd52f2145a6b9bdd0a79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982769"
---
# <a name="jet_lgposequality-operator"></a><span data-ttu-id="4824f-103">JET_LGPOS。等號比較運算子</span><span class="sxs-lookup"><span data-stu-id="4824f-103">JET_LGPOS.Equality operator</span></span>

<span data-ttu-id="4824f-104">判斷 JET_LGPOS 的兩個指定實例是否相等。</span><span class="sxs-lookup"><span data-stu-id="4824f-104">Determines whether two specified instances of JET_LGPOS are equal.</span></span>

<span data-ttu-id="4824f-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4824f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4824f-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="4824f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4824f-107">語法</span><span class="sxs-lookup"><span data-stu-id="4824f-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_LGPOS, _
    rhs As JET_LGPOS _
) As Boolean
'Usage
Dim lhs As JET_LGPOS
Dim rhs As JET_LGPOS
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_LGPOS lhs,
    JET_LGPOS rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="4824f-108">參數</span><span class="sxs-lookup"><span data-stu-id="4824f-108">Parameters</span></span>

  - <span data-ttu-id="4824f-109">lhs</span><span class="sxs-lookup"><span data-stu-id="4824f-109">lhs</span></span>  
    <span data-ttu-id="4824f-110">類型： [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="4824f-110">Type: [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span></span>  
    
    <span data-ttu-id="4824f-111">要比較的第一個執行個體。</span><span class="sxs-lookup"><span data-stu-id="4824f-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="4824f-112">rhs</span><span class="sxs-lookup"><span data-stu-id="4824f-112">rhs</span></span>  
    <span data-ttu-id="4824f-113">類型： [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="4824f-113">Type: [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span></span>  
    
    <span data-ttu-id="4824f-114">要比較的第二個執行個體。</span><span class="sxs-lookup"><span data-stu-id="4824f-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="4824f-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="4824f-115">Return value</span></span>

<span data-ttu-id="4824f-116">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="4824f-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="4824f-117">如果兩個實例相等，則為 True。</span><span class="sxs-lookup"><span data-stu-id="4824f-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4824f-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4824f-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4824f-119">參考</span><span class="sxs-lookup"><span data-stu-id="4824f-119">Reference</span></span>

[<span data-ttu-id="4824f-120">JET_LGPOS 結構</span><span class="sxs-lookup"><span data-stu-id="4824f-120">JET_LGPOS structure</span></span>](./jet-lgpos-structure2.md)

[<span data-ttu-id="4824f-121">JET_LGPOS 成員</span><span class="sxs-lookup"><span data-stu-id="4824f-121">JET_LGPOS members</span></span>](./jet-lgpos-members.md)

[<span data-ttu-id="4824f-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="4824f-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
