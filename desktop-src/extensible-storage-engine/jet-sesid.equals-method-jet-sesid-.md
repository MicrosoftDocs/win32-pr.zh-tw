---
description: '深入瞭解： JET_SESID。Equals 方法 (JET_SESID) '
title: 'JET_SESID。Equals 方法 (JET_SESID) '
TOCTitle: Equals method (JET_SESID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_SESID.Equals(Microsoft.Isam.Esent.Interop.JET_SESID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_sesid.equals(v=EXCHG.10)
ms:contentKeyID: 39511762
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_SESID.Equals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3f840230047fbb1b0347e399bc60b4b905d868b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973817"
---
# <a name="jet_sesidequals-method-jet_sesid"></a><span data-ttu-id="40510-103">JET_SESID。Equals 方法 (JET_SESID) </span><span class="sxs-lookup"><span data-stu-id="40510-103">JET_SESID.Equals method (JET_SESID)</span></span>

<span data-ttu-id="40510-104">傳回值，這個值表示這個實例是否等於另一個實例。</span><span class="sxs-lookup"><span data-stu-id="40510-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="40510-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="40510-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="40510-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="40510-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="40510-107">語法</span><span class="sxs-lookup"><span data-stu-id="40510-107">Syntax</span></span>

``` vb
'Declaration
Public Function Equals ( _
    other As JET_SESID _
) As Boolean
'Usage
Dim instance As JET_SESID
Dim other As JET_SESID
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_SESID other
)
```

#### <a name="parameters"></a><span data-ttu-id="40510-108">參數</span><span class="sxs-lookup"><span data-stu-id="40510-108">Parameters</span></span>

  - <span data-ttu-id="40510-109">其他</span><span class="sxs-lookup"><span data-stu-id="40510-109">other</span></span>  
    <span data-ttu-id="40510-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="40510-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="40510-111">要與這個實例比較的實例。</span><span class="sxs-lookup"><span data-stu-id="40510-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="40510-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="40510-112">Return value</span></span>

<span data-ttu-id="40510-113">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="40510-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="40510-114">如果兩個實例相等，則為 True。</span><span class="sxs-lookup"><span data-stu-id="40510-114">True if the two instances are equal.</span></span>  

#### <a name="implements"></a><span data-ttu-id="40510-115">實作</span><span class="sxs-lookup"><span data-stu-id="40510-115">Implements</span></span>

[<span data-ttu-id="40510-116">IEquatable \<T\> 。等於 (T) </span><span class="sxs-lookup"><span data-stu-id="40510-116">IEquatable\<T\>.Equals(T)</span></span>](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a><span data-ttu-id="40510-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="40510-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="40510-118">參考</span><span class="sxs-lookup"><span data-stu-id="40510-118">Reference</span></span>

[<span data-ttu-id="40510-119">JET_SESID 結構</span><span class="sxs-lookup"><span data-stu-id="40510-119">JET_SESID structure</span></span>](./jet-sesid-structure.md)

[<span data-ttu-id="40510-120">JET_SESID 成員</span><span class="sxs-lookup"><span data-stu-id="40510-120">JET_SESID members</span></span>](./jet-sesid-members.md)

[<span data-ttu-id="40510-121">等於多載</span><span class="sxs-lookup"><span data-stu-id="40510-121">Equals overload</span></span>](./jet-sesid.equals-method.md)

[<span data-ttu-id="40510-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="40510-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
