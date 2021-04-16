---
description: '深入瞭解： JET_SIGNATURE。Equals 方法 (JET_SIGNATURE) '
title: 'JET_SIGNATURE。Equals 方法 (JET_SIGNATURE) '
TOCTitle: Equals method (JET_SIGNATURE)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_SIGNATURE.Equals(Microsoft.Isam.Esent.Interop.JET_SIGNATURE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_signature.equals(v=EXCHG.10)
ms:contentKeyID: 39511830
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE.Equals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5f099b74af84e1a75289313c5bb9d4de646b51a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511940"
---
# <a name="jet_signatureequals-method-jet_signature"></a><span data-ttu-id="00c5a-103">JET_SIGNATURE。Equals 方法 (JET_SIGNATURE) </span><span class="sxs-lookup"><span data-stu-id="00c5a-103">JET_SIGNATURE.Equals method (JET_SIGNATURE)</span></span>

<span data-ttu-id="00c5a-104">傳回值，這個值表示這個實例是否等於另一個實例。</span><span class="sxs-lookup"><span data-stu-id="00c5a-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="00c5a-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="00c5a-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="00c5a-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="00c5a-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="00c5a-107">語法</span><span class="sxs-lookup"><span data-stu-id="00c5a-107">Syntax</span></span>

``` vb
'Declaration
Public Function Equals ( _
    other As JET_SIGNATURE _
) As Boolean
'Usage
Dim instance As JET_SIGNATURE
Dim other As JET_SIGNATURE
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_SIGNATURE other
)
```

#### <a name="parameters"></a><span data-ttu-id="00c5a-108">參數</span><span class="sxs-lookup"><span data-stu-id="00c5a-108">Parameters</span></span>

  - <span data-ttu-id="00c5a-109">其他</span><span class="sxs-lookup"><span data-stu-id="00c5a-109">other</span></span>  
    <span data-ttu-id="00c5a-110">類型： [Microsoft.Isam.Esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="00c5a-110">Type: [Microsoft.Isam.Esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span></span>  
    
    <span data-ttu-id="00c5a-111">要與這個實例比較的實例。</span><span class="sxs-lookup"><span data-stu-id="00c5a-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="00c5a-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="00c5a-112">Return value</span></span>

<span data-ttu-id="00c5a-113">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="00c5a-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="00c5a-114">如果兩個實例相等，則為 True。</span><span class="sxs-lookup"><span data-stu-id="00c5a-114">True if the two instances are equal.</span></span>  

#### <a name="implements"></a><span data-ttu-id="00c5a-115">實作</span><span class="sxs-lookup"><span data-stu-id="00c5a-115">Implements</span></span>

[<span data-ttu-id="00c5a-116">IEquatable \<T\> 。等於 (T) </span><span class="sxs-lookup"><span data-stu-id="00c5a-116">IEquatable\<T\>.Equals(T)</span></span>](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a><span data-ttu-id="00c5a-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="00c5a-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="00c5a-118">參考</span><span class="sxs-lookup"><span data-stu-id="00c5a-118">Reference</span></span>

[<span data-ttu-id="00c5a-119">JET_SIGNATURE 結構</span><span class="sxs-lookup"><span data-stu-id="00c5a-119">JET_SIGNATURE structure</span></span>](./jet-signature-structure2.md)

[<span data-ttu-id="00c5a-120">JET_SIGNATURE 成員</span><span class="sxs-lookup"><span data-stu-id="00c5a-120">JET_SIGNATURE members</span></span>](./jet-signature-members.md)

[<span data-ttu-id="00c5a-121">等於多載</span><span class="sxs-lookup"><span data-stu-id="00c5a-121">Equals overload</span></span>](./jet-signature.equals-method.md)

[<span data-ttu-id="00c5a-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="00c5a-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
