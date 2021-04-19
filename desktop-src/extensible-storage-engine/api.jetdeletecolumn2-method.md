---
description: 深入瞭解： JetDeleteColumn2 方法
title: JetDeleteColumn2 方法
TOCTitle: 'JetDeleteColumn2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDeleteColumn2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.DeleteColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdeletecolumn2(v=EXCHG.10)
ms:contentKeyID: 55100680
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDeleteColumn2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDeleteColumn2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0426ca2557dac11c565211162438db6d5c77a563
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970582"
---
# <a name="apijetdeletecolumn2-method"></a><span data-ttu-id="c0ec8-103">JetDeleteColumn2 方法</span><span class="sxs-lookup"><span data-stu-id="c0ec8-103">Api.JetDeleteColumn2 method</span></span>

<span data-ttu-id="c0ec8-104">從資料庫資料表中刪除資料行。</span><span class="sxs-lookup"><span data-stu-id="c0ec8-104">Deletes a column from a database table.</span></span>

<span data-ttu-id="c0ec8-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c0ec8-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c0ec8-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="c0ec8-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c0ec8-107">語法</span><span class="sxs-lookup"><span data-stu-id="c0ec8-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetDeleteColumn2 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    column As String, _
    grbit As DeleteColumnGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim column As String
Dim grbit As DeleteColumnGrbitApi.JetDeleteColumn2(sesid, tableid, _
    column, grbit)
```

``` csharp
public static void JetDeleteColumn2(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string column,
    DeleteColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="c0ec8-108">參數</span><span class="sxs-lookup"><span data-stu-id="c0ec8-108">Parameters</span></span>

  - <span data-ttu-id="c0ec8-109">sesid</span><span class="sxs-lookup"><span data-stu-id="c0ec8-109">sesid</span></span>  
    <span data-ttu-id="c0ec8-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c0ec8-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="c0ec8-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="c0ec8-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="c0ec8-112">tableid</span><span class="sxs-lookup"><span data-stu-id="c0ec8-112">tableid</span></span>  
    <span data-ttu-id="c0ec8-113">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c0ec8-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="c0ec8-114">要從中刪除資料行的資料表上的資料指標。</span><span class="sxs-lookup"><span data-stu-id="c0ec8-114">A cursor on the table to delete the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="c0ec8-115">直條圖</span><span class="sxs-lookup"><span data-stu-id="c0ec8-115">column</span></span>  
    <span data-ttu-id="c0ec8-116">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="c0ec8-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="c0ec8-117">要刪除的資料行名稱。</span><span class="sxs-lookup"><span data-stu-id="c0ec8-117">The name of the column to be deleted.</span></span>

<!-- end list -->

  - <span data-ttu-id="c0ec8-118">grbit</span><span class="sxs-lookup"><span data-stu-id="c0ec8-118">grbit</span></span>  
    <span data-ttu-id="c0ec8-119">型別： [DeleteColumnGrbit](./deletecolumngrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="c0ec8-119">Type: [Microsoft.Isam.Esent.Interop.DeleteColumnGrbit](./deletecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="c0ec8-120">資料行刪除選項。</span><span class="sxs-lookup"><span data-stu-id="c0ec8-120">Column deletion options.</span></span>

## <a name="see-also"></a><span data-ttu-id="c0ec8-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c0ec8-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c0ec8-122">參考</span><span class="sxs-lookup"><span data-stu-id="c0ec8-122">Reference</span></span>

[<span data-ttu-id="c0ec8-123">Api 類別</span><span class="sxs-lookup"><span data-stu-id="c0ec8-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="c0ec8-124">Api 成員</span><span class="sxs-lookup"><span data-stu-id="c0ec8-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="c0ec8-125">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="c0ec8-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
