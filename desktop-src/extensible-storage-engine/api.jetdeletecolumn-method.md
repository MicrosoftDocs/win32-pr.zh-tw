---
description: 深入瞭解： JetDeleteColumn 方法
title: JetDeleteColumn 方法
TOCTitle: 'JetDeleteColumn method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDeleteColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdeletecolumn(v=EXCHG.10)
ms:contentKeyID: 55100684
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDeleteColumn
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDeleteColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0801ffae0429b0c1d16d452d4170bdc6ce74937f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112601"
---
# <a name="apijetdeletecolumn-method"></a><span data-ttu-id="0de3d-103">JetDeleteColumn 方法</span><span class="sxs-lookup"><span data-stu-id="0de3d-103">Api.JetDeleteColumn method</span></span>

<span data-ttu-id="0de3d-104">從資料庫資料表中刪除資料行。</span><span class="sxs-lookup"><span data-stu-id="0de3d-104">Deletes a column from a database table.</span></span>

<span data-ttu-id="0de3d-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0de3d-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0de3d-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="0de3d-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0de3d-107">語法</span><span class="sxs-lookup"><span data-stu-id="0de3d-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetDeleteColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    column As String _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim column As StringApi.JetDeleteColumn(sesid, tableid, _
    column)
```

``` csharp
public static void JetDeleteColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string column
)
```

#### <a name="parameters"></a><span data-ttu-id="0de3d-108">參數</span><span class="sxs-lookup"><span data-stu-id="0de3d-108">Parameters</span></span>

  - <span data-ttu-id="0de3d-109">sesid</span><span class="sxs-lookup"><span data-stu-id="0de3d-109">sesid</span></span>  
    <span data-ttu-id="0de3d-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0de3d-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="0de3d-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="0de3d-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="0de3d-112">tableid</span><span class="sxs-lookup"><span data-stu-id="0de3d-112">tableid</span></span>  
    <span data-ttu-id="0de3d-113">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0de3d-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="0de3d-114">要從中刪除資料行的資料表上的資料指標。</span><span class="sxs-lookup"><span data-stu-id="0de3d-114">A cursor on the table to delete the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="0de3d-115">直條圖</span><span class="sxs-lookup"><span data-stu-id="0de3d-115">column</span></span>  
    <span data-ttu-id="0de3d-116">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="0de3d-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="0de3d-117">要刪除的資料行名稱。</span><span class="sxs-lookup"><span data-stu-id="0de3d-117">The name of the column to be deleted.</span></span>

## <a name="see-also"></a><span data-ttu-id="0de3d-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0de3d-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0de3d-119">參考</span><span class="sxs-lookup"><span data-stu-id="0de3d-119">Reference</span></span>

[<span data-ttu-id="0de3d-120">Api 類別</span><span class="sxs-lookup"><span data-stu-id="0de3d-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="0de3d-121">Api 成員</span><span class="sxs-lookup"><span data-stu-id="0de3d-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="0de3d-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="0de3d-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
