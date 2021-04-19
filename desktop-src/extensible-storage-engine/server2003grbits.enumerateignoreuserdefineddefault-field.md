---
description: 深入瞭解： Server2003Grbits. EnumerateIgnoreUserDefinedDefault 欄位
title: 'Server2003Grbits. EnumerateIgnoreUserDefinedDefault 欄位 (欄位，Server2003) '
TOCTitle: EnumerateIgnoreUserDefinedDefault field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.EnumerateIgnoreUserDefinedDefault
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003grbits.enumerateignoreuserdefineddefault(v=EXCHG.10)
ms:contentKeyID: 55104099
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.EnumerateIgnoreUserDefinedDefault
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.EnumerateIgnoreUserDefinedDefault
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 508565c518b67d31b0299014817b669f9484f743
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992468"
---
# <a name="server2003grbitsenumerateignoreuserdefineddefault-field"></a><span data-ttu-id="25bd7-103">Server2003Grbits. EnumerateIgnoreUserDefinedDefault 欄位</span><span class="sxs-lookup"><span data-stu-id="25bd7-103">Server2003Grbits.EnumerateIgnoreUserDefinedDefault field</span></span>

<span data-ttu-id="25bd7-104">如果指定的資料行不存在於記錄中，而且它具有使用者定義的預設值，則不會傳回任何資料行值。</span><span class="sxs-lookup"><span data-stu-id="25bd7-104">If a given column is not present in the record and it has a user defined default value then no column value will be returned.</span></span> <span data-ttu-id="25bd7-105">此選項可防止在列舉該資料行的值時，計算資料行之使用者定義預設值的回呼。</span><span class="sxs-lookup"><span data-stu-id="25bd7-105">This option will prevent the callback that computes the user defined default value for the column from being called when enumerating the values for that column.</span></span>

<span data-ttu-id="25bd7-106">**命名空間：**  [Microsoft Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="25bd7-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span></span>  
<span data-ttu-id="25bd7-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="25bd7-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="25bd7-108">語法</span><span class="sxs-lookup"><span data-stu-id="25bd7-108">Syntax</span></span>

``` vb
'Declaration
Public Const EnumerateIgnoreUserDefinedDefault As EnumerateColumnsGrbit
'Usage
Dim value As EnumerateColumnsGrbit

value = Server2003Grbits.EnumerateIgnoreUserDefinedDefault
```

``` csharp
public const EnumerateColumnsGrbit EnumerateIgnoreUserDefinedDefault
```

## <a name="remarks"></a><span data-ttu-id="25bd7-109">備註</span><span class="sxs-lookup"><span data-stu-id="25bd7-109">Remarks</span></span>

<span data-ttu-id="25bd7-110">此選項僅適用于 Windows Server 2003 SP1 和更新版本的作業系統。</span><span class="sxs-lookup"><span data-stu-id="25bd7-110">This option is only available for Windows Server 2003 SP1 and later operating systems.</span></span>

## <a name="see-also"></a><span data-ttu-id="25bd7-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="25bd7-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="25bd7-112">參考</span><span class="sxs-lookup"><span data-stu-id="25bd7-112">Reference</span></span>

[<span data-ttu-id="25bd7-113">Server2003Grbits 類別</span><span class="sxs-lookup"><span data-stu-id="25bd7-113">Server2003Grbits class</span></span>](./server2003grbits-class.md)

[<span data-ttu-id="25bd7-114">Server2003Grbits 成員</span><span class="sxs-lookup"><span data-stu-id="25bd7-114">Server2003Grbits members</span></span>](./server2003grbits-members.md)

[<span data-ttu-id="25bd7-115">Server2003 命名空間。</span><span class="sxs-lookup"><span data-stu-id="25bd7-115">Microsoft.Isam.Esent.Interop.Server2003 namespace</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)
