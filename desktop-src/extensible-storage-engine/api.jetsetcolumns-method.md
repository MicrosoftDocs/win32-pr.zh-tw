---
description: 深入瞭解： JetSetColumns 方法
title: JetSetColumns 方法
TOCTitle: 'JetSetColumns method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_SETCOLUMN[],System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcolumns(v=EXCHG.10)
ms:contentKeyID: 55100800
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetColumns
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetColumns
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 59d1d16a21996937357d0358625772a4b6712019
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690055"
---
# <a name="apijetsetcolumns-method"></a><span data-ttu-id="26690-103">JetSetColumns 方法</span><span class="sxs-lookup"><span data-stu-id="26690-103">Api.JetSetColumns method</span></span>

<span data-ttu-id="26690-104">允許應用程式在單一作業中設定多個資料行值。</span><span class="sxs-lookup"><span data-stu-id="26690-104">Allows an application to set multiple column values in a single operation.</span></span> <span data-ttu-id="26690-105">[JET_SETCOLUMN](./jet-setcolumn-class.md)結構的陣列用來描述要設定的資料行值集合，以及描述要設定之每個資料行值的輸入緩衝區。</span><span class="sxs-lookup"><span data-stu-id="26690-105">An array of [JET_SETCOLUMN](./jet-setcolumn-class.md) structures is used to describe the set of column values to be set, and to describe input buffers for each column value to be set.</span></span>

<span data-ttu-id="26690-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="26690-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="26690-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="26690-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="26690-108">語法</span><span class="sxs-lookup"><span data-stu-id="26690-108">Syntax</span></span>

``` vb
'Declaration
<SecurityPermissionAttribute(SecurityAction.LinkDemand)> _
Public Shared Function JetSetColumns ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    setcolumns As JET_SETCOLUMN(), _
    numColumns As Integer _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim setcolumns As JET_SETCOLUMN()
Dim numColumns As Integer
Dim returnValue As JET_wrn

returnValue = Api.JetSetColumns(sesid, _
    tableid, setcolumns, numColumns)
```

``` csharp
[SecurityPermissionAttribute(SecurityAction.LinkDemand)]
public static JET_wrn JetSetColumns(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_SETCOLUMN[] setcolumns,
    int numColumns
)
```

#### <a name="parameters"></a><span data-ttu-id="26690-109">參數</span><span class="sxs-lookup"><span data-stu-id="26690-109">Parameters</span></span>

  - <span data-ttu-id="26690-110">sesid</span><span class="sxs-lookup"><span data-stu-id="26690-110">sesid</span></span>  
    <span data-ttu-id="26690-111">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="26690-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="26690-112">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="26690-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="26690-113">tableid</span><span class="sxs-lookup"><span data-stu-id="26690-113">tableid</span></span>  
    <span data-ttu-id="26690-114">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="26690-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="26690-115">要在其上設定資料行的資料指標。</span><span class="sxs-lookup"><span data-stu-id="26690-115">The cursor to set the columns on.</span></span>

<!-- end list -->

  - <span data-ttu-id="26690-116">setcolumns</span><span class="sxs-lookup"><span data-stu-id="26690-116">setcolumns</span></span>  
    <span data-ttu-id="26690-117">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="26690-117">Type: \[\]</span></span>  
    
    <span data-ttu-id="26690-118">[JET_SETCOLUMN](./jet-setcolumn-class.md)結構的陣列，描述要設定的資料。</span><span class="sxs-lookup"><span data-stu-id="26690-118">An array of [JET_SETCOLUMN](./jet-setcolumn-class.md) structures describing the data to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="26690-119">numColumns</span><span class="sxs-lookup"><span data-stu-id="26690-119">numColumns</span></span>  
    <span data-ttu-id="26690-120">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="26690-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="26690-121">Setcolumns 參數中的專案數。</span><span class="sxs-lookup"><span data-stu-id="26690-121">Number of entries in the setcolumns parameter.</span></span>

#### <a name="return-value"></a><span data-ttu-id="26690-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="26690-122">Return value</span></span>

<span data-ttu-id="26690-123">類型： [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="26690-123">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="26690-124">警告。</span><span class="sxs-lookup"><span data-stu-id="26690-124">A warning.</span></span> <span data-ttu-id="26690-125">如果最後一個資料行集有警告，則會從 JetSetColumns 本身傳回此警告。</span><span class="sxs-lookup"><span data-stu-id="26690-125">If the last column set has a warning, then this warning will be returned from JetSetColumns itself.</span></span>  

## <a name="see-also"></a><span data-ttu-id="26690-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="26690-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="26690-127">參考</span><span class="sxs-lookup"><span data-stu-id="26690-127">Reference</span></span>

[<span data-ttu-id="26690-128">Api 類別</span><span class="sxs-lookup"><span data-stu-id="26690-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="26690-129">Api 成員</span><span class="sxs-lookup"><span data-stu-id="26690-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="26690-130">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="26690-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
