---
description: '深入瞭解： JET_DBINFOMISC。Equals 方法 (JET_DBINFOMISC) '
title: 'JET_DBINFOMISC。Equals 方法 (JET_DBINFOMISC) '
TOCTitle: Equals method (JET_DBINFOMISC)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.Equals(Microsoft.Isam.Esent.Interop.JET_DBINFOMISC)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc.equals(v=EXCHG.10)
ms:contentKeyID: 39514332
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.Equals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bbe29fe112b82b5c88673d9301b3feb4b0c94536
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112129"
---
# <a name="jet_dbinfomiscequals-method-jet_dbinfomisc"></a><span data-ttu-id="631a1-103">JET_DBINFOMISC。Equals 方法 (JET_DBINFOMISC) </span><span class="sxs-lookup"><span data-stu-id="631a1-103">JET_DBINFOMISC.Equals method (JET_DBINFOMISC)</span></span>

<span data-ttu-id="631a1-104">指出目前的物件是否等於另一個相同類型的物件。</span><span class="sxs-lookup"><span data-stu-id="631a1-104">Indicates whether the current object is equal to another object of the same type.</span></span>

<span data-ttu-id="631a1-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="631a1-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="631a1-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="631a1-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="631a1-107">語法</span><span class="sxs-lookup"><span data-stu-id="631a1-107">Syntax</span></span>

``` vb
'Declaration
Public Function Equals ( _
    other As JET_DBINFOMISC _
) As Boolean
'Usage
Dim instance As JET_DBINFOMISC
Dim other As JET_DBINFOMISC
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_DBINFOMISC other
)
```

#### <a name="parameters"></a><span data-ttu-id="631a1-108">參數</span><span class="sxs-lookup"><span data-stu-id="631a1-108">Parameters</span></span>

  - <span data-ttu-id="631a1-109">其他</span><span class="sxs-lookup"><span data-stu-id="631a1-109">other</span></span>  
    <span data-ttu-id="631a1-110">類型： [Microsoft.Isam.Esent.Interop.JET_DBINFOMISC](./jet-dbinfomisc-class.md)</span><span class="sxs-lookup"><span data-stu-id="631a1-110">Type: [Microsoft.Isam.Esent.Interop.JET_DBINFOMISC](./jet-dbinfomisc-class.md)</span></span>  
    
    <span data-ttu-id="631a1-111">要與此物件進行比較的物件。</span><span class="sxs-lookup"><span data-stu-id="631a1-111">An object to compare with this object.</span></span>

#### <a name="return-value"></a><span data-ttu-id="631a1-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="631a1-112">Return value</span></span>

<span data-ttu-id="631a1-113">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="631a1-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="631a1-114">如果目前的物件等於另一個參數，則為 True;否則為 false。</span><span class="sxs-lookup"><span data-stu-id="631a1-114">True if the current object is equal to the other parameter; otherwise, false.</span></span>  

#### <a name="implements"></a><span data-ttu-id="631a1-115">實作</span><span class="sxs-lookup"><span data-stu-id="631a1-115">Implements</span></span>

[<span data-ttu-id="631a1-116">IEquatable \<T\> 。等於 (T) </span><span class="sxs-lookup"><span data-stu-id="631a1-116">IEquatable\<T\>.Equals(T)</span></span>](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a><span data-ttu-id="631a1-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="631a1-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="631a1-118">參考</span><span class="sxs-lookup"><span data-stu-id="631a1-118">Reference</span></span>

[<span data-ttu-id="631a1-119">JET_DBINFOMISC 類別</span><span class="sxs-lookup"><span data-stu-id="631a1-119">JET_DBINFOMISC class</span></span>](./jet-dbinfomisc-class.md)

[<span data-ttu-id="631a1-120">JET_DBINFOMISC 成員</span><span class="sxs-lookup"><span data-stu-id="631a1-120">JET_DBINFOMISC members</span></span>](./jet-dbinfomisc-members.md)

[<span data-ttu-id="631a1-121">等於多載</span><span class="sxs-lookup"><span data-stu-id="631a1-121">Equals overload</span></span>](./jet-dbinfomisc.equals-method.md)

[<span data-ttu-id="631a1-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="631a1-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
