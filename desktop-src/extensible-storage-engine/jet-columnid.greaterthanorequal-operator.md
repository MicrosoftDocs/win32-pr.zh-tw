---
description: 深入瞭解： JET_COLUMNID。GreaterThanOrEqual 運算子
title: JET_COLUMNID。GreaterThanOrEqual 運算子
TOCTitle: 'GreaterThanOrEqual operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_GreaterThanOrEqual(Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnid.op_greaterthanorequal(v=EXCHG.10)
ms:contentKeyID: 39509674
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.GreaterThanOrEqual
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_GreaterThanOrEqual
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.GreaterThanOrEqual
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 344d1ed95ebc6a4a79d17f8b664f3f8a76740367
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997480"
---
# <a name="jet_columnidgreaterthanorequal-operator"></a><span data-ttu-id="f6a44-103">JET_COLUMNID。GreaterThanOrEqual 運算子</span><span class="sxs-lookup"><span data-stu-id="f6a44-103">JET_COLUMNID.GreaterThanOrEqual operator</span></span>

<span data-ttu-id="f6a44-104">判斷其中一個 columnid 是否位於或等於另一個 columnid。</span><span class="sxs-lookup"><span data-stu-id="f6a44-104">Determine whether one columnid is after or equal to another columnid.</span></span>

<span data-ttu-id="f6a44-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f6a44-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f6a44-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="f6a44-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f6a44-107">語法</span><span class="sxs-lookup"><span data-stu-id="f6a44-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator >= ( _
    lhs As JET_COLUMNID, _
    rhs As JET_COLUMNID _
) As Boolean
'Usage
Dim lhs As JET_COLUMNID
Dim rhs As JET_COLUMNID
Dim returnValue As Boolean

returnValue = (lhs >= rhs)
```

``` csharp
public static bool operator >=(
    JET_COLUMNID lhs,
    JET_COLUMNID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="f6a44-108">參數</span><span class="sxs-lookup"><span data-stu-id="f6a44-108">Parameters</span></span>

  - <span data-ttu-id="f6a44-109">lhs</span><span class="sxs-lookup"><span data-stu-id="f6a44-109">lhs</span></span>  
    <span data-ttu-id="f6a44-110">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f6a44-110">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="f6a44-111">要比較的第一個 columnid。</span><span class="sxs-lookup"><span data-stu-id="f6a44-111">The first columnid to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="f6a44-112">rhs</span><span class="sxs-lookup"><span data-stu-id="f6a44-112">rhs</span></span>  
    <span data-ttu-id="f6a44-113">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f6a44-113">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="f6a44-114">要比較的第二個 columnid。</span><span class="sxs-lookup"><span data-stu-id="f6a44-114">The second columnid to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f6a44-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="f6a44-115">Return value</span></span>

<span data-ttu-id="f6a44-116">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="f6a44-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="f6a44-117">如果 lhs 在或等於 rhs，則為 True。</span><span class="sxs-lookup"><span data-stu-id="f6a44-117">True if lhs comes after or is equal to rhs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f6a44-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f6a44-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f6a44-119">參考</span><span class="sxs-lookup"><span data-stu-id="f6a44-119">Reference</span></span>

[<span data-ttu-id="f6a44-120">JET_COLUMNID 結構</span><span class="sxs-lookup"><span data-stu-id="f6a44-120">JET_COLUMNID structure</span></span>](./jet-columnid-structure.md)

[<span data-ttu-id="f6a44-121">JET_COLUMNID 成員</span><span class="sxs-lookup"><span data-stu-id="f6a44-121">JET_COLUMNID members</span></span>](./jet-columnid-members.md)

[<span data-ttu-id="f6a44-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="f6a44-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
