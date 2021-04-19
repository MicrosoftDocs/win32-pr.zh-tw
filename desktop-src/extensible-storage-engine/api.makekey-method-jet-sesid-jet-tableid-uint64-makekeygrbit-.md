---
description: '深入瞭解： MakeKey 方法 (JET_SESID、JET_TABLEID、UInt64、MakeKeyGrbit) '
title: 'MakeKey 方法 (JET_SESID、JET_TABLEID、UInt64、MakeKeyGrbit) '
TOCTitle: MakeKey method (JET_SESID, JET_TABLEID, UInt64, MakeKeyGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.MakeKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.UInt64,Microsoft.Isam.Esent.Interop.MakeKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.makekey(v=EXCHG.10)
ms:contentKeyID: 55100827
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.MakeKey
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0cb4b26015e67e6801fe0e19ee0b0ca8d41ac4e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984636"
---
# <a name="apimakekey-method-jet_sesid-jet_tableid-uint64-makekeygrbit"></a><span data-ttu-id="a0e8b-103">MakeKey 方法 (JET_SESID、JET_TABLEID、UInt64、MakeKeyGrbit) </span><span class="sxs-lookup"><span data-stu-id="a0e8b-103">Api.MakeKey method (JET_SESID, JET_TABLEID, UInt64, MakeKeyGrbit)</span></span>

<span data-ttu-id="a0e8b-104">建立可供 [JetSeek (JET_SESID、JET_TABLEID、SeekGrbit) ](./api.jetseek-method.md) 和 [JetSetIndexRange (JET_SESID、JET_TABLEID、SetIndexRangeGrbit) ](./api.jetsetindexrange-method.md)使用的搜尋索引鍵。</span><span class="sxs-lookup"><span data-stu-id="a0e8b-104">Constructs a search key that may then be used by [JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) and [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md).</span></span>

<span data-ttu-id="a0e8b-105">此 API 不符合 CLS 規範。</span><span class="sxs-lookup"><span data-stu-id="a0e8b-105">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="a0e8b-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a0e8b-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a0e8b-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="a0e8b-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a0e8b-108">語法</span><span class="sxs-lookup"><span data-stu-id="a0e8b-108">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Sub MakeKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    data As ULong, _
    grbit As MakeKeyGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim data As ULong
Dim grbit As MakeKeyGrbitApi.MakeKey(sesid, tableid, data, _
    grbit)
```

``` csharp
[CLSCompliantAttribute(false)]
public static void MakeKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
    ulong data,
    MakeKeyGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="a0e8b-109">參數</span><span class="sxs-lookup"><span data-stu-id="a0e8b-109">Parameters</span></span>

  - <span data-ttu-id="a0e8b-110">sesid</span><span class="sxs-lookup"><span data-stu-id="a0e8b-110">sesid</span></span>  
    <span data-ttu-id="a0e8b-111">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a0e8b-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="a0e8b-112">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="a0e8b-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="a0e8b-113">tableid</span><span class="sxs-lookup"><span data-stu-id="a0e8b-113">tableid</span></span>  
    <span data-ttu-id="a0e8b-114">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a0e8b-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="a0e8b-115">要在其上建立索引鍵的資料指標。</span><span class="sxs-lookup"><span data-stu-id="a0e8b-115">The cursor to create the key on.</span></span>

<!-- end list -->

  - <span data-ttu-id="a0e8b-116">data</span><span class="sxs-lookup"><span data-stu-id="a0e8b-116">data</span></span>  
    <span data-ttu-id="a0e8b-117">類型： [system.object](/dotnet/api/system.uint64)</span><span class="sxs-lookup"><span data-stu-id="a0e8b-117">Type: [System.UInt64](/dotnet/api/system.uint64)</span></span>  
    
    <span data-ttu-id="a0e8b-118">目前索引之目前索引鍵資料行的資料行資料。</span><span class="sxs-lookup"><span data-stu-id="a0e8b-118">Column data for the current key column of the current index.</span></span>

<!-- end list -->

  - <span data-ttu-id="a0e8b-119">grbit</span><span class="sxs-lookup"><span data-stu-id="a0e8b-119">grbit</span></span>  
    <span data-ttu-id="a0e8b-120">型別： [MakeKeyGrbit](./makekeygrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="a0e8b-120">Type: [Microsoft.Isam.Esent.Interop.MakeKeyGrbit](./makekeygrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="a0e8b-121">索引鍵選項。</span><span class="sxs-lookup"><span data-stu-id="a0e8b-121">Key options.</span></span>

## <a name="see-also"></a><span data-ttu-id="a0e8b-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a0e8b-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a0e8b-123">參考</span><span class="sxs-lookup"><span data-stu-id="a0e8b-123">Reference</span></span>

[<span data-ttu-id="a0e8b-124">Api 類別</span><span class="sxs-lookup"><span data-stu-id="a0e8b-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="a0e8b-125">Api 成員</span><span class="sxs-lookup"><span data-stu-id="a0e8b-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="a0e8b-126">MakeKey 多載</span><span class="sxs-lookup"><span data-stu-id="a0e8b-126">MakeKey overload</span></span>](./api.makekey-method.md)

[<span data-ttu-id="a0e8b-127">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="a0e8b-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
