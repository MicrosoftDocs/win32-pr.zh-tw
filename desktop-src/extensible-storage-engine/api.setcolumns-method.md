---
description: 深入瞭解： SetColumns 方法
title: SetColumns 方法
TOCTitle: 'SetColumns method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SetColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.ColumnValue[])
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.setcolumns(v=EXCHG.10)
ms:contentKeyID: 55100936
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.SetColumns
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.SetColumns
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f4ed75c668c0000c1d01d521a57ead46055bc8e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689415"
---
# <a name="apisetcolumns-method"></a><span data-ttu-id="6d36e-103">SetColumns 方法</span><span class="sxs-lookup"><span data-stu-id="6d36e-103">Api.SetColumns method</span></span>

<span data-ttu-id="6d36e-104">設定 ColumnValue 物件中的資料行。</span><span class="sxs-lookup"><span data-stu-id="6d36e-104">Sets columns from ColumnValue objects.</span></span>

<span data-ttu-id="6d36e-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6d36e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6d36e-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="6d36e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6d36e-107">語法</span><span class="sxs-lookup"><span data-stu-id="6d36e-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub SetColumns ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    ParamArray values As ColumnValue() _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim values As ColumnValue()

Api.SetColumns(sesid, tableid, values)
```

``` csharp
public static void SetColumns(
    JET_SESID sesid,
    JET_TABLEID tableid,
    params ColumnValue[] values
)
```

#### <a name="parameters"></a><span data-ttu-id="6d36e-108">參數</span><span class="sxs-lookup"><span data-stu-id="6d36e-108">Parameters</span></span>

  - <span data-ttu-id="6d36e-109">sesid</span><span class="sxs-lookup"><span data-stu-id="6d36e-109">sesid</span></span>  
    <span data-ttu-id="6d36e-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6d36e-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="6d36e-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="6d36e-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="6d36e-112">tableid</span><span class="sxs-lookup"><span data-stu-id="6d36e-112">tableid</span></span>  
    <span data-ttu-id="6d36e-113">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6d36e-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="6d36e-114">要更新的資料指標。</span><span class="sxs-lookup"><span data-stu-id="6d36e-114">The cursor to update.</span></span> <span data-ttu-id="6d36e-115">應備妥更新。</span><span class="sxs-lookup"><span data-stu-id="6d36e-115">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="6d36e-116">值</span><span class="sxs-lookup"><span data-stu-id="6d36e-116">values</span></span>  
    <span data-ttu-id="6d36e-117">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="6d36e-117">Type: \[\]</span></span>  
    
    <span data-ttu-id="6d36e-118">要設定的值。</span><span class="sxs-lookup"><span data-stu-id="6d36e-118">The values to set.</span></span>

## <a name="see-also"></a><span data-ttu-id="6d36e-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6d36e-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6d36e-120">參考</span><span class="sxs-lookup"><span data-stu-id="6d36e-120">Reference</span></span>

[<span data-ttu-id="6d36e-121">Api 類別</span><span class="sxs-lookup"><span data-stu-id="6d36e-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="6d36e-122">Api 成員</span><span class="sxs-lookup"><span data-stu-id="6d36e-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="6d36e-123">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="6d36e-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
