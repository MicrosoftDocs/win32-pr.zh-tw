---
description: 深入瞭解： JetDefragment 方法
title: JetDefragment 方法
TOCTitle: 'JetDefragment method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDefragment(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.Int32@,System.Int32@,Microsoft.Isam.Esent.Interop.DefragGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdefragment(v=EXCHG.10)
ms:contentKeyID: 55100679
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDefragment
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDefragment
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 69428d785bf9d607199cb62bfe02d2e373e7dbe4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970583"
---
# <a name="apijetdefragment-method"></a><span data-ttu-id="92011-103">JetDefragment 方法</span><span class="sxs-lookup"><span data-stu-id="92011-103">Api.JetDefragment method</span></span>

<span data-ttu-id="92011-104">啟動和停止資料庫重組工作，以改善資料庫中的資料組織。</span><span class="sxs-lookup"><span data-stu-id="92011-104">Starts and stops database defragmentation tasks that improves data organization within a database.</span></span>

<span data-ttu-id="92011-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="92011-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="92011-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="92011-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="92011-107">語法</span><span class="sxs-lookup"><span data-stu-id="92011-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetDefragment ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tableName As String, _
    ByRef passes As Integer, _
    ByRef seconds As Integer, _
    grbit As DefragGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tableName As String
Dim passes As Integer
Dim seconds As Integer
Dim grbit As DefragGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetDefragment(sesid, _
    dbid, tableName, passes, seconds, _
    grbit)
```

``` csharp
public static JET_wrn JetDefragment(
    JET_SESID sesid,
    JET_DBID dbid,
    string tableName,
    ref int passes,
    ref int seconds,
    DefragGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="92011-108">參數</span><span class="sxs-lookup"><span data-stu-id="92011-108">Parameters</span></span>

  - <span data-ttu-id="92011-109">sesid</span><span class="sxs-lookup"><span data-stu-id="92011-109">sesid</span></span>  
    <span data-ttu-id="92011-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="92011-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="92011-111">要用於呼叫的會話。</span><span class="sxs-lookup"><span data-stu-id="92011-111">The session to use for the call.</span></span>

<!-- end list -->

  - <span data-ttu-id="92011-112">dbid</span><span class="sxs-lookup"><span data-stu-id="92011-112">dbid</span></span>  
    <span data-ttu-id="92011-113">類型： [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="92011-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="92011-114">要進行磁碟重組的資料庫。</span><span class="sxs-lookup"><span data-stu-id="92011-114">The database to be defragmented.</span></span>

<!-- end list -->

  - <span data-ttu-id="92011-115">tableName</span><span class="sxs-lookup"><span data-stu-id="92011-115">tableName</span></span>  
    <span data-ttu-id="92011-116">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="92011-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="92011-117">未使用的參數。</span><span class="sxs-lookup"><span data-stu-id="92011-117">Unused parameter.</span></span> <span data-ttu-id="92011-118">針對指定資料庫識別碼所描述的整個資料庫執行磁碟重組。</span><span class="sxs-lookup"><span data-stu-id="92011-118">Defragmentation is performed for the entire database described by the given database ID.</span></span>

<!-- end list -->

  - <span data-ttu-id="92011-119">通過</span><span class="sxs-lookup"><span data-stu-id="92011-119">passes</span></span>  
    <span data-ttu-id="92011-120">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="92011-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="92011-121">開始進行線上磁碟重組工作時，此參數會設定磁碟重組傳遞的最大數目。</span><span class="sxs-lookup"><span data-stu-id="92011-121">When starting an online defragmentation task, this parameter sets the maximum number of defragmentation passes.</span></span> <span data-ttu-id="92011-122">停止線上磁碟重組工作時，此參數會設定為所執行的行程數目。</span><span class="sxs-lookup"><span data-stu-id="92011-122">When stopping an online defragmentation task, this parameter is set to the number of passes performed.</span></span>

<!-- end list -->

  - <span data-ttu-id="92011-123">seconds</span><span class="sxs-lookup"><span data-stu-id="92011-123">seconds</span></span>  
    <span data-ttu-id="92011-124">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="92011-124">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="92011-125">開始進行線上磁碟重組工作時，此參數會設定磁碟重組的最長時間。</span><span class="sxs-lookup"><span data-stu-id="92011-125">When starting an online defragmentation task, this parameter sets the maximum time for defragmentation.</span></span> <span data-ttu-id="92011-126">停止線上磁碟重組工作時，此輸出緩衝區會設定為用於重組的時間長度。</span><span class="sxs-lookup"><span data-stu-id="92011-126">When stopping an online defragmentation task, this output buffer is set to the length of time used for defragmentation.</span></span>

<!-- end list -->

  - <span data-ttu-id="92011-127">grbit</span><span class="sxs-lookup"><span data-stu-id="92011-127">grbit</span></span>  
    <span data-ttu-id="92011-128">型別： [DefragGrbit](./defraggrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="92011-128">Type: [Microsoft.Isam.Esent.Interop.DefragGrbit](./defraggrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="92011-129">磁碟重組選項。</span><span class="sxs-lookup"><span data-stu-id="92011-129">Defragmentation options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="92011-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="92011-130">Return value</span></span>

<span data-ttu-id="92011-131">類型： [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="92011-131">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="92011-132">警告碼。</span><span class="sxs-lookup"><span data-stu-id="92011-132">A warning code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="92011-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="92011-133">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="92011-134">參考</span><span class="sxs-lookup"><span data-stu-id="92011-134">Reference</span></span>

[<span data-ttu-id="92011-135">Api 類別</span><span class="sxs-lookup"><span data-stu-id="92011-135">Api class</span></span>](./api-class.md)

[<span data-ttu-id="92011-136">Api 成員</span><span class="sxs-lookup"><span data-stu-id="92011-136">Api members</span></span>](./api-members.md)

[<span data-ttu-id="92011-137">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="92011-137">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
