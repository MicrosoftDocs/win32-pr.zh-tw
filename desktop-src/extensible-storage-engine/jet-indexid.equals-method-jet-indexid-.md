---
description: '深入瞭解： JET_INDEXID。Equals 方法 (JET_INDEXID) '
title: 'JET_INDEXID。Equals 方法 (JET_INDEXID) '
TOCTitle: Equals method (JET_INDEXID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_INDEXID.Equals(Microsoft.Isam.Esent.Interop.JET_INDEXID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexid.equals(v=EXCHG.10)
ms:contentKeyID: 39515277
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXID.Equals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 10877a283e10d6126c46fa1c5687b23814aa2ac9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000184"
---
# <a name="jet_indexidequals-method-jet_indexid"></a><span data-ttu-id="afd3f-103">JET_INDEXID。Equals 方法 (JET_INDEXID) </span><span class="sxs-lookup"><span data-stu-id="afd3f-103">JET_INDEXID.Equals method (JET_INDEXID)</span></span>

<span data-ttu-id="afd3f-104">傳回值，這個值表示這個實例是否等於另一個實例。</span><span class="sxs-lookup"><span data-stu-id="afd3f-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="afd3f-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="afd3f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="afd3f-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="afd3f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="afd3f-107">語法</span><span class="sxs-lookup"><span data-stu-id="afd3f-107">Syntax</span></span>

``` vb
'Declaration
Public Function Equals ( _
    other As JET_INDEXID _
) As Boolean
'Usage
Dim instance As JET_INDEXID
Dim other As JET_INDEXID
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_INDEXID other
)
```

#### <a name="parameters"></a><span data-ttu-id="afd3f-108">參數</span><span class="sxs-lookup"><span data-stu-id="afd3f-108">Parameters</span></span>

  - <span data-ttu-id="afd3f-109">其他</span><span class="sxs-lookup"><span data-stu-id="afd3f-109">other</span></span>  
    <span data-ttu-id="afd3f-110">類型： [Microsoft.Isam.Esent.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="afd3f-110">Type: [Microsoft.Isam.Esent.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span></span>  
    
    <span data-ttu-id="afd3f-111">要與這個實例比較的實例。</span><span class="sxs-lookup"><span data-stu-id="afd3f-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="afd3f-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="afd3f-112">Return value</span></span>

<span data-ttu-id="afd3f-113">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="afd3f-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="afd3f-114">如果兩個實例相等，則為 True。</span><span class="sxs-lookup"><span data-stu-id="afd3f-114">True if the two instances are equal.</span></span>  

#### <a name="implements"></a><span data-ttu-id="afd3f-115">實作</span><span class="sxs-lookup"><span data-stu-id="afd3f-115">Implements</span></span>

[<span data-ttu-id="afd3f-116">IEquatable \<T\> 。等於 (T) </span><span class="sxs-lookup"><span data-stu-id="afd3f-116">IEquatable\<T\>.Equals(T)</span></span>](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a><span data-ttu-id="afd3f-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="afd3f-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="afd3f-118">參考</span><span class="sxs-lookup"><span data-stu-id="afd3f-118">Reference</span></span>

[<span data-ttu-id="afd3f-119">JET_INDEXID 結構</span><span class="sxs-lookup"><span data-stu-id="afd3f-119">JET_INDEXID structure</span></span>](./jet-indexid-structure2.md)

[<span data-ttu-id="afd3f-120">JET_INDEXID 成員</span><span class="sxs-lookup"><span data-stu-id="afd3f-120">JET_INDEXID members</span></span>](./jet-indexid-members.md)

[<span data-ttu-id="afd3f-121">等於多載</span><span class="sxs-lookup"><span data-stu-id="afd3f-121">Equals overload</span></span>](./jet-indexid.equals-method.md)

[<span data-ttu-id="afd3f-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="afd3f-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
