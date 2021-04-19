---
description: 深入瞭解： DeleteColumnGrbit 列舉
title: DeleteColumnGrbit 列舉
TOCTitle: DeleteColumnGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.DeleteColumnGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.deletecolumngrbit(v=EXCHG.10)
ms:contentKeyID: 39512792
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.DeleteColumnGrbit
- Microsoft.Isam.Esent.Interop.DeleteColumnGrbit.IgnoreTemplateColumns
- Microsoft.Isam.Esent.Interop.DeleteColumnGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.DeleteColumnGrbit
- Microsoft.Isam.Esent.Interop.DeleteColumnGrbit.None
- Microsoft.Isam.Esent.Interop.DeleteColumnGrbit.IgnoreTemplateColumns
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3191d3c73883d0bd27b4944718f2a0b3423e2c8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977181"
---
# <a name="deletecolumngrbit-enumeration"></a><span data-ttu-id="cb764-103">DeleteColumnGrbit 列舉</span><span class="sxs-lookup"><span data-stu-id="cb764-103">DeleteColumnGrbit enumeration</span></span>

<span data-ttu-id="cb764-104">[JetDeleteColumn2 (JET_SESID、JET_TABLEID、String、DeleteColumnGrbit) ](./api.jetdeletecolumn2-method.md)的選項。</span><span class="sxs-lookup"><span data-stu-id="cb764-104">Options for [JetDeleteColumn2(JET_SESID, JET_TABLEID, String, DeleteColumnGrbit)](./api.jetdeletecolumn2-method.md).</span></span>

<span data-ttu-id="cb764-105">此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。</span><span class="sxs-lookup"><span data-stu-id="cb764-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="cb764-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="cb764-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="cb764-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="cb764-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="cb764-108">語法</span><span class="sxs-lookup"><span data-stu-id="cb764-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration DeleteColumnGrbit
'Usage
Dim instance As DeleteColumnGrbit
```

``` csharp
[FlagsAttribute]
public enum DeleteColumnGrbit
```

## <a name="members"></a><span data-ttu-id="cb764-109">成員</span><span class="sxs-lookup"><span data-stu-id="cb764-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="cb764-110">成員名稱</span><span class="sxs-lookup"><span data-stu-id="cb764-110">Member name</span></span></th>
<th><span data-ttu-id="cb764-111">描述</span><span class="sxs-lookup"><span data-stu-id="cb764-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="cb764-112">無</span><span class="sxs-lookup"><span data-stu-id="cb764-112">None</span></span></td>
<td><span data-ttu-id="cb764-113">預設選項。</span><span class="sxs-lookup"><span data-stu-id="cb764-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="cb764-114">IgnoreTemplateColumns</span><span class="sxs-lookup"><span data-stu-id="cb764-114">IgnoreTemplateColumns</span></span></td>
<td><span data-ttu-id="cb764-115">API 應該只會嘗試刪除衍生資料表中的資料行。</span><span class="sxs-lookup"><span data-stu-id="cb764-115">The API should only attempt to delete columns in the derived table.</span></span> <span data-ttu-id="cb764-116">如果基表中有該名稱的資料行，則會忽略該名稱的資料行。</span><span class="sxs-lookup"><span data-stu-id="cb764-116">If a column of that name exists in the base table it will be ignored.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="cb764-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cb764-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="cb764-118">參考</span><span class="sxs-lookup"><span data-stu-id="cb764-118">Reference</span></span>

[<span data-ttu-id="cb764-119">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="cb764-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
