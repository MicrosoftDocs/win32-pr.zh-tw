---
description: 深入瞭解： JetComputeStats 方法
title: JetComputeStats 方法
TOCTitle: 'JetComputeStats method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetComputeStats(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcomputestats(v=EXCHG.10)
ms:contentKeyID: 55100667
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetComputeStats
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetComputeStats
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2b102aca5971656232fae02684aeab30322d208b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191104"
---
# <a name="apijetcomputestats-method"></a><span data-ttu-id="fe2f4-103">JetComputeStats 方法</span><span class="sxs-lookup"><span data-stu-id="fe2f4-103">Api.JetComputeStats method</span></span>

<span data-ttu-id="fe2f4-104">逐步解說資料表的每個索引，以精確計算索引中的專案數，以及索引中的相異索引鍵數目。</span><span class="sxs-lookup"><span data-stu-id="fe2f4-104">Walks each index of a table to exactly compute the number of entries in an index, and the number of distinct keys in an index.</span></span> <span data-ttu-id="fe2f4-105">這項資訊，以及配置給索引的資料庫頁面數目和目前的計算時間，都會儲存在資料庫的索引中繼資料中。</span><span class="sxs-lookup"><span data-stu-id="fe2f4-105">This information, together with the number of database pages allocated for an index and the current time of the computation is stored in index metadata in the database.</span></span> <span data-ttu-id="fe2f4-106">之後可以使用資訊作業來抓取此資料。</span><span class="sxs-lookup"><span data-stu-id="fe2f4-106">This data can be subsequently retrieved with information operations.</span></span>

<span data-ttu-id="fe2f4-107">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fe2f4-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="fe2f4-108">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="fe2f4-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fe2f4-109">語法</span><span class="sxs-lookup"><span data-stu-id="fe2f4-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetComputeStats ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEIDApi.JetComputeStats(sesid, tableid)
```

``` csharp
public static void JetComputeStats(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="fe2f4-110">參數</span><span class="sxs-lookup"><span data-stu-id="fe2f4-110">Parameters</span></span>

  - <span data-ttu-id="fe2f4-111">sesid</span><span class="sxs-lookup"><span data-stu-id="fe2f4-111">sesid</span></span>  
    <span data-ttu-id="fe2f4-112">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="fe2f4-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="fe2f4-113">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="fe2f4-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="fe2f4-114">tableid</span><span class="sxs-lookup"><span data-stu-id="fe2f4-114">tableid</span></span>  
    <span data-ttu-id="fe2f4-115">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="fe2f4-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="fe2f4-116">將計算統計資料的資料表。</span><span class="sxs-lookup"><span data-stu-id="fe2f4-116">The table that the statistics will be computed on.</span></span>

## <a name="see-also"></a><span data-ttu-id="fe2f4-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fe2f4-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fe2f4-118">參考</span><span class="sxs-lookup"><span data-stu-id="fe2f4-118">Reference</span></span>

[<span data-ttu-id="fe2f4-119">Api 類別</span><span class="sxs-lookup"><span data-stu-id="fe2f4-119">Api class</span></span>](./api-class.md)

[<span data-ttu-id="fe2f4-120">Api 成員</span><span class="sxs-lookup"><span data-stu-id="fe2f4-120">Api members</span></span>](./api-members.md)

[<span data-ttu-id="fe2f4-121">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="fe2f4-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
