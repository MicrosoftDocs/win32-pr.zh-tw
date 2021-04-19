---
description: 深入瞭解： JET_INDEXID 結構
title: JET_INDEXID 結構
TOCTitle: JET_INDEXID structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_INDEXID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexid(v=EXCHG.10)
ms:contentKeyID: 39510071
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXID
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXID
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 13ff0984926fe821d666d18c1907c9bd1bf93b16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975918"
---
# <a name="jet_indexid-structure"></a><span data-ttu-id="1fbc3-103">JET_INDEXID 結構</span><span class="sxs-lookup"><span data-stu-id="1fbc3-103">JET_INDEXID structure</span></span>

<span data-ttu-id="1fbc3-104">保存索引識別碼。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-104">Holds an index ID.</span></span> <span data-ttu-id="1fbc3-105">索引識別碼是用來加速使用 JetSetCurrentIndex 來選取目前索引的提示。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-105">An index ID is a hint that is used to accelerate the selection of the current index using JetSetCurrentIndex.</span></span> <span data-ttu-id="1fbc3-106">當資料表的索引數量非常龐大時，最有用。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-106">It is most useful when there is a very large number of indexes over a table.</span></span> <span data-ttu-id="1fbc3-107">您可以使用 JetGetIndexInfo 或 JetGetTableIndexInfo 來取出索引識別碼。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-107">The index ID can be retrieved using JetGetIndexInfo or JetGetTableIndexInfo.</span></span>

<span data-ttu-id="1fbc3-108">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1fbc3-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1fbc3-109">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1fbc3-110">語法</span><span class="sxs-lookup"><span data-stu-id="1fbc3-110">Syntax</span></span>

``` vb
'Declaration
Public Structure JET_INDEXID _
    Implements IEquatable(Of JET_INDEXID)
'Usage
Dim instance As JET_INDEXID
```

``` csharp
public struct JET_INDEXID : IEquatable<JET_INDEXID>
```

## <a name="remarks"></a><span data-ttu-id="1fbc3-111">備註</span><span class="sxs-lookup"><span data-stu-id="1fbc3-111">Remarks</span></span>

<span data-ttu-id="1fbc3-112">因為 c + + 版本定義為位元組陣列，所以需要 Pack 屬性。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-112">The Pack attribute is necessary because the C++ version is defined as a byte array.</span></span> <span data-ttu-id="1fbc3-113">如果 C \# 編譯器在 Uint cbStruct 和 IntPtr 之間插入一般的填補，則結構最後會太大。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-113">If the C\# compiler inserts the usual padding between the uint cbStruct and the IntPtr, then the structure ends up too large.</span></span>

## <a name="thread-safety"></a><span data-ttu-id="1fbc3-114">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="1fbc3-114">Thread safety</span></span>

<span data-ttu-id="1fbc3-115">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-115">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="1fbc3-116">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-116">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="1fbc3-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1fbc3-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1fbc3-118">參考</span><span class="sxs-lookup"><span data-stu-id="1fbc3-118">Reference</span></span>

[<span data-ttu-id="1fbc3-119">JET_INDEXID 成員</span><span class="sxs-lookup"><span data-stu-id="1fbc3-119">JET_INDEXID members</span></span>](./jet-indexid-members.md)

[<span data-ttu-id="1fbc3-120">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="1fbc3-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
