---
description: 深入瞭解： JET_InstanceMiscInfo 列舉
title: 'JET_InstanceMiscInfo 列舉 (的 < a0/&gt; < a1/&gt;) '
TOCTitle: JET_InstanceMiscInfo enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Vista.JET_InstanceMiscInfo
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_instancemiscinfo(v=EXCHG.10)
ms:contentKeyID: 39516547
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_InstanceMiscInfo
- Microsoft.Isam.Esent.Interop.Vista.JET_InstanceMiscInfo.LogSignature
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_InstanceMiscInfo.LogSignature
- Microsoft.Isam.Esent.Interop.Vista.JET_InstanceMiscInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: acf008b1a349ab2ddfe735dab45214cb19a71fe9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106976364"
---
# <a name="jet_instancemiscinfo-enumeration"></a><span data-ttu-id="ecc8e-103">JET_InstanceMiscInfo 列舉</span><span class="sxs-lookup"><span data-stu-id="ecc8e-103">JET_InstanceMiscInfo enumeration</span></span>

<span data-ttu-id="ecc8e-104">[JetGetInstanceMiscInfo (JET_INSTANCE、JET_SIGNATURE JET_InstanceMiscInfo) ](./vistaapi.jetgetinstancemiscinfo-method.md)的資訊層級。</span><span class="sxs-lookup"><span data-stu-id="ecc8e-104">Information levels for [JetGetInstanceMiscInfo(JET_INSTANCE, JET_SIGNATURE, JET_InstanceMiscInfo)](./vistaapi.jetgetinstancemiscinfo-method.md).</span></span>

<span data-ttu-id="ecc8e-105">此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。</span><span class="sxs-lookup"><span data-stu-id="ecc8e-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="ecc8e-106">**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。  </span><span class="sxs-lookup"><span data-stu-id="ecc8e-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="ecc8e-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="ecc8e-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ecc8e-108">語法</span><span class="sxs-lookup"><span data-stu-id="ecc8e-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration JET_InstanceMiscInfo
'Usage
Dim instance As JET_InstanceMiscInfo
```

``` csharp
[FlagsAttribute]
public enum JET_InstanceMiscInfo
```

## <a name="members"></a><span data-ttu-id="ecc8e-109">成員</span><span class="sxs-lookup"><span data-stu-id="ecc8e-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="ecc8e-110">成員名稱</span><span class="sxs-lookup"><span data-stu-id="ecc8e-110">Member name</span></span></th>
<th><span data-ttu-id="ecc8e-111">說明</span><span class="sxs-lookup"><span data-stu-id="ecc8e-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="ecc8e-112">LogSignature</span><span class="sxs-lookup"><span data-stu-id="ecc8e-112">LogSignature</span></span></td>
<td><span data-ttu-id="ecc8e-113">取得與此順序相關聯之交易記錄的簽章。</span><span class="sxs-lookup"><span data-stu-id="ecc8e-113">Get the signature of the transaction log associated with this sequence.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="ecc8e-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ecc8e-114">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ecc8e-115">參考</span><span class="sxs-lookup"><span data-stu-id="ecc8e-115">Reference</span></span>

[<span data-ttu-id="ecc8e-116">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="ecc8e-116">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
