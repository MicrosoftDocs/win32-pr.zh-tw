---
description: 深入瞭解： JET_ENUMCOLUMN 類別
title: JET_ENUMCOLUMN 類別
TOCTitle: JET_ENUMCOLUMN class
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumn(v=EXCHG.10)
ms:contentKeyID: 55103488
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dab7b5b8dc886f60f508c49f67e5dd3167e0cf5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971394"
---
# <a name="jet_enumcolumn-class"></a><span data-ttu-id="c3f69-103">JET_ENUMCOLUMN 類別</span><span class="sxs-lookup"><span data-stu-id="c3f69-103">JET_ENUMCOLUMN class</span></span>

<span data-ttu-id="c3f69-104">使用 JetEnumerateColumns 函數來列舉記錄的資料行值。</span><span class="sxs-lookup"><span data-stu-id="c3f69-104">Enumerates the column values of a record using the JetEnumerateColumns function.</span></span> <span data-ttu-id="c3f69-105">JetEnumerateColumns 會傳回 JET_ENUMCOLUMNVALUE 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="c3f69-105">JetEnumerateColumns returns an array of JET_ENUMCOLUMNVALUE structures.</span></span> <span data-ttu-id="c3f69-106">陣列會在使用提供給該函式之回呼配置的記憶體中傳回。</span><span class="sxs-lookup"><span data-stu-id="c3f69-106">The array is returned in memory that was allocated using the callback that was supplied to that function.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="c3f69-107">繼承階層</span><span class="sxs-lookup"><span data-stu-id="c3f69-107">Inheritance hierarchy</span></span>

[<span data-ttu-id="c3f69-108">System.Object</span><span class="sxs-lookup"><span data-stu-id="c3f69-108">System.Object</span></span>](/dotnet/api/system.object)  
  <span data-ttu-id="c3f69-109">Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="c3f69-109">Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN</span></span>  

<span data-ttu-id="c3f69-110">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c3f69-110">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c3f69-111">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="c3f69-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c3f69-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3f69-112">Syntax</span></span>

``` vb
'Declaration
Public Class JET_ENUMCOLUMN
'Usage
Dim instance As JET_ENUMCOLUMN
```

``` csharp
public class JET_ENUMCOLUMN
```

## <a name="thread-safety"></a><span data-ttu-id="c3f69-113">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="c3f69-113">Thread safety</span></span>

<span data-ttu-id="c3f69-114">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="c3f69-114">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="c3f69-115">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="c3f69-115">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="c3f69-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c3f69-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c3f69-117">參考</span><span class="sxs-lookup"><span data-stu-id="c3f69-117">Reference</span></span>

[<span data-ttu-id="c3f69-118">JET_ENUMCOLUMN 成員</span><span class="sxs-lookup"><span data-stu-id="c3f69-118">JET_ENUMCOLUMN members</span></span>](./jet-enumcolumn-members.md)

[<span data-ttu-id="c3f69-119">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="c3f69-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
