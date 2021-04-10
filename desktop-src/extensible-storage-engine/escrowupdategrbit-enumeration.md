---
description: 深入瞭解： EscrowUpdateGrbit 列舉
title: EscrowUpdateGrbit 列舉
TOCTitle: EscrowUpdateGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.escrowupdategrbit(v=EXCHG.10)
ms:contentKeyID: 39514160
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit
- Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit.None
- Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit.NoRollback
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit
- Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit.None
- Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit.NoRollback
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d301ef801a5685057a9e33beb794f3b6cf13e646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945279"
---
# <a name="escrowupdategrbit-enumeration"></a><span data-ttu-id="c349b-103">EscrowUpdateGrbit 列舉</span><span class="sxs-lookup"><span data-stu-id="c349b-103">EscrowUpdateGrbit enumeration</span></span>

<span data-ttu-id="c349b-104">JetEscrowUpdate 的選項。</span><span class="sxs-lookup"><span data-stu-id="c349b-104">Options for JetEscrowUpdate.</span></span>

<span data-ttu-id="c349b-105">此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。</span><span class="sxs-lookup"><span data-stu-id="c349b-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="c349b-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c349b-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c349b-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="c349b-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c349b-108">語法</span><span class="sxs-lookup"><span data-stu-id="c349b-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration EscrowUpdateGrbit
'Usage
Dim instance As EscrowUpdateGrbit
```

``` csharp
[FlagsAttribute]
public enum EscrowUpdateGrbit
```

## <a name="members"></a><span data-ttu-id="c349b-109">成員</span><span class="sxs-lookup"><span data-stu-id="c349b-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="c349b-110">成員名稱</span><span class="sxs-lookup"><span data-stu-id="c349b-110">Member name</span></span></th>
<th><span data-ttu-id="c349b-111">描述</span><span class="sxs-lookup"><span data-stu-id="c349b-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="c349b-112">無</span><span class="sxs-lookup"><span data-stu-id="c349b-112">None</span></span></td>
<td><span data-ttu-id="c349b-113">預設選項。</span><span class="sxs-lookup"><span data-stu-id="c349b-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="c349b-114">NoRollback</span><span class="sxs-lookup"><span data-stu-id="c349b-114">NoRollback</span></span></td>
<td><span data-ttu-id="c349b-115">即使執行保管更新的會話具有其交易回復，但這種更新將不會復原。</span><span class="sxs-lookup"><span data-stu-id="c349b-115">Even if the session performing the escrow update has its transaction rollback this update will not be undone.</span></span> <span data-ttu-id="c349b-116">因為記錄檔記錄可能不會排清到磁片，所以使用此旗標完成的最新的證書處理更新可能會在發生損毀時遺失。</span><span class="sxs-lookup"><span data-stu-id="c349b-116">As the log records may not be flushed to disk, recent escrow updates done with this flag may be lost if there is a crash.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="c349b-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c349b-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c349b-118">參考</span><span class="sxs-lookup"><span data-stu-id="c349b-118">Reference</span></span>

[<span data-ttu-id="c349b-119">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="c349b-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
