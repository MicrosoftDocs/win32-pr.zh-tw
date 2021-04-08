---
description: 深入瞭解： LsGrbit 列舉
title: LsGrbit 列舉
TOCTitle: LsGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.LsGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.lsgrbit(v=EXCHG.10)
ms:contentKeyID: 39514518
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.LsGrbit
- Microsoft.Isam.Esent.Interop.LsGrbit.Cursor
- Microsoft.Isam.Esent.Interop.LsGrbit.None
- Microsoft.Isam.Esent.Interop.LsGrbit.Reset
- Microsoft.Isam.Esent.Interop.LsGrbit.Table
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.LsGrbit
- Microsoft.Isam.Esent.Interop.LsGrbit.Reset
- Microsoft.Isam.Esent.Interop.LsGrbit.None
- Microsoft.Isam.Esent.Interop.LsGrbit.Table
- Microsoft.Isam.Esent.Interop.LsGrbit.Cursor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5fc0a60d039d0eb1307558d42a3e7a3c7e99eb86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026285"
---
# <a name="lsgrbit-enumeration"></a><span data-ttu-id="2a895-103">LsGrbit 列舉</span><span class="sxs-lookup"><span data-stu-id="2a895-103">LsGrbit enumeration</span></span>

<span data-ttu-id="2a895-104">[JetSetLS (JET_SESID、JET_TABLEID、JET_LS、LsGrbit) ](./api.jetsetls-method.md)和[JetGetLS (JET_SESID、JET_TABLEID、JET_LS、LsGrbit) ](./api.jetgetls-method.md)的選項。</span><span class="sxs-lookup"><span data-stu-id="2a895-104">Options for [JetSetLS(JET_SESID, JET_TABLEID, JET_LS, LsGrbit)](./api.jetsetls-method.md) and [JetGetLS(JET_SESID, JET_TABLEID, JET_LS, LsGrbit)](./api.jetgetls-method.md).</span></span>

<span data-ttu-id="2a895-105">此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。</span><span class="sxs-lookup"><span data-stu-id="2a895-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="2a895-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2a895-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2a895-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="2a895-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2a895-108">語法</span><span class="sxs-lookup"><span data-stu-id="2a895-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration LsGrbit
'Usage
Dim instance As LsGrbit
```

``` csharp
[FlagsAttribute]
public enum LsGrbit
```

## <a name="members"></a><span data-ttu-id="2a895-109">成員</span><span class="sxs-lookup"><span data-stu-id="2a895-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="2a895-110">成員名稱</span><span class="sxs-lookup"><span data-stu-id="2a895-110">Member name</span></span></th>
<th><span data-ttu-id="2a895-111">描述</span><span class="sxs-lookup"><span data-stu-id="2a895-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="2a895-112">無</span><span class="sxs-lookup"><span data-stu-id="2a895-112">None</span></span></td>
<td><span data-ttu-id="2a895-113">預設選項。</span><span class="sxs-lookup"><span data-stu-id="2a895-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="2a895-114">重設</span><span class="sxs-lookup"><span data-stu-id="2a895-114">Reset</span></span></td>
<td><span data-ttu-id="2a895-115">所選物件的內容控制碼應該重設為 JET_LSNil。</span><span class="sxs-lookup"><span data-stu-id="2a895-115">The context handle for the chosen object should be reset to JET_LSNil.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="2a895-116">資料指標</span><span class="sxs-lookup"><span data-stu-id="2a895-116">Cursor</span></span></td>
<td><span data-ttu-id="2a895-117">指定應該與指定的資料指標相關聯的內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="2a895-117">Specifies the context handle should be associated with the given cursor.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="2a895-118">資料表</span><span class="sxs-lookup"><span data-stu-id="2a895-118">Table</span></span></td>
<td><span data-ttu-id="2a895-119">指定內容控制碼應該與指定資料指標相關聯的資料表相關聯。</span><span class="sxs-lookup"><span data-stu-id="2a895-119">Specifies that the context handle should be associated with the table associated with the given cursor.</span></span> <span data-ttu-id="2a895-120">搭配使用此選項與資料指標是不合法的。</span><span class="sxs-lookup"><span data-stu-id="2a895-120">It is illegal to use this option with Cursor.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="2a895-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2a895-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2a895-122">參考</span><span class="sxs-lookup"><span data-stu-id="2a895-122">Reference</span></span>

[<span data-ttu-id="2a895-123">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="2a895-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
