---
description: 深入瞭解： JET_COMMIT_ID CompareTo 方法
title: " (CompareTo 方法) 的 JET_COMMIT_ID. Windows8"
TOCTitle: 'CompareTo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.CompareTo(Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_commit_id.compareto(v=EXCHG.10)
ms:contentKeyID: 55104397
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.CompareTo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.CompareTo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bb52be18054b0d9da723ca15073868a6baff6b12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975430"
---
# <a name="jet_commit_idcompareto-method"></a><span data-ttu-id="d0938-103">JET_COMMIT_ID CompareTo 方法</span><span class="sxs-lookup"><span data-stu-id="d0938-103">JET_COMMIT_ID.CompareTo method</span></span>

<span data-ttu-id="d0938-104">傳回值，這個值會比較這個實例與另一個實例。</span><span class="sxs-lookup"><span data-stu-id="d0938-104">Returns a value comparing this instance with another.</span></span>

<span data-ttu-id="d0938-105">**命名空間：**  [Microsoft Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d0938-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="d0938-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="d0938-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d0938-107">語法</span><span class="sxs-lookup"><span data-stu-id="d0938-107">Syntax</span></span>

``` vb
'Declaration
Public Function CompareTo ( _
    other As JET_COMMIT_ID _
) As Integer
'Usage
Dim instance As JET_COMMIT_ID
Dim other As JET_COMMIT_ID
Dim returnValue As Integer

returnValue = instance.CompareTo(other)
```

``` csharp
public int CompareTo(
    JET_COMMIT_ID other
)
```

#### <a name="parameters"></a><span data-ttu-id="d0938-108">參數</span><span class="sxs-lookup"><span data-stu-id="d0938-108">Parameters</span></span>

  - <span data-ttu-id="d0938-109">其他</span><span class="sxs-lookup"><span data-stu-id="d0938-109">other</span></span>  
    <span data-ttu-id="d0938-110">類型： [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span><span class="sxs-lookup"><span data-stu-id="d0938-110">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span></span>  
    
    <span data-ttu-id="d0938-111">要與這個實例比較的實例。</span><span class="sxs-lookup"><span data-stu-id="d0938-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="d0938-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="d0938-112">Return value</span></span>

<span data-ttu-id="d0938-113">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="d0938-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
<span data-ttu-id="d0938-114">代表實例之相對位置的帶正負號值。</span><span class="sxs-lookup"><span data-stu-id="d0938-114">A signed value representing the relative positions of the instances.</span></span>  

#### <a name="implements"></a><span data-ttu-id="d0938-115">實作</span><span class="sxs-lookup"><span data-stu-id="d0938-115">Implements</span></span>

[<span data-ttu-id="d0938-116">IComparable \<T\> 。CompareTo (T) </span><span class="sxs-lookup"><span data-stu-id="d0938-116">IComparable\<T\>.CompareTo(T)</span></span>](/dotnet/api/system.icomparable-1.compareto#System_IComparable_1_CompareTo__0_)  

## <a name="see-also"></a><span data-ttu-id="d0938-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d0938-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d0938-118">參考</span><span class="sxs-lookup"><span data-stu-id="d0938-118">Reference</span></span>

[<span data-ttu-id="d0938-119">JET_COMMIT_ID 類別</span><span class="sxs-lookup"><span data-stu-id="d0938-119">JET_COMMIT_ID class</span></span>](./jet-commit-id-class.md)

[<span data-ttu-id="d0938-120">JET_COMMIT_ID 成員</span><span class="sxs-lookup"><span data-stu-id="d0938-120">JET_COMMIT_ID members</span></span>](./jet-commit-id-members.md)

[<span data-ttu-id="d0938-121">Windows8 命名空間。</span><span class="sxs-lookup"><span data-stu-id="d0938-121">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
