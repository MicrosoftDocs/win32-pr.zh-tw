---
description: 深入瞭解： JET_COLUMNID CompareTo 方法
title: JET_COLUMNID CompareTo 方法
TOCTitle: 'CompareTo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNID.CompareTo(Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnid.compareto(v=EXCHG.10)
ms:contentKeyID: 39509744
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.CompareTo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.CompareTo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7eea24875b0639f7f5b7968084a3fff2aa7cccec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114060"
---
# <a name="jet_columnidcompareto-method"></a><span data-ttu-id="bf395-103">JET_COLUMNID CompareTo 方法</span><span class="sxs-lookup"><span data-stu-id="bf395-103">JET_COLUMNID.CompareTo method</span></span>

<span data-ttu-id="bf395-104">比較這個 columnid 與另一個 columnid，並判斷這個實例是否在另一個實例之前、相同的或之後。</span><span class="sxs-lookup"><span data-stu-id="bf395-104">Compares this columnid to another columnid and determines whether this instance is before, the same as or after the other instance.</span></span>

<span data-ttu-id="bf395-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="bf395-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="bf395-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="bf395-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="bf395-107">語法</span><span class="sxs-lookup"><span data-stu-id="bf395-107">Syntax</span></span>

``` vb
'Declaration
Public Function CompareTo ( _
    other As JET_COLUMNID _
) As Integer
'Usage
Dim instance As JET_COLUMNID
Dim other As JET_COLUMNID
Dim returnValue As Integer

returnValue = instance.CompareTo(other)
```

``` csharp
public int CompareTo(
    JET_COLUMNID other
)
```

#### <a name="parameters"></a><span data-ttu-id="bf395-108">參數</span><span class="sxs-lookup"><span data-stu-id="bf395-108">Parameters</span></span>

  - <span data-ttu-id="bf395-109">其他</span><span class="sxs-lookup"><span data-stu-id="bf395-109">other</span></span>  
    <span data-ttu-id="bf395-110">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="bf395-110">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="bf395-111">要與目前實例比較的 columnid。</span><span class="sxs-lookup"><span data-stu-id="bf395-111">The columnid to compare to the current instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="bf395-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="bf395-112">Return value</span></span>

<span data-ttu-id="bf395-113">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="bf395-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
<span data-ttu-id="bf395-114">帶正負號的數位，指出這個實例和值參數的相對位置。</span><span class="sxs-lookup"><span data-stu-id="bf395-114">A signed number indicating the relative positions of this instance and the value parameter.</span></span>  

#### <a name="implements"></a><span data-ttu-id="bf395-115">實作</span><span class="sxs-lookup"><span data-stu-id="bf395-115">Implements</span></span>

[<span data-ttu-id="bf395-116">IComparable \<T\> 。CompareTo (T) </span><span class="sxs-lookup"><span data-stu-id="bf395-116">IComparable\<T\>.CompareTo(T)</span></span>](/dotnet/api/system.icomparable-1.compareto#System_IComparable_1_CompareTo__0_)  

## <a name="see-also"></a><span data-ttu-id="bf395-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bf395-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bf395-118">參考</span><span class="sxs-lookup"><span data-stu-id="bf395-118">Reference</span></span>

[<span data-ttu-id="bf395-119">JET_COLUMNID 結構</span><span class="sxs-lookup"><span data-stu-id="bf395-119">JET_COLUMNID structure</span></span>](./jet-columnid-structure.md)

[<span data-ttu-id="bf395-120">JET_COLUMNID 成員</span><span class="sxs-lookup"><span data-stu-id="bf395-120">JET_COLUMNID members</span></span>](./jet-columnid-members.md)

[<span data-ttu-id="bf395-121">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="bf395-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
