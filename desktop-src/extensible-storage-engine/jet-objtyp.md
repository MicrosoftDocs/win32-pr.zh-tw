---
description: 深入瞭解： JET_OBJTYP
title: JET_OBJTYP
TOCTitle: JET_OBJTYP
ms:assetid: 7f549c84-584b-42b6-a4a5-385cf6dc25df
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269312(v=EXCHG.10)
ms:contentKeyID: 32765602
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
ms.openlocfilehash: b4366c8fdac3d94ef65006adb0fd3e869832cdf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321151"
---
# <a name="jet_objtyp"></a><span data-ttu-id="2466a-103">JET_OBJTYP</span><span class="sxs-lookup"><span data-stu-id="2466a-103">JET_OBJTYP</span></span>


<span data-ttu-id="2466a-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="2466a-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_objtyp"></a><span data-ttu-id="2466a-105">JET_OBJTYP</span><span class="sxs-lookup"><span data-stu-id="2466a-105">JET_OBJTYP</span></span>

<span data-ttu-id="2466a-106">**JET_OBJTYP** 的常數群組代表資料庫物件的型別。</span><span class="sxs-lookup"><span data-stu-id="2466a-106">The **JET_OBJTYP** group of constants represent the type of a database object.</span></span> <span data-ttu-id="2466a-107">目前只支援資料表。</span><span class="sxs-lookup"><span data-stu-id="2466a-107">Currently, only tables are supported.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2466a-108">常數/值</span><span class="sxs-lookup"><span data-stu-id="2466a-108">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="2466a-109">Description</span><span class="sxs-lookup"><span data-stu-id="2466a-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2466a-110">JET_objtypNil</span><span class="sxs-lookup"><span data-stu-id="2466a-110">JET_objtypNil</span></span><br />
<span data-ttu-id="2466a-111">0</span><span class="sxs-lookup"><span data-stu-id="2466a-111">0</span></span></p></td>
<td><p><span data-ttu-id="2466a-112">代表所有類型的物件。</span><span class="sxs-lookup"><span data-stu-id="2466a-112">Represents all types of objects.</span></span> <span data-ttu-id="2466a-113">目前只支援資料表。</span><span class="sxs-lookup"><span data-stu-id="2466a-113">Currently, only tables are supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2466a-114">JET_objtypTable</span><span class="sxs-lookup"><span data-stu-id="2466a-114">JET_objtypTable</span></span><br />
<span data-ttu-id="2466a-115">1</span><span class="sxs-lookup"><span data-stu-id="2466a-115">1</span></span></p></td>
<td><p><span data-ttu-id="2466a-116">表示資料表。</span><span class="sxs-lookup"><span data-stu-id="2466a-116">Represents a table.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="2466a-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="2466a-117">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2466a-118"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="2466a-118"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="2466a-119">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="2466a-119">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2466a-120"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="2466a-120"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="2466a-121">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="2466a-121">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2466a-122"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="2466a-122"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="2466a-123">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="2466a-123">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

