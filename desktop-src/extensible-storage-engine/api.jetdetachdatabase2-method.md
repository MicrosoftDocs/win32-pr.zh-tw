---
description: 深入瞭解： JetDetachDatabase2 方法
title: JetDetachDatabase2 方法
TOCTitle: 'JetDetachDatabase2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDetachDatabase2(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdetachdatabase2(v=EXCHG.10)
ms:contentKeyID: 55100685
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDetachDatabase2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDetachDatabase2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 44cc8b5d03ba720f1acb7d0e8603bf29906a611e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112596"
---
# <a name="apijetdetachdatabase2-method"></a><span data-ttu-id="38aba-103">JetDetachDatabase2 方法</span><span class="sxs-lookup"><span data-stu-id="38aba-103">Api.JetDetachDatabase2 method</span></span>

<span data-ttu-id="38aba-104">釋放先前附加至資料庫會話的資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="38aba-104">Releases a database file that was previously attached to a database session.</span></span>

<span data-ttu-id="38aba-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="38aba-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="38aba-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="38aba-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="38aba-107">語法</span><span class="sxs-lookup"><span data-stu-id="38aba-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetDetachDatabase2 ( _
    sesid As JET_SESID, _
    database As String, _
    grbit As DetachDatabaseGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim database As String
Dim grbit As DetachDatabaseGrbitApi.JetDetachDatabase2(sesid, database, _
    grbit)
```

``` csharp
public static void JetDetachDatabase2(
    JET_SESID sesid,
    string database,
    DetachDatabaseGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="38aba-108">參數</span><span class="sxs-lookup"><span data-stu-id="38aba-108">Parameters</span></span>

  - <span data-ttu-id="38aba-109">sesid</span><span class="sxs-lookup"><span data-stu-id="38aba-109">sesid</span></span>  
    <span data-ttu-id="38aba-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="38aba-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="38aba-111">要使用的資料庫會話。</span><span class="sxs-lookup"><span data-stu-id="38aba-111">The database session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="38aba-112">[資料庫]</span><span class="sxs-lookup"><span data-stu-id="38aba-112">database</span></span>  
    <span data-ttu-id="38aba-113">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="38aba-113">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="38aba-114">要卸離的資料庫。</span><span class="sxs-lookup"><span data-stu-id="38aba-114">The database to detach.</span></span>

<!-- end list -->

  - <span data-ttu-id="38aba-115">grbit</span><span class="sxs-lookup"><span data-stu-id="38aba-115">grbit</span></span>  
    <span data-ttu-id="38aba-116">型別： [DetachDatabaseGrbit](./detachdatabasegrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="38aba-116">Type: [Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit](./detachdatabasegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="38aba-117">卸離選項。</span><span class="sxs-lookup"><span data-stu-id="38aba-117">Detach options.</span></span>

## <a name="see-also"></a><span data-ttu-id="38aba-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="38aba-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="38aba-119">參考</span><span class="sxs-lookup"><span data-stu-id="38aba-119">Reference</span></span>

[<span data-ttu-id="38aba-120">Api 類別</span><span class="sxs-lookup"><span data-stu-id="38aba-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="38aba-121">Api 成員</span><span class="sxs-lookup"><span data-stu-id="38aba-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="38aba-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="38aba-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
