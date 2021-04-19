---
description: '深入瞭解： JET_RECSIZE。Equals 方法 (JET_RECSIZE) '
title: JET_RECSIZE。Equals 方法 (JET_RECSIZE)  (的) 。
TOCTitle: Equals method (JET_RECSIZE)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Equals(Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.equals(v=EXCHG.10)
ms:contentKeyID: 39511266
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Equals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ecc4aff26b80754d47fdffb70dbdeb1963cf065f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974002"
---
# <a name="jet_recsizeequals-method-jet_recsize"></a><span data-ttu-id="2093a-103">JET_RECSIZE。Equals 方法 (JET_RECSIZE) </span><span class="sxs-lookup"><span data-stu-id="2093a-103">JET_RECSIZE.Equals method (JET_RECSIZE)</span></span>

<span data-ttu-id="2093a-104">傳回值，這個值表示這個實例是否等於另一個實例。</span><span class="sxs-lookup"><span data-stu-id="2093a-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="2093a-105">**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。  </span><span class="sxs-lookup"><span data-stu-id="2093a-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="2093a-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="2093a-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2093a-107">語法</span><span class="sxs-lookup"><span data-stu-id="2093a-107">Syntax</span></span>

``` vb
'Declaration
Public Function Equals ( _
    other As JET_RECSIZE _
) As Boolean
'Usage
Dim instance As JET_RECSIZE
Dim other As JET_RECSIZE
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_RECSIZE other
)
```

#### <a name="parameters"></a><span data-ttu-id="2093a-108">參數</span><span class="sxs-lookup"><span data-stu-id="2093a-108">Parameters</span></span>

  - <span data-ttu-id="2093a-109">其他</span><span class="sxs-lookup"><span data-stu-id="2093a-109">other</span></span>  
    <span data-ttu-id="2093a-110">類型： [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="2093a-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="2093a-111">與這個執行個體相互比較的物件。</span><span class="sxs-lookup"><span data-stu-id="2093a-111">An object to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="2093a-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="2093a-112">Return value</span></span>

<span data-ttu-id="2093a-113">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="2093a-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="2093a-114">如果兩個實例相等，則為 True。</span><span class="sxs-lookup"><span data-stu-id="2093a-114">True if the two instances are equal.</span></span>  

#### <a name="implements"></a><span data-ttu-id="2093a-115">實作</span><span class="sxs-lookup"><span data-stu-id="2093a-115">Implements</span></span>

[<span data-ttu-id="2093a-116">IEquatable \<T\> 。等於 (T) </span><span class="sxs-lookup"><span data-stu-id="2093a-116">IEquatable\<T\>.Equals(T)</span></span>](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a><span data-ttu-id="2093a-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2093a-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2093a-118">參考</span><span class="sxs-lookup"><span data-stu-id="2093a-118">Reference</span></span>

[<span data-ttu-id="2093a-119">JET_RECSIZE 結構</span><span class="sxs-lookup"><span data-stu-id="2093a-119">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="2093a-120">JET_RECSIZE 成員</span><span class="sxs-lookup"><span data-stu-id="2093a-120">JET_RECSIZE members</span></span>](./jet-recsize-members.md)

[<span data-ttu-id="2093a-121">等於多載</span><span class="sxs-lookup"><span data-stu-id="2093a-121">Equals overload</span></span>](./jet-recsize.equals-method.md)

[<span data-ttu-id="2093a-122">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="2093a-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
