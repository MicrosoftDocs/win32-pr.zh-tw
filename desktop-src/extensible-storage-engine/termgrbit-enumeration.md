---
description: 深入瞭解： TermGrbit 列舉
title: TermGrbit 列舉
TOCTitle: TermGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.TermGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.termgrbit(v=EXCHG.10)
ms:contentKeyID: 39511147
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.TermGrbit
- Microsoft.Isam.Esent.Interop.TermGrbit.Abrupt
- Microsoft.Isam.Esent.Interop.TermGrbit.Complete
- Microsoft.Isam.Esent.Interop.TermGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.TermGrbit.None
- Microsoft.Isam.Esent.Interop.TermGrbit
- Microsoft.Isam.Esent.Interop.TermGrbit.Complete
- Microsoft.Isam.Esent.Interop.TermGrbit.Abrupt
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 49b466b298a78d7bfd6822904aed977e7117b927
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694699"
---
# <a name="termgrbit-enumeration"></a><span data-ttu-id="23b72-103">TermGrbit 列舉</span><span class="sxs-lookup"><span data-stu-id="23b72-103">TermGrbit enumeration</span></span>

<span data-ttu-id="23b72-104">[JetTerm2 (JET_INSTANCE、TermGrbit) ](./api.jetterm2-method.md)的選項。</span><span class="sxs-lookup"><span data-stu-id="23b72-104">Options for [JetTerm2(JET_INSTANCE, TermGrbit)](./api.jetterm2-method.md).</span></span>

<span data-ttu-id="23b72-105">此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。</span><span class="sxs-lookup"><span data-stu-id="23b72-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="23b72-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="23b72-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="23b72-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="23b72-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="23b72-108">語法</span><span class="sxs-lookup"><span data-stu-id="23b72-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration TermGrbit
'Usage
Dim instance As TermGrbit
```

``` csharp
[FlagsAttribute]
public enum TermGrbit
```

## <a name="members"></a><span data-ttu-id="23b72-109">成員</span><span class="sxs-lookup"><span data-stu-id="23b72-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="23b72-110">成員名稱</span><span class="sxs-lookup"><span data-stu-id="23b72-110">Member name</span></span></th>
<th><span data-ttu-id="23b72-111">描述</span><span class="sxs-lookup"><span data-stu-id="23b72-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="23b72-112">無</span><span class="sxs-lookup"><span data-stu-id="23b72-112">None</span></span></td>
<td><span data-ttu-id="23b72-113">預設選項。</span><span class="sxs-lookup"><span data-stu-id="23b72-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="23b72-114">完成</span><span class="sxs-lookup"><span data-stu-id="23b72-114">Complete</span></span></td>
<td><span data-ttu-id="23b72-115">要求完全關閉實例。</span><span class="sxs-lookup"><span data-stu-id="23b72-115">Requests that the instance be shut down cleanly.</span></span> <span data-ttu-id="23b72-116">通常會在執行時間于背景中完成的任何選擇性清除工作會立即完成。</span><span class="sxs-lookup"><span data-stu-id="23b72-116">Any optional cleanup work that would ordinarily be done in the background at run time is completed immediately.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="23b72-117">突然</span><span class="sxs-lookup"><span data-stu-id="23b72-117">Abrupt</span></span></td>
<td><span data-ttu-id="23b72-118">要求實例盡可能快速關閉。</span><span class="sxs-lookup"><span data-stu-id="23b72-118">Requests that the instance be shut down as quickly as possible.</span></span> <span data-ttu-id="23b72-119">在執行時間，通常會在背景中完成的任何選擇性工作都會被放棄。</span><span class="sxs-lookup"><span data-stu-id="23b72-119">Any optional work that would ordinarily be done in the background at run time is abandoned.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="23b72-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="23b72-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="23b72-121">參考</span><span class="sxs-lookup"><span data-stu-id="23b72-121">Reference</span></span>

[<span data-ttu-id="23b72-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="23b72-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

[<span data-ttu-id="23b72-123">髒</span><span class="sxs-lookup"><span data-stu-id="23b72-123">Dirty</span></span>](./windows7grbits.dirty-field.md)
