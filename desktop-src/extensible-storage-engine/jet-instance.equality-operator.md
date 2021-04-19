---
description: 深入瞭解： JET_INSTANCE。等號比較運算子
title: JET_INSTANCE。等號比較運算子
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_INSTANCE.op_Equality(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_INSTANCE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance.op_equality(v=EXCHG.10)
ms:contentKeyID: 39512671
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE.Equality
- Microsoft.Isam.Esent.Interop.JET_INSTANCE.op_Equality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 41a3ffe2eebeb7566d431c655a27360c9380413c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977952"
---
# <a name="jet_instanceequality-operator"></a><span data-ttu-id="630c9-103">JET_INSTANCE。等號比較運算子</span><span class="sxs-lookup"><span data-stu-id="630c9-103">JET_INSTANCE.Equality operator</span></span>

<span data-ttu-id="630c9-104">判斷 JET_INSTANCE 的兩個指定實例是否相等。</span><span class="sxs-lookup"><span data-stu-id="630c9-104">Determines whether two specified instances of JET_INSTANCE are equal.</span></span>

<span data-ttu-id="630c9-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="630c9-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="630c9-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="630c9-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="630c9-107">語法</span><span class="sxs-lookup"><span data-stu-id="630c9-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_INSTANCE, _
    rhs As JET_INSTANCE _
) As Boolean
'Usage
Dim lhs As JET_INSTANCE
Dim rhs As JET_INSTANCE
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_INSTANCE lhs,
    JET_INSTANCE rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="630c9-108">參數</span><span class="sxs-lookup"><span data-stu-id="630c9-108">Parameters</span></span>

  - <span data-ttu-id="630c9-109">lhs</span><span class="sxs-lookup"><span data-stu-id="630c9-109">lhs</span></span>  
    <span data-ttu-id="630c9-110">類型： [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="630c9-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="630c9-111">要比較的第一個執行個體。</span><span class="sxs-lookup"><span data-stu-id="630c9-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="630c9-112">rhs</span><span class="sxs-lookup"><span data-stu-id="630c9-112">rhs</span></span>  
    <span data-ttu-id="630c9-113">類型： [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="630c9-113">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="630c9-114">要比較的第二個執行個體。</span><span class="sxs-lookup"><span data-stu-id="630c9-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="630c9-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="630c9-115">Return value</span></span>

<span data-ttu-id="630c9-116">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="630c9-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="630c9-117">如果兩個實例相等，則為 True。</span><span class="sxs-lookup"><span data-stu-id="630c9-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="630c9-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="630c9-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="630c9-119">參考</span><span class="sxs-lookup"><span data-stu-id="630c9-119">Reference</span></span>

[<span data-ttu-id="630c9-120">JET_INSTANCE 結構</span><span class="sxs-lookup"><span data-stu-id="630c9-120">JET_INSTANCE structure</span></span>](./jet-instance-structure.md)

[<span data-ttu-id="630c9-121">JET_INSTANCE 成員</span><span class="sxs-lookup"><span data-stu-id="630c9-121">JET_INSTANCE members</span></span>](./jet-instance-members.md)

[<span data-ttu-id="630c9-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="630c9-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
