---
description: 深入瞭解： JET_HANDLE。不等比較運算子
title: JET_HANDLE。不等比較運算子
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_HANDLE.op_Inequality(Microsoft.Isam.Esent.Interop.JET_HANDLE,Microsoft.Isam.Esent.Interop.JET_HANDLE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_handle.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39511285
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_HANDLE.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_HANDLE.op_Inequality
- Microsoft.Isam.Esent.Interop.JET_HANDLE.Inequality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5feee9739ad57103b71786ae7d1cdbf5f7e858ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320503"
---
# <a name="jet_handleinequality-operator"></a><span data-ttu-id="87fc8-103">JET_HANDLE。不等比較運算子</span><span class="sxs-lookup"><span data-stu-id="87fc8-103">JET_HANDLE.Inequality operator</span></span>

<span data-ttu-id="87fc8-104">判斷 JET_HANDLE 的兩個指定實例是否不相等。</span><span class="sxs-lookup"><span data-stu-id="87fc8-104">Determines whether two specified instances of JET_HANDLE are not equal.</span></span>

<span data-ttu-id="87fc8-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="87fc8-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="87fc8-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="87fc8-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="87fc8-107">語法</span><span class="sxs-lookup"><span data-stu-id="87fc8-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_HANDLE, _
    rhs As JET_HANDLE _
) As Boolean
'Usage
Dim lhs As JET_HANDLE
Dim rhs As JET_HANDLE
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_HANDLE lhs,
    JET_HANDLE rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="87fc8-108">參數</span><span class="sxs-lookup"><span data-stu-id="87fc8-108">Parameters</span></span>

  - <span data-ttu-id="87fc8-109">lhs</span><span class="sxs-lookup"><span data-stu-id="87fc8-109">lhs</span></span>  
    <span data-ttu-id="87fc8-110">類型： [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span><span class="sxs-lookup"><span data-stu-id="87fc8-110">Type: [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span></span>  
    
    <span data-ttu-id="87fc8-111">要比較的第一個執行個體。</span><span class="sxs-lookup"><span data-stu-id="87fc8-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="87fc8-112">rhs</span><span class="sxs-lookup"><span data-stu-id="87fc8-112">rhs</span></span>  
    <span data-ttu-id="87fc8-113">類型： [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span><span class="sxs-lookup"><span data-stu-id="87fc8-113">Type: [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span></span>  
    
    <span data-ttu-id="87fc8-114">要比較的第二個執行個體。</span><span class="sxs-lookup"><span data-stu-id="87fc8-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="87fc8-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="87fc8-115">Return value</span></span>

<span data-ttu-id="87fc8-116">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="87fc8-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="87fc8-117">如果兩個實例不相等，則為 True。</span><span class="sxs-lookup"><span data-stu-id="87fc8-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="87fc8-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="87fc8-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="87fc8-119">參考</span><span class="sxs-lookup"><span data-stu-id="87fc8-119">Reference</span></span>

[<span data-ttu-id="87fc8-120">JET_HANDLE 結構</span><span class="sxs-lookup"><span data-stu-id="87fc8-120">JET_HANDLE structure</span></span>](./jet-handle-structure.md)

[<span data-ttu-id="87fc8-121">JET_HANDLE 成員</span><span class="sxs-lookup"><span data-stu-id="87fc8-121">JET_HANDLE members</span></span>](./jet-handle-members.md)

[<span data-ttu-id="87fc8-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="87fc8-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
