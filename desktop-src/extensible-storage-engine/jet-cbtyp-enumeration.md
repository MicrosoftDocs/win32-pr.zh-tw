---
description: 深入瞭解： JET_cbtyp 列舉
title: JET_cbtyp 列舉
TOCTitle: JET_cbtyp enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_cbtyp
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_cbtyp(v=EXCHG.10)
ms:contentKeyID: 39511758
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeDelete
- Microsoft.Isam.Esent.Interop.JET_cbtyp.Finalize
- Microsoft.Isam.Esent.Interop.JET_cbtyp.OnlineDefragCompleted
- Microsoft.Isam.Esent.Interop.JET_cbtyp.UserDefinedDefaultValue
- Microsoft.Isam.Esent.Interop.JET_cbtyp
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterDelete
- Microsoft.Isam.Esent.Interop.JET_cbtyp.FreeCursorLS
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterReplace
- Microsoft.Isam.Esent.Interop.JET_cbtyp.FreeTableLS
- Microsoft.Isam.Esent.Interop.JET_cbtyp.Null
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeReplace
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeInsert
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterInsert
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeReplace
- Microsoft.Isam.Esent.Interop.JET_cbtyp.FreeCursorLS
- Microsoft.Isam.Esent.Interop.JET_cbtyp.FreeTableLS
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeDelete
- Microsoft.Isam.Esent.Interop.JET_cbtyp.Null
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterReplace
- Microsoft.Isam.Esent.Interop.JET_cbtyp
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterDelete
- Microsoft.Isam.Esent.Interop.JET_cbtyp.OnlineDefragCompleted
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterInsert
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeInsert
- Microsoft.Isam.Esent.Interop.JET_cbtyp.Finalize
- Microsoft.Isam.Esent.Interop.JET_cbtyp.UserDefinedDefaultValue
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3d2e545fea9c1942dc09df82eb93eafa1d3e4e89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976770"
---
# <a name="jet_cbtyp-enumeration"></a><span data-ttu-id="0dd0d-103">JET_cbtyp 列舉</span><span class="sxs-lookup"><span data-stu-id="0dd0d-103">JET_cbtyp enumeration</span></span>

<span data-ttu-id="0dd0d-104">要報告的進度類型。</span><span class="sxs-lookup"><span data-stu-id="0dd0d-104">Type of progress being reported.</span></span>

