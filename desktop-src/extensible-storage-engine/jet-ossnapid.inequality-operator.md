---
description: 深入瞭解： JET_OSSNAPID。不等比較運算子
title: JET_OSSNAPID。不等比較運算子
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_OSSNAPID.op_Inequality(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.JET_OSSNAPID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_ossnapid.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39510705
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_OSSNAPID.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_OSSNAPID.Inequality
- Microsoft.Isam.Esent.Interop.JET_OSSNAPID.op_Inequality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4bb19425b9f4ce9a3d404c5b5019adf1b3a84d28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695451"
---
# <a name="jet_ossnapidinequality-operator"></a><span data-ttu-id="b56f2-103">JET_OSSNAPID。不等比較運算子</span><span class="sxs-lookup"><span data-stu-id="b56f2-103">JET_OSSNAPID.Inequality operator</span></span>

<span data-ttu-id="b56f2-104">判斷 JET_OSSNAPID 的兩個指定實例是否不相等。</span><span class="sxs-lookup"><span data-stu-id="b56f2-104">Determines whether two specified instances of JET_OSSNAPID are not equal.</span></span>

<span data-ttu-id="b56f2-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b56f2-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b56f2-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="b56f2-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b56f2-107">語法</span><span class="sxs-lookup"><span data-stu-id="b56f2-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_OSSNAPID, _
    rhs As JET_OSSNAPID _
) As Boolean
'Usage
Dim lhs As JET_OSSNAPID
Dim rhs As JET_OSSNAPID
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_OSSNAPID lhs,
    JET_OSSNAPID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="b56f2-108">參數</span><span class="sxs-lookup"><span data-stu-id="b56f2-108">Parameters</span></span>

  - <span data-ttu-id="b56f2-109">lhs</span><span class="sxs-lookup"><span data-stu-id="b56f2-109">lhs</span></span>  
    <span data-ttu-id="b56f2-110">類型： [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b56f2-110">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="b56f2-111">要比較的第一個執行個體。</span><span class="sxs-lookup"><span data-stu-id="b56f2-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="b56f2-112">rhs</span><span class="sxs-lookup"><span data-stu-id="b56f2-112">rhs</span></span>  
    <span data-ttu-id="b56f2-113">類型： [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b56f2-113">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="b56f2-114">要比較的第二個執行個體。</span><span class="sxs-lookup"><span data-stu-id="b56f2-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="b56f2-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="b56f2-115">Return value</span></span>

<span data-ttu-id="b56f2-116">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="b56f2-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="b56f2-117">如果兩個實例不相等，則為 True。</span><span class="sxs-lookup"><span data-stu-id="b56f2-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b56f2-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b56f2-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b56f2-119">參考</span><span class="sxs-lookup"><span data-stu-id="b56f2-119">Reference</span></span>

[<span data-ttu-id="b56f2-120">JET_OSSNAPID 結構</span><span class="sxs-lookup"><span data-stu-id="b56f2-120">JET_OSSNAPID structure</span></span>](./jet-ossnapid-structure.md)

[<span data-ttu-id="b56f2-121">JET_OSSNAPID 成員</span><span class="sxs-lookup"><span data-stu-id="b56f2-121">JET_OSSNAPID members</span></span>](./jet-ossnapid-members.md)

[<span data-ttu-id="b56f2-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="b56f2-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
