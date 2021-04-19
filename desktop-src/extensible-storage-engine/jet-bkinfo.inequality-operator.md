---
description: 深入瞭解： JET_BKINFO。不等比較運算子
title: JET_BKINFO。不等比較運算子
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_BKINFO.op_Inequality(Microsoft.Isam.Esent.Interop.JET_BKINFO,Microsoft.Isam.Esent.Interop.JET_BKINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_bkinfo.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39513804
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_BKINFO.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_BKINFO.op_Inequality
- Microsoft.Isam.Esent.Interop.JET_BKINFO.Inequality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b8ccc18ea535f6b202c8e08976b52c090fd543cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994404"
---
# <a name="jet_bkinfoinequality-operator"></a><span data-ttu-id="ad48c-103">JET_BKINFO。不等比較運算子</span><span class="sxs-lookup"><span data-stu-id="ad48c-103">JET_BKINFO.Inequality operator</span></span>

<span data-ttu-id="ad48c-104">判斷 JET_BKINFO 的兩個指定實例是否不相等。</span><span class="sxs-lookup"><span data-stu-id="ad48c-104">Determines whether two specified instances of JET_BKINFO are not equal.</span></span>

<span data-ttu-id="ad48c-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ad48c-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ad48c-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="ad48c-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ad48c-107">語法</span><span class="sxs-lookup"><span data-stu-id="ad48c-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_BKINFO, _
    rhs As JET_BKINFO _
) As Boolean
'Usage
Dim lhs As JET_BKINFO
Dim rhs As JET_BKINFO
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_BKINFO lhs,
    JET_BKINFO rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="ad48c-108">參數</span><span class="sxs-lookup"><span data-stu-id="ad48c-108">Parameters</span></span>

  - <span data-ttu-id="ad48c-109">lhs</span><span class="sxs-lookup"><span data-stu-id="ad48c-109">lhs</span></span>  
    <span data-ttu-id="ad48c-110">類型： [Microsoft.Isam.Esent.Interop.JET_BKINFO](./jet-bkinfo-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="ad48c-110">Type: [Microsoft.Isam.Esent.Interop.JET_BKINFO](./jet-bkinfo-structure2.md)</span></span>  
    
    <span data-ttu-id="ad48c-111">要比較的第一個執行個體。</span><span class="sxs-lookup"><span data-stu-id="ad48c-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="ad48c-112">rhs</span><span class="sxs-lookup"><span data-stu-id="ad48c-112">rhs</span></span>  
    <span data-ttu-id="ad48c-113">類型： [Microsoft.Isam.Esent.Interop.JET_BKINFO](./jet-bkinfo-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="ad48c-113">Type: [Microsoft.Isam.Esent.Interop.JET_BKINFO](./jet-bkinfo-structure2.md)</span></span>  
    
    <span data-ttu-id="ad48c-114">要比較的第二個執行個體。</span><span class="sxs-lookup"><span data-stu-id="ad48c-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="ad48c-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="ad48c-115">Return value</span></span>

<span data-ttu-id="ad48c-116">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="ad48c-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="ad48c-117">如果兩個實例不相等，則為 True。</span><span class="sxs-lookup"><span data-stu-id="ad48c-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ad48c-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ad48c-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ad48c-119">參考</span><span class="sxs-lookup"><span data-stu-id="ad48c-119">Reference</span></span>

[<span data-ttu-id="ad48c-120">JET_BKINFO 結構</span><span class="sxs-lookup"><span data-stu-id="ad48c-120">JET_BKINFO structure</span></span>](./jet-bkinfo-structure2.md)

[<span data-ttu-id="ad48c-121">JET_BKINFO 成員</span><span class="sxs-lookup"><span data-stu-id="ad48c-121">JET_BKINFO members</span></span>](./jet-bkinfo-members.md)

[<span data-ttu-id="ad48c-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="ad48c-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
