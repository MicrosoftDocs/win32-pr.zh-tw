---
description: 深入瞭解： JetSeek 方法
title: JetSeek 方法
TOCTitle: 'JetSeek method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSeek(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.SeekGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetseek(v=EXCHG.10)
ms:contentKeyID: 55100796
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSeek
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSeek
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 85c8c61bd4e56b342b33d26f22ae3946967640e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945287"
---
# <a name="apijetseek-method"></a><span data-ttu-id="6268c-103">JetSeek 方法</span><span class="sxs-lookup"><span data-stu-id="6268c-103">Api.JetSeek method</span></span>

<span data-ttu-id="6268c-104">有效率地將游標放在索引項目目，以符合該資料指標中的搜尋索引鍵所指定的搜尋條件，以及指定的不相等。</span><span class="sxs-lookup"><span data-stu-id="6268c-104">Efficiently positions a cursor to an index entry that matches the search criteria specified by the search key in that cursor and the specified inequality.</span></span> <span data-ttu-id="6268c-105">您先前必須使用[JetMakeKey (JET_SESID、JET_TABLEID、 \[ \] 、Int32、MakeKeyGrbit) ](./api.jetmakekey-method.md)來建立搜尋索引鍵。</span><span class="sxs-lookup"><span data-stu-id="6268c-105">A search key must have been previously constructed using [JetMakeKey(JET_SESID, JET_TABLEID, \[\], Int32, MakeKeyGrbit)](./api.jetmakekey-method.md).</span></span> <span data-ttu-id="6268c-106">另請參閱 [TrySeek (JET_SESID、JET_TABLEID、SeekGrbit) ](./api.tryseek-method.md)。</span><span class="sxs-lookup"><span data-stu-id="6268c-106">Also see [TrySeek(JET_SESID, JET_TABLEID, SeekGrbit)](./api.tryseek-method.md).</span></span>

<span data-ttu-id="6268c-107">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6268c-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6268c-108">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="6268c-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6268c-109">語法</span><span class="sxs-lookup"><span data-stu-id="6268c-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetSeek ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As SeekGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As SeekGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetSeek(sesid, _
    tableid, grbit)
```

``` csharp
public static JET_wrn JetSeek(
    JET_SESID sesid,
    JET_TABLEID tableid,
    SeekGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="6268c-110">參數</span><span class="sxs-lookup"><span data-stu-id="6268c-110">Parameters</span></span>

  - <span data-ttu-id="6268c-111">sesid</span><span class="sxs-lookup"><span data-stu-id="6268c-111">sesid</span></span>  
    <span data-ttu-id="6268c-112">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6268c-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="6268c-113">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="6268c-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="6268c-114">tableid</span><span class="sxs-lookup"><span data-stu-id="6268c-114">tableid</span></span>  
    <span data-ttu-id="6268c-115">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6268c-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="6268c-116">要放置的游標。</span><span class="sxs-lookup"><span data-stu-id="6268c-116">The cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="6268c-117">grbit</span><span class="sxs-lookup"><span data-stu-id="6268c-117">grbit</span></span>  
    <span data-ttu-id="6268c-118">型別： [SeekGrbit](./seekgrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="6268c-118">Type: [Microsoft.Isam.Esent.Interop.SeekGrbit](./seekgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="6268c-119">搜尋選項。</span><span class="sxs-lookup"><span data-stu-id="6268c-119">Seek options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="6268c-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="6268c-120">Return value</span></span>

<span data-ttu-id="6268c-121">類型： [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="6268c-121">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="6268c-122">ESENT 警告。</span><span class="sxs-lookup"><span data-stu-id="6268c-122">An ESENT warning.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6268c-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6268c-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6268c-124">參考</span><span class="sxs-lookup"><span data-stu-id="6268c-124">Reference</span></span>

[<span data-ttu-id="6268c-125">Api 類別</span><span class="sxs-lookup"><span data-stu-id="6268c-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="6268c-126">Api 成員</span><span class="sxs-lookup"><span data-stu-id="6268c-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="6268c-127">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="6268c-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
