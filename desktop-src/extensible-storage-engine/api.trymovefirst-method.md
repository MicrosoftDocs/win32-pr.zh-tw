---
description: 深入瞭解： TryMoveFirst 方法
title: TryMoveFirst 方法
TOCTitle: 'TryMoveFirst method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TryMoveFirst(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.trymovefirst(v=EXCHG.10)
ms:contentKeyID: 55100946
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TryMoveFirst
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TryMoveFirst
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 624fba29ab6fe653b7af674e32b907ea3934d643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991665"
---
# <a name="apitrymovefirst-method"></a><span data-ttu-id="4b4c3-103">TryMoveFirst 方法</span><span class="sxs-lookup"><span data-stu-id="4b4c3-103">Api.TryMoveFirst method</span></span>

<span data-ttu-id="4b4c3-104">請嘗試移至資料表中的第一筆記錄。</span><span class="sxs-lookup"><span data-stu-id="4b4c3-104">Try to move to the first record in the table.</span></span> <span data-ttu-id="4b4c3-105">如果資料表是空的，則會傳回 false，如果發生不同的錯誤，則會擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="4b4c3-105">If the table is empty this returns false, if a different error is encountered an exception is thrown.</span></span>

<span data-ttu-id="4b4c3-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4b4c3-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4b4c3-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="4b4c3-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4b4c3-108">語法</span><span class="sxs-lookup"><span data-stu-id="4b4c3-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function TryMoveFirst ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim returnValue As Boolean

returnValue = Api.TryMoveFirst(sesid, _
    tableid)
```

``` csharp
public static bool TryMoveFirst(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="4b4c3-109">參數</span><span class="sxs-lookup"><span data-stu-id="4b4c3-109">Parameters</span></span>

  - <span data-ttu-id="4b4c3-110">sesid</span><span class="sxs-lookup"><span data-stu-id="4b4c3-110">sesid</span></span>  
    <span data-ttu-id="4b4c3-111">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4b4c3-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="4b4c3-112">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="4b4c3-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="4b4c3-113">tableid</span><span class="sxs-lookup"><span data-stu-id="4b4c3-113">tableid</span></span>  
    <span data-ttu-id="4b4c3-114">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4b4c3-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="4b4c3-115">要放置的游標。</span><span class="sxs-lookup"><span data-stu-id="4b4c3-115">The cursor to position.</span></span>

#### <a name="return-value"></a><span data-ttu-id="4b4c3-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="4b4c3-116">Return value</span></span>

<span data-ttu-id="4b4c3-117">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="4b4c3-117">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="4b4c3-118">如果移動成功則為 True。</span><span class="sxs-lookup"><span data-stu-id="4b4c3-118">True if the move was successful.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4b4c3-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4b4c3-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4b4c3-120">參考</span><span class="sxs-lookup"><span data-stu-id="4b4c3-120">Reference</span></span>

[<span data-ttu-id="4b4c3-121">Api 類別</span><span class="sxs-lookup"><span data-stu-id="4b4c3-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="4b4c3-122">Api 成員</span><span class="sxs-lookup"><span data-stu-id="4b4c3-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="4b4c3-123">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="4b4c3-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
