---
description: 深入瞭解： IContentEquatable <T> 。ContentEquals 方法
title: IContentEquatable (T) 。ContentEquals 方法
TOCTitle: 'ContentEquals method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.IContentEquatable`1.ContentEquals(`0)
ms:mtpsurl: https://msdn.microsoft.com/library/Hh538970(v=EXCHG.10)
ms:contentKeyID: 39509953
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.IContentEquatable`1.ContentEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.IContentEquatable`1.ContentEquals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c3b06307f7c4ebc44242e02ee5ae99a182f9ab3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993022"
---
# <a name="icontentequatabletcontentequals-method"></a><span data-ttu-id="db3f9-103">IContentEquatable \<T\> 。ContentEquals 方法</span><span class="sxs-lookup"><span data-stu-id="db3f9-103">IContentEquatable\<T\>.ContentEquals method</span></span>

<span data-ttu-id="db3f9-104">傳回值，這個值表示這個實例是否等於另一個實例。</span><span class="sxs-lookup"><span data-stu-id="db3f9-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="db3f9-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="db3f9-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="db3f9-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="db3f9-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="db3f9-107">語法</span><span class="sxs-lookup"><span data-stu-id="db3f9-107">Syntax</span></span>

``` vb
'Declaration
Function ContentEquals ( _
    other As T _
) As Boolean
'Usage
Dim instance As IContentEquatable
Dim other As T
Dim returnValue As Boolean

returnValue = instance.ContentEquals(other)
```

``` csharp
bool ContentEquals(
    T other
)
```

#### <a name="parameters"></a><span data-ttu-id="db3f9-108">參數</span><span class="sxs-lookup"><span data-stu-id="db3f9-108">Parameters</span></span>

  - <span data-ttu-id="db3f9-109">其他</span><span class="sxs-lookup"><span data-stu-id="db3f9-109">other</span></span>  
    <span data-ttu-id="db3f9-110">類型： [T](./icontentequatable-t-interface.md)</span><span class="sxs-lookup"><span data-stu-id="db3f9-110">Type: [T](./icontentequatable-t-interface.md)</span></span>  
    
    <span data-ttu-id="db3f9-111">要與這個實例比較的實例。</span><span class="sxs-lookup"><span data-stu-id="db3f9-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="db3f9-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="db3f9-112">Return value</span></span>

<span data-ttu-id="db3f9-113">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="db3f9-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="db3f9-114">如果兩個實例相等，則為 True。</span><span class="sxs-lookup"><span data-stu-id="db3f9-114">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="db3f9-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="db3f9-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="db3f9-116">參考</span><span class="sxs-lookup"><span data-stu-id="db3f9-116">Reference</span></span>

[<span data-ttu-id="db3f9-117">IContentEquatable \<T\> 介面</span><span class="sxs-lookup"><span data-stu-id="db3f9-117">IContentEquatable\<T\> interface</span></span>](./icontentequatable-t-interface.md)

[<span data-ttu-id="db3f9-118">IContentEquatable \<T\> 成員</span><span class="sxs-lookup"><span data-stu-id="db3f9-118">IContentEquatable\<T\> members</span></span>](./icontentequatable-t-members.md)

[<span data-ttu-id="db3f9-119">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="db3f9-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
