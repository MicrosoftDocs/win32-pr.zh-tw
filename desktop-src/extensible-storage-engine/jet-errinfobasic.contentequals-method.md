---
description: 深入瞭解： JET_ERRINFOBASIC。ContentEquals 方法
title: JET_ERRINFOBASIC。Windows8) 的 ContentEquals 方法 (
TOCTitle: 'ContentEquals method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC.ContentEquals(Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_errinfobasic.contentequals(v=EXCHG.10)
ms:contentKeyID: 55104306
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC.ContentEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC.ContentEquals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e1f527fae20d24e97114afa1f07b427d799c26c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971838"
---
# <a name="jet_errinfobasiccontentequals-method"></a><span data-ttu-id="a7a83-103">JET_ERRINFOBASIC。ContentEquals 方法</span><span class="sxs-lookup"><span data-stu-id="a7a83-103">JET_ERRINFOBASIC.ContentEquals method</span></span>

<span data-ttu-id="a7a83-104">傳回值，這個值表示這個實例是否等於另一個實例。</span><span class="sxs-lookup"><span data-stu-id="a7a83-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="a7a83-105">**命名空間：**  [Microsoft Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a7a83-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="a7a83-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="a7a83-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a7a83-107">語法</span><span class="sxs-lookup"><span data-stu-id="a7a83-107">Syntax</span></span>

``` vb
'Declaration
Public Function ContentEquals ( _
    other As JET_ERRINFOBASIC _
) As Boolean
'Usage
Dim instance As JET_ERRINFOBASIC
Dim other As JET_ERRINFOBASIC
Dim returnValue As Boolean

returnValue = instance.ContentEquals(other)
```

``` csharp
public bool ContentEquals(
    JET_ERRINFOBASIC other
)
```

#### <a name="parameters"></a><span data-ttu-id="a7a83-108">參數</span><span class="sxs-lookup"><span data-stu-id="a7a83-108">Parameters</span></span>

  - <span data-ttu-id="a7a83-109">其他</span><span class="sxs-lookup"><span data-stu-id="a7a83-109">other</span></span>  
    <span data-ttu-id="a7a83-110">類型： [Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC](./jet-errinfobasic-class.md)</span><span class="sxs-lookup"><span data-stu-id="a7a83-110">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC](./jet-errinfobasic-class.md)</span></span>  
    
    <span data-ttu-id="a7a83-111">要與這個實例比較的實例。</span><span class="sxs-lookup"><span data-stu-id="a7a83-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="a7a83-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="a7a83-112">Return value</span></span>

<span data-ttu-id="a7a83-113">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="a7a83-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="a7a83-114">如果兩個實例相等，則為 True。</span><span class="sxs-lookup"><span data-stu-id="a7a83-114">True if the two instances are equal.</span></span>  

#### <a name="implements"></a><span data-ttu-id="a7a83-115">實作</span><span class="sxs-lookup"><span data-stu-id="a7a83-115">Implements</span></span>

[<span data-ttu-id="a7a83-116">IContentEquatable \<T\> 。ContentEquals (T) </span><span class="sxs-lookup"><span data-stu-id="a7a83-116">IContentEquatable\<T\>.ContentEquals(T)</span></span>](./icontentequatable-t-.contentequals-method.md)  

## <a name="see-also"></a><span data-ttu-id="a7a83-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a7a83-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a7a83-118">參考</span><span class="sxs-lookup"><span data-stu-id="a7a83-118">Reference</span></span>

[<span data-ttu-id="a7a83-119">JET_ERRINFOBASIC 類別</span><span class="sxs-lookup"><span data-stu-id="a7a83-119">JET_ERRINFOBASIC class</span></span>](./jet-errinfobasic-class.md)

[<span data-ttu-id="a7a83-120">JET_ERRINFOBASIC 成員</span><span class="sxs-lookup"><span data-stu-id="a7a83-120">JET_ERRINFOBASIC members</span></span>](./jet-errinfobasic-members.md)

[<span data-ttu-id="a7a83-121">Windows8 命名空間。</span><span class="sxs-lookup"><span data-stu-id="a7a83-121">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
