---
description: 深入瞭解： RetrieveColumnGrbit 列舉
title: RetrieveColumnGrbit 列舉
TOCTitle: RetrieveColumnGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.retrievecolumngrbit(v=EXCHG.10)
ms:contentKeyID: 39511391
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.None
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromPrimaryBookmark
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveCopy
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromIndex
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveNull
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveIgnoreDefault
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveTag
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromIndex
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveCopy
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveNull
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.None
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromPrimaryBookmark
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveIgnoreDefault
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveTag
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a223a288b8ad2d2e976be3bb9f2f524f78b9a8fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979184"
---
# <a name="retrievecolumngrbit-enumeration"></a><span data-ttu-id="4e86f-103">RetrieveColumnGrbit 列舉</span><span class="sxs-lookup"><span data-stu-id="4e86f-103">RetrieveColumnGrbit enumeration</span></span>

<span data-ttu-id="4e86f-104">JetRetrieveColumn 的選項。</span><span class="sxs-lookup"><span data-stu-id="4e86f-104">Options for JetRetrieveColumn.</span></span>

<span data-ttu-id="4e86f-105">此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。</span><span class="sxs-lookup"><span data-stu-id="4e86f-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="4e86f-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4e86f-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4e86f-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="4e86f-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4e86f-108">語法</span><span class="sxs-lookup"><span data-stu-id="4e86f-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration RetrieveColumnGrbit
'Usage
Dim instance As RetrieveColumnGrbit
```

``` csharp
[FlagsAttribute]
public enum RetrieveColumnGrbit
```

## <a name="members"></a><span data-ttu-id="4e86f-109">成員</span><span class="sxs-lookup"><span data-stu-id="4e86f-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="4e86f-110">成員名稱</span><span class="sxs-lookup"><span data-stu-id="4e86f-110">Member name</span></span></th>
<th><span data-ttu-id="4e86f-111">描述</span><span class="sxs-lookup"><span data-stu-id="4e86f-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="4e86f-112">無</span><span class="sxs-lookup"><span data-stu-id="4e86f-112">None</span></span></td>
<td><span data-ttu-id="4e86f-113">預設選項。</span><span class="sxs-lookup"><span data-stu-id="4e86f-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="4e86f-114">RetrieveCopy</span><span class="sxs-lookup"><span data-stu-id="4e86f-114">RetrieveCopy</span></span></td>
<td><span data-ttu-id="4e86f-115">此旗標會使抓取資料行抓取修改過的值，而不是原始的值。</span><span class="sxs-lookup"><span data-stu-id="4e86f-115">This flag causes retrieve column to retrieve the modified value instead of the original value.</span></span> <span data-ttu-id="4e86f-116">如果尚未修改此值，則會取出原始值。</span><span class="sxs-lookup"><span data-stu-id="4e86f-116">If the value has not been modified, then the original value is retrieved.</span></span> <span data-ttu-id="4e86f-117">如此一來，在插入或更新記錄的作業期間，可能會取出尚未插入或更新的值。</span><span class="sxs-lookup"><span data-stu-id="4e86f-117">In this way, a value that has not yet been inserted or updated may be retrieved during the operation of inserting or updating a record.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="4e86f-118">RetrieveFromIndex</span><span class="sxs-lookup"><span data-stu-id="4e86f-118">RetrieveFromIndex</span></span></td>
<td><span data-ttu-id="4e86f-119">此選項可用來從索引取出資料行值（如果可能的話），而不需要存取記錄。</span><span class="sxs-lookup"><span data-stu-id="4e86f-119">This option is used to retrieve column values from the index, if possible, without accessing the record.</span></span> <span data-ttu-id="4e86f-120">如此一來，當索引項目本身有需要的資料時，就可以避免不必要的記錄載入。</span><span class="sxs-lookup"><span data-stu-id="4e86f-120">In this way, unnecessary loading of records can be avoided when needed data is available from index entries themselves.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="4e86f-121">RetrieveFromPrimaryBookmark</span><span class="sxs-lookup"><span data-stu-id="4e86f-121">RetrieveFromPrimaryBookmark</span></span></td>
<td><span data-ttu-id="4e86f-122">此選項是用來從索引書簽中取出資料行值，而且當資料行同時出現在主要索引和目前索引中時，可能會與索引值不同。</span><span class="sxs-lookup"><span data-stu-id="4e86f-122">This option is used to retrieve column values from the index bookmark, and may differ from the index value when a column appears both in the primary index and the current index.</span></span> <span data-ttu-id="4e86f-123">如果目前的索引是叢集或主要索引，則不應指定此選項。</span><span class="sxs-lookup"><span data-stu-id="4e86f-123">This option should not be specified if the current index is the clustered, or primary, index.</span></span> <span data-ttu-id="4e86f-124">如果也設定了 RetrieveFromIndex，則無法設定此位。</span><span class="sxs-lookup"><span data-stu-id="4e86f-124">This bit cannot be set if RetrieveFromIndex is also set.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="4e86f-125">RetrieveTag</span><span class="sxs-lookup"><span data-stu-id="4e86f-125">RetrieveTag</span></span></td>
<td><span data-ttu-id="4e86f-126">此選項可用來在 JET_RETINFO itagSequence 中取出多重值資料行值的序號。</span><span class="sxs-lookup"><span data-stu-id="4e86f-126">This option is used to retrieve the sequence number of a multi-valued column value in JET_RETINFO.itagSequence.</span></span> <span data-ttu-id="4e86f-127">抓取序號可能是成本高昂的作業，而且只在必要時才執行。</span><span class="sxs-lookup"><span data-stu-id="4e86f-127">Retrieving the sequence number can be a costly operation and should only be done if necessary.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="4e86f-128">RetrieveNull</span><span class="sxs-lookup"><span data-stu-id="4e86f-128">RetrieveNull</span></span></td>
<td><span data-ttu-id="4e86f-129">此選項可用來取出多值資料行 Null 值。</span><span class="sxs-lookup"><span data-stu-id="4e86f-129">This option is used to retrieve multi-valued column NULL values.</span></span> <span data-ttu-id="4e86f-130">如果未指定此選項，則會自動略過多重值資料行的 Null 值。</span><span class="sxs-lookup"><span data-stu-id="4e86f-130">If this option is not specified, multi-valued column NULL values will automatically be skipped.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="4e86f-131">RetrieveIgnoreDefault</span><span class="sxs-lookup"><span data-stu-id="4e86f-131">RetrieveIgnoreDefault</span></span></td>
<td><span data-ttu-id="4e86f-132">此選項只會影響多重值資料行，而且當要求的序號為1，而且記錄中的資料行沒有設定值時，就會傳回 Null 值。</span><span class="sxs-lookup"><span data-stu-id="4e86f-132">This option affects only multi-valued columns and causes a NULL value to be returned when the requested sequence number is 1 and there are no set values for the column in the record.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="4e86f-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4e86f-133">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4e86f-134">參考</span><span class="sxs-lookup"><span data-stu-id="4e86f-134">Reference</span></span>

[<span data-ttu-id="4e86f-135">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="4e86f-135">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
