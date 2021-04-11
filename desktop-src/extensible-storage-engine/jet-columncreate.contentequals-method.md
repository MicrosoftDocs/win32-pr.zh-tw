---
description: 深入瞭解： JET_COLUMNCREATE。ContentEquals 方法
title: JET_COLUMNCREATE。ContentEquals 方法
TOCTitle: 'ContentEquals method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.ContentEquals(Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columncreate.contentequals(v=EXCHG.10)
ms:contentKeyID: 55103471
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.ContentEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.ContentEquals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: db39608007705284b4690893cb6e3196dca8dc35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115941"
---
# <a name="jet_columncreatecontentequals-method"></a><span data-ttu-id="4063d-103">JET_COLUMNCREATE。ContentEquals 方法</span><span class="sxs-lookup"><span data-stu-id="4063d-103">JET_COLUMNCREATE.ContentEquals method</span></span>

<span data-ttu-id="4063d-104">傳回值，這個值表示這個實例是否等於另一個實例。</span><span class="sxs-lookup"><span data-stu-id="4063d-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="4063d-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4063d-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4063d-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="4063d-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4063d-107">語法</span><span class="sxs-lookup"><span data-stu-id="4063d-107">Syntax</span></span>

``` vb
'Declaration
Public Function ContentEquals ( _
    other As JET_COLUMNCREATE _
) As Boolean
'Usage
Dim instance As JET_COLUMNCREATE
Dim other As JET_COLUMNCREATE
Dim returnValue As Boolean

returnValue = instance.ContentEquals(other)
```

``` csharp
public bool ContentEquals(
    JET_COLUMNCREATE other
)
```

#### <a name="parameters"></a><span data-ttu-id="4063d-108">參數</span><span class="sxs-lookup"><span data-stu-id="4063d-108">Parameters</span></span>

  - <span data-ttu-id="4063d-109">其他</span><span class="sxs-lookup"><span data-stu-id="4063d-109">other</span></span>  
    <span data-ttu-id="4063d-110">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE](./jet-columncreate-class.md)</span><span class="sxs-lookup"><span data-stu-id="4063d-110">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE](./jet-columncreate-class.md)</span></span>  
    
    <span data-ttu-id="4063d-111">要與這個實例比較的實例。</span><span class="sxs-lookup"><span data-stu-id="4063d-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="4063d-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="4063d-112">Return value</span></span>

<span data-ttu-id="4063d-113">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="4063d-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="4063d-114">如果兩個實例相等，則為 True。</span><span class="sxs-lookup"><span data-stu-id="4063d-114">True if the two instances are equal.</span></span>  

#### <a name="implements"></a><span data-ttu-id="4063d-115">實作</span><span class="sxs-lookup"><span data-stu-id="4063d-115">Implements</span></span>

[<span data-ttu-id="4063d-116">IContentEquatable \<T\> 。ContentEquals (T) </span><span class="sxs-lookup"><span data-stu-id="4063d-116">IContentEquatable\<T\>.ContentEquals(T)</span></span>](./icontentequatable-t-.contentequals-method.md)  

## <a name="see-also"></a><span data-ttu-id="4063d-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4063d-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4063d-118">參考</span><span class="sxs-lookup"><span data-stu-id="4063d-118">Reference</span></span>

[<span data-ttu-id="4063d-119">JET_COLUMNCREATE 類別</span><span class="sxs-lookup"><span data-stu-id="4063d-119">JET_COLUMNCREATE class</span></span>](./jet-columncreate-class.md)

[<span data-ttu-id="4063d-120">JET_COLUMNCREATE 成員</span><span class="sxs-lookup"><span data-stu-id="4063d-120">JET_COLUMNCREATE members</span></span>](./jet-columncreate-members.md)

[<span data-ttu-id="4063d-121">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="4063d-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
