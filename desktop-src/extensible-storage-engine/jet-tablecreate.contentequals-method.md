---
description: 深入瞭解： JET_TABLECREATE。ContentEquals 方法
title: JET_TABLECREATE。ContentEquals 方法
TOCTitle: 'ContentEquals method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_TABLECREATE.ContentEquals(Microsoft.Isam.Esent.Interop.JET_TABLECREATE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tablecreate.contentequals(v=EXCHG.10)
ms:contentKeyID: 55103993
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.ContentEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.ContentEquals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c06cd8769dee6e56006b0225a75572b642e35d93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997572"
---
# <a name="jet_tablecreatecontentequals-method"></a><span data-ttu-id="ae845-103">JET_TABLECREATE。ContentEquals 方法</span><span class="sxs-lookup"><span data-stu-id="ae845-103">JET_TABLECREATE.ContentEquals method</span></span>

<span data-ttu-id="ae845-104">傳回值，這個值表示這個實例是否等於另一個實例。</span><span class="sxs-lookup"><span data-stu-id="ae845-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="ae845-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ae845-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ae845-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="ae845-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ae845-107">語法</span><span class="sxs-lookup"><span data-stu-id="ae845-107">Syntax</span></span>

``` vb
'Declaration
Public Function ContentEquals ( _
    other As JET_TABLECREATE _
) As Boolean
'Usage
Dim instance As JET_TABLECREATE
Dim other As JET_TABLECREATE
Dim returnValue As Boolean

returnValue = instance.ContentEquals(other)
```

``` csharp
public bool ContentEquals(
    JET_TABLECREATE other
)
```

#### <a name="parameters"></a><span data-ttu-id="ae845-108">參數</span><span class="sxs-lookup"><span data-stu-id="ae845-108">Parameters</span></span>

  - <span data-ttu-id="ae845-109">其他</span><span class="sxs-lookup"><span data-stu-id="ae845-109">other</span></span>  
    <span data-ttu-id="ae845-110">類型： [Microsoft.Isam.Esent.Interop.JET_TABLECREATE](./jet-tablecreate-class.md)</span><span class="sxs-lookup"><span data-stu-id="ae845-110">Type: [Microsoft.Isam.Esent.Interop.JET_TABLECREATE](./jet-tablecreate-class.md)</span></span>  
    
    <span data-ttu-id="ae845-111">要與這個實例比較的實例。</span><span class="sxs-lookup"><span data-stu-id="ae845-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="ae845-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="ae845-112">Return value</span></span>

<span data-ttu-id="ae845-113">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="ae845-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="ae845-114">如果兩個實例相等，則為 True。</span><span class="sxs-lookup"><span data-stu-id="ae845-114">True if the two instances are equal.</span></span>  

#### <a name="implements"></a><span data-ttu-id="ae845-115">實作</span><span class="sxs-lookup"><span data-stu-id="ae845-115">Implements</span></span>

[<span data-ttu-id="ae845-116">IContentEquatable \<T\> 。ContentEquals (T) </span><span class="sxs-lookup"><span data-stu-id="ae845-116">IContentEquatable\<T\>.ContentEquals(T)</span></span>](./icontentequatable-t-.contentequals-method.md)  

## <a name="see-also"></a><span data-ttu-id="ae845-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ae845-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ae845-118">參考</span><span class="sxs-lookup"><span data-stu-id="ae845-118">Reference</span></span>

[<span data-ttu-id="ae845-119">JET_TABLECREATE 類別</span><span class="sxs-lookup"><span data-stu-id="ae845-119">JET_TABLECREATE class</span></span>](./jet-tablecreate-class.md)

[<span data-ttu-id="ae845-120">JET_TABLECREATE 成員</span><span class="sxs-lookup"><span data-stu-id="ae845-120">JET_TABLECREATE members</span></span>](./jet-tablecreate-members.md)

[<span data-ttu-id="ae845-121">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="ae845-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
