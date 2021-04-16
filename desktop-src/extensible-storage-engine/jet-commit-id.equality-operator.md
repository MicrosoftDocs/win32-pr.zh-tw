---
description: 深入瞭解： JET_COMMIT_ID 等號比較運算子
title: 'JET_COMMIT_ID 的等號比較運算子 (Windows8) '
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.op_Equality(Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID,Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_commit_id.op_equality(v=EXCHG.10)
ms:contentKeyID: 55104297
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.op_Equality
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.Equality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 36815693c078146faec7d604dd28e5d74d475af2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512296"
---
# <a name="jet_commit_idequality-operator"></a><span data-ttu-id="65725-103">JET_COMMIT_ID 等號比較運算子</span><span class="sxs-lookup"><span data-stu-id="65725-103">JET_COMMIT_ID.Equality operator</span></span>

<span data-ttu-id="65725-104">判斷其中一個 commitid 是否等於另一個 commitid。</span><span class="sxs-lookup"><span data-stu-id="65725-104">Determine whether one commitid is is equal to another commitid.</span></span>

<span data-ttu-id="65725-105">**命名空間：**  [Microsoft Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="65725-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="65725-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="65725-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="65725-107">語法</span><span class="sxs-lookup"><span data-stu-id="65725-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_COMMIT_ID, _
    rhs As JET_COMMIT_ID _
) As Boolean
'Usage
Dim lhs As JET_COMMIT_ID
Dim rhs As JET_COMMIT_ID
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_COMMIT_ID lhs,
    JET_COMMIT_ID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="65725-108">參數</span><span class="sxs-lookup"><span data-stu-id="65725-108">Parameters</span></span>

  - <span data-ttu-id="65725-109">lhs</span><span class="sxs-lookup"><span data-stu-id="65725-109">lhs</span></span>  
    <span data-ttu-id="65725-110">類型： [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span><span class="sxs-lookup"><span data-stu-id="65725-110">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span></span>  
    
    <span data-ttu-id="65725-111">要比較的第一個 commitid。</span><span class="sxs-lookup"><span data-stu-id="65725-111">The first commitid to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="65725-112">rhs</span><span class="sxs-lookup"><span data-stu-id="65725-112">rhs</span></span>  
    <span data-ttu-id="65725-113">類型： [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span><span class="sxs-lookup"><span data-stu-id="65725-113">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span></span>  
    
    <span data-ttu-id="65725-114">要比較的第二個 commitid。</span><span class="sxs-lookup"><span data-stu-id="65725-114">The second commitid to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="65725-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="65725-115">Return value</span></span>

<span data-ttu-id="65725-116">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="65725-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="65725-117">如果 lhs 等於 rhs，則為 True。</span><span class="sxs-lookup"><span data-stu-id="65725-117">True if lhs comes is equal to rhs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="65725-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="65725-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="65725-119">參考</span><span class="sxs-lookup"><span data-stu-id="65725-119">Reference</span></span>

[<span data-ttu-id="65725-120">JET_COMMIT_ID 類別</span><span class="sxs-lookup"><span data-stu-id="65725-120">JET_COMMIT_ID class</span></span>](./jet-commit-id-class.md)

[<span data-ttu-id="65725-121">JET_COMMIT_ID 成員</span><span class="sxs-lookup"><span data-stu-id="65725-121">JET_COMMIT_ID members</span></span>](./jet-commit-id-members.md)

[<span data-ttu-id="65725-122">Windows8 命名空間。</span><span class="sxs-lookup"><span data-stu-id="65725-122">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
