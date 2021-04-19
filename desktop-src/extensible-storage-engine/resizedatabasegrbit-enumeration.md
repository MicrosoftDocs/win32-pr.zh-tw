---
description: 深入瞭解： ResizeDatabaseGrbit 列舉
title: ResizeDatabaseGrbit 列舉 (Windows8) 的列舉
TOCTitle: ResizeDatabaseGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.resizedatabasegrbit(v=EXCHG.10)
ms:contentKeyID: 55104329
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit
- Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit.OnlyGrow
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit
- Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit.OnlyGrow
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 51d703f96882136e2b88f1a2df37609573c725e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980887"
---
# <a name="resizedatabasegrbit-enumeration"></a><span data-ttu-id="8e062-103">ResizeDatabaseGrbit 列舉</span><span class="sxs-lookup"><span data-stu-id="8e062-103">ResizeDatabaseGrbit enumeration</span></span>

<span data-ttu-id="8e062-104">[JetResizeDatabase (JET_SESID、JET_DBID、int32、int32、ResizeDatabaseGrbit) ](./windows8api.jetresizedatabase-method.md)的選項。</span><span class="sxs-lookup"><span data-stu-id="8e062-104">Options for [JetResizeDatabase(JET_SESID, JET_DBID, Int32, Int32, ResizeDatabaseGrbit)](./windows8api.jetresizedatabase-method.md).</span></span>

<span data-ttu-id="8e062-105">此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。</span><span class="sxs-lookup"><span data-stu-id="8e062-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="8e062-106">**命名空間：**  [Microsoft Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8e062-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="8e062-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="8e062-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8e062-108">語法</span><span class="sxs-lookup"><span data-stu-id="8e062-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration ResizeDatabaseGrbit
'Usage
Dim instance As ResizeDatabaseGrbit
```

``` csharp
[FlagsAttribute]
public enum ResizeDatabaseGrbit
```

## <a name="members"></a><span data-ttu-id="8e062-109">成員</span><span class="sxs-lookup"><span data-stu-id="8e062-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="8e062-110">成員名稱</span><span class="sxs-lookup"><span data-stu-id="8e062-110">Member name</span></span></th>
<th><span data-ttu-id="8e062-111">描述</span><span class="sxs-lookup"><span data-stu-id="8e062-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="8e062-112">無</span><span class="sxs-lookup"><span data-stu-id="8e062-112">None</span></span></td>
<td><span data-ttu-id="8e062-113">沒有選項。</span><span class="sxs-lookup"><span data-stu-id="8e062-113">No option.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="8e062-114">OnlyGrow</span><span class="sxs-lookup"><span data-stu-id="8e062-114">OnlyGrow</span></span></td>
<td><span data-ttu-id="8e062-115">只增加資料庫。</span><span class="sxs-lookup"><span data-stu-id="8e062-115">Only grow the database.</span></span> <span data-ttu-id="8e062-116">如果調整大小呼叫會壓縮資料庫，則不執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="8e062-116">If the resize call would shrink the database, do nothing.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="8e062-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8e062-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8e062-118">參考</span><span class="sxs-lookup"><span data-stu-id="8e062-118">Reference</span></span>

[<span data-ttu-id="8e062-119">Windows8 命名空間。</span><span class="sxs-lookup"><span data-stu-id="8e062-119">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
