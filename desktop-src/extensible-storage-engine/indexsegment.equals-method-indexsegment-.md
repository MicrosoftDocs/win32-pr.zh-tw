---
description: '深入瞭解： IndexSegment： Equals 方法 (IndexSegment) '
title: IndexSegment)  (的 Equals 方法
TOCTitle: Equals method (IndexSegment)
ms:assetid: M:Microsoft.Isam.Esent.Interop.IndexSegment.Equals(Microsoft.Isam.Esent.Interop.IndexSegment)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.indexsegment.equals(v=EXCHG.10)
ms:contentKeyID: 55103276
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.IndexSegment.Equals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ad14e8a22ab3e64f9df870f1e0a218e83f30a0aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191650"
---
# <a name="indexsegmentequals-method-indexsegment"></a><span data-ttu-id="6d29f-103">IndexSegment)  (的 Equals 方法</span><span class="sxs-lookup"><span data-stu-id="6d29f-103">IndexSegment.Equals method (IndexSegment)</span></span>

<span data-ttu-id="6d29f-104">傳回值，這個值表示這個實例是否等於另一個實例。</span><span class="sxs-lookup"><span data-stu-id="6d29f-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="6d29f-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6d29f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6d29f-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="6d29f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6d29f-107">語法</span><span class="sxs-lookup"><span data-stu-id="6d29f-107">Syntax</span></span>

``` vb
'Declaration
Public Function Equals ( _
    other As IndexSegment _
) As Boolean
'Usage
Dim instance As IndexSegment
Dim other As IndexSegment
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    IndexSegment other
)
```

#### <a name="parameters"></a><span data-ttu-id="6d29f-108">參數</span><span class="sxs-lookup"><span data-stu-id="6d29f-108">Parameters</span></span>

  - <span data-ttu-id="6d29f-109">其他</span><span class="sxs-lookup"><span data-stu-id="6d29f-109">other</span></span>  
    <span data-ttu-id="6d29f-110">型別： [IndexSegment](./indexsegment-class.md) 。</span><span class="sxs-lookup"><span data-stu-id="6d29f-110">Type: [Microsoft.Isam.Esent.Interop.IndexSegment](./indexsegment-class.md)</span></span>  
    
    <span data-ttu-id="6d29f-111">要與這個實例比較的實例。</span><span class="sxs-lookup"><span data-stu-id="6d29f-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="6d29f-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="6d29f-112">Return value</span></span>

<span data-ttu-id="6d29f-113">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="6d29f-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="6d29f-114">如果兩個實例相等，則為 True。</span><span class="sxs-lookup"><span data-stu-id="6d29f-114">True if the two instances are equal.</span></span>  

#### <a name="implements"></a><span data-ttu-id="6d29f-115">實作</span><span class="sxs-lookup"><span data-stu-id="6d29f-115">Implements</span></span>

[<span data-ttu-id="6d29f-116">IEquatable \<T\> 。等於 (T) </span><span class="sxs-lookup"><span data-stu-id="6d29f-116">IEquatable\<T\>.Equals(T)</span></span>](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a><span data-ttu-id="6d29f-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6d29f-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6d29f-118">參考</span><span class="sxs-lookup"><span data-stu-id="6d29f-118">Reference</span></span>

[<span data-ttu-id="6d29f-119">IndexSegment 類別</span><span class="sxs-lookup"><span data-stu-id="6d29f-119">IndexSegment class</span></span>](./indexsegment-class.md)

[<span data-ttu-id="6d29f-120">IndexSegment 成員</span><span class="sxs-lookup"><span data-stu-id="6d29f-120">IndexSegment members</span></span>](./indexsegment-members.md)

[<span data-ttu-id="6d29f-121">等於多載</span><span class="sxs-lookup"><span data-stu-id="6d29f-121">Equals overload</span></span>](./indexsegment.equals-method.md)

[<span data-ttu-id="6d29f-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="6d29f-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
