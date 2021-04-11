---
description: '深入瞭解： SetColumn 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID、字串、編碼、SetColumnGrbit) '
title: 'SetColumn 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID、字串、編碼、SetColumnGrbit) '
TOCTitle: SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, String, Encoding, SetColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.String,System.Text.Encoding,Microsoft.Isam.Esent.Interop.SetColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.setcolumn(v=EXCHG.10)
ms:contentKeyID: 55100886
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.SetColumn
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3f208f6d07bb7bf02c352263933f7eff68613d37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318011"
---
# <a name="apisetcolumn-method-jet_sesid-jet_tableid-jet_columnid-string-encoding-setcolumngrbit"></a><span data-ttu-id="ce157-103">SetColumn 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID、字串、編碼、SetColumnGrbit) </span><span class="sxs-lookup"><span data-stu-id="ce157-103">Api.SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, String, Encoding, SetColumnGrbit)</span></span>

<span data-ttu-id="ce157-104">修改修改過的記錄中要插入的單一資料行值，或更新目前的記錄。</span><span class="sxs-lookup"><span data-stu-id="ce157-104">Modifies a single column value in a modified record to be inserted or to update the current record.</span></span>

<span data-ttu-id="ce157-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ce157-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ce157-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="ce157-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ce157-107">語法</span><span class="sxs-lookup"><span data-stu-id="ce157-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub SetColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As String, _
    encoding As Encoding, _
    grbit As SetColumnGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As String
Dim encoding As Encoding
Dim grbit As SetColumnGrbitApi.SetColumn(sesid, tableid, columnid, _
    data, encoding, grbit)
```

``` csharp
public static void SetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    string data,
    Encoding encoding,
    SetColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="ce157-108">參數</span><span class="sxs-lookup"><span data-stu-id="ce157-108">Parameters</span></span>

  - <span data-ttu-id="ce157-109">sesid</span><span class="sxs-lookup"><span data-stu-id="ce157-109">sesid</span></span>  
    <span data-ttu-id="ce157-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ce157-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="ce157-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="ce157-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="ce157-112">tableid</span><span class="sxs-lookup"><span data-stu-id="ce157-112">tableid</span></span>  
    <span data-ttu-id="ce157-113">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ce157-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="ce157-114">要更新的資料指標。</span><span class="sxs-lookup"><span data-stu-id="ce157-114">The cursor to update.</span></span> <span data-ttu-id="ce157-115">應備妥更新。</span><span class="sxs-lookup"><span data-stu-id="ce157-115">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="ce157-116">columnid</span><span class="sxs-lookup"><span data-stu-id="ce157-116">columnid</span></span>  
    <span data-ttu-id="ce157-117">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ce157-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="ce157-118">要設定的 columnid。</span><span class="sxs-lookup"><span data-stu-id="ce157-118">The columnid to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="ce157-119">data</span><span class="sxs-lookup"><span data-stu-id="ce157-119">data</span></span>  
    <span data-ttu-id="ce157-120">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="ce157-120">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="ce157-121">要設定的資料。</span><span class="sxs-lookup"><span data-stu-id="ce157-121">The data to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="ce157-122">編碼</span><span class="sxs-lookup"><span data-stu-id="ce157-122">encoding</span></span>  
    <span data-ttu-id="ce157-123">類型： [system.object。編碼](/dotnet/api/system.text.encoding)</span><span class="sxs-lookup"><span data-stu-id="ce157-123">Type: [System.Text.Encoding](/dotnet/api/system.text.encoding)</span></span>  
    
    <span data-ttu-id="ce157-124">用來轉換字串的編碼方式。</span><span class="sxs-lookup"><span data-stu-id="ce157-124">The encoding used to convert the string.</span></span>

<!-- end list -->

  - <span data-ttu-id="ce157-125">grbit</span><span class="sxs-lookup"><span data-stu-id="ce157-125">grbit</span></span>  
    <span data-ttu-id="ce157-126">型別： [SetColumnGrbit](./setcolumngrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="ce157-126">Type: [Microsoft.Isam.Esent.Interop.SetColumnGrbit](./setcolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="ce157-127">SetColumn 選項。</span><span class="sxs-lookup"><span data-stu-id="ce157-127">SetColumn options.</span></span>

## <a name="see-also"></a><span data-ttu-id="ce157-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ce157-128">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ce157-129">參考</span><span class="sxs-lookup"><span data-stu-id="ce157-129">Reference</span></span>

[<span data-ttu-id="ce157-130">Api 類別</span><span class="sxs-lookup"><span data-stu-id="ce157-130">Api class</span></span>](./api-class.md)

[<span data-ttu-id="ce157-131">Api 成員</span><span class="sxs-lookup"><span data-stu-id="ce157-131">Api members</span></span>](./api-members.md)

[<span data-ttu-id="ce157-132">SetColumn 多載</span><span class="sxs-lookup"><span data-stu-id="ce157-132">SetColumn overload</span></span>](./api.setcolumn-method.md)

[<span data-ttu-id="ce157-133">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="ce157-133">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
