---
description: 深入瞭解： JET_filetype 列舉
title: JET_filetype 列舉
TOCTitle: JET_filetype enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_filetype
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_filetype(v=EXCHG.10)
ms:contentKeyID: 39516829
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_filetype
- Microsoft.Isam.Esent.Interop.JET_filetype.Checkpoint
- Microsoft.Isam.Esent.Interop.JET_filetype.Database
- Microsoft.Isam.Esent.Interop.JET_filetype.Log
- Microsoft.Isam.Esent.Interop.JET_filetype.TempDatabase
- Microsoft.Isam.Esent.Interop.JET_filetype.Unknown
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_filetype.Database
- Microsoft.Isam.Esent.Interop.JET_filetype
- Microsoft.Isam.Esent.Interop.JET_filetype.Unknown
- Microsoft.Isam.Esent.Interop.JET_filetype.Log
- Microsoft.Isam.Esent.Interop.JET_filetype.Checkpoint
- Microsoft.Isam.Esent.Interop.JET_filetype.TempDatabase
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6e1f6b21d521babdf7b5c36411ea8bd19d5ebba3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849550"
---
# <a name="jet_filetype-enumeration"></a><span data-ttu-id="787b8-103">JET_filetype 列舉</span><span class="sxs-lookup"><span data-stu-id="787b8-103">JET_filetype enumeration</span></span>

<span data-ttu-id="787b8-104">Esent 檔案類型。</span><span class="sxs-lookup"><span data-stu-id="787b8-104">Esent file types.</span></span>

<span data-ttu-id="787b8-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="787b8-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="787b8-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="787b8-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="787b8-107">語法</span><span class="sxs-lookup"><span data-stu-id="787b8-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_filetype
'Usage
Dim instance As JET_filetype
```

``` csharp
public enum JET_filetype
```

## <a name="members"></a><span data-ttu-id="787b8-108">成員</span><span class="sxs-lookup"><span data-stu-id="787b8-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="787b8-109">成員名稱</span><span class="sxs-lookup"><span data-stu-id="787b8-109">Member name</span></span></th>
<th><span data-ttu-id="787b8-110">說明</span><span class="sxs-lookup"><span data-stu-id="787b8-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="787b8-111">Unknown</span><span class="sxs-lookup"><span data-stu-id="787b8-111">Unknown</span></span></td>
<td><span data-ttu-id="787b8-112">未知的檔案。</span><span class="sxs-lookup"><span data-stu-id="787b8-112">Unknown file.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="787b8-113">資料庫</span><span class="sxs-lookup"><span data-stu-id="787b8-113">Database</span></span></td>
<td><span data-ttu-id="787b8-114">資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="787b8-114">Database file.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="787b8-115">記錄</span><span class="sxs-lookup"><span data-stu-id="787b8-115">Log</span></span></td>
<td><span data-ttu-id="787b8-116">交易記錄檔。</span><span class="sxs-lookup"><span data-stu-id="787b8-116">Transaction log.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="787b8-117">Checkpoint</span><span class="sxs-lookup"><span data-stu-id="787b8-117">Checkpoint</span></span></td>
<td><span data-ttu-id="787b8-118">檢查點檔案。</span><span class="sxs-lookup"><span data-stu-id="787b8-118">Checkpoint file.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="787b8-119">TempDatabase</span><span class="sxs-lookup"><span data-stu-id="787b8-119">TempDatabase</span></span></td>
<td><span data-ttu-id="787b8-120">暫存資料庫。</span><span class="sxs-lookup"><span data-stu-id="787b8-120">Temporary database.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="787b8-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="787b8-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="787b8-122">參考</span><span class="sxs-lookup"><span data-stu-id="787b8-122">Reference</span></span>

[<span data-ttu-id="787b8-123">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="787b8-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
