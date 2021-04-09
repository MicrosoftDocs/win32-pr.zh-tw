---
description: 深入瞭解： JetOpenTable 方法
title: JetOpenTable 方法
TOCTitle: 'JetOpenTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOpenTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.Byte[],System.Int32,Microsoft.Isam.Esent.Interop.OpenTableGrbit,Microsoft.Isam.Esent.Interop.JET_TABLEID@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetopentable(v=EXCHG.10)
ms:contentKeyID: 55100776
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTable
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5764138d4ea387b68c94805c6966f7ce0e817c37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945223"
---
# <a name="apijetopentable-method"></a><span data-ttu-id="8e407-103">JetOpenTable 方法</span><span class="sxs-lookup"><span data-stu-id="8e407-103">Api.JetOpenTable method</span></span>

<span data-ttu-id="8e407-104">在先前建立的資料表上開啟資料指標。</span><span class="sxs-lookup"><span data-stu-id="8e407-104">Opens a cursor on a previously created table.</span></span>

<span data-ttu-id="8e407-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8e407-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8e407-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="8e407-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8e407-107">語法</span><span class="sxs-lookup"><span data-stu-id="8e407-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetOpenTable ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    parameters As Byte(), _
    parametersSize As Integer, _
    grbit As OpenTableGrbit, _
    <OutAttribute> ByRef tableid As JET_TABLEID _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim parameters As Byte()
Dim parametersSize As Integer
Dim grbit As OpenTableGrbit
Dim tableid As JET_TABLEID
Dim returnValue As JET_wrn

returnValue = Api.JetOpenTable(sesid, _
    dbid, tablename, parameters, parametersSize, _
    grbit, tableid)
```

``` csharp
public static JET_wrn JetOpenTable(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    byte[] parameters,
    int parametersSize,
    OpenTableGrbit grbit,
    out JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="8e407-108">參數</span><span class="sxs-lookup"><span data-stu-id="8e407-108">Parameters</span></span>

  - <span data-ttu-id="8e407-109">sesid</span><span class="sxs-lookup"><span data-stu-id="8e407-109">sesid</span></span>  
    <span data-ttu-id="8e407-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8e407-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="8e407-111">要使用的資料庫會話。</span><span class="sxs-lookup"><span data-stu-id="8e407-111">The database session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="8e407-112">dbid</span><span class="sxs-lookup"><span data-stu-id="8e407-112">dbid</span></span>  
    <span data-ttu-id="8e407-113">類型： [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8e407-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="8e407-114">要在其中開啟資料表的資料庫。</span><span class="sxs-lookup"><span data-stu-id="8e407-114">The database to open the table in.</span></span>

<!-- end list -->

  - <span data-ttu-id="8e407-115">tablename</span><span class="sxs-lookup"><span data-stu-id="8e407-115">tablename</span></span>  
    <span data-ttu-id="8e407-116">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="8e407-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="8e407-117">要開啟之資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e407-117">The name of the table to open.</span></span>

<!-- end list -->

  - <span data-ttu-id="8e407-118">參數</span><span class="sxs-lookup"><span data-stu-id="8e407-118">parameters</span></span>  
    <span data-ttu-id="8e407-119">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="8e407-119">Type: \[\]</span></span>  
    
    <span data-ttu-id="8e407-120">不使用參數。</span><span class="sxs-lookup"><span data-stu-id="8e407-120">The parameter is not used.</span></span>

<!-- end list -->

  - <span data-ttu-id="8e407-121">parametersSize</span><span class="sxs-lookup"><span data-stu-id="8e407-121">parametersSize</span></span>  
    <span data-ttu-id="8e407-122">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="8e407-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="8e407-123">不使用參數。</span><span class="sxs-lookup"><span data-stu-id="8e407-123">The parameter is not used.</span></span>

<!-- end list -->

  - <span data-ttu-id="8e407-124">grbit</span><span class="sxs-lookup"><span data-stu-id="8e407-124">grbit</span></span>  
    <span data-ttu-id="8e407-125">型別： [OpenTableGrbit](./opentablegrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="8e407-125">Type: [Microsoft.Isam.Esent.Interop.OpenTableGrbit](./opentablegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="8e407-126">資料表開啟的選項。</span><span class="sxs-lookup"><span data-stu-id="8e407-126">Table open options.</span></span>

<!-- end list -->

  - <span data-ttu-id="8e407-127">tableid</span><span class="sxs-lookup"><span data-stu-id="8e407-127">tableid</span></span>  
    <span data-ttu-id="8e407-128">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8e407-128">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="8e407-129">傳回開啟的資料表。</span><span class="sxs-lookup"><span data-stu-id="8e407-129">Returns the opened table.</span></span>

#### <a name="return-value"></a><span data-ttu-id="8e407-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="8e407-130">Return value</span></span>

<span data-ttu-id="8e407-131">類型： [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="8e407-131">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="8e407-132">ESENT 警告。</span><span class="sxs-lookup"><span data-stu-id="8e407-132">An ESENT warning.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8e407-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8e407-133">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8e407-134">參考</span><span class="sxs-lookup"><span data-stu-id="8e407-134">Reference</span></span>

[<span data-ttu-id="8e407-135">Api 類別</span><span class="sxs-lookup"><span data-stu-id="8e407-135">Api class</span></span>](./api-class.md)

[<span data-ttu-id="8e407-136">Api 成員</span><span class="sxs-lookup"><span data-stu-id="8e407-136">Api members</span></span>](./api-members.md)

[<span data-ttu-id="8e407-137">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="8e407-137">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
