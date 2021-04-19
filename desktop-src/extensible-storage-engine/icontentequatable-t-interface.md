---
description: 深入瞭解： IContentEquatable <T> 介面
title: IContentEquatable (T) 介面
TOCTitle: IContentEquatable(T) interface
ms:assetid: T:Microsoft.Isam.Esent.Interop.IContentEquatable`1
ms:mtpsurl: https://msdn.microsoft.com/library/Hh578046(v=EXCHG.10)
ms:contentKeyID: 39511318
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.IContentEquatable`1
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.IContentEquatable`1
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 02e237714f020f5bafa3ce8b7465f1c8e2615c01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974981"
---
# <a name="icontentequatablet-interface"></a><span data-ttu-id="01432-103">IContentEquatable \<T\> 介面</span><span class="sxs-lookup"><span data-stu-id="01432-103">IContentEquatable\<T\> interface</span></span>

<span data-ttu-id="01432-104">物件的介面，其內容可以彼此比較。</span><span class="sxs-lookup"><span data-stu-id="01432-104">Interface for objects that can have their contents compared against each other.</span></span> <span data-ttu-id="01432-105">這應該用於覆寫 Equals () 的可變參考物件的相等比較，而 GetHashCode () 並不是個好主意。</span><span class="sxs-lookup"><span data-stu-id="01432-105">This should be used for equality comparisons on mutable reference objects where overriding Equals() and GetHashCode() isn't a good idea.</span></span>

<span data-ttu-id="01432-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="01432-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="01432-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="01432-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="01432-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="01432-108">Syntax</span></span>

``` vb
'Declaration
Public Interface IContentEquatable(Of T)
'Usage
Dim instance As IContentEquatable(Of T)
```

``` csharp
public interface IContentEquatable<T>
```

#### <a name="type-parameters"></a><span data-ttu-id="01432-109">型別參數</span><span class="sxs-lookup"><span data-stu-id="01432-109">Type parameters</span></span>

  - <span data-ttu-id="01432-110">T</span><span class="sxs-lookup"><span data-stu-id="01432-110">T</span></span>  
    <span data-ttu-id="01432-111">要 comapre 的物件類型。</span><span class="sxs-lookup"><span data-stu-id="01432-111">The type of objects to comapre.</span></span>

## <a name="see-also"></a><span data-ttu-id="01432-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="01432-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="01432-113">參考</span><span class="sxs-lookup"><span data-stu-id="01432-113">Reference</span></span>

[<span data-ttu-id="01432-114">IContentEquatable \<T\> 成員</span><span class="sxs-lookup"><span data-stu-id="01432-114">IContentEquatable\<T\> members</span></span>](./icontentequatable-t-members.md)

[<span data-ttu-id="01432-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="01432-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
