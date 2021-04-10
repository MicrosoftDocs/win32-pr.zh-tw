---
description: 深入瞭解： JET_SIGNATURE。等號比較運算子
title: JET_SIGNATURE。等號比較運算子
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_SIGNATURE.op_Equality(Microsoft.Isam.Esent.Interop.JET_SIGNATURE,Microsoft.Isam.Esent.Interop.JET_SIGNATURE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_signature.op_equality(v=EXCHG.10)
ms:contentKeyID: 39512803
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE.op_Equality
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE.Equality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 011510343f79724c2c529c2b6b18537b43facbef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690911"
---
# <a name="jet_signatureequality-operator"></a><span data-ttu-id="aa02e-103">JET_SIGNATURE。等號比較運算子</span><span class="sxs-lookup"><span data-stu-id="aa02e-103">JET_SIGNATURE.Equality operator</span></span>

<span data-ttu-id="aa02e-104">判斷 JET_SIGNATURE 的兩個指定實例是否相等。</span><span class="sxs-lookup"><span data-stu-id="aa02e-104">Determines whether two specified instances of JET_SIGNATURE are equal.</span></span>

<span data-ttu-id="aa02e-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="aa02e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="aa02e-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="aa02e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="aa02e-107">語法</span><span class="sxs-lookup"><span data-stu-id="aa02e-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_SIGNATURE, _
    rhs As JET_SIGNATURE _
) As Boolean
'Usage
Dim lhs As JET_SIGNATURE
Dim rhs As JET_SIGNATURE
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_SIGNATURE lhs,
    JET_SIGNATURE rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="aa02e-108">參數</span><span class="sxs-lookup"><span data-stu-id="aa02e-108">Parameters</span></span>

  - <span data-ttu-id="aa02e-109">lhs</span><span class="sxs-lookup"><span data-stu-id="aa02e-109">lhs</span></span>  
    <span data-ttu-id="aa02e-110">類型： [Microsoft.Isam.Esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="aa02e-110">Type: [Microsoft.Isam.Esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span></span>  
    
    <span data-ttu-id="aa02e-111">要比較的第一個執行個體。</span><span class="sxs-lookup"><span data-stu-id="aa02e-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="aa02e-112">rhs</span><span class="sxs-lookup"><span data-stu-id="aa02e-112">rhs</span></span>  
    <span data-ttu-id="aa02e-113">類型： [Microsoft.Isam.Esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="aa02e-113">Type: [Microsoft.Isam.Esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span></span>  
    
    <span data-ttu-id="aa02e-114">要比較的第二個執行個體。</span><span class="sxs-lookup"><span data-stu-id="aa02e-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="aa02e-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="aa02e-115">Return value</span></span>

<span data-ttu-id="aa02e-116">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="aa02e-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="aa02e-117">如果兩個實例相等，則為 True。</span><span class="sxs-lookup"><span data-stu-id="aa02e-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="aa02e-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aa02e-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="aa02e-119">參考</span><span class="sxs-lookup"><span data-stu-id="aa02e-119">Reference</span></span>

[<span data-ttu-id="aa02e-120">JET_SIGNATURE 結構</span><span class="sxs-lookup"><span data-stu-id="aa02e-120">JET_SIGNATURE structure</span></span>](./jet-signature-structure2.md)

[<span data-ttu-id="aa02e-121">JET_SIGNATURE 成員</span><span class="sxs-lookup"><span data-stu-id="aa02e-121">JET_SIGNATURE members</span></span>](./jet-signature-members.md)

[<span data-ttu-id="aa02e-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="aa02e-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
