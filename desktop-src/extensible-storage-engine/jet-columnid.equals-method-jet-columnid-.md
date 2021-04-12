---
description: '深入瞭解： JET_COLUMNID。Equals 方法 (JET_COLUMNID) '
title: 'JET_COLUMNID。Equals 方法 (JET_COLUMNID) '
TOCTitle: Equals method (JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNID.Equals(Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnid.equals(v=EXCHG.10)
ms:contentKeyID: 39516458
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.Equals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cb0cc59a465f48474e2fe63f5ef78f1fea85f37c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191644"
---
# <a name="jet_columnidequals-method-jet_columnid"></a><span data-ttu-id="181c2-103">JET_COLUMNID。Equals 方法 (JET_COLUMNID) </span><span class="sxs-lookup"><span data-stu-id="181c2-103">JET_COLUMNID.Equals method (JET_COLUMNID)</span></span>

<span data-ttu-id="181c2-104">傳回值，這個值表示這個實例是否等於另一個實例。</span><span class="sxs-lookup"><span data-stu-id="181c2-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="181c2-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="181c2-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="181c2-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="181c2-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="181c2-107">語法</span><span class="sxs-lookup"><span data-stu-id="181c2-107">Syntax</span></span>

``` vb
'Declaration
Public Function Equals ( _
    other As JET_COLUMNID _
) As Boolean
'Usage
Dim instance As JET_COLUMNID
Dim other As JET_COLUMNID
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_COLUMNID other
)
```

#### <a name="parameters"></a><span data-ttu-id="181c2-108">參數</span><span class="sxs-lookup"><span data-stu-id="181c2-108">Parameters</span></span>

  - <span data-ttu-id="181c2-109">其他</span><span class="sxs-lookup"><span data-stu-id="181c2-109">other</span></span>  
    <span data-ttu-id="181c2-110">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="181c2-110">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="181c2-111">要與這個實例比較的實例。</span><span class="sxs-lookup"><span data-stu-id="181c2-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="181c2-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="181c2-112">Return value</span></span>

<span data-ttu-id="181c2-113">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="181c2-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="181c2-114">如果兩個實例相等，則為 True。</span><span class="sxs-lookup"><span data-stu-id="181c2-114">True if the two instances are equal.</span></span>  

#### <a name="implements"></a><span data-ttu-id="181c2-115">實作</span><span class="sxs-lookup"><span data-stu-id="181c2-115">Implements</span></span>

[<span data-ttu-id="181c2-116">IEquatable \<T\> 。等於 (T) </span><span class="sxs-lookup"><span data-stu-id="181c2-116">IEquatable\<T\>.Equals(T)</span></span>](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a><span data-ttu-id="181c2-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="181c2-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="181c2-118">參考</span><span class="sxs-lookup"><span data-stu-id="181c2-118">Reference</span></span>

[<span data-ttu-id="181c2-119">JET_COLUMNID 結構</span><span class="sxs-lookup"><span data-stu-id="181c2-119">JET_COLUMNID structure</span></span>](./jet-columnid-structure.md)

[<span data-ttu-id="181c2-120">JET_COLUMNID 成員</span><span class="sxs-lookup"><span data-stu-id="181c2-120">JET_COLUMNID members</span></span>](./jet-columnid-members.md)

[<span data-ttu-id="181c2-121">等於多載</span><span class="sxs-lookup"><span data-stu-id="181c2-121">Equals overload</span></span>](./jet-columnid.equals-method.md)

[<span data-ttu-id="181c2-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="181c2-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
