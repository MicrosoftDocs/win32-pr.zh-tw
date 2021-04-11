---
description: 深入瞭解： JET_sesparam 列舉
title: 'JET_sesparam 列舉的 (Windows8) '
TOCTitle: JET_sesparam enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_sesparam(v=EXCHG.10)
ms:contentKeyID: 55104452
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam.Base
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam.CommitDefault
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam.CommitGenericContext
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam.Base
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam.CommitGenericContext
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam.CommitDefault
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d5ddfd613eecf5e9a6d9b6cec9eebcbab04e9b38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112533"
---
# <a name="jet_sesparam-enumeration"></a><span data-ttu-id="5bd1d-103">JET_sesparam 列舉</span><span class="sxs-lookup"><span data-stu-id="5bd1d-103">JET_sesparam enumeration</span></span>

<span data-ttu-id="5bd1d-104">ESENT 會話參數。</span><span class="sxs-lookup"><span data-stu-id="5bd1d-104">ESENT session parameters.</span></span>

<span data-ttu-id="5bd1d-105">**命名空間：**  [Microsoft Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5bd1d-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="5bd1d-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="5bd1d-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5bd1d-107">語法</span><span class="sxs-lookup"><span data-stu-id="5bd1d-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_sesparam
'Usage
Dim instance As JET_sesparam
```

``` csharp
public enum JET_sesparam
```

## <a name="members"></a><span data-ttu-id="5bd1d-108">成員</span><span class="sxs-lookup"><span data-stu-id="5bd1d-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="5bd1d-109">成員名稱</span><span class="sxs-lookup"><span data-stu-id="5bd1d-109">Member name</span></span></th>
<th><span data-ttu-id="5bd1d-110">說明</span><span class="sxs-lookup"><span data-stu-id="5bd1d-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="5bd1d-111">基本</span><span class="sxs-lookup"><span data-stu-id="5bd1d-111">Base</span></span></td>
<td><span data-ttu-id="5bd1d-112">不應使用此參數。</span><span class="sxs-lookup"><span data-stu-id="5bd1d-112">This parameter is not meant to be used.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="5bd1d-113">CommitDefault</span><span class="sxs-lookup"><span data-stu-id="5bd1d-113">CommitDefault</span></span></td>
<td><span data-ttu-id="5bd1d-114">此參數會設定認可的 grbits。</span><span class="sxs-lookup"><span data-stu-id="5bd1d-114">This parameter sets the grbits for commit.</span></span> <span data-ttu-id="5bd1d-115">與實例和 sesid 搭配使用時，它的功能與系統參數 JET_param CommitDefault 相同。</span><span class="sxs-lookup"><span data-stu-id="5bd1d-115">It is functionally the same as the system parameter JET_param.CommitDefault when used with an instance and a sesid.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="5bd1d-116">CommitGenericCoNtext</span><span class="sxs-lookup"><span data-stu-id="5bd1d-116">CommitGenericContext</span></span></td>
<td><span data-ttu-id="5bd1d-117">此參數會設定將在認可至層級0時放置於交易記錄中的使用者特定認可內容。</span><span class="sxs-lookup"><span data-stu-id="5bd1d-117">This parameter sets a user specific commit context that will be placed in the transaction log on commit to level 0.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="5bd1d-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5bd1d-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5bd1d-119">參考</span><span class="sxs-lookup"><span data-stu-id="5bd1d-119">Reference</span></span>

[<span data-ttu-id="5bd1d-120">Windows8 命名空間。</span><span class="sxs-lookup"><span data-stu-id="5bd1d-120">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
