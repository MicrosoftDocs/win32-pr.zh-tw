---
description: 深入瞭解： JET_COLUMNID。GreaterThan 運算子
title: JET_COLUMNID。GreaterThan 運算子
TOCTitle: 'GreaterThan operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_GreaterThan(Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnid.op_greaterthan(v=EXCHG.10)
ms:contentKeyID: 39513070
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.GreaterThan
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_GreaterThan
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.GreaterThan
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 16105651443aad050a1bbaf4a9dee1e68a5042fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982712"
---
# <a name="jet_columnidgreaterthan-operator"></a><span data-ttu-id="ff21e-103">JET_COLUMNID。GreaterThan 運算子</span><span class="sxs-lookup"><span data-stu-id="ff21e-103">JET_COLUMNID.GreaterThan operator</span></span>

<span data-ttu-id="ff21e-104">判斷一個 columnid 是否位於另一個 columnid 之後。</span><span class="sxs-lookup"><span data-stu-id="ff21e-104">Determine whether one columnid is after another columnid.</span></span>

<span data-ttu-id="ff21e-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ff21e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ff21e-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="ff21e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ff21e-107">語法</span><span class="sxs-lookup"><span data-stu-id="ff21e-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator > ( _
    lhs As JET_COLUMNID, _
    rhs As JET_COLUMNID _
) As Boolean
'Usage
Dim lhs As JET_COLUMNID
Dim rhs As JET_COLUMNID
Dim returnValue As Boolean

returnValue = (lhs > rhs)
```

``` csharp
public static bool operator >(
    JET_COLUMNID lhs,
    JET_COLUMNID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="ff21e-108">參數</span><span class="sxs-lookup"><span data-stu-id="ff21e-108">Parameters</span></span>

  - <span data-ttu-id="ff21e-109">lhs</span><span class="sxs-lookup"><span data-stu-id="ff21e-109">lhs</span></span>  
    <span data-ttu-id="ff21e-110">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ff21e-110">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="ff21e-111">要比較的第一個 columnid。</span><span class="sxs-lookup"><span data-stu-id="ff21e-111">The first columnid to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="ff21e-112">rhs</span><span class="sxs-lookup"><span data-stu-id="ff21e-112">rhs</span></span>  
    <span data-ttu-id="ff21e-113">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ff21e-113">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="ff21e-114">要比較的第二個 columnid。</span><span class="sxs-lookup"><span data-stu-id="ff21e-114">The second columnid to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="ff21e-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="ff21e-115">Return value</span></span>

<span data-ttu-id="ff21e-116">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="ff21e-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="ff21e-117">如果 lhs 在 rhs 之後，則為 True。</span><span class="sxs-lookup"><span data-stu-id="ff21e-117">True if lhs comes after rhs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ff21e-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ff21e-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ff21e-119">參考</span><span class="sxs-lookup"><span data-stu-id="ff21e-119">Reference</span></span>

[<span data-ttu-id="ff21e-120">JET_COLUMNID 結構</span><span class="sxs-lookup"><span data-stu-id="ff21e-120">JET_COLUMNID structure</span></span>](./jet-columnid-structure.md)

[<span data-ttu-id="ff21e-121">JET_COLUMNID 成員</span><span class="sxs-lookup"><span data-stu-id="ff21e-121">JET_COLUMNID members</span></span>](./jet-columnid-members.md)

[<span data-ttu-id="ff21e-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="ff21e-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
