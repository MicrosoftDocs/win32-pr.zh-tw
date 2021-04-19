---
description: 深入瞭解： JET_prep 列舉
title: JET_prep 列舉
TOCTitle: JET_prep enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_prep
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_prep(v=EXCHG.10)
ms:contentKeyID: 39510193
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_prep.Replace
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopy
- Microsoft.Isam.Esent.Interop.JET_prep.Cancel
- Microsoft.Isam.Esent.Interop.JET_prep.Insert
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopyDeleteOriginal
- Microsoft.Isam.Esent.Interop.JET_prep
- Microsoft.Isam.Esent.Interop.JET_prep.ReplaceNoLock
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopyDeleteOriginal
- Microsoft.Isam.Esent.Interop.JET_prep.ReplaceNoLock
- Microsoft.Isam.Esent.Interop.JET_prep
- Microsoft.Isam.Esent.Interop.JET_prep.Cancel
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopy
- Microsoft.Isam.Esent.Interop.JET_prep.Insert
- Microsoft.Isam.Esent.Interop.JET_prep.Replace
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: edeaef8144fe6e13674ec6d3dfcb8adf7522e148
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996901"
---
# <a name="jet_prep-enumeration"></a><span data-ttu-id="75b2f-103">JET_prep 列舉</span><span class="sxs-lookup"><span data-stu-id="75b2f-103">JET_prep enumeration</span></span>

<span data-ttu-id="75b2f-104">更新 JetPrepareUpdate 的類型。</span><span class="sxs-lookup"><span data-stu-id="75b2f-104">Update types for JetPrepareUpdate.</span></span>

<span data-ttu-id="75b2f-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="75b2f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="75b2f-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="75b2f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="75b2f-107">語法</span><span class="sxs-lookup"><span data-stu-id="75b2f-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_prep
'Usage
Dim instance As JET_prep
```

``` csharp
public enum JET_prep
```

## <a name="members"></a><span data-ttu-id="75b2f-108">成員</span><span class="sxs-lookup"><span data-stu-id="75b2f-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="75b2f-109">成員名稱</span><span class="sxs-lookup"><span data-stu-id="75b2f-109">Member name</span></span></th>
<th><span data-ttu-id="75b2f-110">說明</span><span class="sxs-lookup"><span data-stu-id="75b2f-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="75b2f-111">插入</span><span class="sxs-lookup"><span data-stu-id="75b2f-111">Insert</span></span></td>
<td><span data-ttu-id="75b2f-112">此旗標會讓資料指標準備插入新的記錄。</span><span class="sxs-lookup"><span data-stu-id="75b2f-112">This flag causes the cursor to prepare for an insert of a new record.</span></span> <span data-ttu-id="75b2f-113">所有資料都會初始化為記錄的預設狀態。</span><span class="sxs-lookup"><span data-stu-id="75b2f-113">All the data is initialized to the default state for the record.</span></span> <span data-ttu-id="75b2f-114">如果資料表具有自動遞增資料行，就會將新的值指派給此記錄，而不論更新最終成功、失敗或已取消。</span><span class="sxs-lookup"><span data-stu-id="75b2f-114">If the table has an auto-increment column, then a new value is assigned to this record regardless of whether the update ultimately succeeds, fails or is cancelled.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="75b2f-115">取代</span><span class="sxs-lookup"><span data-stu-id="75b2f-115">Replace</span></span></td>
<td><span data-ttu-id="75b2f-116">此旗標會讓資料指標準備取代目前的記錄。</span><span class="sxs-lookup"><span data-stu-id="75b2f-116">This flag causes the cursor to prepare for a replace of the current record.</span></span> <span data-ttu-id="75b2f-117">如果資料表有版本資料行，則 [版本] 欄會設定為其序列中的下一個值。</span><span class="sxs-lookup"><span data-stu-id="75b2f-117">If the table has a version column, then the version column is set to the next value in its sequence.</span></span> <span data-ttu-id="75b2f-118">如果此更新未完成，則記錄中的版本值不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="75b2f-118">If this update does not complete, then the version value in the record will be unaffected.</span></span> <span data-ttu-id="75b2f-119">記錄上會執行更新鎖定，以防止其他會話在此會話完成之前更新此記錄。</span><span class="sxs-lookup"><span data-stu-id="75b2f-119">An update lock is taken on the record to prevent other sessions from updating this record before this session completes.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="75b2f-120">取消</span><span class="sxs-lookup"><span data-stu-id="75b2f-120">Cancel</span></span></td>
<td><span data-ttu-id="75b2f-121">此旗標會使 JetPrepareUpdate 取消此資料指標的更新。</span><span class="sxs-lookup"><span data-stu-id="75b2f-121">This flag causes JetPrepareUpdate to cancel the update for this cursor.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="75b2f-122">ReplaceNoLock</span><span class="sxs-lookup"><span data-stu-id="75b2f-122">ReplaceNoLock</span></span></td>
<td><span data-ttu-id="75b2f-123">此旗標類似于 JET_prepReplace，但不會採取任何鎖定來防止其他會話更新此記錄。</span><span class="sxs-lookup"><span data-stu-id="75b2f-123">This flag is similar to JET_prepReplace, but no lock is taken to prevent other sessions from updating this record.</span></span> <span data-ttu-id="75b2f-124">相反地，此會話可能會在呼叫 JetUpdate 來完成更新時收到 JET_errWriteConflict。</span><span class="sxs-lookup"><span data-stu-id="75b2f-124">Instead, this session may receive JET_errWriteConflict when it calls JetUpdate to complete the update.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="75b2f-125">InsertCopy</span><span class="sxs-lookup"><span data-stu-id="75b2f-125">InsertCopy</span></span></td>
<td><span data-ttu-id="75b2f-126">此旗標會讓資料指標準備插入現有記錄的複本。</span><span class="sxs-lookup"><span data-stu-id="75b2f-126">This flag causes the cursor to prepare for an insert of a copy of the existing record.</span></span> <span data-ttu-id="75b2f-127">如果使用此選項，則必須要有目前的記錄。</span><span class="sxs-lookup"><span data-stu-id="75b2f-127">There must be a current record if this option is used.</span></span> <span data-ttu-id="75b2f-128">新記錄的初始狀態會從目前記錄複製。</span><span class="sxs-lookup"><span data-stu-id="75b2f-128">The initial state of the new record is copied from the current record.</span></span> <span data-ttu-id="75b2f-129">幾乎會複製儲存在登出的 Long 值。</span><span class="sxs-lookup"><span data-stu-id="75b2f-129">Long values that are stored off-record are virtually copied.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="75b2f-130">InsertCopyDeleteOriginal</span><span class="sxs-lookup"><span data-stu-id="75b2f-130">InsertCopyDeleteOriginal</span></span></td>
<td><span data-ttu-id="75b2f-131">此旗標會讓資料指標準備插入相同的記錄，以及刪除或原始記錄。</span><span class="sxs-lookup"><span data-stu-id="75b2f-131">This flag causes the cursor to prepare for an insert of the same record, and a delete or the original record.</span></span> <span data-ttu-id="75b2f-132">當主要金鑰已變更時，就會使用它。</span><span class="sxs-lookup"><span data-stu-id="75b2f-132">It is used in cases in which the primary key has changed.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="75b2f-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="75b2f-133">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="75b2f-134">參考</span><span class="sxs-lookup"><span data-stu-id="75b2f-134">Reference</span></span>

[<span data-ttu-id="75b2f-135">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="75b2f-135">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
