---
description: 深入瞭解： GetRecordSizeGrbit 列舉
title: GetRecordSizeGrbit 列舉
TOCTitle: GetRecordSizeGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.getrecordsizegrbit(v=EXCHG.10)
ms:contentKeyID: 39514742
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.InCopyBuffer
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.Local
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.None
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.RunningTotal
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.None
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.RunningTotal
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.InCopyBuffer
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.Local
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ee95d29ed1913993aa37062137807bf8d635eecc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980739"
---
# <a name="getrecordsizegrbit-enumeration"></a><span data-ttu-id="6badf-103">GetRecordSizeGrbit 列舉</span><span class="sxs-lookup"><span data-stu-id="6badf-103">GetRecordSizeGrbit enumeration</span></span>

<span data-ttu-id="6badf-104">[JetGetRecordSize (JET_SESID、JET_TABLEID、JET_RECSIZE、GetRecordSizeGrbit) ](./vistaapi.jetgetrecordsize-method.md)的選項。</span><span class="sxs-lookup"><span data-stu-id="6badf-104">Options for [JetGetRecordSize(JET_SESID, JET_TABLEID, JET_RECSIZE, GetRecordSizeGrbit)](./vistaapi.jetgetrecordsize-method.md).</span></span>

<span data-ttu-id="6badf-105">此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。</span><span class="sxs-lookup"><span data-stu-id="6badf-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="6badf-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6badf-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6badf-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="6badf-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6badf-108">語法</span><span class="sxs-lookup"><span data-stu-id="6badf-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration GetRecordSizeGrbit
'Usage
Dim instance As GetRecordSizeGrbit
```

``` csharp
[FlagsAttribute]
public enum GetRecordSizeGrbit
```

## <a name="members"></a><span data-ttu-id="6badf-109">成員</span><span class="sxs-lookup"><span data-stu-id="6badf-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="6badf-110">成員名稱</span><span class="sxs-lookup"><span data-stu-id="6badf-110">Member name</span></span></th>
<th><span data-ttu-id="6badf-111">描述</span><span class="sxs-lookup"><span data-stu-id="6badf-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="6badf-112">無</span><span class="sxs-lookup"><span data-stu-id="6badf-112">None</span></span></td>
<td><span data-ttu-id="6badf-113">預設選項。</span><span class="sxs-lookup"><span data-stu-id="6badf-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="6badf-114">InCopyBuffer</span><span class="sxs-lookup"><span data-stu-id="6badf-114">InCopyBuffer</span></span></td>
<td><span data-ttu-id="6badf-115">取得已備妥或更新之複製緩衝區中的記錄大小。</span><span class="sxs-lookup"><span data-stu-id="6badf-115">Retrieve the size of the record that is in the copy buffer prepared or update.</span></span> <span data-ttu-id="6badf-116">否則，tableid 必須位於記錄上，而且將會使用該記錄。</span><span class="sxs-lookup"><span data-stu-id="6badf-116">Otherwise, the tableid must be positioned on a record, and that record will be used.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="6badf-117">>runningtotal</span><span class="sxs-lookup"><span data-stu-id="6badf-117">RunningTotal</span></span></td>
<td><span data-ttu-id="6badf-118">在填滿內容之前，JET_RECSIZE 不會歸零，可有效地做為已造訪或更新之多筆記錄的統計資料累積。</span><span class="sxs-lookup"><span data-stu-id="6badf-118">The JET_RECSIZE is not zeroed before filling the contents, effectively acting as an accumulation of the statistics for multiple records visited or updated.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="6badf-119">本機</span><span class="sxs-lookup"><span data-stu-id="6badf-119">Local</span></span></td>
<td><span data-ttu-id="6badf-120">忽略非內建函式的 Long 值。</span><span class="sxs-lookup"><span data-stu-id="6badf-120">Ignore non-intrinsic Long Values.</span></span> <span data-ttu-id="6badf-121">只會使用頁面上的本機記錄。</span><span class="sxs-lookup"><span data-stu-id="6badf-121">Only the local record on the page will be used.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="6badf-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6badf-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6badf-123">參考</span><span class="sxs-lookup"><span data-stu-id="6badf-123">Reference</span></span>

[<span data-ttu-id="6badf-124">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="6badf-124">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
