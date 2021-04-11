---
description: 深入瞭解： MoveGrbit 列舉
title: MoveGrbit 列舉
TOCTitle: MoveGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.MoveGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.movegrbit(v=EXCHG.10)
ms:contentKeyID: 39513771
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.MoveGrbit
- Microsoft.Isam.Esent.Interop.MoveGrbit.MoveKeyNE
- Microsoft.Isam.Esent.Interop.MoveGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.MoveGrbit
- Microsoft.Isam.Esent.Interop.MoveGrbit.None
- Microsoft.Isam.Esent.Interop.MoveGrbit.MoveKeyNE
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 81f047cd69bca668a5eae2b5147d8c0a137011e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026839"
---
# <a name="movegrbit-enumeration"></a><span data-ttu-id="3f797-103">MoveGrbit 列舉</span><span class="sxs-lookup"><span data-stu-id="3f797-103">MoveGrbit enumeration</span></span>

<span data-ttu-id="3f797-104">JetMove 的選項。</span><span class="sxs-lookup"><span data-stu-id="3f797-104">Options for JetMove.</span></span>

<span data-ttu-id="3f797-105">此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。</span><span class="sxs-lookup"><span data-stu-id="3f797-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="3f797-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3f797-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3f797-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="3f797-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3f797-108">語法</span><span class="sxs-lookup"><span data-stu-id="3f797-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration MoveGrbit
'Usage
Dim instance As MoveGrbit
```

``` csharp
[FlagsAttribute]
public enum MoveGrbit
```

## <a name="members"></a><span data-ttu-id="3f797-109">成員</span><span class="sxs-lookup"><span data-stu-id="3f797-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="3f797-110">成員名稱</span><span class="sxs-lookup"><span data-stu-id="3f797-110">Member name</span></span></th>
<th><span data-ttu-id="3f797-111">描述</span><span class="sxs-lookup"><span data-stu-id="3f797-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="3f797-112">無</span><span class="sxs-lookup"><span data-stu-id="3f797-112">None</span></span></td>
<td><span data-ttu-id="3f797-113">預設選項。</span><span class="sxs-lookup"><span data-stu-id="3f797-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="3f797-114">MoveKeyNE</span><span class="sxs-lookup"><span data-stu-id="3f797-114">MoveKeyNE</span></span></td>
<td><span data-ttu-id="3f797-115">向前或向後移動游標，以略過索引中所遇到的索引鍵值數目。</span><span class="sxs-lookup"><span data-stu-id="3f797-115">Moves the cursor forward or backward by the number of index entries required to skip the requested number of index key values encountered in the index.</span></span> <span data-ttu-id="3f797-116">這會將具有重複索引鍵值的索引項目轉換成單一索引項目的效果。</span><span class="sxs-lookup"><span data-stu-id="3f797-116">This has the effect of collapsing index entries with duplicate key values into a single index entry.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="3f797-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3f797-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3f797-118">參考</span><span class="sxs-lookup"><span data-stu-id="3f797-118">Reference</span></span>

[<span data-ttu-id="3f797-119">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="3f797-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
