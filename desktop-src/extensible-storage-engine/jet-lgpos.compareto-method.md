---
description: 深入瞭解： JET_LGPOS CompareTo 方法
title: JET_LGPOS CompareTo 方法
TOCTitle: 'CompareTo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LGPOS.CompareTo(Microsoft.Isam.Esent.Interop.JET_LGPOS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_lgpos.compareto(v=EXCHG.10)
ms:contentKeyID: 39514516
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.CompareTo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.CompareTo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 83012ed755ab876618147c013e99868927e16f1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987690"
---
# <a name="jet_lgposcompareto-method"></a><span data-ttu-id="9ad75-103">JET_LGPOS CompareTo 方法</span><span class="sxs-lookup"><span data-stu-id="9ad75-103">JET_LGPOS.CompareTo method</span></span>

<span data-ttu-id="9ad75-104">將這個記錄檔位置與另一個記錄位置進行比較，並判斷這個實例是否在另一個實例之前、相同的或之後。</span><span class="sxs-lookup"><span data-stu-id="9ad75-104">Compares this log position to another log position and determines whether this instance is before, the same as or after the other instance.</span></span>

<span data-ttu-id="9ad75-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9ad75-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9ad75-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="9ad75-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9ad75-107">語法</span><span class="sxs-lookup"><span data-stu-id="9ad75-107">Syntax</span></span>

``` vb
'Declaration
Public Function CompareTo ( _
    other As JET_LGPOS _
) As Integer
'Usage
Dim instance As JET_LGPOS
Dim other As JET_LGPOS
Dim returnValue As Integer

returnValue = instance.CompareTo(other)
```

``` csharp
public int CompareTo(
    JET_LGPOS other
)
```

#### <a name="parameters"></a><span data-ttu-id="9ad75-108">參數</span><span class="sxs-lookup"><span data-stu-id="9ad75-108">Parameters</span></span>

  - <span data-ttu-id="9ad75-109">其他</span><span class="sxs-lookup"><span data-stu-id="9ad75-109">other</span></span>  
    <span data-ttu-id="9ad75-110">類型： [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="9ad75-110">Type: [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span></span>  
    
    <span data-ttu-id="9ad75-111">要與目前實例比較的記錄檔位置。</span><span class="sxs-lookup"><span data-stu-id="9ad75-111">The log position to compare to the current instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="9ad75-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="9ad75-112">Return value</span></span>

<span data-ttu-id="9ad75-113">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="9ad75-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
<span data-ttu-id="9ad75-114">帶正負號的數位，指出這個實例和值參數的相對位置。</span><span class="sxs-lookup"><span data-stu-id="9ad75-114">A signed number indicating the relative positions of this instance and the value parameter.</span></span>  

#### <a name="implements"></a><span data-ttu-id="9ad75-115">實作</span><span class="sxs-lookup"><span data-stu-id="9ad75-115">Implements</span></span>

[<span data-ttu-id="9ad75-116">IComparable \<T\> 。CompareTo (T) </span><span class="sxs-lookup"><span data-stu-id="9ad75-116">IComparable\<T\>.CompareTo(T)</span></span>](/dotnet/api/system.icomparable-1.compareto#System_IComparable_1_CompareTo__0_)  

## <a name="see-also"></a><span data-ttu-id="9ad75-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9ad75-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9ad75-118">參考</span><span class="sxs-lookup"><span data-stu-id="9ad75-118">Reference</span></span>

[<span data-ttu-id="9ad75-119">JET_LGPOS 結構</span><span class="sxs-lookup"><span data-stu-id="9ad75-119">JET_LGPOS structure</span></span>](./jet-lgpos-structure2.md)

[<span data-ttu-id="9ad75-120">JET_LGPOS 成員</span><span class="sxs-lookup"><span data-stu-id="9ad75-120">JET_LGPOS members</span></span>](./jet-lgpos-members.md)

[<span data-ttu-id="9ad75-121">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="9ad75-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
