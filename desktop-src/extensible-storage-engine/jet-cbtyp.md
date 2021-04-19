---
description: 深入瞭解： JET_CBTYP
title: JET_CBTYP
TOCTitle: JET_CBTYP
ms:assetid: babbfa11-01a7-477b-a525-cff27a983b60
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294071(v=EXCHG.10)
ms:contentKeyID: 32765686
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0b01bafad091ed17e018793ea701596aef6d0d72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984689"
---
# <a name="jet_cbtyp"></a><span data-ttu-id="cd02d-103">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="cd02d-103">JET_CBTYP</span></span>


<span data-ttu-id="cd02d-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="cd02d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_cbtyp"></a><span data-ttu-id="cd02d-105">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="cd02d-105">JET_CBTYP</span></span>

<span data-ttu-id="cd02d-106">**JET_CBTYP** 的常數群組會描述作業中的所有可能點，資料庫引擎會呼叫 [JET_CALLBACK](./jet-callback-callback-function.md)回呼函數來通知應用程式。</span><span class="sxs-lookup"><span data-stu-id="cd02d-106">The **JET_CBTYP** group of constants describes all possible points in an operation that the database engine will notify an application by calling the [JET_CALLBACK](./jet-callback-callback-function.md) callback function.</span></span> <span data-ttu-id="cd02d-107">資料庫引擎會在回呼函數的 *cbtyp* 參數中傳遞這些常數的其中一個。</span><span class="sxs-lookup"><span data-stu-id="cd02d-107">The database engine passes one of these constants in the *cbtyp* parameter of the callback function.</span></span> <span data-ttu-id="cd02d-108">資料庫引擎在此呼叫中傳遞的其他參數的意義取決於傳遞的特定 **JET_CBTYP** 。</span><span class="sxs-lookup"><span data-stu-id="cd02d-108">The meaning of the other parameters passed by the database engine in this call depend on the specific **JET_CBTYP** passed.</span></span>

