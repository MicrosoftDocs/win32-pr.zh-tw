---
description: 深入瞭解： JetSetDatabaseSize 方法
title: JetSetDatabaseSize 方法
TOCTitle: 'JetSetDatabaseSize method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetDatabaseSize(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetdatabasesize(v=EXCHG.10)
ms:contentKeyID: 55100807
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetDatabaseSize
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetDatabaseSize
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c90ba5ef2ebc96cbe6d50fa6c0888db9a09a0a99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978068"
---
# <a name="apijetsetdatabasesize-method"></a><span data-ttu-id="4ef6e-103">JetSetDatabaseSize 方法</span><span class="sxs-lookup"><span data-stu-id="4ef6e-103">Api.JetSetDatabaseSize method</span></span>

<span data-ttu-id="4ef6e-104">設定未開啟之資料庫檔案的大小。</span><span class="sxs-lookup"><span data-stu-id="4ef6e-104">Sets the size of an unopened database file.</span></span>

<span data-ttu-id="4ef6e-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4ef6e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4ef6e-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="4ef6e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4ef6e-107">語法</span><span class="sxs-lookup"><span data-stu-id="4ef6e-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetDatabaseSize ( _
    sesid As JET_SESID, _
    database As String, _
    desiredPages As Integer, _
    <OutAttribute> ByRef actualPages As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim database As String
Dim desiredPages As Integer
Dim actualPages As IntegerApi.JetSetDatabaseSize(sesid, database, _
    desiredPages, actualPages)
```

``` csharp
public static void JetSetDatabaseSize(
    JET_SESID sesid,
    string database,
    int desiredPages,
    out int actualPages
)
```

#### <a name="parameters"></a><span data-ttu-id="4ef6e-108">參數</span><span class="sxs-lookup"><span data-stu-id="4ef6e-108">Parameters</span></span>

  - <span data-ttu-id="4ef6e-109">sesid</span><span class="sxs-lookup"><span data-stu-id="4ef6e-109">sesid</span></span>  
    <span data-ttu-id="4ef6e-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4ef6e-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="4ef6e-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="4ef6e-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="4ef6e-112">[資料庫]</span><span class="sxs-lookup"><span data-stu-id="4ef6e-112">database</span></span>  
    <span data-ttu-id="4ef6e-113">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="4ef6e-113">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="4ef6e-114">資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="4ef6e-114">The name of the database.</span></span>

<!-- end list -->

  - <span data-ttu-id="4ef6e-115">desiredPages</span><span class="sxs-lookup"><span data-stu-id="4ef6e-115">desiredPages</span></span>  
    <span data-ttu-id="4ef6e-116">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="4ef6e-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="4ef6e-117">所需的資料庫大小（以頁面為限）。</span><span class="sxs-lookup"><span data-stu-id="4ef6e-117">The desired size of the database, in pages.</span></span>

<!-- end list -->

  - <span data-ttu-id="4ef6e-118">actualPages</span><span class="sxs-lookup"><span data-stu-id="4ef6e-118">actualPages</span></span>  
    <span data-ttu-id="4ef6e-119">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="4ef6e-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="4ef6e-120">在呼叫之後，資料庫的大小（以頁面為限）。</span><span class="sxs-lookup"><span data-stu-id="4ef6e-120">The size of the database, in pages, after the call.</span></span>

## <a name="see-also"></a><span data-ttu-id="4ef6e-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4ef6e-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4ef6e-122">參考</span><span class="sxs-lookup"><span data-stu-id="4ef6e-122">Reference</span></span>

[<span data-ttu-id="4ef6e-123">Api 類別</span><span class="sxs-lookup"><span data-stu-id="4ef6e-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="4ef6e-124">Api 成員</span><span class="sxs-lookup"><span data-stu-id="4ef6e-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="4ef6e-125">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="4ef6e-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
