---
description: '深入瞭解： JET_OSSNAPID。Equals 方法 (JET_OSSNAPID) '
title: 'JET_OSSNAPID。Equals 方法 (JET_OSSNAPID) '
TOCTitle: Equals method (JET_OSSNAPID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_OSSNAPID.Equals(Microsoft.Isam.Esent.Interop.JET_OSSNAPID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_ossnapid.equals(v=EXCHG.10)
ms:contentKeyID: 39516381
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_OSSNAPID.Equals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 383b8641cb9f0ee37da0ae3ddabd8311ab38495f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106991906"
---
# <a name="jet_ossnapidequals-method-jet_ossnapid"></a><span data-ttu-id="6f167-103">JET_OSSNAPID。Equals 方法 (JET_OSSNAPID) </span><span class="sxs-lookup"><span data-stu-id="6f167-103">JET_OSSNAPID.Equals method (JET_OSSNAPID)</span></span>

<span data-ttu-id="6f167-104">傳回值，這個值表示這個實例是否等於另一個實例。</span><span class="sxs-lookup"><span data-stu-id="6f167-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="6f167-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6f167-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6f167-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="6f167-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6f167-107">語法</span><span class="sxs-lookup"><span data-stu-id="6f167-107">Syntax</span></span>

``` vb
'Declaration
Public Function Equals ( _
    other As JET_OSSNAPID _
) As Boolean
'Usage
Dim instance As JET_OSSNAPID
Dim other As JET_OSSNAPID
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_OSSNAPID other
)
```

#### <a name="parameters"></a><span data-ttu-id="6f167-108">參數</span><span class="sxs-lookup"><span data-stu-id="6f167-108">Parameters</span></span>

  - <span data-ttu-id="6f167-109">其他</span><span class="sxs-lookup"><span data-stu-id="6f167-109">other</span></span>  
    <span data-ttu-id="6f167-110">類型： [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6f167-110">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="6f167-111">要與這個實例比較的實例。</span><span class="sxs-lookup"><span data-stu-id="6f167-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="6f167-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="6f167-112">Return value</span></span>

<span data-ttu-id="6f167-113">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="6f167-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="6f167-114">如果兩個實例相等，則為 True。</span><span class="sxs-lookup"><span data-stu-id="6f167-114">True if the two instances are equal.</span></span>  

#### <a name="implements"></a><span data-ttu-id="6f167-115">實作</span><span class="sxs-lookup"><span data-stu-id="6f167-115">Implements</span></span>

[<span data-ttu-id="6f167-116">IEquatable \<T\> 。等於 (T) </span><span class="sxs-lookup"><span data-stu-id="6f167-116">IEquatable\<T\>.Equals(T)</span></span>](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a><span data-ttu-id="6f167-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6f167-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6f167-118">參考</span><span class="sxs-lookup"><span data-stu-id="6f167-118">Reference</span></span>

[<span data-ttu-id="6f167-119">JET_OSSNAPID 結構</span><span class="sxs-lookup"><span data-stu-id="6f167-119">JET_OSSNAPID structure</span></span>](./jet-ossnapid-structure.md)

[<span data-ttu-id="6f167-120">JET_OSSNAPID 成員</span><span class="sxs-lookup"><span data-stu-id="6f167-120">JET_OSSNAPID members</span></span>](./jet-ossnapid-members.md)

[<span data-ttu-id="6f167-121">等於多載</span><span class="sxs-lookup"><span data-stu-id="6f167-121">Equals overload</span></span>](./jet-ossnapid.equals-method.md)

[<span data-ttu-id="6f167-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="6f167-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
