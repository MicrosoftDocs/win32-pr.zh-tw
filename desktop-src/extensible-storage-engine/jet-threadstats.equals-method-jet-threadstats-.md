---
description: '深入瞭解： JET_THREADSTATS。Equals 方法 (JET_THREADSTATS) '
title: JET_THREADSTATS。Equals 方法 (JET_THREADSTATS)  (的) 。
TOCTitle: Equals method (JET_THREADSTATS)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Equals(Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.equals(v=EXCHG.10)
ms:contentKeyID: 39515931
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Equals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 716b9d45002c0182fd4a629b018f9287aff812e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193987"
---
# <a name="jet_threadstatsequals-method-jet_threadstats"></a><span data-ttu-id="2bb8c-103">JET_THREADSTATS。Equals 方法 (JET_THREADSTATS) </span><span class="sxs-lookup"><span data-stu-id="2bb8c-103">JET_THREADSTATS.Equals method (JET_THREADSTATS)</span></span>

<span data-ttu-id="2bb8c-104">傳回值，這個值表示這個實例是否等於另一個實例。</span><span class="sxs-lookup"><span data-stu-id="2bb8c-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="2bb8c-105">**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。  </span><span class="sxs-lookup"><span data-stu-id="2bb8c-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="2bb8c-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="2bb8c-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2bb8c-107">語法</span><span class="sxs-lookup"><span data-stu-id="2bb8c-107">Syntax</span></span>

``` vb
'Declaration
Public Function Equals ( _
    other As JET_THREADSTATS _
) As Boolean
'Usage
Dim instance As JET_THREADSTATS
Dim other As JET_THREADSTATS
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_THREADSTATS other
)
```

#### <a name="parameters"></a><span data-ttu-id="2bb8c-108">參數</span><span class="sxs-lookup"><span data-stu-id="2bb8c-108">Parameters</span></span>

  - <span data-ttu-id="2bb8c-109">其他</span><span class="sxs-lookup"><span data-stu-id="2bb8c-109">other</span></span>  
    <span data-ttu-id="2bb8c-110">類型： [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="2bb8c-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="2bb8c-111">要與這個實例比較的實例。</span><span class="sxs-lookup"><span data-stu-id="2bb8c-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="2bb8c-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="2bb8c-112">Return value</span></span>

<span data-ttu-id="2bb8c-113">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="2bb8c-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="2bb8c-114">如果兩個實例相等，則為 True。</span><span class="sxs-lookup"><span data-stu-id="2bb8c-114">True if the two instances are equal.</span></span>  

#### <a name="implements"></a><span data-ttu-id="2bb8c-115">實作</span><span class="sxs-lookup"><span data-stu-id="2bb8c-115">Implements</span></span>

[<span data-ttu-id="2bb8c-116">IEquatable \<T\> 。等於 (T) </span><span class="sxs-lookup"><span data-stu-id="2bb8c-116">IEquatable\<T\>.Equals(T)</span></span>](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a><span data-ttu-id="2bb8c-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2bb8c-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2bb8c-118">參考</span><span class="sxs-lookup"><span data-stu-id="2bb8c-118">Reference</span></span>

[<span data-ttu-id="2bb8c-119">JET_THREADSTATS 結構</span><span class="sxs-lookup"><span data-stu-id="2bb8c-119">JET_THREADSTATS structure</span></span>](./jet-threadstats-structure2.md)

[<span data-ttu-id="2bb8c-120">JET_THREADSTATS 成員</span><span class="sxs-lookup"><span data-stu-id="2bb8c-120">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="2bb8c-121">等於多載</span><span class="sxs-lookup"><span data-stu-id="2bb8c-121">Equals overload</span></span>](./jet-threadstats.equals-method.md)

[<span data-ttu-id="2bb8c-122">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="2bb8c-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
