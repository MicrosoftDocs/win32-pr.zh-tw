---
description: '深入瞭解： JET_DBID。Equals 方法 (JET_DBID) '
title: 'JET_DBID。Equals 方法 (JET_DBID) '
TOCTitle: Equals method (JET_DBID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_DBID.Equals(Microsoft.Isam.Esent.Interop.JET_DBID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbid.equals(v=EXCHG.10)
ms:contentKeyID: 39514199
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBID.Equals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9023108f1a1b3ffe565519607ab1498af363d40d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985044"
---
# <a name="jet_dbidequals-method-jet_dbid"></a><span data-ttu-id="3a900-103">JET_DBID。Equals 方法 (JET_DBID) </span><span class="sxs-lookup"><span data-stu-id="3a900-103">JET_DBID.Equals method (JET_DBID)</span></span>

<span data-ttu-id="3a900-104">傳回值，這個值表示這個實例是否等於另一個實例。</span><span class="sxs-lookup"><span data-stu-id="3a900-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="3a900-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3a900-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3a900-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="3a900-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3a900-107">語法</span><span class="sxs-lookup"><span data-stu-id="3a900-107">Syntax</span></span>

``` vb
'Declaration
Public Function Equals ( _
    other As JET_DBID _
) As Boolean
'Usage
Dim instance As JET_DBID
Dim other As JET_DBID
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_DBID other
)
```

#### <a name="parameters"></a><span data-ttu-id="3a900-108">參數</span><span class="sxs-lookup"><span data-stu-id="3a900-108">Parameters</span></span>

  - <span data-ttu-id="3a900-109">其他</span><span class="sxs-lookup"><span data-stu-id="3a900-109">other</span></span>  
    <span data-ttu-id="3a900-110">類型： [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3a900-110">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="3a900-111">要與這個實例比較的實例。</span><span class="sxs-lookup"><span data-stu-id="3a900-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="3a900-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="3a900-112">Return value</span></span>

<span data-ttu-id="3a900-113">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="3a900-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="3a900-114">如果兩個實例相等，則為 True。</span><span class="sxs-lookup"><span data-stu-id="3a900-114">True if the two instances are equal.</span></span>  

#### <a name="implements"></a><span data-ttu-id="3a900-115">實作</span><span class="sxs-lookup"><span data-stu-id="3a900-115">Implements</span></span>

[<span data-ttu-id="3a900-116">IEquatable \<T\> 。等於 (T) </span><span class="sxs-lookup"><span data-stu-id="3a900-116">IEquatable\<T\>.Equals(T)</span></span>](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a><span data-ttu-id="3a900-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3a900-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3a900-118">參考</span><span class="sxs-lookup"><span data-stu-id="3a900-118">Reference</span></span>

[<span data-ttu-id="3a900-119">JET_DBID 結構</span><span class="sxs-lookup"><span data-stu-id="3a900-119">JET_DBID structure</span></span>](./jet-dbid-structure.md)

[<span data-ttu-id="3a900-120">JET_DBID 成員</span><span class="sxs-lookup"><span data-stu-id="3a900-120">JET_DBID members</span></span>](./jet-dbid-members.md)

[<span data-ttu-id="3a900-121">等於多載</span><span class="sxs-lookup"><span data-stu-id="3a900-121">Equals overload</span></span>](./jet-dbid.equals-method.md)

[<span data-ttu-id="3a900-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="3a900-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
