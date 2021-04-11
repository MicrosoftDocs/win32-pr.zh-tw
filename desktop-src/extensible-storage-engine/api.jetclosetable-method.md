---
description: 深入瞭解： JetCloseTable 方法
title: JetCloseTable 方法
TOCTitle: 'JetCloseTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCloseTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetclosetable(v=EXCHG.10)
ms:contentKeyID: 55100664
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCloseTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCloseTable
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fee4ad7d7accf71bd4c3439f954ee36badd2ea20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943307"
---
# <a name="apijetclosetable-method"></a><span data-ttu-id="052a3-103">JetCloseTable 方法</span><span class="sxs-lookup"><span data-stu-id="052a3-103">Api.JetCloseTable method</span></span>

<span data-ttu-id="052a3-104">關閉開啟的資料表。</span><span class="sxs-lookup"><span data-stu-id="052a3-104">Close an open table.</span></span>

<span data-ttu-id="052a3-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="052a3-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="052a3-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="052a3-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="052a3-107">語法</span><span class="sxs-lookup"><span data-stu-id="052a3-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCloseTable ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEIDApi.JetCloseTable(sesid, tableid)
```

``` csharp
public static void JetCloseTable(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="052a3-108">參數</span><span class="sxs-lookup"><span data-stu-id="052a3-108">Parameters</span></span>

  - <span data-ttu-id="052a3-109">sesid</span><span class="sxs-lookup"><span data-stu-id="052a3-109">sesid</span></span>  
    <span data-ttu-id="052a3-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="052a3-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="052a3-111">開啟資料表的會話。</span><span class="sxs-lookup"><span data-stu-id="052a3-111">The session which opened the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="052a3-112">tableid</span><span class="sxs-lookup"><span data-stu-id="052a3-112">tableid</span></span>  
    <span data-ttu-id="052a3-113">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="052a3-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="052a3-114">要關閉的資料表。</span><span class="sxs-lookup"><span data-stu-id="052a3-114">The table to close.</span></span>

## <a name="see-also"></a><span data-ttu-id="052a3-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="052a3-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="052a3-116">參考</span><span class="sxs-lookup"><span data-stu-id="052a3-116">Reference</span></span>

[<span data-ttu-id="052a3-117">Api 類別</span><span class="sxs-lookup"><span data-stu-id="052a3-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="052a3-118">Api 成員</span><span class="sxs-lookup"><span data-stu-id="052a3-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="052a3-119">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="052a3-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
