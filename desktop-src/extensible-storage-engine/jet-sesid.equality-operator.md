---
description: 深入瞭解： JET_SESID。等號比較運算子
title: JET_SESID。等號比較運算子
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_SESID.op_Equality(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_SESID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_sesid.op_equality(v=EXCHG.10)
ms:contentKeyID: 39511173
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SESID.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SESID.Equality
- Microsoft.Isam.Esent.Interop.JET_SESID.op_Equality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 19e0550452fb0053978cabcdb393222c814c85f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468832"
---
# <a name="jet_sesidequality-operator"></a><span data-ttu-id="bba33-103">JET_SESID。等號比較運算子</span><span class="sxs-lookup"><span data-stu-id="bba33-103">JET_SESID.Equality operator</span></span>

<span data-ttu-id="bba33-104">判斷 JET_SESID 的兩個指定實例是否相等。</span><span class="sxs-lookup"><span data-stu-id="bba33-104">Determines whether two specified instances of JET_SESID are equal.</span></span>

<span data-ttu-id="bba33-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="bba33-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="bba33-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="bba33-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="bba33-107">語法</span><span class="sxs-lookup"><span data-stu-id="bba33-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_SESID, _
    rhs As JET_SESID _
) As Boolean
'Usage
Dim lhs As JET_SESID
Dim rhs As JET_SESID
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_SESID lhs,
    JET_SESID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="bba33-108">參數</span><span class="sxs-lookup"><span data-stu-id="bba33-108">Parameters</span></span>

  - <span data-ttu-id="bba33-109">lhs</span><span class="sxs-lookup"><span data-stu-id="bba33-109">lhs</span></span>  
    <span data-ttu-id="bba33-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="bba33-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="bba33-111">要比較的第一個執行個體。</span><span class="sxs-lookup"><span data-stu-id="bba33-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="bba33-112">rhs</span><span class="sxs-lookup"><span data-stu-id="bba33-112">rhs</span></span>  
    <span data-ttu-id="bba33-113">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="bba33-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="bba33-114">要比較的第二個執行個體。</span><span class="sxs-lookup"><span data-stu-id="bba33-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="bba33-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="bba33-115">Return value</span></span>

<span data-ttu-id="bba33-116">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="bba33-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="bba33-117">如果兩個實例相等，則為 True。</span><span class="sxs-lookup"><span data-stu-id="bba33-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="bba33-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bba33-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bba33-119">參考</span><span class="sxs-lookup"><span data-stu-id="bba33-119">Reference</span></span>

[<span data-ttu-id="bba33-120">JET_SESID 結構</span><span class="sxs-lookup"><span data-stu-id="bba33-120">JET_SESID structure</span></span>](./jet-sesid-structure.md)

[<span data-ttu-id="bba33-121">JET_SESID 成員</span><span class="sxs-lookup"><span data-stu-id="bba33-121">JET_SESID members</span></span>](./jet-sesid-members.md)

[<span data-ttu-id="bba33-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="bba33-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
