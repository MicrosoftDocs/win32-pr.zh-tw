---
description: 深入瞭解： JET_RSTMAP。ContentEquals 方法
title: JET_RSTMAP。ContentEquals 方法
TOCTitle: 'ContentEquals method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_RSTMAP.ContentEquals(Microsoft.Isam.Esent.Interop.JET_RSTMAP)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_rstmap.contentequals(v=EXCHG.10)
ms:contentKeyID: 55107668
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RSTMAP.ContentEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RSTMAP.ContentEquals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4c03c9dcb0cb9b0362a7c9efa348ba4c479f16cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112545"
---
# <a name="jet_rstmapcontentequals-method"></a><span data-ttu-id="eeed0-103">JET_RSTMAP。ContentEquals 方法</span><span class="sxs-lookup"><span data-stu-id="eeed0-103">JET_RSTMAP.ContentEquals method</span></span>

<span data-ttu-id="eeed0-104">傳回值，這個值表示這個實例是否等於另一個實例。</span><span class="sxs-lookup"><span data-stu-id="eeed0-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="eeed0-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="eeed0-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="eeed0-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="eeed0-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="eeed0-107">語法</span><span class="sxs-lookup"><span data-stu-id="eeed0-107">Syntax</span></span>

``` vb
'Declaration
Public Function ContentEquals ( _
    other As JET_RSTMAP _
) As Boolean
'Usage
Dim instance As JET_RSTMAP
Dim other As JET_RSTMAP
Dim returnValue As Boolean

returnValue = instance.ContentEquals(other)
```

``` csharp
public bool ContentEquals(
    JET_RSTMAP other
)
```

#### <a name="parameters"></a><span data-ttu-id="eeed0-108">參數</span><span class="sxs-lookup"><span data-stu-id="eeed0-108">Parameters</span></span>

  - <span data-ttu-id="eeed0-109">其他</span><span class="sxs-lookup"><span data-stu-id="eeed0-109">other</span></span>  
    <span data-ttu-id="eeed0-110">類型： [Microsoft.Isam.Esent.Interop.JET_RSTMAP](./jet-rstmap-class.md)</span><span class="sxs-lookup"><span data-stu-id="eeed0-110">Type: [Microsoft.Isam.Esent.Interop.JET_RSTMAP](./jet-rstmap-class.md)</span></span>  
    
    <span data-ttu-id="eeed0-111">要與這個實例比較的實例。</span><span class="sxs-lookup"><span data-stu-id="eeed0-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="eeed0-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="eeed0-112">Return value</span></span>

<span data-ttu-id="eeed0-113">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="eeed0-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="eeed0-114">如果兩個實例相等，則為 True。</span><span class="sxs-lookup"><span data-stu-id="eeed0-114">True if the two instances are equal.</span></span>  

#### <a name="implements"></a><span data-ttu-id="eeed0-115">實作</span><span class="sxs-lookup"><span data-stu-id="eeed0-115">Implements</span></span>

[<span data-ttu-id="eeed0-116">IContentEquatable \<T\> 。ContentEquals (T) </span><span class="sxs-lookup"><span data-stu-id="eeed0-116">IContentEquatable\<T\>.ContentEquals(T)</span></span>](./icontentequatable-t-.contentequals-method.md)  

## <a name="see-also"></a><span data-ttu-id="eeed0-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eeed0-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="eeed0-118">參考</span><span class="sxs-lookup"><span data-stu-id="eeed0-118">Reference</span></span>

[<span data-ttu-id="eeed0-119">JET_RSTMAP 類別</span><span class="sxs-lookup"><span data-stu-id="eeed0-119">JET_RSTMAP class</span></span>](./jet-rstmap-class.md)

[<span data-ttu-id="eeed0-120">JET_RSTMAP 成員</span><span class="sxs-lookup"><span data-stu-id="eeed0-120">JET_RSTMAP members</span></span>](./jet-rstmap-members.md)

[<span data-ttu-id="eeed0-121">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="eeed0-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
