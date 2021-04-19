---
description: 深入瞭解： MoveAfterLast 方法
title: MoveAfterLast 方法
TOCTitle: 'MoveAfterLast method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.MoveAfterLast(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.moveafterlast(v=EXCHG.10)
ms:contentKeyID: 55100851
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.MoveAfterLast
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.MoveAfterLast
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37d3e4eae32c9540f3ee469e4b782c893aa15c38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997995"
---
# <a name="apimoveafterlast-method"></a><span data-ttu-id="500b8-103">MoveAfterLast 方法</span><span class="sxs-lookup"><span data-stu-id="500b8-103">Api.MoveAfterLast method</span></span>

<span data-ttu-id="500b8-104">將游標放在資料表中的最後一筆記錄之後。</span><span class="sxs-lookup"><span data-stu-id="500b8-104">Position the cursor after the last record in the table.</span></span> <span data-ttu-id="500b8-105">接下來的移動會將游標放在最後一筆記錄上。</span><span class="sxs-lookup"><span data-stu-id="500b8-105">A subsequent move previous will position the cursor on the last record.</span></span>

<span data-ttu-id="500b8-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="500b8-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="500b8-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="500b8-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="500b8-108">語法</span><span class="sxs-lookup"><span data-stu-id="500b8-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub MoveAfterLast ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEIDApi.MoveAfterLast(sesid, tableid)
```

``` csharp
public static void MoveAfterLast(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="500b8-109">參數</span><span class="sxs-lookup"><span data-stu-id="500b8-109">Parameters</span></span>

  - <span data-ttu-id="500b8-110">sesid</span><span class="sxs-lookup"><span data-stu-id="500b8-110">sesid</span></span>  
    <span data-ttu-id="500b8-111">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="500b8-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="500b8-112">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="500b8-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="500b8-113">tableid</span><span class="sxs-lookup"><span data-stu-id="500b8-113">tableid</span></span>  
    <span data-ttu-id="500b8-114">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="500b8-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="500b8-115">要放置的資料表。</span><span class="sxs-lookup"><span data-stu-id="500b8-115">The table to position.</span></span>

## <a name="see-also"></a><span data-ttu-id="500b8-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="500b8-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="500b8-117">參考</span><span class="sxs-lookup"><span data-stu-id="500b8-117">Reference</span></span>

[<span data-ttu-id="500b8-118">Api 類別</span><span class="sxs-lookup"><span data-stu-id="500b8-118">Api class</span></span>](./api-class.md)

[<span data-ttu-id="500b8-119">Api 成員</span><span class="sxs-lookup"><span data-stu-id="500b8-119">Api members</span></span>](./api-members.md)

[<span data-ttu-id="500b8-120">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="500b8-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
