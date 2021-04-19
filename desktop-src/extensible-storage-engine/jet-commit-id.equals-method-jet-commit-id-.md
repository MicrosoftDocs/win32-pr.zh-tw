---
description: '深入瞭解： JET_COMMIT_ID Equals 方法 (JET_COMMIT_ID) '
title: 'JET_COMMIT_ID. Equals 方法 (JET_COMMIT_ID)  (Windows8) '
TOCTitle: Equals method (JET_COMMIT_ID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.Equals(Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_commit_id.equals(v=EXCHG.10)
ms:contentKeyID: 55104294
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.Equals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c833b137b1e5df9f6d70e206b2f517977375e29b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998527"
---
# <a name="jet_commit_idequals-method-jet_commit_id"></a><span data-ttu-id="00627-103">JET_COMMIT_ID Equals 方法 (JET_COMMIT_ID) </span><span class="sxs-lookup"><span data-stu-id="00627-103">JET_COMMIT_ID.Equals method (JET_COMMIT_ID)</span></span>

<span data-ttu-id="00627-104">傳回值，這個值表示這個實例是否等於另一個實例。</span><span class="sxs-lookup"><span data-stu-id="00627-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="00627-105">**命名空間：**  [Microsoft Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="00627-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="00627-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="00627-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="00627-107">語法</span><span class="sxs-lookup"><span data-stu-id="00627-107">Syntax</span></span>

``` vb
'Declaration
Public Function Equals ( _
    other As JET_COMMIT_ID _
) As Boolean
'Usage
Dim instance As JET_COMMIT_ID
Dim other As JET_COMMIT_ID
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_COMMIT_ID other
)
```

#### <a name="parameters"></a><span data-ttu-id="00627-108">參數</span><span class="sxs-lookup"><span data-stu-id="00627-108">Parameters</span></span>

  - <span data-ttu-id="00627-109">其他</span><span class="sxs-lookup"><span data-stu-id="00627-109">other</span></span>  
    <span data-ttu-id="00627-110">類型： [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span><span class="sxs-lookup"><span data-stu-id="00627-110">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span></span>  
    
    <span data-ttu-id="00627-111">與這個執行個體相互比較的物件。</span><span class="sxs-lookup"><span data-stu-id="00627-111">An object to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="00627-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="00627-112">Return value</span></span>

<span data-ttu-id="00627-113">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="00627-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="00627-114">如果兩個實例相等，則為 true。</span><span class="sxs-lookup"><span data-stu-id="00627-114">true if the two instances are equal.</span></span>  

#### <a name="implements"></a><span data-ttu-id="00627-115">實作</span><span class="sxs-lookup"><span data-stu-id="00627-115">Implements</span></span>

[<span data-ttu-id="00627-116">IEquatable \<T\> 。等於 (T) </span><span class="sxs-lookup"><span data-stu-id="00627-116">IEquatable\<T\>.Equals(T)</span></span>](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a><span data-ttu-id="00627-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="00627-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="00627-118">參考</span><span class="sxs-lookup"><span data-stu-id="00627-118">Reference</span></span>

[<span data-ttu-id="00627-119">JET_COMMIT_ID 類別</span><span class="sxs-lookup"><span data-stu-id="00627-119">JET_COMMIT_ID class</span></span>](./jet-commit-id-class.md)

[<span data-ttu-id="00627-120">JET_COMMIT_ID 成員</span><span class="sxs-lookup"><span data-stu-id="00627-120">JET_COMMIT_ID members</span></span>](./jet-commit-id-members.md)

[<span data-ttu-id="00627-121">等於多載</span><span class="sxs-lookup"><span data-stu-id="00627-121">Equals overload</span></span>](./jet-commit-id.equals-method.md)

[<span data-ttu-id="00627-122">Windows8 命名空間。</span><span class="sxs-lookup"><span data-stu-id="00627-122">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
