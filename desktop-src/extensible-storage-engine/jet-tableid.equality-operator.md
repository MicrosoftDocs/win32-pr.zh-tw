---
description: 深入瞭解： JET_TABLEID。等號比較運算子
title: JET_TABLEID。等號比較運算子
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_TABLEID.op_Equality(Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tableid.op_equality(v=EXCHG.10)
ms:contentKeyID: 39515925
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_TABLEID.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_TABLEID.Equality
- Microsoft.Isam.Esent.Interop.JET_TABLEID.op_Equality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b653fcd4576a1069a2c2d896d4e2cb58b9864ece
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193992"
---
# <a name="jet_tableidequality-operator"></a><span data-ttu-id="c5601-103">JET_TABLEID。等號比較運算子</span><span class="sxs-lookup"><span data-stu-id="c5601-103">JET_TABLEID.Equality operator</span></span>

<span data-ttu-id="c5601-104">判斷 JET_TABLEID 的兩個指定實例是否相等。</span><span class="sxs-lookup"><span data-stu-id="c5601-104">Determines whether two specified instances of JET_TABLEID are equal.</span></span>

<span data-ttu-id="c5601-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c5601-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c5601-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="c5601-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c5601-107">語法</span><span class="sxs-lookup"><span data-stu-id="c5601-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_TABLEID, _
    rhs As JET_TABLEID _
) As Boolean
'Usage
Dim lhs As JET_TABLEID
Dim rhs As JET_TABLEID
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_TABLEID lhs,
    JET_TABLEID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="c5601-108">參數</span><span class="sxs-lookup"><span data-stu-id="c5601-108">Parameters</span></span>

  - <span data-ttu-id="c5601-109">lhs</span><span class="sxs-lookup"><span data-stu-id="c5601-109">lhs</span></span>  
    <span data-ttu-id="c5601-110">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c5601-110">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="c5601-111">要比較的第一個執行個體。</span><span class="sxs-lookup"><span data-stu-id="c5601-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="c5601-112">rhs</span><span class="sxs-lookup"><span data-stu-id="c5601-112">rhs</span></span>  
    <span data-ttu-id="c5601-113">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c5601-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="c5601-114">要比較的第二個執行個體。</span><span class="sxs-lookup"><span data-stu-id="c5601-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="c5601-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="c5601-115">Return value</span></span>

<span data-ttu-id="c5601-116">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="c5601-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="c5601-117">如果兩個實例相等，則為 True。</span><span class="sxs-lookup"><span data-stu-id="c5601-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c5601-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c5601-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c5601-119">參考</span><span class="sxs-lookup"><span data-stu-id="c5601-119">Reference</span></span>

[<span data-ttu-id="c5601-120">JET_TABLEID 結構</span><span class="sxs-lookup"><span data-stu-id="c5601-120">JET_TABLEID structure</span></span>](./jet-tableid-structure.md)

[<span data-ttu-id="c5601-121">JET_TABLEID 成員</span><span class="sxs-lookup"><span data-stu-id="c5601-121">JET_TABLEID members</span></span>](./jet-tableid-members.md)

[<span data-ttu-id="c5601-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="c5601-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
