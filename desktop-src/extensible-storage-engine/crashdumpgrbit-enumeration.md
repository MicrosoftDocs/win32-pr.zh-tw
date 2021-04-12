---
description: 深入瞭解： CrashDumpGrbit 列舉
title: CrashDumpGrbit 列舉 (最為理想) 的列舉
TOCTitle: CrashDumpGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows7.crashdumpgrbit(v=EXCHG.10)
ms:contentKeyID: 39515535
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheIncludeCachedPages
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheMinimum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.Maximum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheIncludeCorruptedPages
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheMaximum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheIncludeDirtyPages
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.Minimum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheIncludeDirtyPages
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheMaximum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheMinimum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheIncludeCachedPages
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheIncludeCorruptedPages
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.Minimum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.Maximum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3108190143115b1e6be5b7e0981d49c4bd9d4afa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318672"
---
# <a name="crashdumpgrbit-enumeration"></a><span data-ttu-id="af9db-103">CrashDumpGrbit 列舉</span><span class="sxs-lookup"><span data-stu-id="af9db-103">CrashDumpGrbit enumeration</span></span>

<span data-ttu-id="af9db-104">JetConfigureProcessForCrashDump 的選項。</span><span class="sxs-lookup"><span data-stu-id="af9db-104">Options for JetConfigureProcessForCrashDump.</span></span>

<span data-ttu-id="af9db-105">此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。</span><span class="sxs-lookup"><span data-stu-id="af9db-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="af9db-106">**命名空間：**  [Microsoft 最為理想](./microsoft.isam.esent.interop.windows7-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="af9db-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows7](./microsoft.isam.esent.interop.windows7-namespace.md)</span></span>  
<span data-ttu-id="af9db-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="af9db-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="af9db-108">語法</span><span class="sxs-lookup"><span data-stu-id="af9db-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CrashDumpGrbit
'Usage
Dim instance As CrashDumpGrbit
```

``` csharp
[FlagsAttribute]
public enum CrashDumpGrbit
```

## <a name="members"></a><span data-ttu-id="af9db-109">成員</span><span class="sxs-lookup"><span data-stu-id="af9db-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="af9db-110">成員名稱</span><span class="sxs-lookup"><span data-stu-id="af9db-110">Member name</span></span></th>
<th><span data-ttu-id="af9db-111">描述</span><span class="sxs-lookup"><span data-stu-id="af9db-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="af9db-112">無</span><span class="sxs-lookup"><span data-stu-id="af9db-112">None</span></span></td>
<td><span data-ttu-id="af9db-113">預設選項。</span><span class="sxs-lookup"><span data-stu-id="af9db-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="af9db-114">最小值</span><span class="sxs-lookup"><span data-stu-id="af9db-114">Minimum</span></span></td>
<td><span data-ttu-id="af9db-115">傾印最小值包括 CacheMinimum。</span><span class="sxs-lookup"><span data-stu-id="af9db-115">Dump minimum includes CacheMinimum.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="af9db-116">最大值</span><span class="sxs-lookup"><span data-stu-id="af9db-116">Maximum</span></span></td>
<td><span data-ttu-id="af9db-117">傾印最大值包括 CacheMaximum。</span><span class="sxs-lookup"><span data-stu-id="af9db-117">Dump maximum includes CacheMaximum.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="af9db-118">CacheMinimum</span><span class="sxs-lookup"><span data-stu-id="af9db-118">CacheMinimum</span></span></td>
<td><span data-ttu-id="af9db-119">CacheMinimum 包含已鎖定的頁面。</span><span class="sxs-lookup"><span data-stu-id="af9db-119">CacheMinimum includes pages that are latched.</span></span> <span data-ttu-id="af9db-120">CacheMinimum 包含用於記憶體的頁面。</span><span class="sxs-lookup"><span data-stu-id="af9db-120">CacheMinimum includes pages that are used for memory.</span></span> <span data-ttu-id="af9db-121">CacheMinimum 包含標示錯誤的頁面。</span><span class="sxs-lookup"><span data-stu-id="af9db-121">CacheMinimum includes pages that are flagged with errors.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="af9db-122">CacheMaximum</span><span class="sxs-lookup"><span data-stu-id="af9db-122">CacheMaximum</span></span></td>
<td><span data-ttu-id="af9db-123">快取最大值包含快取最小值。</span><span class="sxs-lookup"><span data-stu-id="af9db-123">Cache maximum includes cache minimum.</span></span> <span data-ttu-id="af9db-124">快取最大值包含整個快取映射。</span><span class="sxs-lookup"><span data-stu-id="af9db-124">Cache maximum includes the entire cache image.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="af9db-125">CacheIncludeDirtyPages</span><span class="sxs-lookup"><span data-stu-id="af9db-125">CacheIncludeDirtyPages</span></span></td>
<td><span data-ttu-id="af9db-126">傾印包含已修改的頁面。</span><span class="sxs-lookup"><span data-stu-id="af9db-126">Dump includes pages that are modified.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="af9db-127">CacheIncludeCachedPages</span><span class="sxs-lookup"><span data-stu-id="af9db-127">CacheIncludeCachedPages</span></span></td>
<td><span data-ttu-id="af9db-128">傾印包含包含有效資料的頁面。</span><span class="sxs-lookup"><span data-stu-id="af9db-128">Dump includes pages that contain valid data.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="af9db-129">CacheIncludeCorruptedPages</span><span class="sxs-lookup"><span data-stu-id="af9db-129">CacheIncludeCorruptedPages</span></span></td>
<td><span data-ttu-id="af9db-130">傾印包含已損毀的頁面， (昂貴的計算) 。</span><span class="sxs-lookup"><span data-stu-id="af9db-130">Dump includes pages that are corrupted (expensive to compute).</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="af9db-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="af9db-131">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="af9db-132">參考</span><span class="sxs-lookup"><span data-stu-id="af9db-132">Reference</span></span>

[<span data-ttu-id="af9db-133">最為理想命名空間。</span><span class="sxs-lookup"><span data-stu-id="af9db-133">Microsoft.Isam.Esent.Interop.Windows7 namespace</span></span>](./microsoft.isam.esent.interop.windows7-namespace.md)
