---
description: 深入瞭解： JET_RETINFO。ContentEquals 方法
title: JET_RETINFO。ContentEquals 方法
TOCTitle: 'ContentEquals method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_RETINFO.ContentEquals(Microsoft.Isam.Esent.Interop.JET_RETINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retinfo.contentequals(v=EXCHG.10)
ms:contentKeyID: 55103869
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RETINFO.ContentEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RETINFO.ContentEquals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bac25d8184b1dd62e8c622cbdd79df42d4996314
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690923"
---
# <a name="jet_retinfocontentequals-method"></a><span data-ttu-id="382ef-103">JET_RETINFO。ContentEquals 方法</span><span class="sxs-lookup"><span data-stu-id="382ef-103">JET_RETINFO.ContentEquals method</span></span>

<span data-ttu-id="382ef-104">傳回值，這個值表示這個實例是否等於另一個實例。</span><span class="sxs-lookup"><span data-stu-id="382ef-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="382ef-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="382ef-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="382ef-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="382ef-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="382ef-107">語法</span><span class="sxs-lookup"><span data-stu-id="382ef-107">Syntax</span></span>

``` vb
'Declaration
Public Function ContentEquals ( _
    other As JET_RETINFO _
) As Boolean
'Usage
Dim instance As JET_RETINFO
Dim other As JET_RETINFO
Dim returnValue As Boolean

returnValue = instance.ContentEquals(other)
```

``` csharp
public bool ContentEquals(
    JET_RETINFO other
)
```

#### <a name="parameters"></a><span data-ttu-id="382ef-108">參數</span><span class="sxs-lookup"><span data-stu-id="382ef-108">Parameters</span></span>

  - <span data-ttu-id="382ef-109">其他</span><span class="sxs-lookup"><span data-stu-id="382ef-109">other</span></span>  
    <span data-ttu-id="382ef-110">類型： [Microsoft.Isam.Esent.Interop.JET_RETINFO](./jet-retinfo-class.md)</span><span class="sxs-lookup"><span data-stu-id="382ef-110">Type: [Microsoft.Isam.Esent.Interop.JET_RETINFO](./jet-retinfo-class.md)</span></span>  
    
    <span data-ttu-id="382ef-111">要與這個實例比較的實例。</span><span class="sxs-lookup"><span data-stu-id="382ef-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="382ef-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="382ef-112">Return value</span></span>

<span data-ttu-id="382ef-113">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="382ef-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="382ef-114">如果兩個實例相等，則為 True。</span><span class="sxs-lookup"><span data-stu-id="382ef-114">True if the two instances are equal.</span></span>  

#### <a name="implements"></a><span data-ttu-id="382ef-115">實作</span><span class="sxs-lookup"><span data-stu-id="382ef-115">Implements</span></span>

[<span data-ttu-id="382ef-116">IContentEquatable \<T\> 。ContentEquals (T) </span><span class="sxs-lookup"><span data-stu-id="382ef-116">IContentEquatable\<T\>.ContentEquals(T)</span></span>](./icontentequatable-t-.contentequals-method.md)  

## <a name="see-also"></a><span data-ttu-id="382ef-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="382ef-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="382ef-118">參考</span><span class="sxs-lookup"><span data-stu-id="382ef-118">Reference</span></span>

[<span data-ttu-id="382ef-119">JET_RETINFO 類別</span><span class="sxs-lookup"><span data-stu-id="382ef-119">JET_RETINFO class</span></span>](./jet-retinfo-class.md)

[<span data-ttu-id="382ef-120">JET_RETINFO 成員</span><span class="sxs-lookup"><span data-stu-id="382ef-120">JET_RETINFO members</span></span>](./jet-retinfo-members.md)

[<span data-ttu-id="382ef-121">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="382ef-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
