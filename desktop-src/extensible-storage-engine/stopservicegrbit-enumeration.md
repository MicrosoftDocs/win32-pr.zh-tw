---
description: 深入瞭解： StopServiceGrbit 列舉
title: StopServiceGrbit 列舉 (Windows8) 的列舉
TOCTitle: StopServiceGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.stopservicegrbit(v=EXCHG.10)
ms:contentKeyID: 55104330
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.All
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.BackgroundUserTasks
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.QuiesceCaches
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.Resume
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.BackgroundUserTasks
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.All
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.QuiesceCaches
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.Resume
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 54e54576dfb1023ec4e3bc55ddd198a77f0ddf25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998253"
---
# <a name="stopservicegrbit-enumeration"></a><span data-ttu-id="b9b90-103">StopServiceGrbit 列舉</span><span class="sxs-lookup"><span data-stu-id="b9b90-103">StopServiceGrbit enumeration</span></span>

<span data-ttu-id="b9b90-104">[JetStopServiceInstance2 (JET_INSTANCE、StopServiceGrbit) ](./windows8api.jetstopserviceinstance2-method.md)的選項。</span><span class="sxs-lookup"><span data-stu-id="b9b90-104">Options for [JetStopServiceInstance2(JET_INSTANCE, StopServiceGrbit)](./windows8api.jetstopserviceinstance2-method.md).</span></span>

<span data-ttu-id="b9b90-105">此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。</span><span class="sxs-lookup"><span data-stu-id="b9b90-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="b9b90-106">**命名空間：**  [Microsoft Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b9b90-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="b9b90-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="b9b90-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b9b90-108">語法</span><span class="sxs-lookup"><span data-stu-id="b9b90-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration StopServiceGrbit
'Usage
Dim instance As StopServiceGrbit
```

``` csharp
[FlagsAttribute]
public enum StopServiceGrbit
```

## <a name="members"></a><span data-ttu-id="b9b90-109">成員</span><span class="sxs-lookup"><span data-stu-id="b9b90-109">Members</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="b9b90-110">成員名稱</span><span class="sxs-lookup"><span data-stu-id="b9b90-110">Member name</span></span></th>
<th><span data-ttu-id="b9b90-111">描述</span><span class="sxs-lookup"><span data-stu-id="b9b90-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="b9b90-112">全部</span><span class="sxs-lookup"><span data-stu-id="b9b90-112">All</span></span></td>
<td><span data-ttu-id="b9b90-113">停止指定之實例的所有 ESE 服務。</span><span class="sxs-lookup"><span data-stu-id="b9b90-113">Stops all ESE services for the specified instance.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="b9b90-114">BackgroundUserTasks</span><span class="sxs-lookup"><span data-stu-id="b9b90-114">BackgroundUserTasks</span></span></td>
<td><span data-ttu-id="b9b90-115">停止可重新開機的用戶端指定背景維護工作 (B + 樹重組) 。</span><span class="sxs-lookup"><span data-stu-id="b9b90-115">Stops restartable client specificed background maintenance tasks (B+ Tree Defrag).</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="b9b90-116">QuiesceCaches</span><span class="sxs-lookup"><span data-stu-id="b9b90-116">QuiesceCaches</span></span></td>
<td><span data-ttu-id="b9b90-117">將所有中途快取 Quiesces 至磁片。</span><span class="sxs-lookup"><span data-stu-id="b9b90-117">Quiesces all dirty caches to disk.</span></span> <span data-ttu-id="b9b90-118">非同步：</span><span class="sxs-lookup"><span data-stu-id="b9b90-118">Asynchronous.</span></span> <span data-ttu-id="b9b90-119">如果後續呼叫了 Resume 位，則會取消靜止。</span><span class="sxs-lookup"><span data-stu-id="b9b90-119">Quiescing is cancelled if the Resume bit is called subsequently.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="b9b90-120">繼續</span><span class="sxs-lookup"><span data-stu-id="b9b90-120">Resume</span></span></td>
<td><span data-ttu-id="b9b90-121">繼續先前發出的 StopService 作業，亦即 &quot; 重新開機服務 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="b9b90-121">Resumes previously issued StopService operations, i.e. &quot;restarts service&quot;.</span></span> <span data-ttu-id="b9b90-122">可以與上述 grbits 結合以繼續特定服務，或使用0x0 繼續所有先前已停止的服務。</span><span class="sxs-lookup"><span data-stu-id="b9b90-122">Can be combined with above grbits to Resume specific services, or with 0x0 Resumes all previous stopped services.</span></span>
<p><span data-ttu-id="b9b90-123">警告：這個位只能用來繼續 JET_bitStopServiceBackground，JET_bitStopServiceQuiesceCaches，如果您已 JET_bitStopServiceAll 或 JET_bitStopServiceAPI，嘗試使用 JET_bitStopServiceResume 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="b9b90-123">Warning: This bit can only be used to resume JET_bitStopServiceBackground and JET_bitStopServiceQuiesceCaches, if you did a JET_bitStopServiceAll or JET_bitStopServiceAPI, attempting to use JET_bitStopServiceResume will fail.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="b9b90-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b9b90-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b9b90-125">參考</span><span class="sxs-lookup"><span data-stu-id="b9b90-125">Reference</span></span>

[<span data-ttu-id="b9b90-126">Windows8 命名空間。</span><span class="sxs-lookup"><span data-stu-id="b9b90-126">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
