---
description: 深入瞭解： IndexKeyGrbit 列舉
title: IndexKeyGrbit 列舉
TOCTitle: IndexKeyGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.IndexKeyGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.indexkeygrbit(v=EXCHG.10)
ms:contentKeyID: 39514044
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.IndexKeyGrbit
- Microsoft.Isam.Esent.Interop.IndexKeyGrbit.Ascending
- Microsoft.Isam.Esent.Interop.IndexKeyGrbit.Descending
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.IndexKeyGrbit
- Microsoft.Isam.Esent.Interop.IndexKeyGrbit.Descending
- Microsoft.Isam.Esent.Interop.IndexKeyGrbit.Ascending
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f28a3f0c7d69f8ce7e8e688b6fb7b2fecafcce44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191654"
---
# <a name="indexkeygrbit-enumeration"></a><span data-ttu-id="f470d-103">IndexKeyGrbit 列舉</span><span class="sxs-lookup"><span data-stu-id="f470d-103">IndexKeyGrbit enumeration</span></span>

<span data-ttu-id="f470d-104">索引鍵定義 grbits。</span><span class="sxs-lookup"><span data-stu-id="f470d-104">Key definition grbits.</span></span> <span data-ttu-id="f470d-105">在抓取索引的相關資訊時使用。</span><span class="sxs-lookup"><span data-stu-id="f470d-105">Used when retrieving information about an index.</span></span>

<span data-ttu-id="f470d-106">此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。</span><span class="sxs-lookup"><span data-stu-id="f470d-106">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="f470d-107">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f470d-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f470d-108">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="f470d-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f470d-109">語法</span><span class="sxs-lookup"><span data-stu-id="f470d-109">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration IndexKeyGrbit
'Usage
Dim instance As IndexKeyGrbit
```

``` csharp
[FlagsAttribute]
public enum IndexKeyGrbit
```

## <a name="members"></a><span data-ttu-id="f470d-110">成員</span><span class="sxs-lookup"><span data-stu-id="f470d-110">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="f470d-111">成員名稱</span><span class="sxs-lookup"><span data-stu-id="f470d-111">Member name</span></span></th>
<th><span data-ttu-id="f470d-112">說明</span><span class="sxs-lookup"><span data-stu-id="f470d-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="f470d-113">遞增</span><span class="sxs-lookup"><span data-stu-id="f470d-113">Ascending</span></span></td>
<td><span data-ttu-id="f470d-114">索引鍵區段是遞增的。</span><span class="sxs-lookup"><span data-stu-id="f470d-114">Key segment is ascending.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="f470d-115">遞減</span><span class="sxs-lookup"><span data-stu-id="f470d-115">Descending</span></span></td>
<td><span data-ttu-id="f470d-116">索引鍵區段會遞減。</span><span class="sxs-lookup"><span data-stu-id="f470d-116">Key segment is descending.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="f470d-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f470d-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f470d-118">參考</span><span class="sxs-lookup"><span data-stu-id="f470d-118">Reference</span></span>

[<span data-ttu-id="f470d-119">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="f470d-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
