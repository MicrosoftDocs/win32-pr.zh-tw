---
description: 深入瞭解： JET_COMMIT_ID 的等號比較運算子
title: 'JET_COMMIT_ID 不等比較運算子 (Windows8) '
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.op_Inequality(Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID,Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_commit_id.op_inequality(v=EXCHG.10)
ms:contentKeyID: 55104411
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.op_Inequality
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.Inequality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b64be3b2c6438490d3e44076b1e553a7abb37d8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984613"
---
# <a name="jet_commit_idinequality-operator"></a><span data-ttu-id="4a62e-103">JET_COMMIT_ID 不等比較運算子</span><span class="sxs-lookup"><span data-stu-id="4a62e-103">JET_COMMIT_ID.Inequality operator</span></span>

<span data-ttu-id="4a62e-104">判斷其中一個 commitid 是否不等於另一個 commitid。</span><span class="sxs-lookup"><span data-stu-id="4a62e-104">Determine whether one commitid is not equal to another commitid.</span></span>

<span data-ttu-id="4a62e-105">**命名空間：**  [Microsoft Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4a62e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="4a62e-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="4a62e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4a62e-107">語法</span><span class="sxs-lookup"><span data-stu-id="4a62e-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_COMMIT_ID, _
    rhs As JET_COMMIT_ID _
) As Boolean
'Usage
Dim lhs As JET_COMMIT_ID
Dim rhs As JET_COMMIT_ID
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_COMMIT_ID lhs,
    JET_COMMIT_ID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="4a62e-108">參數</span><span class="sxs-lookup"><span data-stu-id="4a62e-108">Parameters</span></span>

  - <span data-ttu-id="4a62e-109">lhs</span><span class="sxs-lookup"><span data-stu-id="4a62e-109">lhs</span></span>  
    <span data-ttu-id="4a62e-110">類型： [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span><span class="sxs-lookup"><span data-stu-id="4a62e-110">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span></span>  
    
    <span data-ttu-id="4a62e-111">要比較的第一個 commitid。</span><span class="sxs-lookup"><span data-stu-id="4a62e-111">The first commitid to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="4a62e-112">rhs</span><span class="sxs-lookup"><span data-stu-id="4a62e-112">rhs</span></span>  
    <span data-ttu-id="4a62e-113">類型： [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span><span class="sxs-lookup"><span data-stu-id="4a62e-113">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span></span>  
    
    <span data-ttu-id="4a62e-114">要比較的第二個 commitid。</span><span class="sxs-lookup"><span data-stu-id="4a62e-114">The second commitid to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="4a62e-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="4a62e-115">Return value</span></span>

<span data-ttu-id="4a62e-116">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="4a62e-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="4a62e-117">如果 lhs 不等於 rhs，則為 True。</span><span class="sxs-lookup"><span data-stu-id="4a62e-117">True if lhs comes is not equal to rhs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4a62e-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4a62e-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4a62e-119">參考</span><span class="sxs-lookup"><span data-stu-id="4a62e-119">Reference</span></span>

[<span data-ttu-id="4a62e-120">JET_COMMIT_ID 類別</span><span class="sxs-lookup"><span data-stu-id="4a62e-120">JET_COMMIT_ID class</span></span>](./jet-commit-id-class.md)

[<span data-ttu-id="4a62e-121">JET_COMMIT_ID 成員</span><span class="sxs-lookup"><span data-stu-id="4a62e-121">JET_COMMIT_ID members</span></span>](./jet-commit-id-members.md)

[<span data-ttu-id="4a62e-122">Windows8 命名空間。</span><span class="sxs-lookup"><span data-stu-id="4a62e-122">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