<span data-ttu-id="0dd0d-105">此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。</span><span class="sxs-lookup"><span data-stu-id="0dd0d-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="0dd0d-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0dd0d-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0dd0d-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="0dd0d-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0dd0d-108">語法</span><span class="sxs-lookup"><span data-stu-id="0dd0d-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration JET_cbtyp
'Usage
Dim instance As JET_cbtyp
```

``` csharp
[FlagsAttribute]
public enum JET_cbtyp
```

## <a name="members"></a><span data-ttu-id="0dd0d-109">成員</span><span class="sxs-lookup"><span data-stu-id="0dd0d-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="0dd0d-110">成員名稱</span><span class="sxs-lookup"><span data-stu-id="0dd0d-110">Member name</span></span></th>
<th><span data-ttu-id="0dd0d-111">說明</span><span class="sxs-lookup"><span data-stu-id="0dd0d-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="0dd0d-112">Null</span><span class="sxs-lookup"><span data-stu-id="0dd0d-112">Null</span></span></td>
<td><span data-ttu-id="0dd0d-113">這是保留的回呼，而且一律視為無效。</span><span class="sxs-lookup"><span data-stu-id="0dd0d-113">This callback is reserved and always considered invalid.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="0dd0d-114">定案</span><span class="sxs-lookup"><span data-stu-id="0dd0d-114">Finalize</span></span></td>
<td><span data-ttu-id="0dd0d-115">可結束的資料行已離開零。</span><span class="sxs-lookup"><span data-stu-id="0dd0d-115">A finalizable column has gone to zero.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="0dd0d-116">BeforeInsert</span><span class="sxs-lookup"><span data-stu-id="0dd0d-116">BeforeInsert</span></span></td>
<td><span data-ttu-id="0dd0d-117">這項回呼會在透過呼叫 JetUpdate 將新的記錄插入資料表之前進行。</span><span class="sxs-lookup"><span data-stu-id="0dd0d-117">This callback will occur just before a new record is inserted into a table by a call to JetUpdate.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="0dd0d-118">AfterInsert</span><span class="sxs-lookup"><span data-stu-id="0dd0d-118">AfterInsert</span></span></td>
<td><span data-ttu-id="0dd0d-119">只要呼叫 JetUpdate，但在 JetUpdate 傳回之前，會將新的記錄插入資料表中，就會發生此回呼。</span><span class="sxs-lookup"><span data-stu-id="0dd0d-119">This callback will occur just after a new record has been inserted into a table by a call to JetUpdate but before JetUpdate returns.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="0dd0d-120">BeforeReplace</span><span class="sxs-lookup"><span data-stu-id="0dd0d-120">BeforeReplace</span></span></td>
<td><span data-ttu-id="0dd0d-121">這項回呼會在 JetUpdate 的呼叫變更資料表中的現有記錄之前發生。</span><span class="sxs-lookup"><span data-stu-id="0dd0d-121">This callback will occur just prior to an existing record in a table being changed by a call to JetUpdate.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="0dd0d-122">AfterReplace</span><span class="sxs-lookup"><span data-stu-id="0dd0d-122">AfterReplace</span></span></td>
<td><span data-ttu-id="0dd0d-123">這項回呼將會在資料表中的現有記錄已由呼叫 JetUpdate，但在 JetUpdate 傳回之前變更。</span><span class="sxs-lookup"><span data-stu-id="0dd0d-123">This callback will occur just after an existing record in a table has been changed by a call to JetUpdate but prior to JetUpdate returning.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="0dd0d-124">BeforeDelete</span><span class="sxs-lookup"><span data-stu-id="0dd0d-124">BeforeDelete</span></span></td>
<td><span data-ttu-id="0dd0d-125">這項回呼會在呼叫 JetDelete 來刪除資料表中的現有記錄之前發生。</span><span class="sxs-lookup"><span data-stu-id="0dd0d-125">This callback will occur just before an existing record in a table is deleted by a call to JetDelete.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="0dd0d-126">AfterDelete</span><span class="sxs-lookup"><span data-stu-id="0dd0d-126">AfterDelete</span></span></td>
<td><span data-ttu-id="0dd0d-127">這項回呼會在 JetDelete 的呼叫刪除資料表中的現有記錄之後發生。</span><span class="sxs-lookup"><span data-stu-id="0dd0d-127">This callback will occur just after an existing record in a table is deleted by a call to JetDelete.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="0dd0d-128">UserDefinedDefaultValue</span><span class="sxs-lookup"><span data-stu-id="0dd0d-128">UserDefinedDefaultValue</span></span></td>
<td><span data-ttu-id="0dd0d-129">當引擎需要從應用程式取得使用者定義的資料行預設值時，就會發生此回呼。</span><span class="sxs-lookup"><span data-stu-id="0dd0d-129">This callback will occur when the engine needs to retrieve the user defined default value of a column from the application.</span></span> <span data-ttu-id="0dd0d-130">此回呼基本上是由應用程式評估的 JetRetrieveColumn 有限實作為。</span><span class="sxs-lookup"><span data-stu-id="0dd0d-130">This callback is essentially a limited implementation of JetRetrieveColumn that is evaluated by the application.</span></span> <span data-ttu-id="0dd0d-131">最多可以針對使用者定義的預設值傳回一個資料行值。</span><span class="sxs-lookup"><span data-stu-id="0dd0d-131">A maximum of one column value can be returned for a user defined default value.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="0dd0d-132">OnlineDefragCompleted</span><span class="sxs-lookup"><span data-stu-id="0dd0d-132">OnlineDefragCompleted</span></span></td>
<td><span data-ttu-id="0dd0d-133">當 JetDefragment 所起始的資料庫線上磁碟重組已停止，因為進程已完成或達到時間限制時，就會發生此回呼。</span><span class="sxs-lookup"><span data-stu-id="0dd0d-133">This callback will occur when the online defragmentation of a database as initiated by JetDefragment has stopped due to either the process being completed or the time limit being reached.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="0dd0d-134">FreeCursorLS</span><span class="sxs-lookup"><span data-stu-id="0dd0d-134">FreeCursorLS</span></span></td>
<td><span data-ttu-id="0dd0d-135">當應用程式需要清除與資料庫引擎所釋放之資料指標相關聯之本機儲存體的內容控制碼時，就會發生此回呼。</span><span class="sxs-lookup"><span data-stu-id="0dd0d-135">This callback will occur when the application needs to clean up the context handle for the Local Storage associated with a cursor that is being released by the database engine.</span></span> <span data-ttu-id="0dd0d-136">如需詳細資訊，請參閱 JetSetLS。</span><span class="sxs-lookup"><span data-stu-id="0dd0d-136">For more information, see JetSetLS.</span></span> <span data-ttu-id="0dd0d-137">此回呼原因的委派是透過 JET_paramRuntimeCallback 的 JetSetSystemParameter 來設定。</span><span class="sxs-lookup"><span data-stu-id="0dd0d-137">The delegate for this callback reason is configured by means of JetSetSystemParameter with JET_paramRuntimeCallback.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="0dd0d-138">FreeTableLS</span><span class="sxs-lookup"><span data-stu-id="0dd0d-138">FreeTableLS</span></span></td>
<td><span data-ttu-id="0dd0d-139">這項回呼的原因是，應用程式必須清除與資料庫引擎所釋放之資料表相關聯之本機儲存體的內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="0dd0d-139">This callback will occur as the result of the need for the application to cleanup the context handle for the Local Storage associated with a table that is being released by the database engine.</span></span> <span data-ttu-id="0dd0d-140">如需詳細資訊，請參閱 JetSetLS。</span><span class="sxs-lookup"><span data-stu-id="0dd0d-140">For more information, see JetSetLS.</span></span> <span data-ttu-id="0dd0d-141">此回呼原因的委派是透過 JET_paramRuntimeCallback 的 JetSetSystemParameter 來設定。</span><span class="sxs-lookup"><span data-stu-id="0dd0d-141">The delegate for this callback reason is configured by means of JetSetSystemParameter with JET_paramRuntimeCallback.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="0dd0d-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0dd0d-142">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0dd0d-143">參考</span><span class="sxs-lookup"><span data-stu-id="0dd0d-143">Reference</span></span>

[<span data-ttu-id="0dd0d-144">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="0dd0d-144">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
