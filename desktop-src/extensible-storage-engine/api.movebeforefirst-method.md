---
description: 深入瞭解： MoveBeforeFirst 方法
title: MoveBeforeFirst 方法
TOCTitle: 'MoveBeforeFirst method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.MoveBeforeFirst(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.movebeforefirst(v=EXCHG.10)
ms:contentKeyID: 55100849
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.MoveBeforeFirst
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.MoveBeforeFirst
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1c3e49762c0d2be1f416181f5c07fb06b088d161
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970750"
---
# <a name="apimovebeforefirst-method"></a><span data-ttu-id="367cd-103">MoveBeforeFirst 方法</span><span class="sxs-lookup"><span data-stu-id="367cd-103">Api.MoveBeforeFirst method</span></span>

<span data-ttu-id="367cd-104">將游標放在資料表的第一筆記錄之前。</span><span class="sxs-lookup"><span data-stu-id="367cd-104">Position the cursor before the first record in the table.</span></span> <span data-ttu-id="367cd-105">接下來的移動會將游標放在第一筆記錄。</span><span class="sxs-lookup"><span data-stu-id="367cd-105">A subsequent move next will position the cursor on the first record.</span></span>

<span data-ttu-id="367cd-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="367cd-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="367cd-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="367cd-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="367cd-108">語法</span><span class="sxs-lookup"><span data-stu-id="367cd-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub MoveBeforeFirst ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEIDApi.MoveBeforeFirst(sesid, tableid)
```

``` csharp
public static void MoveBeforeFirst(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="367cd-109">參數</span><span class="sxs-lookup"><span data-stu-id="367cd-109">Parameters</span></span>

  - <span data-ttu-id="367cd-110">sesid</span><span class="sxs-lookup"><span data-stu-id="367cd-110">sesid</span></span>  
    <span data-ttu-id="367cd-111">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="367cd-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="367cd-112">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="367cd-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="367cd-113">tableid</span><span class="sxs-lookup"><span data-stu-id="367cd-113">tableid</span></span>  
    <span data-ttu-id="367cd-114">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="367cd-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="367cd-115">要放置的資料表。</span><span class="sxs-lookup"><span data-stu-id="367cd-115">The table to position.</span></span>

## <a name="see-also"></a><span data-ttu-id="367cd-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="367cd-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="367cd-117">參考</span><span class="sxs-lookup"><span data-stu-id="367cd-117">Reference</span></span>

[<span data-ttu-id="367cd-118">Api 類別</span><span class="sxs-lookup"><span data-stu-id="367cd-118">Api class</span></span>](./api-class.md)

[<span data-ttu-id="367cd-119">Api 成員</span><span class="sxs-lookup"><span data-stu-id="367cd-119">Api members</span></span>](./api-members.md)

[<span data-ttu-id="367cd-120">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="367cd-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
