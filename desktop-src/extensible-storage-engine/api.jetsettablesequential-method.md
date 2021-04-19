---
description: 深入瞭解： JetSetTableSequential 方法
title: JetSetTableSequential 方法
TOCTitle: 'JetSetTableSequential method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetTableSequential(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.SetTableSequentialGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsettablesequential(v=EXCHG.10)
ms:contentKeyID: 55100810
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetTableSequential
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetTableSequential
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 879eca53c4867bb41ee0a231bff9adce39aa58a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997980"
---
# <a name="apijetsettablesequential-method"></a><span data-ttu-id="d54e8-103">JetSetTableSequential 方法</span><span class="sxs-lookup"><span data-stu-id="d54e8-103">Api.JetSetTableSequential method</span></span>

<span data-ttu-id="d54e8-104">通知資料庫引擎應用程式正在掃描資料指標所在的整個索引。</span><span class="sxs-lookup"><span data-stu-id="d54e8-104">Notifies the database engine that the application is scanning the entire index that the cursor is positioned on.</span></span> <span data-ttu-id="d54e8-105">因此，用來存取索引資料的方法將會進行微調，使此案例的速度越快越好。</span><span class="sxs-lookup"><span data-stu-id="d54e8-105">Consequently, the methods that are used to access the index data will be tuned to make this scenario as fast as possible.</span></span> <span data-ttu-id="d54e8-106">另請參閱 [JetResetTableSequential (JET_SESID、JET_TABLEID、ResetTableSequentialGrbit) ](./api.jetresettablesequential-method.md)。</span><span class="sxs-lookup"><span data-stu-id="d54e8-106">Also see [JetResetTableSequential(JET_SESID, JET_TABLEID, ResetTableSequentialGrbit)](./api.jetresettablesequential-method.md).</span></span>

<span data-ttu-id="d54e8-107">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d54e8-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d54e8-108">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="d54e8-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d54e8-109">語法</span><span class="sxs-lookup"><span data-stu-id="d54e8-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetTableSequential ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As SetTableSequentialGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As SetTableSequentialGrbitApi.JetSetTableSequential(sesid, _
    tableid, grbit)
```

``` csharp
public static void JetSetTableSequential(
    JET_SESID sesid,
    JET_TABLEID tableid,
    SetTableSequentialGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="d54e8-110">參數</span><span class="sxs-lookup"><span data-stu-id="d54e8-110">Parameters</span></span>

  - <span data-ttu-id="d54e8-111">sesid</span><span class="sxs-lookup"><span data-stu-id="d54e8-111">sesid</span></span>  
    <span data-ttu-id="d54e8-112">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d54e8-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="d54e8-113">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="d54e8-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="d54e8-114">tableid</span><span class="sxs-lookup"><span data-stu-id="d54e8-114">tableid</span></span>  
    <span data-ttu-id="d54e8-115">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d54e8-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="d54e8-116">將會存取資料的資料指標。</span><span class="sxs-lookup"><span data-stu-id="d54e8-116">The cursor that will be accessing the data.</span></span>

<!-- end list -->

  - <span data-ttu-id="d54e8-117">grbit</span><span class="sxs-lookup"><span data-stu-id="d54e8-117">grbit</span></span>  
    <span data-ttu-id="d54e8-118">型別： [SetTableSequentialGrbit](./settablesequentialgrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="d54e8-118">Type: [Microsoft.Isam.Esent.Interop.SetTableSequentialGrbit](./settablesequentialgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="d54e8-119">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="d54e8-119">Reserved for future use.</span></span>

## <a name="see-also"></a><span data-ttu-id="d54e8-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d54e8-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d54e8-121">參考</span><span class="sxs-lookup"><span data-stu-id="d54e8-121">Reference</span></span>

[<span data-ttu-id="d54e8-122">Api 類別</span><span class="sxs-lookup"><span data-stu-id="d54e8-122">Api class</span></span>](./api-class.md)

[<span data-ttu-id="d54e8-123">Api 成員</span><span class="sxs-lookup"><span data-stu-id="d54e8-123">Api members</span></span>](./api-members.md)

[<span data-ttu-id="d54e8-124">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="d54e8-124">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
