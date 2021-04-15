---
description: 深入瞭解： UpdateGrbit 列舉
title: UpdateGrbit 列舉 (Server2003) 的列舉
TOCTitle: UpdateGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.updategrbit(v=EXCHG.10)
ms:contentKeyID: 39514938
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit.CheckESE97Compatibility
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit.None
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit.CheckESE97Compatibility
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e27809ef16fb00fd538e4c37826d10fefa3b396c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511856"
---
# <a name="updategrbit-enumeration"></a><span data-ttu-id="6cbeb-103">UpdateGrbit 列舉</span><span class="sxs-lookup"><span data-stu-id="6cbeb-103">UpdateGrbit enumeration</span></span>

<span data-ttu-id="6cbeb-104">[JetUpdate2 (JET_SESID、JET_TABLEID、 \[ \] 、int32、int32、UpdateGrbit) ](./server2003api.jetupdate2-method.md)的選項。</span><span class="sxs-lookup"><span data-stu-id="6cbeb-104">Options for [JetUpdate2(JET_SESID, JET_TABLEID, \[\], Int32, Int32, UpdateGrbit)](./server2003api.jetupdate2-method.md).</span></span>

<span data-ttu-id="6cbeb-105">此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。</span><span class="sxs-lookup"><span data-stu-id="6cbeb-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="6cbeb-106">**命名空間：**  [Microsoft Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6cbeb-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span></span>  
<span data-ttu-id="6cbeb-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="6cbeb-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6cbeb-108">語法</span><span class="sxs-lookup"><span data-stu-id="6cbeb-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration UpdateGrbit
'Usage
Dim instance As UpdateGrbit
```

``` csharp
[FlagsAttribute]
public enum UpdateGrbit
```

## <a name="members"></a><span data-ttu-id="6cbeb-109">成員</span><span class="sxs-lookup"><span data-stu-id="6cbeb-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="6cbeb-110">成員名稱</span><span class="sxs-lookup"><span data-stu-id="6cbeb-110">Member name</span></span></th>
<th><span data-ttu-id="6cbeb-111">描述</span><span class="sxs-lookup"><span data-stu-id="6cbeb-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="6cbeb-112">無</span><span class="sxs-lookup"><span data-stu-id="6cbeb-112">None</span></span></td>
<td><span data-ttu-id="6cbeb-113">預設選項。</span><span class="sxs-lookup"><span data-stu-id="6cbeb-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="6cbeb-114">CheckESE97Compatibility</span><span class="sxs-lookup"><span data-stu-id="6cbeb-114">CheckESE97Compatibility</span></span></td>
<td><span data-ttu-id="6cbeb-115"><strong>已淘汰。</strong></span><span class="sxs-lookup"><span data-stu-id="6cbeb-115"><strong>Obsolete.</strong></span></span> <span data-ttu-id="6cbeb-116">如果在 Windows 2000 版的 ESE 中不可能進行更新，此旗標會導致更新傳回錯誤，這會在每一筆記錄中強制執行較小數目的多重值資料行實例，而不是較新的 ESE 版本。</span><span class="sxs-lookup"><span data-stu-id="6cbeb-116">This flag causes the update to return an error if the update would not have been possible in the Windows 2000 version of ESE, which enforced a smaller maximum number of multi-valued column instances in each record than later versions of ESE.</span></span> <span data-ttu-id="6cbeb-117">這僅適用于想要在裝載于 Windows 2000 的應用程式與 Windows 2003 或更新版本的 ESE 上裝載的應用程式之間複寫資料的應用程式。</span><span class="sxs-lookup"><span data-stu-id="6cbeb-117">This is important only for applications that wish to replicate data between applications hosted on Windows 2000 and applications hosted on Windows 2003, or later versions of ESE.</span></span> <span data-ttu-id="6cbeb-118">大部分的應用程式都不需要這麼做。</span><span class="sxs-lookup"><span data-stu-id="6cbeb-118">It should not be necessary for most applications.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="6cbeb-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6cbeb-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6cbeb-120">參考</span><span class="sxs-lookup"><span data-stu-id="6cbeb-120">Reference</span></span>

[<span data-ttu-id="6cbeb-121">Server2003 命名空間。</span><span class="sxs-lookup"><span data-stu-id="6cbeb-121">Microsoft.Isam.Esent.Interop.Server2003 namespace</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)
