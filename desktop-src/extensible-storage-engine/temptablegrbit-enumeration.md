---
description: 深入瞭解： TempTableGrbit 列舉
title: TempTableGrbit 列舉
TOCTitle: TempTableGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.TempTableGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.temptablegrbit(v=EXCHG.10)
ms:contentKeyID: 39515065
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.TempTableGrbit
- Microsoft.Isam.Esent.Interop.TempTableGrbit.ErrorOnDuplicateInsertion
- Microsoft.Isam.Esent.Interop.TempTableGrbit.None
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Unique
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Updatable
- Microsoft.Isam.Esent.Interop.TempTableGrbit.SortNullsHigh
- Microsoft.Isam.Esent.Interop.TempTableGrbit.ForceMaterialization
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Indexed
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Scrollable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.TempTableGrbit.ErrorOnDuplicateInsertion
- Microsoft.Isam.Esent.Interop.TempTableGrbit.None
- Microsoft.Isam.Esent.Interop.TempTableGrbit
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Indexed
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Updatable
- Microsoft.Isam.Esent.Interop.TempTableGrbit.ForceMaterialization
- Microsoft.Isam.Esent.Interop.TempTableGrbit.SortNullsHigh
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Scrollable
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Unique
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 79247bac6e8d3bda9d1aeac4d19b7af894201a57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989909"
---
# <a name="temptablegrbit-enumeration"></a><span data-ttu-id="1132f-103">TempTableGrbit 列舉</span><span class="sxs-lookup"><span data-stu-id="1132f-103">TempTableGrbit enumeration</span></span>

<span data-ttu-id="1132f-104">建立臨時表的選項。</span><span class="sxs-lookup"><span data-stu-id="1132f-104">Options for temporary table creation.</span></span>

