---
description: 深入瞭解： JET_LGPOS。GreaterThan 運算子
title: JET_LGPOS。GreaterThan 運算子
TOCTitle: 'GreaterThan operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LGPOS.op_GreaterThan(Microsoft.Isam.Esent.Interop.JET_LGPOS,Microsoft.Isam.Esent.Interop.JET_LGPOS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_lgpos.op_greaterthan(v=EXCHG.10)
ms:contentKeyID: 39510131
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.GreaterThan
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.GreaterThan
- Microsoft.Isam.Esent.Interop.JET_LGPOS.op_GreaterThan
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4f3e0c060311205d1f5d47bc4678c6ff9458b589
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997217"
---
# <a name="jet_lgposgreaterthan-operator"></a><span data-ttu-id="a020d-103">JET_LGPOS。GreaterThan 運算子</span><span class="sxs-lookup"><span data-stu-id="a020d-103">JET_LGPOS.GreaterThan operator</span></span>

<span data-ttu-id="a020d-104">判斷一個記錄檔位置是否位於另一個記錄檔位置之後。</span><span class="sxs-lookup"><span data-stu-id="a020d-104">Determine whether one log position is after another log position.</span></span>

<span data-ttu-id="a020d-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a020d-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a020d-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="a020d-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a020d-107">語法</span><span class="sxs-lookup"><span data-stu-id="a020d-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator > ( _
    lhs As JET_LGPOS, _
    rhs As JET_LGPOS _
) As Boolean
'Usage
Dim lhs As JET_LGPOS
Dim rhs As JET_LGPOS
Dim returnValue As Boolean

returnValue = (lhs > rhs)
```

``` csharp
public static bool operator >(
    JET_LGPOS lhs,
    JET_LGPOS rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="a020d-108">參數</span><span class="sxs-lookup"><span data-stu-id="a020d-108">Parameters</span></span>

  - <span data-ttu-id="a020d-109">lhs</span><span class="sxs-lookup"><span data-stu-id="a020d-109">lhs</span></span>  
    <span data-ttu-id="a020d-110">類型： [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="a020d-110">Type: [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span></span>  
    
    <span data-ttu-id="a020d-111">要比較的第一個記錄檔位置。</span><span class="sxs-lookup"><span data-stu-id="a020d-111">The first log position to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="a020d-112">rhs</span><span class="sxs-lookup"><span data-stu-id="a020d-112">rhs</span></span>  
    <span data-ttu-id="a020d-113">類型： [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="a020d-113">Type: [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span></span>  
    
    <span data-ttu-id="a020d-114">要比較的第二個記錄檔位置。</span><span class="sxs-lookup"><span data-stu-id="a020d-114">The second log position to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="a020d-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="a020d-115">Return value</span></span>

<span data-ttu-id="a020d-116">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="a020d-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="a020d-117">如果 lhs 在 rhs 之後，則為 True。</span><span class="sxs-lookup"><span data-stu-id="a020d-117">True if lhs comes after rhs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a020d-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a020d-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a020d-119">參考</span><span class="sxs-lookup"><span data-stu-id="a020d-119">Reference</span></span>

[<span data-ttu-id="a020d-120">JET_LGPOS 結構</span><span class="sxs-lookup"><span data-stu-id="a020d-120">JET_LGPOS structure</span></span>](./jet-lgpos-structure2.md)

[<span data-ttu-id="a020d-121">JET_LGPOS 成員</span><span class="sxs-lookup"><span data-stu-id="a020d-121">JET_LGPOS members</span></span>](./jet-lgpos-members.md)

[<span data-ttu-id="a020d-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="a020d-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
