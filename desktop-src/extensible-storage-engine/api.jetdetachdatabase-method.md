---
description: 深入瞭解： JetDetachDatabase 方法
title: JetDetachDatabase 方法
TOCTitle: 'JetDetachDatabase method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDetachDatabase(Microsoft.Isam.Esent.Interop.JET_SESID,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdetachdatabase(v=EXCHG.10)
ms:contentKeyID: 55100687
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDetachDatabase
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDetachDatabase
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8881021d619bac1dae83a4a001e6b88e94e57256
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973619"
---
# <a name="apijetdetachdatabase-method"></a><span data-ttu-id="8640b-103">JetDetachDatabase 方法</span><span class="sxs-lookup"><span data-stu-id="8640b-103">Api.JetDetachDatabase method</span></span>

<span data-ttu-id="8640b-104">釋放先前附加至資料庫會話的資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="8640b-104">Releases a database file that was previously attached to a database session.</span></span>

<span data-ttu-id="8640b-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8640b-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8640b-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="8640b-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8640b-107">語法</span><span class="sxs-lookup"><span data-stu-id="8640b-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetDetachDatabase ( _
    sesid As JET_SESID, _
    database As String _
)
'Usage
Dim sesid As JET_SESID
Dim database As StringApi.JetDetachDatabase(sesid, database)
```

``` csharp
public static void JetDetachDatabase(
    JET_SESID sesid,
    string database
)
```

#### <a name="parameters"></a><span data-ttu-id="8640b-108">參數</span><span class="sxs-lookup"><span data-stu-id="8640b-108">Parameters</span></span>

  - <span data-ttu-id="8640b-109">sesid</span><span class="sxs-lookup"><span data-stu-id="8640b-109">sesid</span></span>  
    <span data-ttu-id="8640b-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8640b-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="8640b-111">要使用的資料庫會話。</span><span class="sxs-lookup"><span data-stu-id="8640b-111">The database session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="8640b-112">[資料庫]</span><span class="sxs-lookup"><span data-stu-id="8640b-112">database</span></span>  
    <span data-ttu-id="8640b-113">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="8640b-113">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="8640b-114">要卸離的資料庫。</span><span class="sxs-lookup"><span data-stu-id="8640b-114">The database to detach.</span></span>

## <a name="see-also"></a><span data-ttu-id="8640b-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8640b-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8640b-116">參考</span><span class="sxs-lookup"><span data-stu-id="8640b-116">Reference</span></span>

[<span data-ttu-id="8640b-117">Api 類別</span><span class="sxs-lookup"><span data-stu-id="8640b-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="8640b-118">Api 成員</span><span class="sxs-lookup"><span data-stu-id="8640b-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="8640b-119">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="8640b-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
