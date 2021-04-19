---
description: 深入瞭解： JET_ENUMCOLUMNVALUE 類別
title: JET_ENUMCOLUMNVALUE 類別
TOCTitle: JET_ENUMCOLUMNVALUE class
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnvalue(v=EXCHG.10)
ms:contentKeyID: 55103622
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2066e6b4b3039ba150f17630afaef967c215823d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986293"
---
# <a name="jet_enumcolumnvalue-class"></a><span data-ttu-id="f25bd-103">JET_ENUMCOLUMNVALUE 類別</span><span class="sxs-lookup"><span data-stu-id="f25bd-103">JET_ENUMCOLUMNVALUE class</span></span>

<span data-ttu-id="f25bd-104">使用 JetEnumerateColumns 函數來列舉記錄的資料行值。</span><span class="sxs-lookup"><span data-stu-id="f25bd-104">Enumerates the column values of a record using the JetEnumerateColumns function.</span></span> <span data-ttu-id="f25bd-105">[JetEnumerateColumns (JET_SESID、JET_TABLEID、Int32、 \[ \] 、int32、 \[ \] 、JET_PFNREALLOC、IntPtr、int32、EnumerateColumnsGrbit) ](./api.jetenumeratecolumns-method.md)會傳回 JET_ENUMCOLUMNVALUE 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="f25bd-105">[JetEnumerateColumns(JET_SESID, JET_TABLEID, Int32, \[\], Int32, \[\], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)](./api.jetenumeratecolumns-method.md) returns an array of JET_ENUMCOLUMNVALUE structures.</span></span> <span data-ttu-id="f25bd-106">陣列會在使用提供給該函式之回呼配置的記憶體中傳回。</span><span class="sxs-lookup"><span data-stu-id="f25bd-106">The array is returned in memory that was allocated using the callback that was supplied to that function.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="f25bd-107">繼承階層</span><span class="sxs-lookup"><span data-stu-id="f25bd-107">Inheritance hierarchy</span></span>

[<span data-ttu-id="f25bd-108">System.Object</span><span class="sxs-lookup"><span data-stu-id="f25bd-108">System.Object</span></span>](/dotnet/api/system.object)  
  <span data-ttu-id="f25bd-109">Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="f25bd-109">Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE</span></span>  

<span data-ttu-id="f25bd-110">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f25bd-110">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f25bd-111">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="f25bd-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f25bd-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="f25bd-112">Syntax</span></span>

``` vb
'Declaration
Public Class JET_ENUMCOLUMNVALUE
'Usage
Dim instance As JET_ENUMCOLUMNVALUE
```

``` csharp
public class JET_ENUMCOLUMNVALUE
```

## <a name="thread-safety"></a><span data-ttu-id="f25bd-113">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="f25bd-113">Thread safety</span></span>

<span data-ttu-id="f25bd-114">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="f25bd-114">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="f25bd-115">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="f25bd-115">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="f25bd-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f25bd-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f25bd-117">參考</span><span class="sxs-lookup"><span data-stu-id="f25bd-117">Reference</span></span>

[<span data-ttu-id="f25bd-118">JET_ENUMCOLUMNVALUE 成員</span><span class="sxs-lookup"><span data-stu-id="f25bd-118">JET_ENUMCOLUMNVALUE members</span></span>](./jet-enumcolumnvalue-members.md)

[<span data-ttu-id="f25bd-119">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="f25bd-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
