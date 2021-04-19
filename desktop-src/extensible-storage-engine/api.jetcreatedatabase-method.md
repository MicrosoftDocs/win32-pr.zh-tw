---
description: 深入瞭解： JetCreateDatabase 方法
title: JetCreateDatabase 方法
TOCTitle: 'JetCreateDatabase method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateDatabase(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_DBID@,Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreatedatabase(v=EXCHG.10)
ms:contentKeyID: 55100748
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateDatabase
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateDatabase
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fe427c270baf8a6d05e5d0ae99e1dc393208da01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986318"
---
# <a name="apijetcreatedatabase-method"></a><span data-ttu-id="75e5e-103">JetCreateDatabase 方法</span><span class="sxs-lookup"><span data-stu-id="75e5e-103">Api.JetCreateDatabase method</span></span>

<span data-ttu-id="75e5e-104">建立和附加資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="75e5e-104">Creates and attaches a database file.</span></span>

<span data-ttu-id="75e5e-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="75e5e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="75e5e-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="75e5e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="75e5e-107">語法</span><span class="sxs-lookup"><span data-stu-id="75e5e-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateDatabase ( _
    sesid As JET_SESID, _
    database As String, _
    connect As String, _
    <OutAttribute> ByRef dbid As JET_DBID, _
    grbit As CreateDatabaseGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim database As String
Dim connect As String
Dim dbid As JET_DBID
Dim grbit As CreateDatabaseGrbitApi.JetCreateDatabase(sesid, database, _
    connect, dbid, grbit)
```

``` csharp
public static void JetCreateDatabase(
    JET_SESID sesid,
    string database,
    string connect,
    out JET_DBID dbid,
    CreateDatabaseGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="75e5e-108">參數</span><span class="sxs-lookup"><span data-stu-id="75e5e-108">Parameters</span></span>

  - <span data-ttu-id="75e5e-109">sesid</span><span class="sxs-lookup"><span data-stu-id="75e5e-109">sesid</span></span>  
    <span data-ttu-id="75e5e-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="75e5e-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="75e5e-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="75e5e-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="75e5e-112">[資料庫]</span><span class="sxs-lookup"><span data-stu-id="75e5e-112">database</span></span>  
    <span data-ttu-id="75e5e-113">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="75e5e-113">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="75e5e-114">要建立之資料庫檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="75e5e-114">The path to the database file to create.</span></span>

<!-- end list -->

  - <span data-ttu-id="75e5e-115">連線</span><span class="sxs-lookup"><span data-stu-id="75e5e-115">connect</span></span>  
    <span data-ttu-id="75e5e-116">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="75e5e-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="75e5e-117">不使用參數。</span><span class="sxs-lookup"><span data-stu-id="75e5e-117">The parameter is not used.</span></span>

<!-- end list -->

  - <span data-ttu-id="75e5e-118">dbid</span><span class="sxs-lookup"><span data-stu-id="75e5e-118">dbid</span></span>  
    <span data-ttu-id="75e5e-119">類型： [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="75e5e-119">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="75e5e-120">傳回新資料庫的 dbid。</span><span class="sxs-lookup"><span data-stu-id="75e5e-120">Returns the dbid of the new database.</span></span>

<!-- end list -->

  - <span data-ttu-id="75e5e-121">grbit</span><span class="sxs-lookup"><span data-stu-id="75e5e-121">grbit</span></span>  
    <span data-ttu-id="75e5e-122">型別： [CreateDatabaseGrbit](./createdatabasegrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="75e5e-122">Type: [Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit](./createdatabasegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="75e5e-123">資料庫建立選項。</span><span class="sxs-lookup"><span data-stu-id="75e5e-123">Database creation options.</span></span>

## <a name="see-also"></a><span data-ttu-id="75e5e-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="75e5e-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="75e5e-125">參考</span><span class="sxs-lookup"><span data-stu-id="75e5e-125">Reference</span></span>

[<span data-ttu-id="75e5e-126">Api 類別</span><span class="sxs-lookup"><span data-stu-id="75e5e-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="75e5e-127">Api 成員</span><span class="sxs-lookup"><span data-stu-id="75e5e-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="75e5e-128">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="75e5e-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
