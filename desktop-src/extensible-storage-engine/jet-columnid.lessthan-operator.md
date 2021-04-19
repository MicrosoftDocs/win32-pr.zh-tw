---
description: 深入瞭解： JET_COLUMNID。LessThan 運算子
title: JET_COLUMNID。LessThan 運算子
TOCTitle: 'LessThan operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_LessThan(Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnid.op_lessthan(v=EXCHG.10)
ms:contentKeyID: 39512911
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.LessThan
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.LessThan
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_LessThan
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 263cb7be0377da007e6294b29701613628ec692d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973005"
---
# <a name="jet_columnidlessthan-operator"></a><span data-ttu-id="25da3-103">JET_COLUMNID。LessThan 運算子</span><span class="sxs-lookup"><span data-stu-id="25da3-103">JET_COLUMNID.LessThan operator</span></span>

<span data-ttu-id="25da3-104">判斷其中一個 columnid 是否在另一個 columnid 之前。</span><span class="sxs-lookup"><span data-stu-id="25da3-104">Determine whether one columnid is before another columnid.</span></span>

<span data-ttu-id="25da3-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="25da3-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="25da3-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="25da3-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="25da3-107">語法</span><span class="sxs-lookup"><span data-stu-id="25da3-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator < ( _
    lhs As JET_COLUMNID, _
    rhs As JET_COLUMNID _
) As Boolean
'Usage
Dim lhs As JET_COLUMNID
Dim rhs As JET_COLUMNID
Dim returnValue As Boolean

returnValue = (lhs < rhs)
```

``` csharp
public static bool operator <(
    JET_COLUMNID lhs,
    JET_COLUMNID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="25da3-108">參數</span><span class="sxs-lookup"><span data-stu-id="25da3-108">Parameters</span></span>

  - <span data-ttu-id="25da3-109">lhs</span><span class="sxs-lookup"><span data-stu-id="25da3-109">lhs</span></span>  
    <span data-ttu-id="25da3-110">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="25da3-110">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="25da3-111">要比較的第一個 columnid。</span><span class="sxs-lookup"><span data-stu-id="25da3-111">The first columnid to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="25da3-112">rhs</span><span class="sxs-lookup"><span data-stu-id="25da3-112">rhs</span></span>  
    <span data-ttu-id="25da3-113">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="25da3-113">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="25da3-114">要比較的第二個 columnid。</span><span class="sxs-lookup"><span data-stu-id="25da3-114">The second columnid to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="25da3-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="25da3-115">Return value</span></span>

<span data-ttu-id="25da3-116">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="25da3-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="25da3-117">如果 lhs 在 rhs 之前，則為 True。</span><span class="sxs-lookup"><span data-stu-id="25da3-117">True if lhs comes before rhs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="25da3-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="25da3-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="25da3-119">參考</span><span class="sxs-lookup"><span data-stu-id="25da3-119">Reference</span></span>

[<span data-ttu-id="25da3-120">JET_COLUMNID 結構</span><span class="sxs-lookup"><span data-stu-id="25da3-120">JET_COLUMNID structure</span></span>](./jet-columnid-structure.md)

[<span data-ttu-id="25da3-121">JET_COLUMNID 成員</span><span class="sxs-lookup"><span data-stu-id="25da3-121">JET_COLUMNID members</span></span>](./jet-columnid-members.md)

[<span data-ttu-id="25da3-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="25da3-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
