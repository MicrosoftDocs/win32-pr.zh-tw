---
description: 深入瞭解： JetCreateDatabase2 方法
title: JetCreateDatabase2 方法
TOCTitle: 'JetCreateDatabase2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateDatabase2(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,System.Int32,Microsoft.Isam.Esent.Interop.JET_DBID@,Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreatedatabase2(v=EXCHG.10)
ms:contentKeyID: 55100671
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateDatabase2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateDatabase2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8293a7c98451b0fd8bc46fbc13dde6b477a0ad09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689427"
---
# <a name="apijetcreatedatabase2-method"></a><span data-ttu-id="1719c-103">JetCreateDatabase2 方法</span><span class="sxs-lookup"><span data-stu-id="1719c-103">Api.JetCreateDatabase2 method</span></span>

<span data-ttu-id="1719c-104">建立並附加資料庫檔案，並指定最大資料庫大小。</span><span class="sxs-lookup"><span data-stu-id="1719c-104">Creates and attaches a database file with a maximum database size specified.</span></span>

<span data-ttu-id="1719c-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1719c-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1719c-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="1719c-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1719c-107">語法</span><span class="sxs-lookup"><span data-stu-id="1719c-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateDatabase2 ( _
    sesid As JET_SESID, _
    database As String, _
    maxPages As Integer, _
    <OutAttribute> ByRef dbid As JET_DBID, _
    grbit As CreateDatabaseGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim database As String
Dim maxPages As Integer
Dim dbid As JET_DBID
Dim grbit As CreateDatabaseGrbitApi.JetCreateDatabase2(sesid, database, _
    maxPages, dbid, grbit)
```

``` csharp
public static void JetCreateDatabase2(
    JET_SESID sesid,
    string database,
    int maxPages,
    out JET_DBID dbid,
    CreateDatabaseGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="1719c-108">參數</span><span class="sxs-lookup"><span data-stu-id="1719c-108">Parameters</span></span>

  - <span data-ttu-id="1719c-109">sesid</span><span class="sxs-lookup"><span data-stu-id="1719c-109">sesid</span></span>  
    <span data-ttu-id="1719c-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1719c-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="1719c-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="1719c-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="1719c-112">[資料庫]</span><span class="sxs-lookup"><span data-stu-id="1719c-112">database</span></span>  
    <span data-ttu-id="1719c-113">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="1719c-113">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="1719c-114">要建立之資料庫檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="1719c-114">The path to the database file to create.</span></span>

<!-- end list -->

  - <span data-ttu-id="1719c-115">maxPages</span><span class="sxs-lookup"><span data-stu-id="1719c-115">maxPages</span></span>  
    <span data-ttu-id="1719c-116">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="1719c-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="1719c-117">資料庫的大小上限（資料庫頁面）。</span><span class="sxs-lookup"><span data-stu-id="1719c-117">The maximum size, in database pages, of the database.</span></span> <span data-ttu-id="1719c-118">傳遞0表示沒有強制執行的最大值。</span><span class="sxs-lookup"><span data-stu-id="1719c-118">Passing 0 means there is no enforced maximum.</span></span>

<!-- end list -->

  - <span data-ttu-id="1719c-119">dbid</span><span class="sxs-lookup"><span data-stu-id="1719c-119">dbid</span></span>  
    <span data-ttu-id="1719c-120">類型： [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1719c-120">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="1719c-121">傳回新資料庫的 dbid。</span><span class="sxs-lookup"><span data-stu-id="1719c-121">Returns the dbid of the new database.</span></span>

<!-- end list -->

  - <span data-ttu-id="1719c-122">grbit</span><span class="sxs-lookup"><span data-stu-id="1719c-122">grbit</span></span>  
    <span data-ttu-id="1719c-123">型別： [CreateDatabaseGrbit](./createdatabasegrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="1719c-123">Type: [Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit](./createdatabasegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="1719c-124">資料庫建立選項。</span><span class="sxs-lookup"><span data-stu-id="1719c-124">Database creation options.</span></span>

## <a name="see-also"></a><span data-ttu-id="1719c-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1719c-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1719c-126">參考</span><span class="sxs-lookup"><span data-stu-id="1719c-126">Reference</span></span>

[<span data-ttu-id="1719c-127">Api 類別</span><span class="sxs-lookup"><span data-stu-id="1719c-127">Api class</span></span>](./api-class.md)

[<span data-ttu-id="1719c-128">Api 成員</span><span class="sxs-lookup"><span data-stu-id="1719c-128">Api members</span></span>](./api-members.md)

[<span data-ttu-id="1719c-129">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="1719c-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
