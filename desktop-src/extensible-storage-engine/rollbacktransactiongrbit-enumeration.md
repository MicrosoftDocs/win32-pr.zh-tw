---
description: 深入瞭解： RollbackTransactionGrbit 列舉
title: RollbackTransactionGrbit 列舉
TOCTitle: RollbackTransactionGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.rollbacktransactiongrbit(v=EXCHG.10)
ms:contentKeyID: 39513584
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit
- Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit.None
- Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit.RollbackAll
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit.RollbackAll
- Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit.None
- Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bf2635d94070fc47bebbd6cdd0e53deddeb4c5eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997536"
---
# <a name="rollbacktransactiongrbit-enumeration"></a><span data-ttu-id="37b1e-103">RollbackTransactionGrbit 列舉</span><span class="sxs-lookup"><span data-stu-id="37b1e-103">RollbackTransactionGrbit enumeration</span></span>

<span data-ttu-id="37b1e-104">JetRollbackTransaction 的選項。</span><span class="sxs-lookup"><span data-stu-id="37b1e-104">Options for JetRollbackTransaction.</span></span>

<span data-ttu-id="37b1e-105">此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。</span><span class="sxs-lookup"><span data-stu-id="37b1e-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="37b1e-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="37b1e-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="37b1e-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="37b1e-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="37b1e-108">語法</span><span class="sxs-lookup"><span data-stu-id="37b1e-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration RollbackTransactionGrbit
'Usage
Dim instance As RollbackTransactionGrbit
```

``` csharp
[FlagsAttribute]
public enum RollbackTransactionGrbit
```

## <a name="members"></a><span data-ttu-id="37b1e-109">成員</span><span class="sxs-lookup"><span data-stu-id="37b1e-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="37b1e-110">成員名稱</span><span class="sxs-lookup"><span data-stu-id="37b1e-110">Member name</span></span></th>
<th><span data-ttu-id="37b1e-111">描述</span><span class="sxs-lookup"><span data-stu-id="37b1e-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="37b1e-112">無</span><span class="sxs-lookup"><span data-stu-id="37b1e-112">None</span></span></td>
<td><span data-ttu-id="37b1e-113">預設選項。</span><span class="sxs-lookup"><span data-stu-id="37b1e-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="37b1e-114">RollbackAll</span><span class="sxs-lookup"><span data-stu-id="37b1e-114">RollbackAll</span></span></td>
<td><span data-ttu-id="37b1e-115">此選項會要求所有儲存點在所有儲存點都復原時，對資料庫狀態所進行的所有變更。</span><span class="sxs-lookup"><span data-stu-id="37b1e-115">This option requests that all changes made to the state of the database during all save points be undone.</span></span> <span data-ttu-id="37b1e-116">因此，會話將會結束交易。</span><span class="sxs-lookup"><span data-stu-id="37b1e-116">As a result, the session will exit the transaction.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="37b1e-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="37b1e-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="37b1e-118">參考</span><span class="sxs-lookup"><span data-stu-id="37b1e-118">Reference</span></span>

[<span data-ttu-id="37b1e-119">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="37b1e-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
