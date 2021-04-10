---
description: 深入瞭解： JET_COMMIT_ID GreaterThan 運算子
title: GreaterThan 運算子 (Windows8) 的 JET_COMMIT_ID。
TOCTitle: 'GreaterThan operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.op_GreaterThan(Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID,Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_commit_id.op_greaterthan(v=EXCHG.10)
ms:contentKeyID: 55104406
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.GreaterThan
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.GreaterThan
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.op_GreaterThan
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bfcb6cdc5a07cd4c114d5f61aaf597711636526b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693939"
---
# <a name="jet_commit_idgreaterthan-operator"></a><span data-ttu-id="4ab95-103">JET_COMMIT_ID. GreaterThan 運算子</span><span class="sxs-lookup"><span data-stu-id="4ab95-103">JET_COMMIT_ID.GreaterThan operator</span></span>

<span data-ttu-id="4ab95-104">判斷其中一個 commitid 是否在另一個 commitid 之前。</span><span class="sxs-lookup"><span data-stu-id="4ab95-104">Determine whether one commitid is before another commitid.</span></span>

<span data-ttu-id="4ab95-105">**命名空間：**  [Microsoft Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4ab95-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="4ab95-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="4ab95-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4ab95-107">語法</span><span class="sxs-lookup"><span data-stu-id="4ab95-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator > ( _
    lhs As JET_COMMIT_ID, _
    rhs As JET_COMMIT_ID _
) As Boolean
'Usage
Dim lhs As JET_COMMIT_ID
Dim rhs As JET_COMMIT_ID
Dim returnValue As Boolean

returnValue = (lhs > rhs)
```

``` csharp
public static bool operator >(
    JET_COMMIT_ID lhs,
    JET_COMMIT_ID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="4ab95-108">參數</span><span class="sxs-lookup"><span data-stu-id="4ab95-108">Parameters</span></span>

  - <span data-ttu-id="4ab95-109">lhs</span><span class="sxs-lookup"><span data-stu-id="4ab95-109">lhs</span></span>  
    <span data-ttu-id="4ab95-110">類型： [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span><span class="sxs-lookup"><span data-stu-id="4ab95-110">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span></span>  
    
    <span data-ttu-id="4ab95-111">要比較的第一個 commitid。</span><span class="sxs-lookup"><span data-stu-id="4ab95-111">The first commitid to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="4ab95-112">rhs</span><span class="sxs-lookup"><span data-stu-id="4ab95-112">rhs</span></span>  
    <span data-ttu-id="4ab95-113">類型： [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span><span class="sxs-lookup"><span data-stu-id="4ab95-113">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span></span>  
    
    <span data-ttu-id="4ab95-114">要比較的第二個 commitid。</span><span class="sxs-lookup"><span data-stu-id="4ab95-114">The second commitid to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="4ab95-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="4ab95-115">Return value</span></span>

<span data-ttu-id="4ab95-116">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="4ab95-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="4ab95-117">如果 lhs 在 rhs 之後，則為 True。</span><span class="sxs-lookup"><span data-stu-id="4ab95-117">True if lhs comes after rhs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4ab95-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4ab95-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4ab95-119">參考</span><span class="sxs-lookup"><span data-stu-id="4ab95-119">Reference</span></span>

[<span data-ttu-id="4ab95-120">JET_COMMIT_ID 類別</span><span class="sxs-lookup"><span data-stu-id="4ab95-120">JET_COMMIT_ID class</span></span>](./jet-commit-id-class.md)

[<span data-ttu-id="4ab95-121">JET_COMMIT_ID 成員</span><span class="sxs-lookup"><span data-stu-id="4ab95-121">JET_COMMIT_ID members</span></span>](./jet-commit-id-members.md)

[<span data-ttu-id="4ab95-122">Windows8 命名空間。</span><span class="sxs-lookup"><span data-stu-id="4ab95-122">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
