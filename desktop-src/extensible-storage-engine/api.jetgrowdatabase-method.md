---
description: 深入瞭解： JetGrowDatabase 方法
title: JetGrowDatabase 方法
TOCTitle: 'JetGrowDatabase method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGrowDatabase(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgrowdatabase(v=EXCHG.10)
ms:contentKeyID: 55100754
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGrowDatabase
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGrowDatabase
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3a51f0d55187b6f6eac66c0cba2ec7b9daa7d1dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848344"
---
# <a name="apijetgrowdatabase-method"></a><span data-ttu-id="21954-103">JetGrowDatabase 方法</span><span class="sxs-lookup"><span data-stu-id="21954-103">Api.JetGrowDatabase method</span></span>

<span data-ttu-id="21954-104">擴充目前開啟之資料庫的大小。</span><span class="sxs-lookup"><span data-stu-id="21954-104">Extends the size of a database that is currently open.</span></span>

<span data-ttu-id="21954-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="21954-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="21954-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="21954-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="21954-107">語法</span><span class="sxs-lookup"><span data-stu-id="21954-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGrowDatabase ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    desiredPages As Integer, _
    <OutAttribute> ByRef actualPages As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim desiredPages As Integer
Dim actualPages As IntegerApi.JetGrowDatabase(sesid, dbid, _
    desiredPages, actualPages)
```

``` csharp
public static void JetGrowDatabase(
    JET_SESID sesid,
    JET_DBID dbid,
    int desiredPages,
    out int actualPages
)
```

#### <a name="parameters"></a><span data-ttu-id="21954-108">參數</span><span class="sxs-lookup"><span data-stu-id="21954-108">Parameters</span></span>

  - <span data-ttu-id="21954-109">sesid</span><span class="sxs-lookup"><span data-stu-id="21954-109">sesid</span></span>  
    <span data-ttu-id="21954-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="21954-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="21954-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="21954-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="21954-112">dbid</span><span class="sxs-lookup"><span data-stu-id="21954-112">dbid</span></span>  
    <span data-ttu-id="21954-113">類型： [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="21954-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="21954-114">要成長的資料庫。</span><span class="sxs-lookup"><span data-stu-id="21954-114">The database to grow.</span></span>

<!-- end list -->

  - <span data-ttu-id="21954-115">desiredPages</span><span class="sxs-lookup"><span data-stu-id="21954-115">desiredPages</span></span>  
    <span data-ttu-id="21954-116">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="21954-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="21954-117">所需的資料庫大小（以頁面為限）。</span><span class="sxs-lookup"><span data-stu-id="21954-117">The desired size of the database, in pages.</span></span>

<!-- end list -->

  - <span data-ttu-id="21954-118">actualPages</span><span class="sxs-lookup"><span data-stu-id="21954-118">actualPages</span></span>  
    <span data-ttu-id="21954-119">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="21954-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="21954-120">在呼叫之後，資料庫的大小（以頁面為限）。</span><span class="sxs-lookup"><span data-stu-id="21954-120">The size of the database, in pages, after the call.</span></span>

## <a name="see-also"></a><span data-ttu-id="21954-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="21954-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="21954-122">參考</span><span class="sxs-lookup"><span data-stu-id="21954-122">Reference</span></span>

[<span data-ttu-id="21954-123">Api 類別</span><span class="sxs-lookup"><span data-stu-id="21954-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="21954-124">Api 成員</span><span class="sxs-lookup"><span data-stu-id="21954-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="21954-125">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="21954-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
