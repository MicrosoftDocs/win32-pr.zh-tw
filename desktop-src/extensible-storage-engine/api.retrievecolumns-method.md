---
description: 深入瞭解： RetrieveColumns 方法
title: RetrieveColumns 方法
TOCTitle: 'RetrieveColumns method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.ColumnValue[])
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumns(v=EXCHG.10)
ms:contentKeyID: 55100867
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumns
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumns
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c981ad8b8e90db10bb8735aa349315b769e6641f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510840"
---
# <a name="apiretrievecolumns-method"></a><span data-ttu-id="36bab-103">RetrieveColumns 方法</span><span class="sxs-lookup"><span data-stu-id="36bab-103">Api.RetrieveColumns method</span></span>

<span data-ttu-id="36bab-104">將資料行抓取 ColumnValue 物件。</span><span class="sxs-lookup"><span data-stu-id="36bab-104">Retrieves columns into ColumnValue objects.</span></span>

<span data-ttu-id="36bab-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="36bab-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="36bab-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="36bab-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="36bab-107">語法</span><span class="sxs-lookup"><span data-stu-id="36bab-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub RetrieveColumns ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    ParamArray values As ColumnValue() _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim values As ColumnValue()

Api.RetrieveColumns(sesid, tableid, _
    values)
```

``` csharp
public static void RetrieveColumns(
    JET_SESID sesid,
    JET_TABLEID tableid,
    params ColumnValue[] values
)
```

#### <a name="parameters"></a><span data-ttu-id="36bab-108">參數</span><span class="sxs-lookup"><span data-stu-id="36bab-108">Parameters</span></span>

  - <span data-ttu-id="36bab-109">sesid</span><span class="sxs-lookup"><span data-stu-id="36bab-109">sesid</span></span>  
    <span data-ttu-id="36bab-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="36bab-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="36bab-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="36bab-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="36bab-112">tableid</span><span class="sxs-lookup"><span data-stu-id="36bab-112">tableid</span></span>  
    <span data-ttu-id="36bab-113">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="36bab-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="36bab-114">資料指標會從取得資料。</span><span class="sxs-lookup"><span data-stu-id="36bab-114">The cursor retrieve the data from.</span></span> <span data-ttu-id="36bab-115">資料指標應放置在記錄上。</span><span class="sxs-lookup"><span data-stu-id="36bab-115">The cursor should be positioned on a record.</span></span>

<!-- end list -->

  - <span data-ttu-id="36bab-116">值</span><span class="sxs-lookup"><span data-stu-id="36bab-116">values</span></span>  
    <span data-ttu-id="36bab-117">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="36bab-117">Type: \[\]</span></span>  
    
    <span data-ttu-id="36bab-118">要取出的值。</span><span class="sxs-lookup"><span data-stu-id="36bab-118">The values to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="36bab-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="36bab-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="36bab-120">參考</span><span class="sxs-lookup"><span data-stu-id="36bab-120">Reference</span></span>

[<span data-ttu-id="36bab-121">Api 類別</span><span class="sxs-lookup"><span data-stu-id="36bab-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="36bab-122">Api 成員</span><span class="sxs-lookup"><span data-stu-id="36bab-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="36bab-123">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="36bab-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
