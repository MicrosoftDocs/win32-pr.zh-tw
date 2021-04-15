---
description: 深入瞭解： Windows8Api. JetResizeDatabase 方法
title: 'Windows8Api. JetResizeDatabase 方法 (Windows8 的) '
TOCTitle: 'JetResizeDatabase method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetResizeDatabase(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetresizedatabase(v=EXCHG.10)
ms:contentKeyID: 55104462
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetResizeDatabase
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetResizeDatabase
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dcca9a4006f8c8da1758a85d12d716b5ce1bba23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512469"
---
# <a name="windows8apijetresizedatabase-method"></a><span data-ttu-id="0aaf2-103">Windows8Api. JetResizeDatabase 方法</span><span class="sxs-lookup"><span data-stu-id="0aaf2-103">Windows8Api.JetResizeDatabase method</span></span>

<span data-ttu-id="0aaf2-104">調整目前開啟之資料庫的大小。</span><span class="sxs-lookup"><span data-stu-id="0aaf2-104">Resizes a currently open database.</span></span>

<span data-ttu-id="0aaf2-105">**命名空間：**  [Microsoft Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0aaf2-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="0aaf2-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="0aaf2-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0aaf2-107">語法</span><span class="sxs-lookup"><span data-stu-id="0aaf2-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetResizeDatabase ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    desiredPages As Integer, _
    <OutAttribute> ByRef actualPages As Integer, _
    grbit As ResizeDatabaseGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim desiredPages As Integer
Dim actualPages As Integer
Dim grbit As ResizeDatabaseGrbitWindows8Api.JetResizeDatabase(sesid, dbid, _
    desiredPages, actualPages, grbit)
```

``` csharp
public static void JetResizeDatabase(
    JET_SESID sesid,
    JET_DBID dbid,
    int desiredPages,
    out int actualPages,
    ResizeDatabaseGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="0aaf2-108">參數</span><span class="sxs-lookup"><span data-stu-id="0aaf2-108">Parameters</span></span>

  - <span data-ttu-id="0aaf2-109">sesid</span><span class="sxs-lookup"><span data-stu-id="0aaf2-109">sesid</span></span>  
    <span data-ttu-id="0aaf2-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0aaf2-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="0aaf2-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="0aaf2-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="0aaf2-112">dbid</span><span class="sxs-lookup"><span data-stu-id="0aaf2-112">dbid</span></span>  
    <span data-ttu-id="0aaf2-113">類型： [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0aaf2-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="0aaf2-114">要成長的資料庫。</span><span class="sxs-lookup"><span data-stu-id="0aaf2-114">The database to grow.</span></span>

<!-- end list -->

  - <span data-ttu-id="0aaf2-115">desiredPages</span><span class="sxs-lookup"><span data-stu-id="0aaf2-115">desiredPages</span></span>  
    <span data-ttu-id="0aaf2-116">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="0aaf2-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="0aaf2-117">所需的資料庫大小（以頁面為限）。</span><span class="sxs-lookup"><span data-stu-id="0aaf2-117">The desired size of the database, in pages.</span></span>

<!-- end list -->

  - <span data-ttu-id="0aaf2-118">actualPages</span><span class="sxs-lookup"><span data-stu-id="0aaf2-118">actualPages</span></span>  
    <span data-ttu-id="0aaf2-119">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="0aaf2-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="0aaf2-120">在呼叫之後，資料庫的大小（以頁面為限）。</span><span class="sxs-lookup"><span data-stu-id="0aaf2-120">The size of the database, in pages, after the call.</span></span>

<!-- end list -->

  - <span data-ttu-id="0aaf2-121">grbit</span><span class="sxs-lookup"><span data-stu-id="0aaf2-121">grbit</span></span>  
    <span data-ttu-id="0aaf2-122">型別： [Windows8. ResizeDatabaseGrbit](./resizedatabasegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="0aaf2-122">Type: [Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit](./resizedatabasegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="0aaf2-123">調整大小選項。</span><span class="sxs-lookup"><span data-stu-id="0aaf2-123">Resize options.</span></span>

## <a name="see-also"></a><span data-ttu-id="0aaf2-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0aaf2-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0aaf2-125">參考</span><span class="sxs-lookup"><span data-stu-id="0aaf2-125">Reference</span></span>

[<span data-ttu-id="0aaf2-126">Windows8Api 類別</span><span class="sxs-lookup"><span data-stu-id="0aaf2-126">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="0aaf2-127">Windows8Api 成員</span><span class="sxs-lookup"><span data-stu-id="0aaf2-127">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="0aaf2-128">Windows8 命名空間。</span><span class="sxs-lookup"><span data-stu-id="0aaf2-128">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
