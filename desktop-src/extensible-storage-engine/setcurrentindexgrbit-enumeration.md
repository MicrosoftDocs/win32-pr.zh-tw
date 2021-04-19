---
description: 深入瞭解： SetCurrentIndexGrbit 列舉
title: SetCurrentIndexGrbit 列舉
TOCTitle: SetCurrentIndexGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.setcurrentindexgrbit(v=EXCHG.10)
ms:contentKeyID: 39515072
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.MoveFirst
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.NoMove
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.None
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.NoMove
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.MoveFirst
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2391715332989bf20aae3d0a666c1cef2ce2e135
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970222"
---
# <a name="setcurrentindexgrbit-enumeration"></a><span data-ttu-id="32d5d-103">SetCurrentIndexGrbit 列舉</span><span class="sxs-lookup"><span data-stu-id="32d5d-103">SetCurrentIndexGrbit enumeration</span></span>

<span data-ttu-id="32d5d-104">[JetSetCurrentIndex2 (JET_SESID、JET_TABLEID、string、SetCurrentIndexGrbit) ](./api.jetsetcurrentindex2-method.md)和[JetSetCurrentIndex3 (JET_SESID、JET_TABLEID、string、SetCurrentIndexGrbit、Int32) ](./api.jetsetcurrentindex3-method.md)的選項。</span><span class="sxs-lookup"><span data-stu-id="32d5d-104">Options for [JetSetCurrentIndex2(JET_SESID, JET_TABLEID, String, SetCurrentIndexGrbit)](./api.jetsetcurrentindex2-method.md) and [JetSetCurrentIndex3(JET_SESID, JET_TABLEID, String, SetCurrentIndexGrbit, Int32)](./api.jetsetcurrentindex3-method.md).</span></span>

<span data-ttu-id="32d5d-105">此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。</span><span class="sxs-lookup"><span data-stu-id="32d5d-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="32d5d-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="32d5d-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="32d5d-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="32d5d-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="32d5d-108">語法</span><span class="sxs-lookup"><span data-stu-id="32d5d-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SetCurrentIndexGrbit
'Usage
Dim instance As SetCurrentIndexGrbit
```

``` csharp
[FlagsAttribute]
public enum SetCurrentIndexGrbit
```

## <a name="members"></a><span data-ttu-id="32d5d-109">成員</span><span class="sxs-lookup"><span data-stu-id="32d5d-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="32d5d-110">成員名稱</span><span class="sxs-lookup"><span data-stu-id="32d5d-110">Member name</span></span></th>
<th><span data-ttu-id="32d5d-111">描述</span><span class="sxs-lookup"><span data-stu-id="32d5d-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="32d5d-112">無</span><span class="sxs-lookup"><span data-stu-id="32d5d-112">None</span></span></td>
<td><span data-ttu-id="32d5d-113">預設選項。</span><span class="sxs-lookup"><span data-stu-id="32d5d-113">Default options.</span></span> <span data-ttu-id="32d5d-114">這與 MoveFirst 相同。</span><span class="sxs-lookup"><span data-stu-id="32d5d-114">This is the same as MoveFirst.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="32d5d-115">MoveFirst</span><span class="sxs-lookup"><span data-stu-id="32d5d-115">MoveFirst</span></span></td>
<td><span data-ttu-id="32d5d-116">表示資料指標應放置在指定之索引的第一個專案。</span><span class="sxs-lookup"><span data-stu-id="32d5d-116">Indicates that the cursor should be positioned on the first entry of the specified index.</span></span> <span data-ttu-id="32d5d-117">如果選取目前的索引，則會忽略此選項。</span><span class="sxs-lookup"><span data-stu-id="32d5d-117">If the current index is being selected then this option is ignored.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="32d5d-118">NoMove</span><span class="sxs-lookup"><span data-stu-id="32d5d-118">NoMove</span></span></td>
<td><span data-ttu-id="32d5d-119">表示資料指標應放置在新索引的索引項目上，此索引會對應到舊索引上資料指標目前位置的索引項目相關記錄。</span><span class="sxs-lookup"><span data-stu-id="32d5d-119">Indicates that the cursor should be positioned on the index entry of the new index that corresponds to the record associated with the index entry at the current position of the cursor on the old index.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="32d5d-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="32d5d-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="32d5d-121">參考</span><span class="sxs-lookup"><span data-stu-id="32d5d-121">Reference</span></span>

[<span data-ttu-id="32d5d-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="32d5d-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