<span data-ttu-id="cd02d-109">**WINDOWS XP：**  在 Windows XP 中引進了 **JET_CBTYP** 的常數群組。</span><span class="sxs-lookup"><span data-stu-id="cd02d-109">**Windows XP:**  The **JET_CBTYP** group of constants are introduced in Windows XP.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cd02d-110">常數/值</span><span class="sxs-lookup"><span data-stu-id="cd02d-110">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="cd02d-111">Description</span><span class="sxs-lookup"><span data-stu-id="cd02d-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd02d-112">JET_cbtypNull</span><span class="sxs-lookup"><span data-stu-id="cd02d-112">JET_cbtypNull</span></span><br />
<span data-ttu-id="cd02d-113">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cd02d-113">0x00000000</span></span></p></td>
<td><p><span data-ttu-id="cd02d-114">這是保留的回呼，而且一律視為無效。</span><span class="sxs-lookup"><span data-stu-id="cd02d-114">This callback is reserved and always considered invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd02d-115">JET_cbtypFinalize</span><span class="sxs-lookup"><span data-stu-id="cd02d-115">JET_cbtypFinalize</span></span><br />
<span data-ttu-id="cd02d-116">0x00000001</span><span class="sxs-lookup"><span data-stu-id="cd02d-116">0x00000001</span></span></p></td>
<td><p><span data-ttu-id="cd02d-117">此回呼已保留供日後使用。</span><span class="sxs-lookup"><span data-stu-id="cd02d-117">This callback is reserved for future use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd02d-118">JET_cbtypBeforeInsert</span><span class="sxs-lookup"><span data-stu-id="cd02d-118">JET_cbtypBeforeInsert</span></span><br />
<span data-ttu-id="cd02d-119">0x00000002</span><span class="sxs-lookup"><span data-stu-id="cd02d-119">0x00000002</span></span></p></td>
<td><p><span data-ttu-id="cd02d-120">這項回呼會在透過呼叫 <a href="gg269288(v=exchg.10).md">JetUpdate</a>將新的記錄插入資料表之前進行。</span><span class="sxs-lookup"><span data-stu-id="cd02d-120">This callback will occur just before a new record is inserted into a table by a call to <a href="gg269288(v=exchg.10).md">JetUpdate</a>.</span></span></p>
<p><span data-ttu-id="cd02d-121">此回呼原因的函式指標是透過<a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a>傳遞給<a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> ，或是在執行時間透過<a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>來設定。</span><span class="sxs-lookup"><span data-stu-id="cd02d-121">The function pointer for this callback reason is either passed to <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> by means of <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or is configured at runtime by means of <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span> <span data-ttu-id="cd02d-122">如需詳細資訊，請參閱 <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> 或 <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>。</span><span class="sxs-lookup"><span data-stu-id="cd02d-122">For more information, see <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span></p>
<p><span data-ttu-id="cd02d-123">回呼參數會有下列值：</span><span class="sxs-lookup"><span data-stu-id="cd02d-123">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="cd02d-124"><em>sesid</em>：要插入記錄的會話。</span><span class="sxs-lookup"><span data-stu-id="cd02d-124"><em>sesid</em>: The session that has the record to be inserted.</span></span></p></li>
<li><p><span data-ttu-id="cd02d-125"><em>dbid</em>：包含要插入之記錄的資料表之資料庫識別碼。</span><span class="sxs-lookup"><span data-stu-id="cd02d-125"><em>dbid</em>: The database ID of the table that contains the record to be inserted.</span></span></p></li>
<li><p><span data-ttu-id="cd02d-126"><em>tableid</em>：已備妥要插入新記錄的資料指標。</span><span class="sxs-lookup"><span data-stu-id="cd02d-126"><em>tableid</em>: The cursor that has prepared the new record to be inserted.</span></span> <span data-ttu-id="cd02d-127">請務必注意，在此時間，任何版本或自動遞增資料行的值可能不正確。</span><span class="sxs-lookup"><span data-stu-id="cd02d-127">It is important to note that the value of any version or auto-increment columns may not be correct at this time.</span></span></p></li>
<li><p><span data-ttu-id="cd02d-128"><em>pvArg1</em>： <strong>Null</strong></span><span class="sxs-lookup"><span data-stu-id="cd02d-128"><em>pvArg1</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="cd02d-129"><em>pvArg2</em>： <strong>Null</strong></span><span class="sxs-lookup"><span data-stu-id="cd02d-129"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="cd02d-130"><em>pvCoNtext</em>：傳遞至 <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> 或 <strong>Null</strong>的內容指標。</span><span class="sxs-lookup"><span data-stu-id="cd02d-130"><em>pvContext</em>: The context pointer passed to <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> or <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="cd02d-131"><em>ulUnused</em>： <strong>Null</strong> 如果回呼傳回錯誤，則源自回呼的作業將會失敗，並出現該錯誤。</span><span class="sxs-lookup"><span data-stu-id="cd02d-131"><em>ulUnused</em>: <strong>NULL</strong> If an error is returned by the callback, the operation originating the callback will fail with that error.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd02d-132">JET_cbtypAfterInsert</span><span class="sxs-lookup"><span data-stu-id="cd02d-132">JET_cbtypAfterInsert</span></span><br />
<span data-ttu-id="cd02d-133">0x00000004</span><span class="sxs-lookup"><span data-stu-id="cd02d-133">0x00000004</span></span></p></td>
<td><p><span data-ttu-id="cd02d-134">只要呼叫 <a href="gg269288(v=exchg.10).md">JetUpdate</a> ，但在 <a href="gg269288(v=exchg.10).md">JetUpdate</a> 回到其呼叫端之前，新的記錄插入資料表中，就會發生此回呼。</span><span class="sxs-lookup"><span data-stu-id="cd02d-134">This callback will occur just after a new record has been inserted into a table by a call to <a href="gg269288(v=exchg.10).md">JetUpdate</a> but before <a href="gg269288(v=exchg.10).md">JetUpdate</a> returns to its caller.</span></span></p>
<p><span data-ttu-id="cd02d-135">此回呼原因的函式指標是透過<a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a>傳遞給<a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> ，或是在執行時間透過<a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>來設定。</span><span class="sxs-lookup"><span data-stu-id="cd02d-135">The function pointer for this callback reason is either passed to <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> by means of <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or is configured at runtime by means of <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span> <span data-ttu-id="cd02d-136">如需詳細資訊，請參閱 <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> 或 <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>。</span><span class="sxs-lookup"><span data-stu-id="cd02d-136">For more information, see <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span></p>
<p><span data-ttu-id="cd02d-137">回呼參數會有下列值：</span><span class="sxs-lookup"><span data-stu-id="cd02d-137">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="cd02d-138"><em>sesid</em>：具有剛插入之記錄的會話。</span><span class="sxs-lookup"><span data-stu-id="cd02d-138"><em>sesid</em>: The session that has the record that was just inserted.</span></span></p></li>
<li><p><span data-ttu-id="cd02d-139"><em>dbid</em>：包含剛插入之記錄的資料表之資料庫識別碼。</span><span class="sxs-lookup"><span data-stu-id="cd02d-139"><em>dbid</em>: The database ID of the table that contains the record that was just inserted.</span></span></p></li>
<li><p><span data-ttu-id="cd02d-140"><em>tableid</em>：資料表上的資料指標，表示剛插入的記錄。</span><span class="sxs-lookup"><span data-stu-id="cd02d-140"><em>tableid</em>: A cursor on the table into which the record that was just inserted.</span></span> <span data-ttu-id="cd02d-141">請注意，資料指標仍位於與 insert 回呼之前相同的索引項目。</span><span class="sxs-lookup"><span data-stu-id="cd02d-141">Note that the cursor is still positioned on the same index entry as it was in the before insert callback.</span></span> <span data-ttu-id="cd02d-142">此外也請注意，此索引項目可能不會以任何方式與插入的記錄相關。</span><span class="sxs-lookup"><span data-stu-id="cd02d-142">Further note that this index entry may not be related in any way to the record being inserted.</span></span></p></li>
<li><p><span data-ttu-id="cd02d-143"><em>pvArg1</em>： <strong>Null</strong></span><span class="sxs-lookup"><span data-stu-id="cd02d-143"><em>pvArg1</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="cd02d-144"><em>pvArg2</em>： <strong>Null</strong></span><span class="sxs-lookup"><span data-stu-id="cd02d-144"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="cd02d-145"><em>pvCoNtext</em>：傳遞至 <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> 或 <strong>Null</strong>的內容指標。</span><span class="sxs-lookup"><span data-stu-id="cd02d-145"><em>pvContext</em>: The context pointer passed to <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> or <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="cd02d-146"><em>ulUnused</em>： <strong>Null</strong> 如果回呼傳回錯誤，則會忽略它。</span><span class="sxs-lookup"><span data-stu-id="cd02d-146"><em>ulUnused</em>: <strong>NULL</strong> If an error is returned by the callback, it will be ignored.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd02d-147">JET_cbtypBeforeReplace</span><span class="sxs-lookup"><span data-stu-id="cd02d-147">JET_cbtypBeforeReplace</span></span><br />
<span data-ttu-id="cd02d-148">0x00000008</span><span class="sxs-lookup"><span data-stu-id="cd02d-148">0x00000008</span></span></p></td>
<td><p><span data-ttu-id="cd02d-149">這項回呼會在 <a href="gg269288(v=exchg.10).md">JetUpdate</a>的呼叫變更資料表中的現有記錄之前發生。</span><span class="sxs-lookup"><span data-stu-id="cd02d-149">This callback will occur just prior to an existing record in a table being changed by a call to <a href="gg269288(v=exchg.10).md">JetUpdate</a>.</span></span></p>
<p><span data-ttu-id="cd02d-150">此回呼原因的函式指標是透過<a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a>傳遞給<a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> ，或是在執行時間透過<a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>來設定。</span><span class="sxs-lookup"><span data-stu-id="cd02d-150">The function pointer for this callback reason is either passed to <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> by means of <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or is configured at runtime by means of <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span> <span data-ttu-id="cd02d-151">如需詳細資訊，請參閱 <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> 或 <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>。</span><span class="sxs-lookup"><span data-stu-id="cd02d-151">For more information, see <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span></p>
<p><span data-ttu-id="cd02d-152">回呼參數會有下列值：</span><span class="sxs-lookup"><span data-stu-id="cd02d-152">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="cd02d-153"><em>sesid</em>：包含要變更之記錄的會話。</span><span class="sxs-lookup"><span data-stu-id="cd02d-153"><em>sesid</em>: The session that has the record to be changed.</span></span></p></li>
<li><p><span data-ttu-id="cd02d-154"><em>dbid</em>：包含要變更之記錄之資料表的資料庫識別碼。</span><span class="sxs-lookup"><span data-stu-id="cd02d-154"><em>dbid</em>: The database ID of the table that contains the record to be changed.</span></span></p></li>
<li><p><span data-ttu-id="cd02d-155"><em>tableid</em>：游標位於與要變更之記錄相關聯的索引項目上。</span><span class="sxs-lookup"><span data-stu-id="cd02d-155"><em>tableid</em>: A cursor positioned on an index entry associated with the record to be changed.</span></span> <span data-ttu-id="cd02d-156">請務必注意，在此時間，任何版本或自動遞增資料行的值可能不正確。</span><span class="sxs-lookup"><span data-stu-id="cd02d-156">It is important to note that the value of any version or auto-increment columns may not be correct at this time.</span></span></p></li>
<li><p><span data-ttu-id="cd02d-157"><em>pvArg1</em>： <strong>Null</strong></span><span class="sxs-lookup"><span data-stu-id="cd02d-157"><em>pvArg1</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="cd02d-158"><em>pvArg2</em>： <strong>Null</strong></span><span class="sxs-lookup"><span data-stu-id="cd02d-158"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="cd02d-159"><em>pvCoNtext</em>：傳遞至 <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> 或 <strong>Null</strong>的內容指標。</span><span class="sxs-lookup"><span data-stu-id="cd02d-159"><em>pvContext</em>: The context pointer passed to <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> or <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="cd02d-160"><em>ulUnused</em>： <strong>Null</strong> 如果回呼傳回錯誤，則源自回呼的作業將會失敗，並出現該錯誤。</span><span class="sxs-lookup"><span data-stu-id="cd02d-160"><em>ulUnused</em>: <strong>NULL</strong> If an error is returned by the callback, the operation originating the callback will fail with that error.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd02d-161">JET_cbtypAfterReplace</span><span class="sxs-lookup"><span data-stu-id="cd02d-161">JET_cbtypAfterReplace</span></span><br />
<span data-ttu-id="cd02d-162">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd02d-162">0x00000010</span></span></p></td>
<td><p><span data-ttu-id="cd02d-163">這項回呼會在資料表中的現有記錄已由呼叫 <a href="gg269288(v=exchg.10).md">JetUpdate</a> ，但在 <a href="gg269288(v=exchg.10).md">JetUpdate</a> 返回其呼叫端之前發生。</span><span class="sxs-lookup"><span data-stu-id="cd02d-163">This callback will occur just after an existing record in a table has been changed by a call to <a href="gg269288(v=exchg.10).md">JetUpdate</a> but prior to <a href="gg269288(v=exchg.10).md">JetUpdate</a> returning to its caller.</span></span></p>
<p><span data-ttu-id="cd02d-164">此回呼原因的函式指標是透過<a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a>傳遞給<a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> ，或是在執行時間透過<a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>來設定。</span><span class="sxs-lookup"><span data-stu-id="cd02d-164">The function pointer for this callback reason is either passed to <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> by means of <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or is configured at runtime by means of <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span> <span data-ttu-id="cd02d-165">如需詳細資訊，請參閱 <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> 或 <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>。</span><span class="sxs-lookup"><span data-stu-id="cd02d-165">For more information, see <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span></p>
<p><span data-ttu-id="cd02d-166">回呼參數會有下列值：</span><span class="sxs-lookup"><span data-stu-id="cd02d-166">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="cd02d-167"><em>sesid</em>：具有剛剛變更之記錄的會話。</span><span class="sxs-lookup"><span data-stu-id="cd02d-167"><em>sesid</em>: The session that has the record that was just changed.</span></span></p></li>
<li><p><span data-ttu-id="cd02d-168"><em>dbid</em>：包含剛變更之記錄的資料表之資料庫識別碼。</span><span class="sxs-lookup"><span data-stu-id="cd02d-168"><em>dbid</em>: The database ID of the table that contains the record that was just changed.</span></span></p></li>
<li><p><span data-ttu-id="cd02d-169"><em>tableid</em>：游標位於與剛剛變更之記錄相關聯的索引項目目上。</span><span class="sxs-lookup"><span data-stu-id="cd02d-169"><em>tableid</em>: A cursor positioned on an index entry associated with the record that was just changed.</span></span></p></li>
<li><p><span data-ttu-id="cd02d-170"><em>pvArg1</em>： <strong>Null</strong></span><span class="sxs-lookup"><span data-stu-id="cd02d-170"><em>pvArg1</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="cd02d-171"><em>pvArg2</em>： <strong>Null</strong></span><span class="sxs-lookup"><span data-stu-id="cd02d-171"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="cd02d-172"><em>pvCoNtext</em>：傳遞至 <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> 或 <strong>Null</strong>的內容指標。</span><span class="sxs-lookup"><span data-stu-id="cd02d-172"><em>pvContext</em>: The context pointer passed to <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> or <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="cd02d-173"><em>ulUnused</em>： <strong>Null</strong> 如果回呼傳回錯誤，則會忽略它。</span><span class="sxs-lookup"><span data-stu-id="cd02d-173"><em>ulUnused</em>: <strong>NULL</strong> If an error is returned by the callback, it will be ignored.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd02d-174">JET_cbtypBeforeDelete</span><span class="sxs-lookup"><span data-stu-id="cd02d-174">JET_cbtypBeforeDelete</span></span><br />
<span data-ttu-id="cd02d-175">0x00000020</span><span class="sxs-lookup"><span data-stu-id="cd02d-175">0x00000020</span></span></p></td>
<td><p><span data-ttu-id="cd02d-176">這項回呼會在呼叫 <a href="gg269315(v=exchg.10).md">JetDelete</a>來刪除資料表中的現有記錄之前發生。</span><span class="sxs-lookup"><span data-stu-id="cd02d-176">This callback will occur just before an existing record in a table is deleted by a call to <a href="gg269315(v=exchg.10).md">JetDelete</a>.</span></span></p>
<p><span data-ttu-id="cd02d-177">此回呼原因的函式指標是透過<a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a>傳遞給<a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> ，或是在執行時間透過<a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>來設定。</span><span class="sxs-lookup"><span data-stu-id="cd02d-177">The function pointer for this callback reason is either passed to <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> by means of <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or is configured at runtime by means of <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span> <span data-ttu-id="cd02d-178">如需詳細資訊，請參閱 <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> 或 <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>。</span><span class="sxs-lookup"><span data-stu-id="cd02d-178">For more information, see <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span></p>
<p><span data-ttu-id="cd02d-179">回呼參數會有下列值：</span><span class="sxs-lookup"><span data-stu-id="cd02d-179">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="cd02d-180"><em>sesid</em>：具有要刪除之記錄的會話。</span><span class="sxs-lookup"><span data-stu-id="cd02d-180"><em>sesid</em>: The session that has the record to be deleted.</span></span></p></li>
<li><p><span data-ttu-id="cd02d-181"><em>dbid</em>：包含要刪除之記錄的資料表之資料庫識別碼。</span><span class="sxs-lookup"><span data-stu-id="cd02d-181"><em>dbid</em>: The database ID of the table that contains the record to be deleted.</span></span></p></li>
<li><p><span data-ttu-id="cd02d-182"><em>tableid</em>：游標位於與要刪除之記錄相關聯的索引項目上。</span><span class="sxs-lookup"><span data-stu-id="cd02d-182"><em>tableid</em>: A cursor positioned on an index entry associated with the record to be deleted.</span></span></p></li>
<li><p><span data-ttu-id="cd02d-183"><em>pvArg1</em>： <strong>Null</strong></span><span class="sxs-lookup"><span data-stu-id="cd02d-183"><em>pvArg1</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="cd02d-184"><em>pvArg2</em>： <strong>Null</strong></span><span class="sxs-lookup"><span data-stu-id="cd02d-184"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="cd02d-185"><em>pvCoNtext</em>：傳遞至 <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> 或 <strong>Null</strong>的內容指標。</span><span class="sxs-lookup"><span data-stu-id="cd02d-185"><em>pvContext</em>: The context pointer passed to <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> or <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="cd02d-186"><em>ulUnused</em>： <strong>Null</strong> 如果回呼傳回錯誤，則源自回呼的作業將會失敗，並出現該錯誤。</span><span class="sxs-lookup"><span data-stu-id="cd02d-186"><em>ulUnused</em>: <strong>NULL</strong> If an error is returned by the callback, the operation originating the callback will fail with that error.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd02d-187">JET_cbtypAfterDelete</span><span class="sxs-lookup"><span data-stu-id="cd02d-187">JET_cbtypAfterDelete</span></span><br />
<span data-ttu-id="cd02d-188">0x00000040</span><span class="sxs-lookup"><span data-stu-id="cd02d-188">0x00000040</span></span></p></td>
<td><p><span data-ttu-id="cd02d-189">這項回呼會在呼叫 <a href="gg269315(v=exchg.10).md">JetDelete</a> 時，但在 <a href="gg269315(v=exchg.10).md">JetDelete</a> 傳回給其呼叫端之前，于資料表中的現有記錄已刪除的情況下發生。</span><span class="sxs-lookup"><span data-stu-id="cd02d-189">This callback will occur just after an existing record in a table has been deleted by a call to <a href="gg269315(v=exchg.10).md">JetDelete</a> but before <a href="gg269315(v=exchg.10).md">JetDelete</a> returns to its caller.</span></span></p>
<p><span data-ttu-id="cd02d-190">此回呼原因的函式指標是透過<a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a>傳遞給<a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> ，或是在執行時間透過<a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>來設定。</span><span class="sxs-lookup"><span data-stu-id="cd02d-190">The function pointer for this callback reason is either passed to <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> by means of <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or is configured at runtime by means of <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span> <span data-ttu-id="cd02d-191">如需詳細資訊，請參閱 <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> 或 <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>。</span><span class="sxs-lookup"><span data-stu-id="cd02d-191">For more information, see <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span></p>
<p><span data-ttu-id="cd02d-192">回呼參數會有下列值：</span><span class="sxs-lookup"><span data-stu-id="cd02d-192">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="cd02d-193"><em>sesid</em>：具有剛刪除記錄的會話。</span><span class="sxs-lookup"><span data-stu-id="cd02d-193"><em>sesid</em>: The session that has the record that was just deleted.</span></span></p></li>
<li><p><span data-ttu-id="cd02d-194"><em>dbid</em>：包含剛刪除記錄之資料表的資料庫識別碼。</span><span class="sxs-lookup"><span data-stu-id="cd02d-194"><em>dbid</em>: The database ID of the table that contains the record that was just deleted.</span></span></p></li>
<li><p><span data-ttu-id="cd02d-195"><em>tableid</em>：游標位於與剛刪除之記錄相關聯的索引項目上。</span><span class="sxs-lookup"><span data-stu-id="cd02d-195"><em>tableid</em>: A cursor positioned on an index entry associated with the record that was just deleted.</span></span></p></li>
<li><p><span data-ttu-id="cd02d-196"><em>pvArg1</em>： <strong>Null</strong></span><span class="sxs-lookup"><span data-stu-id="cd02d-196"><em>pvArg1</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="cd02d-197"><em>pvArg2</em>： <strong>Null</strong></span><span class="sxs-lookup"><span data-stu-id="cd02d-197"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="cd02d-198"><em>pvCoNtext</em>：傳遞至 <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> 或 <strong>Null</strong>的內容指標。</span><span class="sxs-lookup"><span data-stu-id="cd02d-198"><em>pvContext</em>: the context pointer passed to <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> or <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="cd02d-199"><em>ulUnused</em>： <strong>Null</strong></span><span class="sxs-lookup"><span data-stu-id="cd02d-199"><em>ulUnused</em>: <strong>NULL</strong></span></span></p></li>
</ul>
<p><span data-ttu-id="cd02d-200">如果回呼傳回錯誤，則會忽略它。</span><span class="sxs-lookup"><span data-stu-id="cd02d-200">If an error is returned by the callback, it will be ignored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd02d-201">JET_cbtypUserDefinedDefaultValue</span><span class="sxs-lookup"><span data-stu-id="cd02d-201">JET_cbtypUserDefinedDefaultValue</span></span><br />
<span data-ttu-id="cd02d-202">0x00000080</span><span class="sxs-lookup"><span data-stu-id="cd02d-202">0x00000080</span></span></p></td>
<td><p><span data-ttu-id="cd02d-203">當引擎需要從應用程式取得使用者定義的資料行預設值時，就會發生此回呼。</span><span class="sxs-lookup"><span data-stu-id="cd02d-203">This callback will occur when the engine needs to retrieve the user defined default value of a column from the application.</span></span> <span data-ttu-id="cd02d-204">此回呼基本上是由應用程式評估的 <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> 有限實作為。</span><span class="sxs-lookup"><span data-stu-id="cd02d-204">This callback is essentially a limited implementation of <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> that is evaluated by the application.</span></span> <span data-ttu-id="cd02d-205">最多可以針對使用者定義的預設值傳回一個資料行值。</span><span class="sxs-lookup"><span data-stu-id="cd02d-205">A maximum of one column value can be returned for a user defined default value.</span></span></p>
<p><span data-ttu-id="cd02d-206">此回呼原因的函式指標是透過<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>結構傳遞至<a href="gg294122(v=exchg.10).md">JetAddColumn</a> ，或透過<a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a>結構中<a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a>結構的<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>結構傳遞至<a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> 。</span><span class="sxs-lookup"><span data-stu-id="cd02d-206">The function pointer for this callback reason is either passed to <a href="gg294122(v=exchg.10).md">JetAddColumn</a> by means of a <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> structure or passed to <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> by means of a <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> structure in a <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure in a <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> structure.</span></span></p>
<p><span data-ttu-id="cd02d-207">回呼參數會有下列值：</span><span class="sxs-lookup"><span data-stu-id="cd02d-207">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="cd02d-208"><em>sesid</em>：正在計算使用者定義之預設值的會話</span><span class="sxs-lookup"><span data-stu-id="cd02d-208"><em>sesid</em>: The session that is computing the user defined default value</span></span></p></li>
<li><p><span data-ttu-id="cd02d-209"><em>dbid</em>：包含使用者定義之預設值之資料表的資料庫識別碼</span><span class="sxs-lookup"><span data-stu-id="cd02d-209"><em>dbid</em>: The database ID of the table that contains the user defined default value</span></span></p></li>
<li><p><span data-ttu-id="cd02d-210"><em>tableid</em>：位於記錄上的資料指標，該記錄會抓取使用者定義的預設值</span><span class="sxs-lookup"><span data-stu-id="cd02d-210"><em>tableid</em>: A cursor positioned on the record for which the user defined default value is being retrieved</span></span></p></li>
<li><p><span data-ttu-id="cd02d-211"><em>pvArg1</em>：使用者定義之預設值的輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="cd02d-211"><em>pvArg1</em>: The output buffer for the user defined default value</span></span></p></li>
<li><p><span data-ttu-id="cd02d-212"><em>pvArg2</em>：在輸入時，這是輸出緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="cd02d-212"><em>pvArg2</em>: On input, this is the size of the output buffer.</span></span> <span data-ttu-id="cd02d-213">在輸出時，這是使用者定義之預設值的實際大小。</span><span class="sxs-lookup"><span data-stu-id="cd02d-213">On output, this is the actual size of the user defined default value.</span></span> <span data-ttu-id="cd02d-214">在任一種情況下，大小為32位不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="cd02d-214">in either case, the size is a 32-bit unsigned integer.</span></span></p></li>
<li><p><span data-ttu-id="cd02d-215"><em>pvCoNtext</em>：緩衝區的指標，其中包含建立資料行時在 <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> 結構中指定的使用者資料，如果未提供內容則為 Null。</span><span class="sxs-lookup"><span data-stu-id="cd02d-215"><em>pvContext</em>: A pointer to a buffer containing the user data specified in the <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> structure when the column was created or NULL if no context was provided.</span></span></p></li>
<li><p><span data-ttu-id="cd02d-216"><em>ulUnused</em>：即將抓取使用者定義預設值之資料行的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="cd02d-216"><em>ulUnused</em>: The column ID of the column for which the user defined default value is being retrieved.</span></span></p></li>
</ul>
<p><span data-ttu-id="cd02d-217">如果回呼傳回錯誤，則源自回呼的作業將會失敗，並出現該錯誤。</span><span class="sxs-lookup"><span data-stu-id="cd02d-217">If an error is returned by the callback then the operation originating the callback will fail with that error.</span></span></p>
<p><span data-ttu-id="cd02d-218">如果回呼傳回 JET_wrnBufferTruncated，作業將會繼續，但在回呼期間不會取出整個值。</span><span class="sxs-lookup"><span data-stu-id="cd02d-218">If JET_wrnBufferTruncated is returned by the callback, the operation will continue, but the entire value is not retrieved during the callback.</span></span></p>
<p><span data-ttu-id="cd02d-219">如果回呼傳回 JET_wrnColumnNull，此作業將會繼續，但資料行的使用者定義預設值為 Null。</span><span class="sxs-lookup"><span data-stu-id="cd02d-219">If JET_wrnColumnNull is returned by the callback, the operation will continue, but the user defined default value for the column is NULL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd02d-220">JET_cbtypOnlineDefragCompleted</span><span class="sxs-lookup"><span data-stu-id="cd02d-220">JET_cbtypOnlineDefragCompleted</span></span><br />
<span data-ttu-id="cd02d-221">0x00000100</span><span class="sxs-lookup"><span data-stu-id="cd02d-221">0x00000100</span></span></p></td>
<td><p><span data-ttu-id="cd02d-222">當 <a href="gg269317(v=exchg.10).md">JetDefragment</a> 所起始的資料庫線上磁碟重組已停止，因為進程已完成或達到時間限制時，就會發生此回呼。</span><span class="sxs-lookup"><span data-stu-id="cd02d-222">This callback will occur when the online defragmentation of a database as initiated by <a href="gg269317(v=exchg.10).md">JetDefragment</a> has stopped due to either the process being completed or the time limit being reached.</span></span></p>
<p><span data-ttu-id="cd02d-223">此回呼原因的函式指標會傳遞至 <a href="gg269317(v=exchg.10).md">JetDefragment</a>。</span><span class="sxs-lookup"><span data-stu-id="cd02d-223">The function pointer for this callback reason is passed to <a href="gg269317(v=exchg.10).md">JetDefragment</a>.</span></span> <span data-ttu-id="cd02d-224">如需詳細資訊，請參閱 <a href="gg269317(v=exchg.10).md">JetDefragment</a>。</span><span class="sxs-lookup"><span data-stu-id="cd02d-224">For more information, see <a href="gg269317(v=exchg.10).md">JetDefragment</a>.</span></span></p>
<p><span data-ttu-id="cd02d-225">回呼參數會有下列值：</span><span class="sxs-lookup"><span data-stu-id="cd02d-225">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="cd02d-226"><em>sesid</em>：用來對資料流程檔案執行資料庫或 JET_sesidNil 的線上磁碟重組的會話。</span><span class="sxs-lookup"><span data-stu-id="cd02d-226"><em>sesid</em>: The session used to perform online defragmentation for the database or JET_sesidNil for a streaming file.</span></span></p></li>
<li><p><span data-ttu-id="cd02d-227"><em>dbid</em>：要針對資料流程檔案進行磁碟重組或 JET_dbidNil 之資料庫的資料庫識別碼。</span><span class="sxs-lookup"><span data-stu-id="cd02d-227"><em>dbid</em>: The database ID of the database being defragmented or JET_dbidNil for a streaming file.</span></span></p></li>
<li><p><span data-ttu-id="cd02d-228"><em>tableid</em>： JET_tableidNil</span><span class="sxs-lookup"><span data-stu-id="cd02d-228"><em>tableid</em>: JET_tableidNil</span></span></p></li>
<li><p><span data-ttu-id="cd02d-229"><em>pvArg1</em>： <strong>Null</strong></span><span class="sxs-lookup"><span data-stu-id="cd02d-229"><em>pvArg1</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="cd02d-230"><em>pvArg2</em>： <strong>Null</strong></span><span class="sxs-lookup"><span data-stu-id="cd02d-230"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="cd02d-231"><em>pvCoNtext</em>： <strong>Null</strong></span><span class="sxs-lookup"><span data-stu-id="cd02d-231"><em>pvContext</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="cd02d-232"><em>ulUnused</em>： <strong>Null</strong></span><span class="sxs-lookup"><span data-stu-id="cd02d-232"><em>ulUnused</em>: <strong>NULL</strong></span></span></p></li>
</ul>
<p><span data-ttu-id="cd02d-233">如果回呼傳回錯誤，則會忽略它。</span><span class="sxs-lookup"><span data-stu-id="cd02d-233">If an error is returned by the callback, it will be ignored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd02d-234">JET_cbtypFreeCursorLS</span><span class="sxs-lookup"><span data-stu-id="cd02d-234">JET_cbtypFreeCursorLS</span></span><br />
<span data-ttu-id="cd02d-235">0x00000200</span><span class="sxs-lookup"><span data-stu-id="cd02d-235">0x00000200</span></span></p></td>
<td><p><span data-ttu-id="cd02d-236">當應用程式需要清除與資料庫引擎所釋放之資料指標相關聯之本機儲存體的內容控制碼時，就會發生此回呼。</span><span class="sxs-lookup"><span data-stu-id="cd02d-236">This callback will occur when the application needs to clean up the context handle for the Local Storage associated with a cursor that is being released by the database engine.</span></span> <span data-ttu-id="cd02d-237">如需詳細資訊，請參閱 <a href="gg269243(v=exchg.10).md">JetSetLS</a>。</span><span class="sxs-lookup"><span data-stu-id="cd02d-237">For more information, see <a href="gg269243(v=exchg.10).md">JetSetLS</a>.</span></span></p>
<p><span data-ttu-id="cd02d-238">此回呼原因的函式指標是透過<a href="gg269310(v=exchg.10).md">JET_paramRuntimeCallback</a>的<a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a>來設定。</span><span class="sxs-lookup"><span data-stu-id="cd02d-238">The function pointer for this callback reason is configured by means of <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269310(v=exchg.10).md">JET_paramRuntimeCallback</a>.</span></span></p>
<p><span data-ttu-id="cd02d-239">回呼參數會有下列值：</span><span class="sxs-lookup"><span data-stu-id="cd02d-239">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="cd02d-240"><em>sesid</em>： JET_sesidNil</span><span class="sxs-lookup"><span data-stu-id="cd02d-240"><em>sesid</em>: JET_sesidNil</span></span></p></li>
<li><p><span data-ttu-id="cd02d-241"><em>dbid</em>： JET_dbidNil</span><span class="sxs-lookup"><span data-stu-id="cd02d-241"><em>dbid</em>: JET_dbidNil</span></span></p></li>
<li><p><span data-ttu-id="cd02d-242"><em>tableid</em>： JET_tableidNil</span><span class="sxs-lookup"><span data-stu-id="cd02d-242"><em>tableid</em>: JET_tableidNil</span></span></p></li>
<li><p><span data-ttu-id="cd02d-243"><em>pvArg1</em>：使用<a href="gg269243(v=exchg.10).md">JetSetLS</a>設定的內容控制碼</span><span class="sxs-lookup"><span data-stu-id="cd02d-243"><em>pvArg1</em>: The context handle set using <a href="gg269243(v=exchg.10).md">JetSetLS</a></span></span></p></li>
<li><p><span data-ttu-id="cd02d-244"><em>pvArg2</em>： <strong>Null</strong></span><span class="sxs-lookup"><span data-stu-id="cd02d-244"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="cd02d-245"><em>pvCoNtext</em>： <strong>Null</strong></span><span class="sxs-lookup"><span data-stu-id="cd02d-245"><em>pvContext</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="cd02d-246"><em>ulUnused</em>： <strong>Null</strong></span><span class="sxs-lookup"><span data-stu-id="cd02d-246"><em>ulUnused</em>: <strong>NULL</strong></span></span></p></li>
</ul>
<p><span data-ttu-id="cd02d-247">如果回呼傳回錯誤，則會忽略它。</span><span class="sxs-lookup"><span data-stu-id="cd02d-247">If an error is returned by the callback, it will be ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd02d-248">JET_cbtypFreeTableLS</span><span class="sxs-lookup"><span data-stu-id="cd02d-248">JET_cbtypFreeTableLS</span></span><br />
<span data-ttu-id="cd02d-249">0x00000400</span><span class="sxs-lookup"><span data-stu-id="cd02d-249">0x00000400</span></span></p></td>
<td><p><span data-ttu-id="cd02d-250">這項回呼的原因是，應用程式必須清除與資料庫引擎所釋放之資料表相關聯之本機儲存體的內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="cd02d-250">This callback will occur as the result of the need for the application to cleanup the context handle for the Local Storage associated with a table that is being released by the database engine.</span></span> <span data-ttu-id="cd02d-251">如需詳細資訊，請參閱 <a href="gg269243(v=exchg.10).md">JetSetLS</a>。</span><span class="sxs-lookup"><span data-stu-id="cd02d-251">For more information, see <a href="gg269243(v=exchg.10).md">JetSetLS</a>.</span></span></p>
<p><span data-ttu-id="cd02d-252">此回呼原因的函式指標是透過<a href="gg269310(v=exchg.10).md">JET_paramRuntimeCallback</a>的<a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a>來設定。</span><span class="sxs-lookup"><span data-stu-id="cd02d-252">The function pointer for this callback reason is configured by means of <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269310(v=exchg.10).md">JET_paramRuntimeCallback</a>.</span></span></p>
<p><span data-ttu-id="cd02d-253">回呼參數會有下列值：</span><span class="sxs-lookup"><span data-stu-id="cd02d-253">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="cd02d-254"><em>sesid</em>： JET_sesidNil</span><span class="sxs-lookup"><span data-stu-id="cd02d-254"><em>sesid</em>: JET_sesidNil</span></span></p></li>
<li><p><span data-ttu-id="cd02d-255"><em>dbid</em>： JET_dbidNil</span><span class="sxs-lookup"><span data-stu-id="cd02d-255"><em>dbid</em>: JET_dbidNil</span></span></p></li>
<li><p><span data-ttu-id="cd02d-256"><em>tableid</em>： JET_tableidNil</span><span class="sxs-lookup"><span data-stu-id="cd02d-256"><em>tableid</em>: JET_tableidNil</span></span></p></li>
<li><p><span data-ttu-id="cd02d-257"><em>pvArg1</em>：使用 <a href="gg269243(v=exchg.10).md">JetSetLS</a>設定的內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="cd02d-257"><em>pvArg1</em>: The context handle set using <a href="gg269243(v=exchg.10).md">JetSetLS</a>.</span></span></p></li>
<li><p><span data-ttu-id="cd02d-258"><em>pvArg2</em>： <strong>Null</strong></span><span class="sxs-lookup"><span data-stu-id="cd02d-258"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="cd02d-259"><em>pvCoNtext</em>： <strong>Null</strong></span><span class="sxs-lookup"><span data-stu-id="cd02d-259"><em>pvContext</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="cd02d-260"><em>ulUnused</em>： <strong>Null</strong></span><span class="sxs-lookup"><span data-stu-id="cd02d-260"><em>ulUnused</em>: <strong>NULL</strong></span></span></p></li>
</ul>
<p><span data-ttu-id="cd02d-261">如果回呼傳回錯誤，則會忽略它。</span><span class="sxs-lookup"><span data-stu-id="cd02d-261">If an error is returned by the callback, it will be ignored.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="cd02d-262">規格需求</span><span class="sxs-lookup"><span data-stu-id="cd02d-262">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd02d-263"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="cd02d-263"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="cd02d-264">需要 Windows Vista 或 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="cd02d-264">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd02d-265"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="cd02d-265"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="cd02d-266">需要 Windows Server 2008 或 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="cd02d-266">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd02d-267"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="cd02d-267"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="cd02d-268">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="cd02d-268">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="cd02d-269">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cd02d-269">See Also</span></span>

[<span data-ttu-id="cd02d-270">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="cd02d-270">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)
