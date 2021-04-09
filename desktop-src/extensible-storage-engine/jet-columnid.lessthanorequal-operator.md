---
description: 深入瞭解： JET_COLUMNID。LessThanOrEqual 運算子
title: JET_COLUMNID。LessThanOrEqual 運算子
TOCTitle: 'LessThanOrEqual operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_LessThanOrEqual(Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnid.op_lessthanorequal(v=EXCHG.10)
ms:contentKeyID: 39513688
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.LessThanOrEqual
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.LessThanOrEqual
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_LessThanOrEqual
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e9d6f98c5861a57fa4916ebca1b421c538d752d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691308"
---
# <a name="jet_columnidlessthanorequal-operator"></a><span data-ttu-id="7394f-103">JET_COLUMNID。LessThanOrEqual 運算子</span><span class="sxs-lookup"><span data-stu-id="7394f-103">JET_COLUMNID.LessThanOrEqual operator</span></span>

<span data-ttu-id="7394f-104">判斷其中一個 columnid 是否早于或等於另一個 columnid。</span><span class="sxs-lookup"><span data-stu-id="7394f-104">Determine whether one columnid is before or equal to another columnid.</span></span>

<span data-ttu-id="7394f-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7394f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7394f-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="7394f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7394f-107">語法</span><span class="sxs-lookup"><span data-stu-id="7394f-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <= ( _
    lhs As JET_COLUMNID, _
    rhs As JET_COLUMNID _
) As Boolean
'Usage
Dim lhs As JET_COLUMNID
Dim rhs As JET_COLUMNID
Dim returnValue As Boolean

returnValue = (lhs <= rhs)
```

``` csharp
public static bool operator <=(
    JET_COLUMNID lhs,
    JET_COLUMNID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="7394f-108">參數</span><span class="sxs-lookup"><span data-stu-id="7394f-108">Parameters</span></span>

  - <span data-ttu-id="7394f-109">lhs</span><span class="sxs-lookup"><span data-stu-id="7394f-109">lhs</span></span>  
    <span data-ttu-id="7394f-110">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7394f-110">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="7394f-111">要比較的第一個 columnid。</span><span class="sxs-lookup"><span data-stu-id="7394f-111">The first columnid to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="7394f-112">rhs</span><span class="sxs-lookup"><span data-stu-id="7394f-112">rhs</span></span>  
    <span data-ttu-id="7394f-113">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7394f-113">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="7394f-114">要比較的第二個 columnid。</span><span class="sxs-lookup"><span data-stu-id="7394f-114">The second columnid to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="7394f-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="7394f-115">Return value</span></span>

<span data-ttu-id="7394f-116">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="7394f-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="7394f-117">如果 lhs 早于或等於 rhs，則為 True。</span><span class="sxs-lookup"><span data-stu-id="7394f-117">True if lhs comes before or is equal to rhs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7394f-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7394f-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7394f-119">參考</span><span class="sxs-lookup"><span data-stu-id="7394f-119">Reference</span></span>

[<span data-ttu-id="7394f-120">JET_COLUMNID 結構</span><span class="sxs-lookup"><span data-stu-id="7394f-120">JET_COLUMNID structure</span></span>](./jet-columnid-structure.md)

[<span data-ttu-id="7394f-121">JET_COLUMNID 成員</span><span class="sxs-lookup"><span data-stu-id="7394f-121">JET_COLUMNID members</span></span>](./jet-columnid-members.md)

[<span data-ttu-id="7394f-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="7394f-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
