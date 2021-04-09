---
description: 深入瞭解： JET_RECSIZE。加法運算子
title: JET_RECSIZE。 (，) 的加法運算子
TOCTitle: 'Addition operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.op_Addition(Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE,Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.op_addition(v=EXCHG.10)
ms:contentKeyID: 39512451
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Addition
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Addition
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.op_Addition
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c41fae92f6177bf0c39138ad33988a74c482e0ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689591"
---
# <a name="jet_recsizeaddition-operator"></a><span data-ttu-id="7ffab-103">JET_RECSIZE。加法運算子</span><span class="sxs-lookup"><span data-stu-id="7ffab-103">JET_RECSIZE.Addition operator</span></span>

<span data-ttu-id="7ffab-104">將大小新增至兩個 JET_RECSIZE 結構。</span><span class="sxs-lookup"><span data-stu-id="7ffab-104">Add the sizes in two JET_RECSIZE structures.</span></span>

<span data-ttu-id="7ffab-105">**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。  </span><span class="sxs-lookup"><span data-stu-id="7ffab-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="7ffab-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="7ffab-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7ffab-107">語法</span><span class="sxs-lookup"><span data-stu-id="7ffab-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator + ( _
    left As JET_RECSIZE, _
    right As JET_RECSIZE _
) As JET_RECSIZE
'Usage
Dim left As JET_RECSIZE
Dim right As JET_RECSIZE
Dim returnValue As JET_RECSIZE

returnValue = (left + right)
```

``` csharp
public static JET_RECSIZE operator +(
    JET_RECSIZE left,
    JET_RECSIZE right
)
```

#### <a name="parameters"></a><span data-ttu-id="7ffab-108">參數</span><span class="sxs-lookup"><span data-stu-id="7ffab-108">Parameters</span></span>

  - <span data-ttu-id="7ffab-109">left</span><span class="sxs-lookup"><span data-stu-id="7ffab-109">left</span></span>  
    <span data-ttu-id="7ffab-110">類型： [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="7ffab-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="7ffab-111">第一個 JET_RECSIZE。</span><span class="sxs-lookup"><span data-stu-id="7ffab-111">The first JET_RECSIZE.</span></span>

<!-- end list -->

  - <span data-ttu-id="7ffab-112">向右</span><span class="sxs-lookup"><span data-stu-id="7ffab-112">right</span></span>  
    <span data-ttu-id="7ffab-113">類型： [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="7ffab-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="7ffab-114">第二個 JET_RECSIZE。</span><span class="sxs-lookup"><span data-stu-id="7ffab-114">The second JET_RECSIZE.</span></span>

#### <a name="return-value"></a><span data-ttu-id="7ffab-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="7ffab-115">Return value</span></span>

<span data-ttu-id="7ffab-116">類型： [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="7ffab-116">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
<span data-ttu-id="7ffab-117">JET_RECSIZE，其中包含在左邊和右邊新增大小的結果。</span><span class="sxs-lookup"><span data-stu-id="7ffab-117">A JET_RECSIZE containing the result of adding the sizes in left and right.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7ffab-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7ffab-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7ffab-119">參考</span><span class="sxs-lookup"><span data-stu-id="7ffab-119">Reference</span></span>

[<span data-ttu-id="7ffab-120">JET_RECSIZE 結構</span><span class="sxs-lookup"><span data-stu-id="7ffab-120">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="7ffab-121">JET_RECSIZE 成員</span><span class="sxs-lookup"><span data-stu-id="7ffab-121">JET_RECSIZE members</span></span>](./jet-recsize-members.md)

[<span data-ttu-id="7ffab-122">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="7ffab-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
