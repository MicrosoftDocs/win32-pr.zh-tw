---
description: 深入瞭解： JetResetTableSequential 方法
title: JetResetTableSequential 方法
TOCTitle: 'JetResetTableSequential method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetResetTableSequential(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.ResetTableSequentialGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetresettablesequential(v=EXCHG.10)
ms:contentKeyID: 55100789
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetResetTableSequential
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetResetTableSequential
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b45ca118894015df7cda56201733cdaad9b88d69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195018"
---
# <a name="apijetresettablesequential-method"></a><span data-ttu-id="095ef-103">JetResetTableSequential 方法</span><span class="sxs-lookup"><span data-stu-id="095ef-103">Api.JetResetTableSequential method</span></span>

<span data-ttu-id="095ef-104">通知資料庫引擎應用程式不再掃描游標所在的整個索引。</span><span class="sxs-lookup"><span data-stu-id="095ef-104">Notifies the database engine that the application is no longer scanning the entire index the cursor is positioned on.</span></span> <span data-ttu-id="095ef-105">此呼叫會反轉 [JetSetTableSequential (JET_SESID、JET_TABLEID、SetTableSequentialGrbit) ](./api.jetsettablesequential-method.md)所傳送的通知。</span><span class="sxs-lookup"><span data-stu-id="095ef-105">This call reverses a notification sent by [JetSetTableSequential(JET_SESID, JET_TABLEID, SetTableSequentialGrbit)](./api.jetsettablesequential-method.md).</span></span>

<span data-ttu-id="095ef-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="095ef-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="095ef-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="095ef-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="095ef-108">語法</span><span class="sxs-lookup"><span data-stu-id="095ef-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetResetTableSequential ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As ResetTableSequentialGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As ResetTableSequentialGrbitApi.JetResetTableSequential(sesid, _
    tableid, grbit)
```

``` csharp
public static void JetResetTableSequential(
    JET_SESID sesid,
    JET_TABLEID tableid,
    ResetTableSequentialGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="095ef-109">參數</span><span class="sxs-lookup"><span data-stu-id="095ef-109">Parameters</span></span>

  - <span data-ttu-id="095ef-110">sesid</span><span class="sxs-lookup"><span data-stu-id="095ef-110">sesid</span></span>  
    <span data-ttu-id="095ef-111">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="095ef-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="095ef-112">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="095ef-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="095ef-113">tableid</span><span class="sxs-lookup"><span data-stu-id="095ef-113">tableid</span></span>  
    <span data-ttu-id="095ef-114">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="095ef-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="095ef-115">存取資料的資料指標。</span><span class="sxs-lookup"><span data-stu-id="095ef-115">The cursor that was accessing the data.</span></span>

<!-- end list -->

  - <span data-ttu-id="095ef-116">grbit</span><span class="sxs-lookup"><span data-stu-id="095ef-116">grbit</span></span>  
    <span data-ttu-id="095ef-117">型別： [ResetTableSequentialGrbit](./resettablesequentialgrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="095ef-117">Type: [Microsoft.Isam.Esent.Interop.ResetTableSequentialGrbit](./resettablesequentialgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="095ef-118">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="095ef-118">Reserved for future use.</span></span>

## <a name="see-also"></a><span data-ttu-id="095ef-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="095ef-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="095ef-120">參考</span><span class="sxs-lookup"><span data-stu-id="095ef-120">Reference</span></span>

[<span data-ttu-id="095ef-121">Api 類別</span><span class="sxs-lookup"><span data-stu-id="095ef-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="095ef-122">Api 成員</span><span class="sxs-lookup"><span data-stu-id="095ef-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="095ef-123">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="095ef-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
