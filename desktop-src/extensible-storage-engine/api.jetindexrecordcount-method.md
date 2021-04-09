---
description: 深入瞭解： JetIndexRecordCount 方法
title: JetIndexRecordCount 方法
TOCTitle: 'JetIndexRecordCount method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetIndexRecordCount(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Int32@,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetindexrecordcount(v=EXCHG.10)
ms:contentKeyID: 55100758
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetIndexRecordCount
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetIndexRecordCount
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 429239ab7734a594fd2c5a3510650d8f410e94f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694927"
---
# <a name="apijetindexrecordcount-method"></a><span data-ttu-id="1cd7e-103">JetIndexRecordCount 方法</span><span class="sxs-lookup"><span data-stu-id="1cd7e-103">Api.JetIndexRecordCount method</span></span>

<span data-ttu-id="1cd7e-104">計算目前索引中的專案數，從目前的位置向前算。</span><span class="sxs-lookup"><span data-stu-id="1cd7e-104">Counts the number of entries in the current index from the current position forward.</span></span> <span data-ttu-id="1cd7e-105">目前的位置會包含在計數中。</span><span class="sxs-lookup"><span data-stu-id="1cd7e-105">The current position is included in the count.</span></span> <span data-ttu-id="1cd7e-106">如果目前索引超過多重值資料行，而且資料行的實例具有多個值，則計數可以大於資料表中的記錄總數。</span><span class="sxs-lookup"><span data-stu-id="1cd7e-106">The count can be greater than the total number of records in the table if the current index is over a multi-valued column and instances of the column have multiple-values.</span></span> <span data-ttu-id="1cd7e-107">如果資料表是空的，則會傳回計數的0。</span><span class="sxs-lookup"><span data-stu-id="1cd7e-107">If the table is empty, then 0 will be returned for the count.</span></span>

<span data-ttu-id="1cd7e-108">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1cd7e-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1cd7e-109">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="1cd7e-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1cd7e-110">語法</span><span class="sxs-lookup"><span data-stu-id="1cd7e-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetIndexRecordCount ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef numRecords As Integer, _
    maxRecordsToCount As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim numRecords As Integer
Dim maxRecordsToCount As IntegerApi.JetIndexRecordCount(sesid, _
    tableid, numRecords, maxRecordsToCount)
```

``` csharp
public static void JetIndexRecordCount(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out int numRecords,
    int maxRecordsToCount
)
```

#### <a name="parameters"></a><span data-ttu-id="1cd7e-111">參數</span><span class="sxs-lookup"><span data-stu-id="1cd7e-111">Parameters</span></span>

  - <span data-ttu-id="1cd7e-112">sesid</span><span class="sxs-lookup"><span data-stu-id="1cd7e-112">sesid</span></span>  
    <span data-ttu-id="1cd7e-113">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1cd7e-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="1cd7e-114">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="1cd7e-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="1cd7e-115">tableid</span><span class="sxs-lookup"><span data-stu-id="1cd7e-115">tableid</span></span>  
    <span data-ttu-id="1cd7e-116">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1cd7e-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="1cd7e-117">要計算記錄的資料指標。</span><span class="sxs-lookup"><span data-stu-id="1cd7e-117">The cursor to count the records in.</span></span>

<!-- end list -->

  - <span data-ttu-id="1cd7e-118">numRecords</span><span class="sxs-lookup"><span data-stu-id="1cd7e-118">numRecords</span></span>  
    <span data-ttu-id="1cd7e-119">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="1cd7e-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="1cd7e-120">傳回記錄的數目。</span><span class="sxs-lookup"><span data-stu-id="1cd7e-120">Returns the number of records.</span></span>

<!-- end list -->

  - <span data-ttu-id="1cd7e-121">maxRecordsToCount</span><span class="sxs-lookup"><span data-stu-id="1cd7e-121">maxRecordsToCount</span></span>  
    <span data-ttu-id="1cd7e-122">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="1cd7e-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="1cd7e-123">要計算的記錄數目上限。</span><span class="sxs-lookup"><span data-stu-id="1cd7e-123">The maximum number of records to count.</span></span> <span data-ttu-id="1cd7e-124">值為0表示計數是無限制的。</span><span class="sxs-lookup"><span data-stu-id="1cd7e-124">A value of 0 indicates that the count is unlimited.</span></span>

## <a name="see-also"></a><span data-ttu-id="1cd7e-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1cd7e-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1cd7e-126">參考</span><span class="sxs-lookup"><span data-stu-id="1cd7e-126">Reference</span></span>

[<span data-ttu-id="1cd7e-127">Api 類別</span><span class="sxs-lookup"><span data-stu-id="1cd7e-127">Api class</span></span>](./api-class.md)

[<span data-ttu-id="1cd7e-128">Api 成員</span><span class="sxs-lookup"><span data-stu-id="1cd7e-128">Api members</span></span>](./api-members.md)

[<span data-ttu-id="1cd7e-129">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="1cd7e-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
