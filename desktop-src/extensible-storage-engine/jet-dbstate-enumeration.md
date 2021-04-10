---
description: 深入瞭解： JET_dbstate 列舉
title: JET_dbstate 列舉
TOCTitle: JET_dbstate enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_dbstate
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbstate(v=EXCHG.10)
ms:contentKeyID: 39511841
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_dbstate
- Microsoft.Isam.Esent.Interop.JET_dbstate.BeingConverted
- Microsoft.Isam.Esent.Interop.JET_dbstate.CleanShutdown
- Microsoft.Isam.Esent.Interop.JET_dbstate.DirtyShutdown
- Microsoft.Isam.Esent.Interop.JET_dbstate.ForceDetach
- Microsoft.Isam.Esent.Interop.JET_dbstate.JustCreated
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_dbstate.JustCreated
- Microsoft.Isam.Esent.Interop.JET_dbstate.BeingConverted
- Microsoft.Isam.Esent.Interop.JET_dbstate.CleanShutdown
- Microsoft.Isam.Esent.Interop.JET_dbstate.ForceDetach
- Microsoft.Isam.Esent.Interop.JET_dbstate.DirtyShutdown
- Microsoft.Isam.Esent.Interop.JET_dbstate
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a83c8a4313e5e6f21ee885ee7936c90503bfbd3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689619"
---
# <a name="jet_dbstate-enumeration"></a><span data-ttu-id="75509-103">JET_dbstate 列舉</span><span class="sxs-lookup"><span data-stu-id="75509-103">JET_dbstate enumeration</span></span>

<span data-ttu-id="75509-104">[JET_DBINFOMISC](./jet-dbinfomisc-class.md)) 中使用的資料庫狀態 (。</span><span class="sxs-lookup"><span data-stu-id="75509-104">Database states (used in [JET_DBINFOMISC](./jet-dbinfomisc-class.md)).</span></span>

<span data-ttu-id="75509-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="75509-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="75509-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="75509-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="75509-107">語法</span><span class="sxs-lookup"><span data-stu-id="75509-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_dbstate
'Usage
Dim instance As JET_dbstate
```

``` csharp
public enum JET_dbstate
```

## <a name="members"></a><span data-ttu-id="75509-108">成員</span><span class="sxs-lookup"><span data-stu-id="75509-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="75509-109">成員名稱</span><span class="sxs-lookup"><span data-stu-id="75509-109">Member name</span></span></th>
<th><span data-ttu-id="75509-110">說明</span><span class="sxs-lookup"><span data-stu-id="75509-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="75509-111">JustCreated</span><span class="sxs-lookup"><span data-stu-id="75509-111">JustCreated</span></span></td>
<td><span data-ttu-id="75509-112">剛建立資料庫。</span><span class="sxs-lookup"><span data-stu-id="75509-112">The database was just created.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="75509-113">DirtyShutdown</span><span class="sxs-lookup"><span data-stu-id="75509-113">DirtyShutdown</span></span></td>
<td><span data-ttu-id="75509-114">中途關機 (不一致的) 資料庫。</span><span class="sxs-lookup"><span data-stu-id="75509-114">Dirty shutdown (inconsistent) database.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="75509-115">CleanShutdown</span><span class="sxs-lookup"><span data-stu-id="75509-115">CleanShutdown</span></span></td>
<td><span data-ttu-id="75509-116">正常關機 (一致的) 資料庫。</span><span class="sxs-lookup"><span data-stu-id="75509-116">Clean shutdown (consistent) database.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="75509-117">BeingConverted</span><span class="sxs-lookup"><span data-stu-id="75509-117">BeingConverted</span></span></td>
<td><span data-ttu-id="75509-118">正在轉換資料庫。</span><span class="sxs-lookup"><span data-stu-id="75509-118">Database is being converted.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="75509-119">ForceDetach</span><span class="sxs-lookup"><span data-stu-id="75509-119">ForceDetach</span></span></td>
<td><span data-ttu-id="75509-120">已強制卸離資料庫。</span><span class="sxs-lookup"><span data-stu-id="75509-120">Database was force-detached.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="75509-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="75509-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="75509-122">參考</span><span class="sxs-lookup"><span data-stu-id="75509-122">Reference</span></span>

[<span data-ttu-id="75509-123">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="75509-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
