---
description: 深入瞭解： LegacyFileNames 列舉
title: 'LegacyFileNames 列舉 (的列舉) '
TOCTitle: LegacyFileNames enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Vista.LegacyFileNames
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.legacyfilenames(v=EXCHG.10)
ms:contentKeyID: 55104275
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.LegacyFileNames
- Microsoft.Isam.Esent.Interop.Vista.LegacyFileNames.EightDotThreeSoftCompat
- Microsoft.Isam.Esent.Interop.Vista.LegacyFileNames.ESE98FileNames
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.LegacyFileNames.EightDotThreeSoftCompat
- Microsoft.Isam.Esent.Interop.Vista.LegacyFileNames
- Microsoft.Isam.Esent.Interop.Vista.LegacyFileNames.ESE98FileNames
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d7f3cade11450bcfbad13dcdd114dca6701c5369
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943527"
---
# <a name="legacyfilenames-enumeration"></a><span data-ttu-id="61ef9-103">LegacyFileNames 列舉</span><span class="sxs-lookup"><span data-stu-id="61ef9-103">LegacyFileNames enumeration</span></span>

<span data-ttu-id="61ef9-104">LegacyFileNames 的選項</span><span class="sxs-lookup"><span data-stu-id="61ef9-104">Options for LegacyFileNames</span></span>

<span data-ttu-id="61ef9-105">**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。  </span><span class="sxs-lookup"><span data-stu-id="61ef9-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="61ef9-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="61ef9-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="61ef9-107">語法</span><span class="sxs-lookup"><span data-stu-id="61ef9-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration LegacyFileNames
'Usage
Dim instance As LegacyFileNames
```

``` csharp
public enum LegacyFileNames
```

## <a name="members"></a><span data-ttu-id="61ef9-108">成員</span><span class="sxs-lookup"><span data-stu-id="61ef9-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="61ef9-109">成員名稱</span><span class="sxs-lookup"><span data-stu-id="61ef9-109">Member name</span></span></th>
<th><span data-ttu-id="61ef9-110">說明</span><span class="sxs-lookup"><span data-stu-id="61ef9-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="61ef9-111">ESE98FileNames</span><span class="sxs-lookup"><span data-stu-id="61ef9-111">ESE98FileNames</span></span></td>
<td><span data-ttu-id="61ef9-112">當這個選項存在時，database engine 將會針對其檔案使用下列命名慣例： o 交易記錄檔將會使用。記錄檔，其副檔名為 o 的檢查點檔案將會使用。副檔名的 .CHK</span><span class="sxs-lookup"><span data-stu-id="61ef9-112">When this option is present then the database engine will use the following naming conventions for its files: o Transaction Log files will use .LOG for their file extension o Checkpoint files will use .CHK for their file extension</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="61ef9-113">EightDotThreeSoftCompat</span><span class="sxs-lookup"><span data-stu-id="61ef9-113">EightDotThreeSoftCompat</span></span></td>
<td><span data-ttu-id="61ef9-114">盡可能保留8.3 命名語法。</span><span class="sxs-lookup"><span data-stu-id="61ef9-114">Preserve the 8.3 naming syntax for as long as possible.</span></span> <span data-ttu-id="61ef9-115"> (不應變更，請確保沒有記錄檔) </span><span class="sxs-lookup"><span data-stu-id="61ef9-115">(this should not be changed, w/o ensuring there are no log files)</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="61ef9-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="61ef9-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="61ef9-117">參考</span><span class="sxs-lookup"><span data-stu-id="61ef9-117">Reference</span></span>

[<span data-ttu-id="61ef9-118">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="61ef9-118">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
