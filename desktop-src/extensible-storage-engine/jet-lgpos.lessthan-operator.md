---
description: 深入瞭解： JET_LGPOS。LessThan 運算子
title: JET_LGPOS。LessThan 運算子
TOCTitle: 'LessThan operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LGPOS.op_LessThan(Microsoft.Isam.Esent.Interop.JET_LGPOS,Microsoft.Isam.Esent.Interop.JET_LGPOS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_lgpos.op_lessthan(v=EXCHG.10)
ms:contentKeyID: 39510335
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.LessThan
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.LessThan
- Microsoft.Isam.Esent.Interop.JET_LGPOS.op_LessThan
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8ec121f9d13686d3d5c8ad22aa0fb3aed8562b5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319771"
---
# <a name="jet_lgposlessthan-operator"></a><span data-ttu-id="3b14c-103">JET_LGPOS。LessThan 運算子</span><span class="sxs-lookup"><span data-stu-id="3b14c-103">JET_LGPOS.LessThan operator</span></span>

<span data-ttu-id="3b14c-104">判斷一個記錄檔位置是否在另一個記錄位置之前。</span><span class="sxs-lookup"><span data-stu-id="3b14c-104">Determine whether one log position is before another log position.</span></span>

<span data-ttu-id="3b14c-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3b14c-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3b14c-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="3b14c-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3b14c-107">語法</span><span class="sxs-lookup"><span data-stu-id="3b14c-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator < ( _
    lhs As JET_LGPOS, _
    rhs As JET_LGPOS _
) As Boolean
'Usage
Dim lhs As JET_LGPOS
Dim rhs As JET_LGPOS
Dim returnValue As Boolean

returnValue = (lhs < rhs)
```

``` csharp
public static bool operator <(
    JET_LGPOS lhs,
    JET_LGPOS rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="3b14c-108">參數</span><span class="sxs-lookup"><span data-stu-id="3b14c-108">Parameters</span></span>

  - <span data-ttu-id="3b14c-109">lhs</span><span class="sxs-lookup"><span data-stu-id="3b14c-109">lhs</span></span>  
    <span data-ttu-id="3b14c-110">類型： [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="3b14c-110">Type: [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span></span>  
    
    <span data-ttu-id="3b14c-111">要比較的第一個記錄檔位置。</span><span class="sxs-lookup"><span data-stu-id="3b14c-111">The first log position to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="3b14c-112">rhs</span><span class="sxs-lookup"><span data-stu-id="3b14c-112">rhs</span></span>  
    <span data-ttu-id="3b14c-113">類型： [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="3b14c-113">Type: [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span></span>  
    
    <span data-ttu-id="3b14c-114">要比較的第二個記錄檔位置。</span><span class="sxs-lookup"><span data-stu-id="3b14c-114">The second log position to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="3b14c-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="3b14c-115">Return value</span></span>

<span data-ttu-id="3b14c-116">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="3b14c-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="3b14c-117">如果 lhs 在 rhs 之前，則為 True。</span><span class="sxs-lookup"><span data-stu-id="3b14c-117">True if lhs comes before rhs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="3b14c-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3b14c-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3b14c-119">參考</span><span class="sxs-lookup"><span data-stu-id="3b14c-119">Reference</span></span>

[<span data-ttu-id="3b14c-120">JET_LGPOS 結構</span><span class="sxs-lookup"><span data-stu-id="3b14c-120">JET_LGPOS structure</span></span>](./jet-lgpos-structure2.md)

[<span data-ttu-id="3b14c-121">JET_LGPOS 成員</span><span class="sxs-lookup"><span data-stu-id="3b14c-121">JET_LGPOS members</span></span>](./jet-lgpos-members.md)

[<span data-ttu-id="3b14c-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="3b14c-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
