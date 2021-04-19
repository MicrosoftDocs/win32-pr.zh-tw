---
description: '深入瞭解： JET_LS。Equals 方法 (JET_LS) '
title: 'JET_LS。Equals 方法 (JET_LS) '
TOCTitle: Equals method (JET_LS)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LS.Equals(Microsoft.Isam.Esent.Interop.JET_LS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_ls.equals(v=EXCHG.10)
ms:contentKeyID: 39510488
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_LS.Equals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c8a571f97fcf5abc5ff9a69ff476d48adfd8015c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984611"
---
# <a name="jet_lsequals-method-jet_ls"></a><span data-ttu-id="c8771-103">JET_LS。Equals 方法 (JET_LS) </span><span class="sxs-lookup"><span data-stu-id="c8771-103">JET_LS.Equals method (JET_LS)</span></span>

<span data-ttu-id="c8771-104">傳回值，這個值表示這個實例是否等於另一個實例。</span><span class="sxs-lookup"><span data-stu-id="c8771-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="c8771-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c8771-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c8771-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="c8771-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c8771-107">語法</span><span class="sxs-lookup"><span data-stu-id="c8771-107">Syntax</span></span>

``` vb
'Declaration
Public Function Equals ( _
    other As JET_LS _
) As Boolean
'Usage
Dim instance As JET_LS
Dim other As JET_LS
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_LS other
)
```

#### <a name="parameters"></a><span data-ttu-id="c8771-108">參數</span><span class="sxs-lookup"><span data-stu-id="c8771-108">Parameters</span></span>

  - <span data-ttu-id="c8771-109">其他</span><span class="sxs-lookup"><span data-stu-id="c8771-109">other</span></span>  
    <span data-ttu-id="c8771-110">類型： [Microsoft.Isam.Esent.Interop.JET_LS](./jet-ls-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c8771-110">Type: [Microsoft.Isam.Esent.Interop.JET_LS](./jet-ls-structure.md)</span></span>  
    
    <span data-ttu-id="c8771-111">要與這個實例比較的實例。</span><span class="sxs-lookup"><span data-stu-id="c8771-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="c8771-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="c8771-112">Return value</span></span>

<span data-ttu-id="c8771-113">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="c8771-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="c8771-114">如果兩個實例相等，則為 True。</span><span class="sxs-lookup"><span data-stu-id="c8771-114">True if the two instances are equal.</span></span>  

#### <a name="implements"></a><span data-ttu-id="c8771-115">實作</span><span class="sxs-lookup"><span data-stu-id="c8771-115">Implements</span></span>

[<span data-ttu-id="c8771-116">IEquatable \<T\> 。等於 (T) </span><span class="sxs-lookup"><span data-stu-id="c8771-116">IEquatable\<T\>.Equals(T)</span></span>](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a><span data-ttu-id="c8771-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c8771-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c8771-118">參考</span><span class="sxs-lookup"><span data-stu-id="c8771-118">Reference</span></span>

[<span data-ttu-id="c8771-119">JET_LS 結構</span><span class="sxs-lookup"><span data-stu-id="c8771-119">JET_LS structure</span></span>](./jet-ls-structure.md)

[<span data-ttu-id="c8771-120">JET_LS 成員</span><span class="sxs-lookup"><span data-stu-id="c8771-120">JET_LS members</span></span>](./jet-ls-members.md)

[<span data-ttu-id="c8771-121">等於多載</span><span class="sxs-lookup"><span data-stu-id="c8771-121">Equals overload</span></span>](./jet-ls.equals-method.md)

[<span data-ttu-id="c8771-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="c8771-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
