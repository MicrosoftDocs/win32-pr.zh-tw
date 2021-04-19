---
description: 深入瞭解： JET_RECSIZE。減法運算子
title: 'JET_RECSIZE。減法運算子 (的 < a0/&gt; < a1/&gt;) '
TOCTitle: 'Subtraction operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.op_Subtraction(Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE,Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.op_subtraction(v=EXCHG.10)
ms:contentKeyID: 39516016
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Subtraction
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.op_Subtraction
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Subtraction
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: be60da4aeeab78794f087e9c7095a16dd39eb378
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979273"
---
# <a name="jet_recsizesubtraction-operator"></a><span data-ttu-id="d0143-103">JET_RECSIZE。減法運算子</span><span class="sxs-lookup"><span data-stu-id="d0143-103">JET_RECSIZE.Subtraction operator</span></span>

<span data-ttu-id="d0143-104">計算兩個 JET_RECSIZE 結構之間的大小差異。</span><span class="sxs-lookup"><span data-stu-id="d0143-104">Calculate the difference in sizes between two JET_RECSIZE structures.</span></span>

<span data-ttu-id="d0143-105">**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。  </span><span class="sxs-lookup"><span data-stu-id="d0143-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="d0143-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="d0143-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d0143-107">語法</span><span class="sxs-lookup"><span data-stu-id="d0143-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator - ( _
    left As JET_RECSIZE, _
    right As JET_RECSIZE _
) As JET_RECSIZE
'Usage
Dim left As JET_RECSIZE
Dim right As JET_RECSIZE
Dim returnValue As JET_RECSIZE

returnValue = (left - right)
```

``` csharp
public static JET_RECSIZE operator -(
    JET_RECSIZE left,
    JET_RECSIZE right
)
```

#### <a name="parameters"></a><span data-ttu-id="d0143-108">參數</span><span class="sxs-lookup"><span data-stu-id="d0143-108">Parameters</span></span>

  - <span data-ttu-id="d0143-109">left</span><span class="sxs-lookup"><span data-stu-id="d0143-109">left</span></span>  
    <span data-ttu-id="d0143-110">類型： [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="d0143-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="d0143-111">第一個 JET_RECSIZE。</span><span class="sxs-lookup"><span data-stu-id="d0143-111">The first JET_RECSIZE.</span></span>

<!-- end list -->

  - <span data-ttu-id="d0143-112">向右</span><span class="sxs-lookup"><span data-stu-id="d0143-112">right</span></span>  
    <span data-ttu-id="d0143-113">類型： [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="d0143-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="d0143-114">第二個 JET_RECSIZE。</span><span class="sxs-lookup"><span data-stu-id="d0143-114">The second JET_RECSIZE.</span></span>

#### <a name="return-value"></a><span data-ttu-id="d0143-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="d0143-115">Return value</span></span>

<span data-ttu-id="d0143-116">類型： [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="d0143-116">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
<span data-ttu-id="d0143-117">JET_RECSIZE，其中包含左邊和右邊之間的大小差異。</span><span class="sxs-lookup"><span data-stu-id="d0143-117">A JET_RECSIZE containing the difference in sizes between left and right.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d0143-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d0143-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d0143-119">參考</span><span class="sxs-lookup"><span data-stu-id="d0143-119">Reference</span></span>

[<span data-ttu-id="d0143-120">JET_RECSIZE 結構</span><span class="sxs-lookup"><span data-stu-id="d0143-120">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="d0143-121">JET_RECSIZE 成員</span><span class="sxs-lookup"><span data-stu-id="d0143-121">JET_RECSIZE members</span></span>](./jet-recsize-members.md)

[<span data-ttu-id="d0143-122">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="d0143-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
