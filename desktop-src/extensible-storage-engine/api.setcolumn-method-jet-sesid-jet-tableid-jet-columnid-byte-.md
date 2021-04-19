---
description: '深入瞭解： SetColumn 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID、位元組) '
title: 'SetColumn 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID、Byte) '
TOCTitle: SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Byte)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.setcolumn(v=EXCHG.10)
ms:contentKeyID: 55100873
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
ms.openlocfilehash: b2d68fe5e14c1ea972bf4b0f5bb17fa74b8b173f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979395"
---
# <a name="apisetcolumn-method-jet_sesid-jet_tableid-jet_columnid-byte"></a><span data-ttu-id="af72d-103">SetColumn 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID、Byte) </span><span class="sxs-lookup"><span data-stu-id="af72d-103">Api.SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte)</span></span>

<span data-ttu-id="af72d-104">修改修改過的記錄中要插入的單一資料行值，或更新目前的記錄。</span><span class="sxs-lookup"><span data-stu-id="af72d-104">Modifies a single column value in a modified record to be inserted or to update the current record.</span></span>

<span data-ttu-id="af72d-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="af72d-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="af72d-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="af72d-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="af72d-107">語法</span><span class="sxs-lookup"><span data-stu-id="af72d-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub SetColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As Byte _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As ByteApi.SetColumn(sesid, tableid, columnid, _
    data)
```

``` csharp
public static void SetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    byte data
)
```

#### <a name="parameters"></a><span data-ttu-id="af72d-108">參數</span><span class="sxs-lookup"><span data-stu-id="af72d-108">Parameters</span></span>

  - <span data-ttu-id="af72d-109">sesid</span><span class="sxs-lookup"><span data-stu-id="af72d-109">sesid</span></span>  
    <span data-ttu-id="af72d-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="af72d-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="af72d-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="af72d-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="af72d-112">tableid</span><span class="sxs-lookup"><span data-stu-id="af72d-112">tableid</span></span>  
    <span data-ttu-id="af72d-113">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="af72d-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="af72d-114">要更新的資料指標。</span><span class="sxs-lookup"><span data-stu-id="af72d-114">The cursor to update.</span></span> <span data-ttu-id="af72d-115">應備妥更新。</span><span class="sxs-lookup"><span data-stu-id="af72d-115">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="af72d-116">columnid</span><span class="sxs-lookup"><span data-stu-id="af72d-116">columnid</span></span>  
    <span data-ttu-id="af72d-117">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="af72d-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="af72d-118">要設定的 columnid。</span><span class="sxs-lookup"><span data-stu-id="af72d-118">The columnid to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="af72d-119">data</span><span class="sxs-lookup"><span data-stu-id="af72d-119">data</span></span>  
    <span data-ttu-id="af72d-120">類型： [system.string](/dotnet/api/system.byte)</span><span class="sxs-lookup"><span data-stu-id="af72d-120">Type: [System.Byte](/dotnet/api/system.byte)</span></span>  
    
    <span data-ttu-id="af72d-121">要設定的資料。</span><span class="sxs-lookup"><span data-stu-id="af72d-121">The data to set.</span></span>

## <a name="see-also"></a><span data-ttu-id="af72d-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="af72d-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="af72d-123">參考</span><span class="sxs-lookup"><span data-stu-id="af72d-123">Reference</span></span>

[<span data-ttu-id="af72d-124">Api 類別</span><span class="sxs-lookup"><span data-stu-id="af72d-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="af72d-125">Api 成員</span><span class="sxs-lookup"><span data-stu-id="af72d-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="af72d-126">SetColumn 多載</span><span class="sxs-lookup"><span data-stu-id="af72d-126">SetColumn overload</span></span>](./api.setcolumn-method.md)

[<span data-ttu-id="af72d-127">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="af72d-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
