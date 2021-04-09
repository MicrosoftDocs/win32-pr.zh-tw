---
description: 深入瞭解： JetDelete 方法
title: JetDelete 方法
TOCTitle: 'JetDelete method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDelete(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdelete(v=EXCHG.10)
ms:contentKeyID: 55100681
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDelete
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDelete
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cbc3decf125b8d3f3f1df7228852901cca90aae8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847853"
---
# <a name="apijetdelete-method"></a><span data-ttu-id="8e615-103">JetDelete 方法</span><span class="sxs-lookup"><span data-stu-id="8e615-103">Api.JetDelete method</span></span>

<span data-ttu-id="8e615-104">刪除資料庫資料表中的目前記錄。</span><span class="sxs-lookup"><span data-stu-id="8e615-104">Deletes the current record in a database table.</span></span>

<span data-ttu-id="8e615-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8e615-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8e615-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="8e615-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8e615-107">語法</span><span class="sxs-lookup"><span data-stu-id="8e615-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetDelete ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEIDApi.JetDelete(sesid, tableid)
```

``` csharp
public static void JetDelete(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="8e615-108">參數</span><span class="sxs-lookup"><span data-stu-id="8e615-108">Parameters</span></span>

  - <span data-ttu-id="8e615-109">sesid</span><span class="sxs-lookup"><span data-stu-id="8e615-109">sesid</span></span>  
    <span data-ttu-id="8e615-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8e615-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="8e615-111">開啟資料指標的會話。</span><span class="sxs-lookup"><span data-stu-id="8e615-111">The session that opened the cursor.</span></span>

<!-- end list -->

  - <span data-ttu-id="8e615-112">tableid</span><span class="sxs-lookup"><span data-stu-id="8e615-112">tableid</span></span>  
    <span data-ttu-id="8e615-113">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8e615-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="8e615-114">資料庫資料表上的資料指標。</span><span class="sxs-lookup"><span data-stu-id="8e615-114">The cursor on a database table.</span></span> <span data-ttu-id="8e615-115">將會刪除目前的資料列。</span><span class="sxs-lookup"><span data-stu-id="8e615-115">The current row will be deleted.</span></span>

## <a name="see-also"></a><span data-ttu-id="8e615-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8e615-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8e615-117">參考</span><span class="sxs-lookup"><span data-stu-id="8e615-117">Reference</span></span>

[<span data-ttu-id="8e615-118">Api 類別</span><span class="sxs-lookup"><span data-stu-id="8e615-118">Api class</span></span>](./api-class.md)

[<span data-ttu-id="8e615-119">Api 成員</span><span class="sxs-lookup"><span data-stu-id="8e615-119">Api members</span></span>](./api-members.md)

[<span data-ttu-id="8e615-120">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="8e615-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
