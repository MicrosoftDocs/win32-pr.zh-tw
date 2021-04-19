---
description: 深入瞭解： JET_PWSTR
title: JET_PWSTR
TOCTitle: JET_PWSTR
ms:assetid: 6575f0f0-d022-4e70-9f17-c1d884d9e226
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269271(v=EXCHG.10)
ms:contentKeyID: 32765573
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 536ef3bba465f6d152e3483436c1dc1e82277339
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000304"
---
# <a name="jet_pwstr"></a><span data-ttu-id="2c22f-103">JET_PWSTR</span><span class="sxs-lookup"><span data-stu-id="2c22f-103">JET_PWSTR</span></span>


<span data-ttu-id="2c22f-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="2c22f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_pwstr"></a><span data-ttu-id="2c22f-105">JET_PWSTR</span><span class="sxs-lookup"><span data-stu-id="2c22f-105">JET_PWSTR</span></span>

<span data-ttu-id="2c22f-106">**JET_PWSTR** 資料類型包含以 null 終止的 **Unicode** 字串 (char \*) 。</span><span class="sxs-lookup"><span data-stu-id="2c22f-106">The **JET_PWSTR** data type contains a null-terminated **Unicode** string (char \*).</span></span>

<span data-ttu-id="2c22f-107">**Windows vista： JET_PWSTR** 是在 windows vista 中引進。</span><span class="sxs-lookup"><span data-stu-id="2c22f-107">**Windows Vista:  JET_PWSTR** is introduced in Windows Vista.</span></span>

```cpp
    typedef __nullterminated WCHAR * JET_PWSTR;
```

### <a name="data-types"></a><span data-ttu-id="2c22f-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="2c22f-108">Data Types</span></span>

<span data-ttu-id="2c22f-109">JET_PWSTR</span><span class="sxs-lookup"><span data-stu-id="2c22f-109">JET_PWSTR</span></span>

<span data-ttu-id="2c22f-110">以 Null 結束的 Unicode 字串 (char \*) 。</span><span class="sxs-lookup"><span data-stu-id="2c22f-110">Null-terminated, Unicode string (char \*).</span></span>

### <a name="requirements"></a><span data-ttu-id="2c22f-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="2c22f-111">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2c22f-112"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="2c22f-112"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="2c22f-113">需要 Windows Vista。</span><span class="sxs-lookup"><span data-stu-id="2c22f-113">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2c22f-114"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="2c22f-114"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="2c22f-115">需要 Windows Server 2008。</span><span class="sxs-lookup"><span data-stu-id="2c22f-115">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2c22f-116"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="2c22f-116"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="2c22f-117">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="2c22f-117">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

