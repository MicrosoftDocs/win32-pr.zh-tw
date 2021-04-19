---
description: 深入瞭解： ObjectInfoGrbit 列舉
title: ObjectInfoGrbit 列舉
TOCTitle: ObjectInfoGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.ObjectInfoGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.objectinfogrbit(v=EXCHG.10)
ms:contentKeyID: 39516208
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit.Bookmark
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit.Rollback
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit.Updatable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit.Bookmark
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit.Rollback
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit.Updatable
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4028a2a337b32394029960e45bb0e485c2b6b705
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980889"
---
# <a name="objectinfogrbit-enumeration"></a><span data-ttu-id="20d7e-103">ObjectInfoGrbit 列舉</span><span class="sxs-lookup"><span data-stu-id="20d7e-103">ObjectInfoGrbit enumeration</span></span>

<span data-ttu-id="20d7e-104">[JET_OBJECTINFO](./jet-objectinfo-class.md)中使用的資料表選項。</span><span class="sxs-lookup"><span data-stu-id="20d7e-104">Table options, used in [JET_OBJECTINFO](./jet-objectinfo-class.md).</span></span>

<span data-ttu-id="20d7e-105">此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。</span><span class="sxs-lookup"><span data-stu-id="20d7e-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="20d7e-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="20d7e-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="20d7e-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="20d7e-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="20d7e-108">語法</span><span class="sxs-lookup"><span data-stu-id="20d7e-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration ObjectInfoGrbit
'Usage
Dim instance As ObjectInfoGrbit
```

``` csharp
[FlagsAttribute]
public enum ObjectInfoGrbit
```

## <a name="members"></a><span data-ttu-id="20d7e-109">成員</span><span class="sxs-lookup"><span data-stu-id="20d7e-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="20d7e-110">成員名稱</span><span class="sxs-lookup"><span data-stu-id="20d7e-110">Member name</span></span></th>
<th><span data-ttu-id="20d7e-111">說明</span><span class="sxs-lookup"><span data-stu-id="20d7e-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="20d7e-112">書籤</span><span class="sxs-lookup"><span data-stu-id="20d7e-112">Bookmark</span></span></td>
<td><span data-ttu-id="20d7e-113">資料表可以有書簽。</span><span class="sxs-lookup"><span data-stu-id="20d7e-113">The table can have bookmarks.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="20d7e-114">復原</span><span class="sxs-lookup"><span data-stu-id="20d7e-114">Rollback</span></span></td>
<td><span data-ttu-id="20d7e-115">資料表可以復原。</span><span class="sxs-lookup"><span data-stu-id="20d7e-115">The table can be rolled back.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="20d7e-116">可更新</span><span class="sxs-lookup"><span data-stu-id="20d7e-116">Updatable</span></span></td>
<td><span data-ttu-id="20d7e-117">您可以更新資料表。</span><span class="sxs-lookup"><span data-stu-id="20d7e-117">The table can be updated.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="20d7e-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="20d7e-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="20d7e-119">參考</span><span class="sxs-lookup"><span data-stu-id="20d7e-119">Reference</span></span>

[<span data-ttu-id="20d7e-120">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="20d7e-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
