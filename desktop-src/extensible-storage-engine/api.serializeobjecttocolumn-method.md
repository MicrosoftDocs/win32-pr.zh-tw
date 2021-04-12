---
description: 深入瞭解： SerializeObjectToColumn 方法
title: SerializeObjectToColumn 方法
TOCTitle: 'SerializeObjectToColumn method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SerializeObjectToColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Object)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.serializeobjecttocolumn(v=EXCHG.10)
ms:contentKeyID: 55100915
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.SerializeObjectToColumn
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.SerializeObjectToColumn
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 21b0e421b68287b983fc43482e3a2385b2a160f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193440"
---
# <a name="apiserializeobjecttocolumn-method"></a><span data-ttu-id="47d80-103">SerializeObjectToColumn 方法</span><span class="sxs-lookup"><span data-stu-id="47d80-103">Api.SerializeObjectToColumn method</span></span>

<span data-ttu-id="47d80-104">將物件的序列化形式寫入資料行。</span><span class="sxs-lookup"><span data-stu-id="47d80-104">Write a serialized form of an object to a column.</span></span>

<span data-ttu-id="47d80-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="47d80-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="47d80-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="47d80-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="47d80-107">語法</span><span class="sxs-lookup"><span data-stu-id="47d80-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub SerializeObjectToColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    value As Object _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim value As ObjectApi.SerializeObjectToColumn(sesid, _
    tableid, columnid, value)
```

``` csharp
public static void SerializeObjectToColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    Object value
)
```

#### <a name="parameters"></a><span data-ttu-id="47d80-108">參數</span><span class="sxs-lookup"><span data-stu-id="47d80-108">Parameters</span></span>

  - <span data-ttu-id="47d80-109">sesid</span><span class="sxs-lookup"><span data-stu-id="47d80-109">sesid</span></span>  
    <span data-ttu-id="47d80-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="47d80-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="47d80-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="47d80-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="47d80-112">tableid</span><span class="sxs-lookup"><span data-stu-id="47d80-112">tableid</span></span>  
    <span data-ttu-id="47d80-113">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="47d80-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="47d80-114">要寫入的資料表。</span><span class="sxs-lookup"><span data-stu-id="47d80-114">The table to write to.</span></span> <span data-ttu-id="47d80-115">應備妥更新。</span><span class="sxs-lookup"><span data-stu-id="47d80-115">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="47d80-116">columnid</span><span class="sxs-lookup"><span data-stu-id="47d80-116">columnid</span></span>  
    <span data-ttu-id="47d80-117">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="47d80-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="47d80-118">要寫入的資料行。</span><span class="sxs-lookup"><span data-stu-id="47d80-118">The column to write to.</span></span>

<!-- end list -->

  - <span data-ttu-id="47d80-119">value</span><span class="sxs-lookup"><span data-stu-id="47d80-119">value</span></span>  
    <span data-ttu-id="47d80-120">類型： [system.object](/dotnet/api/system.object)</span><span class="sxs-lookup"><span data-stu-id="47d80-120">Type: [System.Object](/dotnet/api/system.object)</span></span>  
    
    <span data-ttu-id="47d80-121">要寫入的物件。</span><span class="sxs-lookup"><span data-stu-id="47d80-121">The object to write.</span></span> <span data-ttu-id="47d80-122">物件必須是可序列化的。</span><span class="sxs-lookup"><span data-stu-id="47d80-122">The object must be serializable.</span></span>

## <a name="see-also"></a><span data-ttu-id="47d80-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="47d80-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="47d80-124">參考</span><span class="sxs-lookup"><span data-stu-id="47d80-124">Reference</span></span>

[<span data-ttu-id="47d80-125">Api 類別</span><span class="sxs-lookup"><span data-stu-id="47d80-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="47d80-126">Api 成員</span><span class="sxs-lookup"><span data-stu-id="47d80-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="47d80-127">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="47d80-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
