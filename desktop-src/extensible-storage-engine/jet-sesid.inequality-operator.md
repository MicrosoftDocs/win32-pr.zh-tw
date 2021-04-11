---
description: 深入瞭解： JET_SESID。不等比較運算子
title: JET_SESID。不等比較運算子
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_SESID.op_Inequality(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_SESID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_sesid.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39514305
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SESID.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SESID.Inequality
- Microsoft.Isam.Esent.Interop.JET_SESID.op_Inequality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4e42b5e21937ae8af4ccd04708520ece40558c5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112541"
---
# <a name="jet_sesidinequality-operator"></a><span data-ttu-id="7e158-103">JET_SESID。不等比較運算子</span><span class="sxs-lookup"><span data-stu-id="7e158-103">JET_SESID.Inequality operator</span></span>

<span data-ttu-id="7e158-104">判斷 JET_SESID 的兩個指定實例是否不相等。</span><span class="sxs-lookup"><span data-stu-id="7e158-104">Determines whether two specified instances of JET_SESID are not equal.</span></span>

<span data-ttu-id="7e158-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7e158-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7e158-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="7e158-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7e158-107">語法</span><span class="sxs-lookup"><span data-stu-id="7e158-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_SESID, _
    rhs As JET_SESID _
) As Boolean
'Usage
Dim lhs As JET_SESID
Dim rhs As JET_SESID
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_SESID lhs,
    JET_SESID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="7e158-108">參數</span><span class="sxs-lookup"><span data-stu-id="7e158-108">Parameters</span></span>

  - <span data-ttu-id="7e158-109">lhs</span><span class="sxs-lookup"><span data-stu-id="7e158-109">lhs</span></span>  
    <span data-ttu-id="7e158-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7e158-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="7e158-111">要比較的第一個執行個體。</span><span class="sxs-lookup"><span data-stu-id="7e158-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="7e158-112">rhs</span><span class="sxs-lookup"><span data-stu-id="7e158-112">rhs</span></span>  
    <span data-ttu-id="7e158-113">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7e158-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="7e158-114">要比較的第二個執行個體。</span><span class="sxs-lookup"><span data-stu-id="7e158-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="7e158-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="7e158-115">Return value</span></span>

<span data-ttu-id="7e158-116">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="7e158-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="7e158-117">如果兩個實例不相等，則為 True。</span><span class="sxs-lookup"><span data-stu-id="7e158-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7e158-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7e158-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7e158-119">參考</span><span class="sxs-lookup"><span data-stu-id="7e158-119">Reference</span></span>

[<span data-ttu-id="7e158-120">JET_SESID 結構</span><span class="sxs-lookup"><span data-stu-id="7e158-120">JET_SESID structure</span></span>](./jet-sesid-structure.md)

[<span data-ttu-id="7e158-121">JET_SESID 成員</span><span class="sxs-lookup"><span data-stu-id="7e158-121">JET_SESID members</span></span>](./jet-sesid-members.md)

[<span data-ttu-id="7e158-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="7e158-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
