---
description: 深入瞭解： EndExternalBackupGrbit 列舉
title: EndExternalBackupGrbit 列舉
TOCTitle: EndExternalBackupGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.endexternalbackupgrbit(v=EXCHG.10)
ms:contentKeyID: 39516835
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit.Abort
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit.None
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit.Normal
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit.Abort
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit.None
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit.Normal
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0bb3fb2f3e959d41c042589f3a280e6466fe4970
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195199"
---
# <a name="endexternalbackupgrbit-enumeration"></a><span data-ttu-id="f69ad-103">EndExternalBackupGrbit 列舉</span><span class="sxs-lookup"><span data-stu-id="f69ad-103">EndExternalBackupGrbit enumeration</span></span>

<span data-ttu-id="f69ad-104">[JetEndExternalBackupInstance (JET_INSTANCE) ](./api.jetendexternalbackupinstance-method.md)的選項。</span><span class="sxs-lookup"><span data-stu-id="f69ad-104">Options for [JetEndExternalBackupInstance(JET_INSTANCE)](./api.jetendexternalbackupinstance-method.md).</span></span>

<span data-ttu-id="f69ad-105">此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。</span><span class="sxs-lookup"><span data-stu-id="f69ad-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="f69ad-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f69ad-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f69ad-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="f69ad-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f69ad-108">語法</span><span class="sxs-lookup"><span data-stu-id="f69ad-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration EndExternalBackupGrbit
'Usage
Dim instance As EndExternalBackupGrbit
```

``` csharp
[FlagsAttribute]
public enum EndExternalBackupGrbit
```

## <a name="members"></a><span data-ttu-id="f69ad-109">成員</span><span class="sxs-lookup"><span data-stu-id="f69ad-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="f69ad-110">成員名稱</span><span class="sxs-lookup"><span data-stu-id="f69ad-110">Member name</span></span></th>
<th><span data-ttu-id="f69ad-111">描述</span><span class="sxs-lookup"><span data-stu-id="f69ad-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="f69ad-112">無</span><span class="sxs-lookup"><span data-stu-id="f69ad-112">None</span></span></td>
<td><span data-ttu-id="f69ad-113">預設選項。</span><span class="sxs-lookup"><span data-stu-id="f69ad-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="f69ad-114">正常</span><span class="sxs-lookup"><span data-stu-id="f69ad-114">Normal</span></span></td>
<td><span data-ttu-id="f69ad-115">用戶端應用程式已完全完成備份，且正常結束。</span><span class="sxs-lookup"><span data-stu-id="f69ad-115">The client application finished the backup completely, and is ending normally.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="f69ad-116">中止</span><span class="sxs-lookup"><span data-stu-id="f69ad-116">Abort</span></span></td>
<td><span data-ttu-id="f69ad-117">用戶端應用程式正在中止備份。</span><span class="sxs-lookup"><span data-stu-id="f69ad-117">The client application is aborting the backup.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="f69ad-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f69ad-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f69ad-119">參考</span><span class="sxs-lookup"><span data-stu-id="f69ad-119">Reference</span></span>

[<span data-ttu-id="f69ad-120">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="f69ad-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