<span data-ttu-id="1132f-105">此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。</span><span class="sxs-lookup"><span data-stu-id="1132f-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="1132f-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1132f-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1132f-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="1132f-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1132f-108">語法</span><span class="sxs-lookup"><span data-stu-id="1132f-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration TempTableGrbit
'Usage
Dim instance As TempTableGrbit
```

``` csharp
[FlagsAttribute]
public enum TempTableGrbit
```

## <a name="members"></a><span data-ttu-id="1132f-109">成員</span><span class="sxs-lookup"><span data-stu-id="1132f-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="1132f-110">成員名稱</span><span class="sxs-lookup"><span data-stu-id="1132f-110">Member name</span></span></th>
<th><span data-ttu-id="1132f-111">描述</span><span class="sxs-lookup"><span data-stu-id="1132f-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="1132f-112">無</span><span class="sxs-lookup"><span data-stu-id="1132f-112">None</span></span></td>
<td><span data-ttu-id="1132f-113">預設選項。</span><span class="sxs-lookup"><span data-stu-id="1132f-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="1132f-114">索引</span><span class="sxs-lookup"><span data-stu-id="1132f-114">Indexed</span></span></td>
<td><span data-ttu-id="1132f-115">此選項會要求臨時表具有足夠的彈性，可允許使用 JetSeek 依索引鍵查閱記錄。</span><span class="sxs-lookup"><span data-stu-id="1132f-115">This option requests that the temporary table be flexible enough to permit the use of JetSeek to lookup records by index key.</span></span> <span data-ttu-id="1132f-116">如果這項功能不是必要的，則最好不要要求它。</span><span class="sxs-lookup"><span data-stu-id="1132f-116">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="1132f-117">如果未要求這項功能，則臨時表管理員可能會選擇管理臨時表的策略，而這會導致效能改進。</span><span class="sxs-lookup"><span data-stu-id="1132f-117">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="1132f-118">唯一</span><span class="sxs-lookup"><span data-stu-id="1132f-118">Unique</span></span></td>
<td><span data-ttu-id="1132f-119">此選項會要求從臨時表的最後一組記錄中，移除具有重複索引鍵的記錄。</span><span class="sxs-lookup"><span data-stu-id="1132f-119">This option requests that records with duplicate index keys be removed from the final set of records in the temporary table.</span></span> <span data-ttu-id="1132f-120">在 Windows Server 2003 之前，資料庫引擎一律會假設這個選項有作用，因為所有叢集索引也必須是主鍵，因此必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="1132f-120">Prior to Windows Server 2003, the database engine always assumed this option to be in effect due to the fact that all clustered indexes must also be a primary key and thus must be unique.</span></span> <span data-ttu-id="1132f-121">從 Windows Server 2003 開始，現在也可以在指定 <a href="dn351284(v=exchg.10).md">ForwardOnly</a> 選項時，建立不會移除重複專案的臨時表。</span><span class="sxs-lookup"><span data-stu-id="1132f-121">As of Windows Server 2003, it is now possible to create a temporary table that does NOT remove duplicates when the <a href="dn351284(v=exchg.10).md">ForwardOnly</a> option is also specified.</span></span> <span data-ttu-id="1132f-122">您無法知道哪些重複專案會獲勝，哪些重複專案會在一般情況下捨棄。</span><span class="sxs-lookup"><span data-stu-id="1132f-122">It is not possible to know which duplicate will win and which duplicates will be discarded in general.</span></span> <span data-ttu-id="1132f-123">不過，當要求 ErrorOnDuplicateInsertion 選項時，會永遠贏得具有指定索引鍵的第一個記錄插入臨時表中。</span><span class="sxs-lookup"><span data-stu-id="1132f-123">However, when the ErrorOnDuplicateInsertion option is requested then the first record with a given index key to be inserted into the temporary table will always win.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="1132f-124">可更新</span><span class="sxs-lookup"><span data-stu-id="1132f-124">Updatable</span></span></td>
<td><span data-ttu-id="1132f-125">此選項會要求臨時表具有足夠的彈性，可讓之前插入的記錄之後變更。</span><span class="sxs-lookup"><span data-stu-id="1132f-125">This option requests that the temporary table be flexible enough to allow records that have previously been inserted to be subsequently changed.</span></span> <span data-ttu-id="1132f-126">如果這項功能不是必要的，則最好不要要求它。</span><span class="sxs-lookup"><span data-stu-id="1132f-126">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="1132f-127">如果未要求這項功能，則臨時表管理員可能會選擇管理臨時表的策略，而這會導致效能改進。</span><span class="sxs-lookup"><span data-stu-id="1132f-127">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="1132f-128">可捲動</span><span class="sxs-lookup"><span data-stu-id="1132f-128">Scrollable</span></span></td>
<td><span data-ttu-id="1132f-129">此選項會要求臨時表具有足夠的彈性，可讓您使用 <a href="dn292217(v=exchg.10).md">JetMove (JET_SESID、JET_TABLEID、Int32、MoveGrbit) </a>，以任意順序和方向來掃描記錄。</span><span class="sxs-lookup"><span data-stu-id="1132f-129">This option requests that the temporary table be flexible enough to allow records to be scanned in arbitrary order and direction using <a href="dn292217(v=exchg.10).md">JetMove(JET_SESID, JET_TABLEID, Int32, MoveGrbit)</a>.</span></span> <span data-ttu-id="1132f-130">如果這項功能不是必要的，則最好不要要求它。</span><span class="sxs-lookup"><span data-stu-id="1132f-130">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="1132f-131">如果未要求這項功能，則臨時表管理員可能會選擇管理臨時表的策略，而這會導致效能改進。</span><span class="sxs-lookup"><span data-stu-id="1132f-131">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="1132f-132">SortNullsHigh</span><span class="sxs-lookup"><span data-stu-id="1132f-132">SortNullsHigh</span></span></td>
<td><span data-ttu-id="1132f-133">此選項會要求 Null 索引鍵資料行值的排序比非 Null 索引鍵資料行值更接近索引的結尾。</span><span class="sxs-lookup"><span data-stu-id="1132f-133">This option requests that NULL key column values sort closer to the end of the index than non-NULL key column values.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="1132f-134">ForceMaterialization</span><span class="sxs-lookup"><span data-stu-id="1132f-134">ForceMaterialization</span></span></td>
<td><span data-ttu-id="1132f-135">此選項會強制臨時表管理員放棄任何嘗試選擇聰明的策略來管理臨時表，以產生增強的效能。</span><span class="sxs-lookup"><span data-stu-id="1132f-135">This option forces the temporary table manager to abandon any attempt to choose a clever strategy for managing the temporary table that will result in enhanced performance.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="1132f-136">ErrorOnDuplicateInsertion</span><span class="sxs-lookup"><span data-stu-id="1132f-136">ErrorOnDuplicateInsertion</span></span></td>
<td><span data-ttu-id="1132f-137">此選項會要求任何嘗試使用與先前所插入記錄相同的索引鍵來插入記錄，將會立即失敗，並出現 <a href="hh564840(v=exchg.10).md">KeyDuplicate</a>。</span><span class="sxs-lookup"><span data-stu-id="1132f-137">This option requests that any attempt to insert a record with the same index key as a previously inserted record will immediately fail with <a href="hh564840(v=exchg.10).md">KeyDuplicate</a>.</span></span> <span data-ttu-id="1132f-138">如果未要求這個選項，則可能會立即偵測到重複的情況，也可能會在稍後根據資料庫引擎根據所要求的功能來執行臨時表所選擇的策略，而失敗或以無訊息方式移除。</span><span class="sxs-lookup"><span data-stu-id="1132f-138">If this option is not requested then a duplicate may be detected immediately and fail or may be silently removed later depending on the strategy chosen by the database engine to implement the temporary table based on the requested functionality.</span></span> <span data-ttu-id="1132f-139">如果這項功能不是必要的，則最好不要要求它。</span><span class="sxs-lookup"><span data-stu-id="1132f-139">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="1132f-140">如果未要求這項功能，則臨時表管理員可能會選擇管理臨時表的策略，而這會導致效能改進。</span><span class="sxs-lookup"><span data-stu-id="1132f-140">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="1132f-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1132f-141">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1132f-142">參考</span><span class="sxs-lookup"><span data-stu-id="1132f-142">Reference</span></span>

[<span data-ttu-id="1132f-143">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="1132f-143">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

[<span data-ttu-id="1132f-144">ForwardOnly</span><span class="sxs-lookup"><span data-stu-id="1132f-144">ForwardOnly</span></span>](./server2003grbits.forwardonly-field.md)

[<span data-ttu-id="1132f-145">IntrinsicLVsOnly</span><span class="sxs-lookup"><span data-stu-id="1132f-145">IntrinsicLVsOnly</span></span>](./windows7grbits.intrinsiclvsonly-field.md)
