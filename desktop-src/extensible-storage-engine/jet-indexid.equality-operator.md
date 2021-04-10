---
description: 深入瞭解： JET_INDEXID。等號比較運算子
title: JET_INDEXID。等號比較運算子
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_INDEXID.op_Equality(Microsoft.Isam.Esent.Interop.JET_INDEXID,Microsoft.Isam.Esent.Interop.JET_INDEXID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexid.op_equality(v=EXCHG.10)
ms:contentKeyID: 39516722
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXID.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXID.Equality
- Microsoft.Isam.Esent.Interop.JET_INDEXID.op_Equality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9fa7574aeed52377b516f63549a6f690dc168d72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945461"
---
# <a name="jet_indexidequality-operator"></a><span data-ttu-id="1372b-103">JET_INDEXID。等號比較運算子</span><span class="sxs-lookup"><span data-stu-id="1372b-103">JET_INDEXID.Equality operator</span></span>

<span data-ttu-id="1372b-104">判斷 JET_INDEXID 的兩個指定實例是否相等。</span><span class="sxs-lookup"><span data-stu-id="1372b-104">Determines whether two specified instances of JET_INDEXID are equal.</span></span>

<span data-ttu-id="1372b-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1372b-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1372b-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="1372b-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1372b-107">語法</span><span class="sxs-lookup"><span data-stu-id="1372b-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_INDEXID, _
    rhs As JET_INDEXID _
) As Boolean
'Usage
Dim lhs As JET_INDEXID
Dim rhs As JET_INDEXID
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_INDEXID lhs,
    JET_INDEXID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="1372b-108">參數</span><span class="sxs-lookup"><span data-stu-id="1372b-108">Parameters</span></span>

  - <span data-ttu-id="1372b-109">lhs</span><span class="sxs-lookup"><span data-stu-id="1372b-109">lhs</span></span>  
    <span data-ttu-id="1372b-110">類型： [Microsoft.Isam.Esent.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="1372b-110">Type: [Microsoft.Isam.Esent.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span></span>  
    
    <span data-ttu-id="1372b-111">要比較的第一個執行個體。</span><span class="sxs-lookup"><span data-stu-id="1372b-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="1372b-112">rhs</span><span class="sxs-lookup"><span data-stu-id="1372b-112">rhs</span></span>  
    <span data-ttu-id="1372b-113">類型： [Microsoft.Isam.Esent.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="1372b-113">Type: [Microsoft.Isam.Esent.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span></span>  
    
    <span data-ttu-id="1372b-114">要比較的第二個執行個體。</span><span class="sxs-lookup"><span data-stu-id="1372b-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="1372b-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="1372b-115">Return value</span></span>

<span data-ttu-id="1372b-116">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="1372b-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="1372b-117">如果兩個實例相等，則為 True。</span><span class="sxs-lookup"><span data-stu-id="1372b-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1372b-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1372b-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1372b-119">參考</span><span class="sxs-lookup"><span data-stu-id="1372b-119">Reference</span></span>

[<span data-ttu-id="1372b-120">JET_INDEXID 結構</span><span class="sxs-lookup"><span data-stu-id="1372b-120">JET_INDEXID structure</span></span>](./jet-indexid-structure2.md)

[<span data-ttu-id="1372b-121">JET_INDEXID 成員</span><span class="sxs-lookup"><span data-stu-id="1372b-121">JET_INDEXID members</span></span>](./jet-indexid-members.md)

[<span data-ttu-id="1372b-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="1372b-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
