---
description: 深入瞭解： JetRenameColumn 方法
title: JetRenameColumn 方法
TOCTitle: 'JetRenameColumn method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRenameColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,System.String,Microsoft.Isam.Esent.Interop.RenameColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetrenamecolumn(v=EXCHG.10)
ms:contentKeyID: 55100786
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRenameColumn
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRenameColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 007bce82d8749611f0fe2b0eae28b54ddedab98f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695140"
---
# <a name="apijetrenamecolumn-method"></a><span data-ttu-id="3a3a8-103">JetRenameColumn 方法</span><span class="sxs-lookup"><span data-stu-id="3a3a8-103">Api.JetRenameColumn method</span></span>

<span data-ttu-id="3a3a8-104">變更現有資料行的名稱。</span><span class="sxs-lookup"><span data-stu-id="3a3a8-104">Changes the name of an existing column.</span></span>

<span data-ttu-id="3a3a8-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3a3a8-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3a3a8-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="3a3a8-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3a3a8-107">語法</span><span class="sxs-lookup"><span data-stu-id="3a3a8-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetRenameColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    name As String, _
    newName As String, _
    grbit As RenameColumnGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim name As String
Dim newName As String
Dim grbit As RenameColumnGrbitApi.JetRenameColumn(sesid, tableid, _
    name, newName, grbit)
```

``` csharp
public static void JetRenameColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string name,
    string newName,
    RenameColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="3a3a8-108">參數</span><span class="sxs-lookup"><span data-stu-id="3a3a8-108">Parameters</span></span>

  - <span data-ttu-id="3a3a8-109">sesid</span><span class="sxs-lookup"><span data-stu-id="3a3a8-109">sesid</span></span>  
    <span data-ttu-id="3a3a8-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3a3a8-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="3a3a8-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="3a3a8-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="3a3a8-112">tableid</span><span class="sxs-lookup"><span data-stu-id="3a3a8-112">tableid</span></span>  
    <span data-ttu-id="3a3a8-113">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3a3a8-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="3a3a8-114">包含資料行的資料表。</span><span class="sxs-lookup"><span data-stu-id="3a3a8-114">The table containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="3a3a8-115">NAME</span><span class="sxs-lookup"><span data-stu-id="3a3a8-115">name</span></span>  
    <span data-ttu-id="3a3a8-116">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="3a3a8-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="3a3a8-117">資料行名稱。</span><span class="sxs-lookup"><span data-stu-id="3a3a8-117">The name of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="3a3a8-118">newName</span><span class="sxs-lookup"><span data-stu-id="3a3a8-118">newName</span></span>  
    <span data-ttu-id="3a3a8-119">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="3a3a8-119">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="3a3a8-120">資料行的新名稱。</span><span class="sxs-lookup"><span data-stu-id="3a3a8-120">The new name of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="3a3a8-121">grbit</span><span class="sxs-lookup"><span data-stu-id="3a3a8-121">grbit</span></span>  
    <span data-ttu-id="3a3a8-122">型別： [RenameColumnGrbit](./renamecolumngrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="3a3a8-122">Type: [Microsoft.Isam.Esent.Interop.RenameColumnGrbit](./renamecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="3a3a8-123">資料行重新命名選項。</span><span class="sxs-lookup"><span data-stu-id="3a3a8-123">Column rename options.</span></span>

## <a name="see-also"></a><span data-ttu-id="3a3a8-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3a3a8-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3a3a8-125">參考</span><span class="sxs-lookup"><span data-stu-id="3a3a8-125">Reference</span></span>

[<span data-ttu-id="3a3a8-126">Api 類別</span><span class="sxs-lookup"><span data-stu-id="3a3a8-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="3a3a8-127">Api 成員</span><span class="sxs-lookup"><span data-stu-id="3a3a8-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="3a3a8-128">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="3a3a8-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
