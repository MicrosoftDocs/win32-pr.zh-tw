---
description: 深入瞭解： JET_INDEXCREATE。ContentEquals 方法
title: JET_INDEXCREATE。ContentEquals 方法
TOCTitle: 'ContentEquals method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.ContentEquals(Microsoft.Isam.Esent.Interop.JET_INDEXCREATE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate.contentequals(v=EXCHG.10)
ms:contentKeyID: 55103543
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.ContentEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.ContentEquals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1e5c61d37cde77137d465aac6791e81a7e5d594e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975206"
---
# <a name="jet_indexcreatecontentequals-method"></a><span data-ttu-id="b784e-103">JET_INDEXCREATE。ContentEquals 方法</span><span class="sxs-lookup"><span data-stu-id="b784e-103">JET_INDEXCREATE.ContentEquals method</span></span>

<span data-ttu-id="b784e-104">傳回值，這個值表示這個實例是否等於另一個實例。</span><span class="sxs-lookup"><span data-stu-id="b784e-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="b784e-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b784e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b784e-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="b784e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b784e-107">語法</span><span class="sxs-lookup"><span data-stu-id="b784e-107">Syntax</span></span>

``` vb
'Declaration
Public Function ContentEquals ( _
    other As JET_INDEXCREATE _
) As Boolean
'Usage
Dim instance As JET_INDEXCREATE
Dim other As JET_INDEXCREATE
Dim returnValue As Boolean

returnValue = instance.ContentEquals(other)
```

``` csharp
public bool ContentEquals(
    JET_INDEXCREATE other
)
```

#### <a name="parameters"></a><span data-ttu-id="b784e-108">參數</span><span class="sxs-lookup"><span data-stu-id="b784e-108">Parameters</span></span>

  - <span data-ttu-id="b784e-109">其他</span><span class="sxs-lookup"><span data-stu-id="b784e-109">other</span></span>  
    <span data-ttu-id="b784e-110">類型： [Microsoft.Isam.Esent.Interop.JET_INDEXCREATE](./jet-indexcreate-class.md)</span><span class="sxs-lookup"><span data-stu-id="b784e-110">Type: [Microsoft.Isam.Esent.Interop.JET_INDEXCREATE](./jet-indexcreate-class.md)</span></span>  
    
    <span data-ttu-id="b784e-111">要與這個實例比較的實例。</span><span class="sxs-lookup"><span data-stu-id="b784e-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="b784e-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="b784e-112">Return value</span></span>

<span data-ttu-id="b784e-113">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="b784e-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="b784e-114">如果兩個實例相等，則為 True。</span><span class="sxs-lookup"><span data-stu-id="b784e-114">True if the two instances are equal.</span></span>  

#### <a name="implements"></a><span data-ttu-id="b784e-115">實作</span><span class="sxs-lookup"><span data-stu-id="b784e-115">Implements</span></span>

[<span data-ttu-id="b784e-116">IContentEquatable \<T\> 。ContentEquals (T) </span><span class="sxs-lookup"><span data-stu-id="b784e-116">IContentEquatable\<T\>.ContentEquals(T)</span></span>](./icontentequatable-t-.contentequals-method.md)  

## <a name="see-also"></a><span data-ttu-id="b784e-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b784e-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b784e-118">參考</span><span class="sxs-lookup"><span data-stu-id="b784e-118">Reference</span></span>

[<span data-ttu-id="b784e-119">JET_INDEXCREATE 類別</span><span class="sxs-lookup"><span data-stu-id="b784e-119">JET_INDEXCREATE class</span></span>](./jet-indexcreate-class.md)

[<span data-ttu-id="b784e-120">JET_INDEXCREATE 成員</span><span class="sxs-lookup"><span data-stu-id="b784e-120">JET_INDEXCREATE members</span></span>](./jet-indexcreate-members.md)

[<span data-ttu-id="b784e-121">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="b784e-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
