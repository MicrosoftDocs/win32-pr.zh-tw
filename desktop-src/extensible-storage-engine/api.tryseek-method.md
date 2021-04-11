---
description: 深入瞭解： TrySeek 方法
title: TrySeek 方法
TOCTitle: 'TrySeek method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TrySeek(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.SeekGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.tryseek(v=EXCHG.10)
ms:contentKeyID: 55100941
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TrySeek
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TrySeek
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 46472c59c14bd515e744a7ccfa908752783d27fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847843"
---
# <a name="apitryseek-method"></a><span data-ttu-id="f9168-103">TrySeek 方法</span><span class="sxs-lookup"><span data-stu-id="f9168-103">Api.TrySeek method</span></span>

<span data-ttu-id="f9168-104">有效率地將游標放在索引項目目，以符合該資料指標中的搜尋索引鍵所指定的搜尋條件，以及指定的不相等。</span><span class="sxs-lookup"><span data-stu-id="f9168-104">Efficiently positions a cursor to an index entry that matches the search criteria specified by the search key in that cursor and the specified inequality.</span></span> <span data-ttu-id="f9168-105">搜尋金鑰必須先前已使用 JetMakeKey 來建立。</span><span class="sxs-lookup"><span data-stu-id="f9168-105">A search key must have been previously constructed using JetMakeKey.</span></span>

<span data-ttu-id="f9168-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f9168-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f9168-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="f9168-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f9168-108">語法</span><span class="sxs-lookup"><span data-stu-id="f9168-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function TrySeek ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As SeekGrbit _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As SeekGrbit
Dim returnValue As Boolean

returnValue = Api.TrySeek(sesid, _
    tableid, grbit)
```

``` csharp
public static bool TrySeek(
    JET_SESID sesid,
    JET_TABLEID tableid,
    SeekGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="f9168-109">參數</span><span class="sxs-lookup"><span data-stu-id="f9168-109">Parameters</span></span>

  - <span data-ttu-id="f9168-110">sesid</span><span class="sxs-lookup"><span data-stu-id="f9168-110">sesid</span></span>  
    <span data-ttu-id="f9168-111">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f9168-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="f9168-112">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="f9168-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="f9168-113">tableid</span><span class="sxs-lookup"><span data-stu-id="f9168-113">tableid</span></span>  
    <span data-ttu-id="f9168-114">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f9168-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="f9168-115">要放置的游標。</span><span class="sxs-lookup"><span data-stu-id="f9168-115">The cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="f9168-116">grbit</span><span class="sxs-lookup"><span data-stu-id="f9168-116">grbit</span></span>  
    <span data-ttu-id="f9168-117">型別： [SeekGrbit](./seekgrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="f9168-117">Type: [Microsoft.Isam.Esent.Interop.SeekGrbit](./seekgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="f9168-118">搜尋選項。</span><span class="sxs-lookup"><span data-stu-id="f9168-118">Seek option.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f9168-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="f9168-119">Return value</span></span>

<span data-ttu-id="f9168-120">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="f9168-120">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="f9168-121">如果找到符合準則的記錄，則為 True。</span><span class="sxs-lookup"><span data-stu-id="f9168-121">True if a record matching the criteria was found.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f9168-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f9168-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f9168-123">參考</span><span class="sxs-lookup"><span data-stu-id="f9168-123">Reference</span></span>

[<span data-ttu-id="f9168-124">Api 類別</span><span class="sxs-lookup"><span data-stu-id="f9168-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="f9168-125">Api 成員</span><span class="sxs-lookup"><span data-stu-id="f9168-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="f9168-126">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="f9168-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
