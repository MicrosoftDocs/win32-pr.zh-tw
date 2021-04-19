---
description: '深入瞭解： MakeKey 方法 (JET_SESID、JET_TABLEID、UInt32、MakeKeyGrbit) '
title: 'MakeKey 方法 (JET_SESID、JET_TABLEID、UInt32、MakeKeyGrbit) '
TOCTitle: MakeKey method (JET_SESID, JET_TABLEID, UInt32, MakeKeyGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.MakeKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.UInt32,Microsoft.Isam.Esent.Interop.MakeKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.makekey(v=EXCHG.10)
ms:contentKeyID: 55100848
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.MakeKey
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 45edbf959058ccb1c50b82a13f0ca84cdd16a7dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980481"
---
# <a name="apimakekey-method-jet_sesid-jet_tableid-uint32-makekeygrbit"></a><span data-ttu-id="43ab3-103">MakeKey 方法 (JET_SESID、JET_TABLEID、UInt32、MakeKeyGrbit) </span><span class="sxs-lookup"><span data-stu-id="43ab3-103">Api.MakeKey method (JET_SESID, JET_TABLEID, UInt32, MakeKeyGrbit)</span></span>

<span data-ttu-id="43ab3-104">建立可供 [JetSeek (JET_SESID、JET_TABLEID、SeekGrbit) ](./api.jetseek-method.md) 和 [JetSetIndexRange (JET_SESID、JET_TABLEID、SetIndexRangeGrbit) ](./api.jetsetindexrange-method.md)使用的搜尋索引鍵。</span><span class="sxs-lookup"><span data-stu-id="43ab3-104">Constructs a search key that may then be used by [JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) and [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md).</span></span>

<span data-ttu-id="43ab3-105">此 API 不符合 CLS 規範。</span><span class="sxs-lookup"><span data-stu-id="43ab3-105">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="43ab3-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="43ab3-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="43ab3-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="43ab3-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="43ab3-108">語法</span><span class="sxs-lookup"><span data-stu-id="43ab3-108">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Sub MakeKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    data As UInteger, _
    grbit As MakeKeyGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim data As UInteger
Dim grbit As MakeKeyGrbitApi.MakeKey(sesid, tableid, data, _
    grbit)
```

``` csharp
[CLSCompliantAttribute(false)]
public static void MakeKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
    uint data,
    MakeKeyGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="43ab3-109">參數</span><span class="sxs-lookup"><span data-stu-id="43ab3-109">Parameters</span></span>

  - <span data-ttu-id="43ab3-110">sesid</span><span class="sxs-lookup"><span data-stu-id="43ab3-110">sesid</span></span>  
    <span data-ttu-id="43ab3-111">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="43ab3-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="43ab3-112">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="43ab3-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="43ab3-113">tableid</span><span class="sxs-lookup"><span data-stu-id="43ab3-113">tableid</span></span>  
    <span data-ttu-id="43ab3-114">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="43ab3-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="43ab3-115">要在其上建立索引鍵的資料指標。</span><span class="sxs-lookup"><span data-stu-id="43ab3-115">The cursor to create the key on.</span></span>

<!-- end list -->

  - <span data-ttu-id="43ab3-116">data</span><span class="sxs-lookup"><span data-stu-id="43ab3-116">data</span></span>  
    <span data-ttu-id="43ab3-117">類型： [system.object](/dotnet/api/system.uint32)</span><span class="sxs-lookup"><span data-stu-id="43ab3-117">Type: [System.UInt32](/dotnet/api/system.uint32)</span></span>  
    
    <span data-ttu-id="43ab3-118">目前索引之目前索引鍵資料行的資料行資料。</span><span class="sxs-lookup"><span data-stu-id="43ab3-118">Column data for the current key column of the current index.</span></span>

<!-- end list -->

  - <span data-ttu-id="43ab3-119">grbit</span><span class="sxs-lookup"><span data-stu-id="43ab3-119">grbit</span></span>  
    <span data-ttu-id="43ab3-120">型別： [MakeKeyGrbit](./makekeygrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="43ab3-120">Type: [Microsoft.Isam.Esent.Interop.MakeKeyGrbit](./makekeygrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="43ab3-121">索引鍵選項。</span><span class="sxs-lookup"><span data-stu-id="43ab3-121">Key options.</span></span>

## <a name="see-also"></a><span data-ttu-id="43ab3-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="43ab3-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="43ab3-123">參考</span><span class="sxs-lookup"><span data-stu-id="43ab3-123">Reference</span></span>

[<span data-ttu-id="43ab3-124">Api 類別</span><span class="sxs-lookup"><span data-stu-id="43ab3-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="43ab3-125">Api 成員</span><span class="sxs-lookup"><span data-stu-id="43ab3-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="43ab3-126">MakeKey 多載</span><span class="sxs-lookup"><span data-stu-id="43ab3-126">MakeKey overload</span></span>](./api.makekey-method.md)

[<span data-ttu-id="43ab3-127">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="43ab3-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
