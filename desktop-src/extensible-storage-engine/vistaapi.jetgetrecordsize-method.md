---
description: 深入瞭解： VistaApi. JetGetRecordSize 方法
title: 'VistaApi. JetGetRecordSize 方法 (< a0/&gt; < a1/&gt;) '
TOCTitle: 'JetGetRecordSize method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetRecordSize(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE@,Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetgetrecordsize(v=EXCHG.10)
ms:contentKeyID: 55104285
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetRecordSize
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetRecordSize
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37576e39d83270dcac3333e4d1f78fce32bb2669
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991829"
---
# <a name="vistaapijetgetrecordsize-method"></a><span data-ttu-id="93ae0-103">VistaApi. JetGetRecordSize 方法</span><span class="sxs-lookup"><span data-stu-id="93ae0-103">VistaApi.JetGetRecordSize method</span></span>

<span data-ttu-id="93ae0-104">從所需的位置抓取記錄大小資訊。</span><span class="sxs-lookup"><span data-stu-id="93ae0-104">Retrieves record size information from the desired location.</span></span>

<span data-ttu-id="93ae0-105">**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。  </span><span class="sxs-lookup"><span data-stu-id="93ae0-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="93ae0-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="93ae0-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="93ae0-107">語法</span><span class="sxs-lookup"><span data-stu-id="93ae0-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetRecordSize ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    ByRef recsize As JET_RECSIZE, _
    grbit As GetRecordSizeGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim recsize As JET_RECSIZE
Dim grbit As GetRecordSizeGrbitVistaApi.JetGetRecordSize(sesid, tableid, _
    recsize, grbit)
```

``` csharp
public static void JetGetRecordSize(
    JET_SESID sesid,
    JET_TABLEID tableid,
    ref JET_RECSIZE recsize,
    GetRecordSizeGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="93ae0-108">參數</span><span class="sxs-lookup"><span data-stu-id="93ae0-108">Parameters</span></span>

  - <span data-ttu-id="93ae0-109">sesid</span><span class="sxs-lookup"><span data-stu-id="93ae0-109">sesid</span></span>  
    <span data-ttu-id="93ae0-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="93ae0-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="93ae0-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="93ae0-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="93ae0-112">tableid</span><span class="sxs-lookup"><span data-stu-id="93ae0-112">tableid</span></span>  
    <span data-ttu-id="93ae0-113">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="93ae0-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="93ae0-114">將用於 API 呼叫的資料指標。</span><span class="sxs-lookup"><span data-stu-id="93ae0-114">The cursor that will be used for the API call.</span></span> <span data-ttu-id="93ae0-115">資料指標必須放置在記錄上，或已備妥更新。</span><span class="sxs-lookup"><span data-stu-id="93ae0-115">The cursor must be positioned on a record, or have an update prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="93ae0-116">recsize</span><span class="sxs-lookup"><span data-stu-id="93ae0-116">recsize</span></span>  
    <span data-ttu-id="93ae0-117">類型： [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="93ae0-117">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="93ae0-118">傳回記錄的大小。</span><span class="sxs-lookup"><span data-stu-id="93ae0-118">Returns the size of the record.</span></span>

<!-- end list -->

  - <span data-ttu-id="93ae0-119">grbit</span><span class="sxs-lookup"><span data-stu-id="93ae0-119">grbit</span></span>  
    <span data-ttu-id="93ae0-120">型別： [GetRecordSizeGrbit](./getrecordsizegrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="93ae0-120">Type: [Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit](./getrecordsizegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="93ae0-121">通話選項。</span><span class="sxs-lookup"><span data-stu-id="93ae0-121">Call options.</span></span>

## <a name="see-also"></a><span data-ttu-id="93ae0-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="93ae0-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="93ae0-123">參考</span><span class="sxs-lookup"><span data-stu-id="93ae0-123">Reference</span></span>

[<span data-ttu-id="93ae0-124">VistaApi 類別</span><span class="sxs-lookup"><span data-stu-id="93ae0-124">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="93ae0-125">VistaApi 成員</span><span class="sxs-lookup"><span data-stu-id="93ae0-125">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="93ae0-126">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="93ae0-126">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
