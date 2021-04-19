---
description: 深入瞭解： EventLoggingLevels 列舉
title: EventLoggingLevels 列舉
TOCTitle: EventLoggingLevels enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.EventLoggingLevels
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.eventlogginglevels(v=EXCHG.10)
ms:contentKeyID: 55103221
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EventLoggingLevels
- Microsoft.Isam.Esent.Interop.EventLoggingLevels.Disable
- Microsoft.Isam.Esent.Interop.EventLoggingLevels.High
- Microsoft.Isam.Esent.Interop.EventLoggingLevels.Low
- Microsoft.Isam.Esent.Interop.EventLoggingLevels.Max
- Microsoft.Isam.Esent.Interop.EventLoggingLevels.Medium
- Microsoft.Isam.Esent.Interop.EventLoggingLevels.Min
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EventLoggingLevels.Disable
- Microsoft.Isam.Esent.Interop.EventLoggingLevels.Min
- Microsoft.Isam.Esent.Interop.EventLoggingLevels
- Microsoft.Isam.Esent.Interop.EventLoggingLevels.High
- Microsoft.Isam.Esent.Interop.EventLoggingLevels.Medium
- Microsoft.Isam.Esent.Interop.EventLoggingLevels.Low
- Microsoft.Isam.Esent.Interop.EventLoggingLevels.Max
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7ec0881a7d217cfdcbc3680eaa3054dbb4fb62a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980915"
---
# <a name="eventlogginglevels-enumeration"></a><span data-ttu-id="1cc90-103">EventLoggingLevels 列舉</span><span class="sxs-lookup"><span data-stu-id="1cc90-103">EventLoggingLevels enumeration</span></span>

<span data-ttu-id="1cc90-104">EventLoggingLevel 的選項。</span><span class="sxs-lookup"><span data-stu-id="1cc90-104">Options for EventLoggingLevel.</span></span>

<span data-ttu-id="1cc90-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1cc90-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1cc90-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="1cc90-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1cc90-107">語法</span><span class="sxs-lookup"><span data-stu-id="1cc90-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration EventLoggingLevels
'Usage
Dim instance As EventLoggingLevels
```

``` csharp
public enum EventLoggingLevels
```

## <a name="members"></a><span data-ttu-id="1cc90-108">成員</span><span class="sxs-lookup"><span data-stu-id="1cc90-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="1cc90-109">成員名稱</span><span class="sxs-lookup"><span data-stu-id="1cc90-109">Member name</span></span></th>
<th><span data-ttu-id="1cc90-110">說明</span><span class="sxs-lookup"><span data-stu-id="1cc90-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="1cc90-111">停用</span><span class="sxs-lookup"><span data-stu-id="1cc90-111">Disable</span></span></td>
<td><span data-ttu-id="1cc90-112">停用所有事件。</span><span class="sxs-lookup"><span data-stu-id="1cc90-112">Disable all events.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="1cc90-113">Min</span><span class="sxs-lookup"><span data-stu-id="1cc90-113">Min</span></span></td>
<td><span data-ttu-id="1cc90-114">預設層級。</span><span class="sxs-lookup"><span data-stu-id="1cc90-114">Default level.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="1cc90-115">低</span><span class="sxs-lookup"><span data-stu-id="1cc90-115">Low</span></span></td>
<td><span data-ttu-id="1cc90-116">低詳細等級和較低。</span><span class="sxs-lookup"><span data-stu-id="1cc90-116">Low verbosity and lower.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="1cc90-117">中</span><span class="sxs-lookup"><span data-stu-id="1cc90-117">Medium</span></span></td>
<td><span data-ttu-id="1cc90-118">中度詳細資訊和更低。</span><span class="sxs-lookup"><span data-stu-id="1cc90-118">Medium verbosity and lower.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="1cc90-119">高</span><span class="sxs-lookup"><span data-stu-id="1cc90-119">High</span></span></td>
<td><span data-ttu-id="1cc90-120">高詳細程度和較低。</span><span class="sxs-lookup"><span data-stu-id="1cc90-120">High verbosity and lower.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="1cc90-121">最大值</span><span class="sxs-lookup"><span data-stu-id="1cc90-121">Max</span></span></td>
<td><span data-ttu-id="1cc90-122">所有事件。</span><span class="sxs-lookup"><span data-stu-id="1cc90-122">All events.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="1cc90-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1cc90-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1cc90-124">參考</span><span class="sxs-lookup"><span data-stu-id="1cc90-124">Reference</span></span>

[<span data-ttu-id="1cc90-125">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="1cc90-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
