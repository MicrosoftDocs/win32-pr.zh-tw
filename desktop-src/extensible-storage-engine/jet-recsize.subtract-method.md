---
description: 深入瞭解： JET_RECSIZE。減法方法
title: JET_RECSIZE。 (的 < a0/&gt; < a1/&gt;) 減去方法
TOCTitle: 'Subtract method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Subtract(Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE,Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.subtract(v=EXCHG.10)
ms:contentKeyID: 39514591
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Subtract
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Subtract
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9789dac524e57ea762243ed47d513d262d7ebb0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106999919"
---
# <a name="jet_recsizesubtract-method"></a><span data-ttu-id="9d768-103">JET_RECSIZE。減法方法</span><span class="sxs-lookup"><span data-stu-id="9d768-103">JET_RECSIZE.Subtract method</span></span>

<span data-ttu-id="9d768-104">計算兩個 JET_RECSIZE 結構之間的大小差異。</span><span class="sxs-lookup"><span data-stu-id="9d768-104">Calculate the difference in sizes between two JET_RECSIZE structures.</span></span>

<span data-ttu-id="9d768-105">**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。  </span><span class="sxs-lookup"><span data-stu-id="9d768-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="9d768-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="9d768-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9d768-107">語法</span><span class="sxs-lookup"><span data-stu-id="9d768-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function Subtract ( _
    s1 As JET_RECSIZE, _
    s2 As JET_RECSIZE _
) As JET_RECSIZE
'Usage
Dim s1 As JET_RECSIZE
Dim s2 As JET_RECSIZE
Dim returnValue As JET_RECSIZE

returnValue = JET_RECSIZE.Subtract(s1, s2)
```

``` csharp
public static JET_RECSIZE Subtract(
    JET_RECSIZE s1,
    JET_RECSIZE s2
)
```

#### <a name="parameters"></a><span data-ttu-id="9d768-108">參數</span><span class="sxs-lookup"><span data-stu-id="9d768-108">Parameters</span></span>

  - <span data-ttu-id="9d768-109">s1</span><span class="sxs-lookup"><span data-stu-id="9d768-109">s1</span></span>  
    <span data-ttu-id="9d768-110">類型： [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="9d768-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="9d768-111">第一個 JET_RECSIZE。</span><span class="sxs-lookup"><span data-stu-id="9d768-111">The first JET_RECSIZE.</span></span>

<!-- end list -->

  - <span data-ttu-id="9d768-112">s2</span><span class="sxs-lookup"><span data-stu-id="9d768-112">s2</span></span>  
    <span data-ttu-id="9d768-113">類型： [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="9d768-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="9d768-114">第二個 JET_RECSIZE。</span><span class="sxs-lookup"><span data-stu-id="9d768-114">The second JET_RECSIZE.</span></span>

#### <a name="return-value"></a><span data-ttu-id="9d768-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="9d768-115">Return value</span></span>

<span data-ttu-id="9d768-116">類型： [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="9d768-116">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
<span data-ttu-id="9d768-117">JET_RECSIZE，其中包含 s1 和 s2 之間的大小差異。</span><span class="sxs-lookup"><span data-stu-id="9d768-117">A JET_RECSIZE containing the difference in sizes between s1 and s2.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9d768-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9d768-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9d768-119">參考</span><span class="sxs-lookup"><span data-stu-id="9d768-119">Reference</span></span>

[<span data-ttu-id="9d768-120">JET_RECSIZE 結構</span><span class="sxs-lookup"><span data-stu-id="9d768-120">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="9d768-121">JET_RECSIZE 成員</span><span class="sxs-lookup"><span data-stu-id="9d768-121">JET_RECSIZE members</span></span>](./jet-recsize-members.md)

[<span data-ttu-id="9d768-122">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="9d768-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
