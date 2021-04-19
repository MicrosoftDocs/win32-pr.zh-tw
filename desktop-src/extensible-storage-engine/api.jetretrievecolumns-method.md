---
description: 深入瞭解： JetRetrieveColumns 方法
title: JetRetrieveColumns 方法
TOCTitle: 'JetRetrieveColumns method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN[],System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetretrievecolumns(v=EXCHG.10)
ms:contentKeyID: 55100797
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumns
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumns
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d3fd4db2ce8cbcad5f74db7d4c95363aa68e9b38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991699"
---
# <a name="apijetretrievecolumns-method"></a><span data-ttu-id="aec41-103">JetRetrieveColumns 方法</span><span class="sxs-lookup"><span data-stu-id="aec41-103">Api.JetRetrieveColumns method</span></span>

<span data-ttu-id="aec41-104">從單一作業中的目前記錄抓取多個資料行值。</span><span class="sxs-lookup"><span data-stu-id="aec41-104">Retrieves multiple column values from the current record in a single operation.</span></span> <span data-ttu-id="aec41-105">JET_RETRIEVECOLUMN 結構的陣列用來描述要抓取的資料行值集合，以及描述要抓取之每個資料行值的輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="aec41-105">An array of JET_RETRIEVECOLUMN structures is used to describe the set of column values to be retrieved, and to describe output buffers for each column value to be retrieved.</span></span>

<span data-ttu-id="aec41-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="aec41-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="aec41-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="aec41-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="aec41-108">語法</span><span class="sxs-lookup"><span data-stu-id="aec41-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetRetrieveColumns ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    retrievecolumns As JET_RETRIEVECOLUMN(), _
    numColumns As Integer _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim retrievecolumns As JET_RETRIEVECOLUMN()
Dim numColumns As Integer
Dim returnValue As JET_wrn

returnValue = Api.JetRetrieveColumns(sesid, _
    tableid, retrievecolumns, numColumns)
```

``` csharp
public static JET_wrn JetRetrieveColumns(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_RETRIEVECOLUMN[] retrievecolumns,
    int numColumns
)
```

#### <a name="parameters"></a><span data-ttu-id="aec41-109">參數</span><span class="sxs-lookup"><span data-stu-id="aec41-109">Parameters</span></span>

  - <span data-ttu-id="aec41-110">sesid</span><span class="sxs-lookup"><span data-stu-id="aec41-110">sesid</span></span>  
    <span data-ttu-id="aec41-111">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="aec41-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="aec41-112">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="aec41-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="aec41-113">tableid</span><span class="sxs-lookup"><span data-stu-id="aec41-113">tableid</span></span>  
    <span data-ttu-id="aec41-114">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="aec41-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="aec41-115">要從中取出資料的資料指標。</span><span class="sxs-lookup"><span data-stu-id="aec41-115">The cursor to retrieve the data from.</span></span>

<!-- end list -->

  - <span data-ttu-id="aec41-116">retrievecolumns</span><span class="sxs-lookup"><span data-stu-id="aec41-116">retrievecolumns</span></span>  
    <span data-ttu-id="aec41-117">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="aec41-117">Type: \[\]</span></span>  
    
    <span data-ttu-id="aec41-118">一或多個 [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) 物件的陣列，描述要取出的資料。</span><span class="sxs-lookup"><span data-stu-id="aec41-118">An array of one or more [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) objects describing the data to be retrieved.</span></span>

<!-- end list -->

  - <span data-ttu-id="aec41-119">numColumns</span><span class="sxs-lookup"><span data-stu-id="aec41-119">numColumns</span></span>  
    <span data-ttu-id="aec41-120">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="aec41-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="aec41-121">Columns 陣列中的專案數。</span><span class="sxs-lookup"><span data-stu-id="aec41-121">The number of entries in the columns array.</span></span>

#### <a name="return-value"></a><span data-ttu-id="aec41-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="aec41-122">Return value</span></span>

<span data-ttu-id="aec41-123">類型： [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="aec41-123">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="aec41-124">如果任何資料行由於長度不足的緩衝區而遭到截斷，則 API 會傳回 [BufferTruncated](./jet-wrn-enumeration.md)。</span><span class="sxs-lookup"><span data-stu-id="aec41-124">If any column retrieved is truncated due to an insufficient length buffer, then the API will return [BufferTruncated](./jet-wrn-enumeration.md).</span></span> <span data-ttu-id="aec41-125">但是，JET_wrnColumnNull 的其他錯誤只會傳回 [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) 物件的錯誤欄位。</span><span class="sxs-lookup"><span data-stu-id="aec41-125">However other errors JET_wrnColumnNull are returned only in the error field of the [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) object.</span></span>  

## <a name="see-also"></a><span data-ttu-id="aec41-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aec41-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="aec41-127">參考</span><span class="sxs-lookup"><span data-stu-id="aec41-127">Reference</span></span>

[<span data-ttu-id="aec41-128">Api 類別</span><span class="sxs-lookup"><span data-stu-id="aec41-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="aec41-129">Api 成員</span><span class="sxs-lookup"><span data-stu-id="aec41-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="aec41-130">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="aec41-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
