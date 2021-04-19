---
description: 深入瞭解： JET_COMMIT_ID LessThan 運算子
title: LessThan 運算子 (Windows8) 的 JET_COMMIT_ID。
TOCTitle: 'LessThan operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.op_LessThan(Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID,Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_commit_id.op_lessthan(v=EXCHG.10)
ms:contentKeyID: 55104300
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.LessThan
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.LessThan
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.op_LessThan
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: faf5363d8e53d14eb022404f7ab39fe1c7850928
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974954"
---
# <a name="jet_commit_idlessthan-operator"></a><span data-ttu-id="207f4-103">JET_COMMIT_ID. LessThan 運算子</span><span class="sxs-lookup"><span data-stu-id="207f4-103">JET_COMMIT_ID.LessThan operator</span></span>

<span data-ttu-id="207f4-104">判斷其中一個 commitid 是否在另一個 commitid 之前。</span><span class="sxs-lookup"><span data-stu-id="207f4-104">Determine whether one commitid is before another commitid.</span></span>

<span data-ttu-id="207f4-105">**命名空間：**  [Microsoft Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="207f4-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="207f4-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="207f4-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="207f4-107">語法</span><span class="sxs-lookup"><span data-stu-id="207f4-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator < ( _
    lhs As JET_COMMIT_ID, _
    rhs As JET_COMMIT_ID _
) As Boolean
'Usage
Dim lhs As JET_COMMIT_ID
Dim rhs As JET_COMMIT_ID
Dim returnValue As Boolean

returnValue = (lhs < rhs)
```

``` csharp
public static bool operator <(
    JET_COMMIT_ID lhs,
    JET_COMMIT_ID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="207f4-108">參數</span><span class="sxs-lookup"><span data-stu-id="207f4-108">Parameters</span></span>

  - <span data-ttu-id="207f4-109">lhs</span><span class="sxs-lookup"><span data-stu-id="207f4-109">lhs</span></span>  
    <span data-ttu-id="207f4-110">類型： [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span><span class="sxs-lookup"><span data-stu-id="207f4-110">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span></span>  
    
    <span data-ttu-id="207f4-111">要比較的第一個 commitid。</span><span class="sxs-lookup"><span data-stu-id="207f4-111">The first commitid to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="207f4-112">rhs</span><span class="sxs-lookup"><span data-stu-id="207f4-112">rhs</span></span>  
    <span data-ttu-id="207f4-113">類型： [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span><span class="sxs-lookup"><span data-stu-id="207f4-113">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span></span>  
    
    <span data-ttu-id="207f4-114">要比較的第二個 commitid。</span><span class="sxs-lookup"><span data-stu-id="207f4-114">The second commitid to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="207f4-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="207f4-115">Return value</span></span>

<span data-ttu-id="207f4-116">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="207f4-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="207f4-117">如果 lhs 在 rhs 之前，則為 True。</span><span class="sxs-lookup"><span data-stu-id="207f4-117">True if lhs comes before rhs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="207f4-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="207f4-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="207f4-119">參考</span><span class="sxs-lookup"><span data-stu-id="207f4-119">Reference</span></span>

[<span data-ttu-id="207f4-120">JET_COMMIT_ID 類別</span><span class="sxs-lookup"><span data-stu-id="207f4-120">JET_COMMIT_ID class</span></span>](./jet-commit-id-class.md)

[<span data-ttu-id="207f4-121">JET_COMMIT_ID 成員</span><span class="sxs-lookup"><span data-stu-id="207f4-121">JET_COMMIT_ID members</span></span>](./jet-commit-id-members.md)

[<span data-ttu-id="207f4-122">Windows8 命名空間。</span><span class="sxs-lookup"><span data-stu-id="207f4-122">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
