---
description: 深入瞭解： JetMakeKey 方法
title: JetMakeKey 方法
TOCTitle: 'JetMakeKey method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetMakeKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,Microsoft.Isam.Esent.Interop.MakeKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetmakekey(v=EXCHG.10)
ms:contentKeyID: 55100764
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetMakeKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetMakeKey
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 13db6e7106f5312e03ffa5acfbd86c72d38c6edb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945105"
---
# <a name="apijetmakekey-method"></a><span data-ttu-id="4bdbc-103">JetMakeKey 方法</span><span class="sxs-lookup"><span data-stu-id="4bdbc-103">Api.JetMakeKey method</span></span>

<span data-ttu-id="4bdbc-104">會建立可供 [JetSeek (JET_SESID、JET_TABLEID、SeekGrbit) ](./api.jetseek-method.md) 和 [JetSetIndexRange (JET_SESID、JET_TABLEID、SetIndexRangeGrbit) ](./api.jetsetindexrange-method.md)使用的搜尋索引鍵。</span><span class="sxs-lookup"><span data-stu-id="4bdbc-104">Constructs search keys that may then be used by [JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) and [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md).</span></span>

<span data-ttu-id="4bdbc-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4bdbc-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4bdbc-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="4bdbc-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4bdbc-107">語法</span><span class="sxs-lookup"><span data-stu-id="4bdbc-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetMakeKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    data As Byte(), _
    dataSize As Integer, _
    grbit As MakeKeyGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim data As Byte()
Dim dataSize As Integer
Dim grbit As MakeKeyGrbitApi.JetMakeKey(sesid, tableid, data, _
    dataSize, grbit)
```

``` csharp
public static void JetMakeKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] data,
    int dataSize,
    MakeKeyGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="4bdbc-108">參數</span><span class="sxs-lookup"><span data-stu-id="4bdbc-108">Parameters</span></span>

  - <span data-ttu-id="4bdbc-109">sesid</span><span class="sxs-lookup"><span data-stu-id="4bdbc-109">sesid</span></span>  
    <span data-ttu-id="4bdbc-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4bdbc-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="4bdbc-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="4bdbc-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="4bdbc-112">tableid</span><span class="sxs-lookup"><span data-stu-id="4bdbc-112">tableid</span></span>  
    <span data-ttu-id="4bdbc-113">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4bdbc-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="4bdbc-114">要在其上建立索引鍵的資料指標。</span><span class="sxs-lookup"><span data-stu-id="4bdbc-114">The cursor to create the key on.</span></span>

<!-- end list -->

  - <span data-ttu-id="4bdbc-115">data</span><span class="sxs-lookup"><span data-stu-id="4bdbc-115">data</span></span>  
    <span data-ttu-id="4bdbc-116">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="4bdbc-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="4bdbc-117">目前索引之目前索引鍵資料行的資料行資料。</span><span class="sxs-lookup"><span data-stu-id="4bdbc-117">Column data for the current key column of the current index.</span></span>

<!-- end list -->

  - <span data-ttu-id="4bdbc-118">dataSize</span><span class="sxs-lookup"><span data-stu-id="4bdbc-118">dataSize</span></span>  
    <span data-ttu-id="4bdbc-119">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="4bdbc-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="4bdbc-120">資料的大小。</span><span class="sxs-lookup"><span data-stu-id="4bdbc-120">Size of the data.</span></span>

<!-- end list -->

  - <span data-ttu-id="4bdbc-121">grbit</span><span class="sxs-lookup"><span data-stu-id="4bdbc-121">grbit</span></span>  
    <span data-ttu-id="4bdbc-122">型別： [MakeKeyGrbit](./makekeygrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="4bdbc-122">Type: [Microsoft.Isam.Esent.Interop.MakeKeyGrbit](./makekeygrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="4bdbc-123">索引鍵選項。</span><span class="sxs-lookup"><span data-stu-id="4bdbc-123">Key options.</span></span>

## <a name="remarks"></a><span data-ttu-id="4bdbc-124">備註</span><span class="sxs-lookup"><span data-stu-id="4bdbc-124">Remarks</span></span>

<span data-ttu-id="4bdbc-125">MakeKey 函式會提供資料類型特有的索引鍵功能。</span><span class="sxs-lookup"><span data-stu-id="4bdbc-125">The MakeKey functions provide datatype-specific make key functionality.</span></span>

## <a name="see-also"></a><span data-ttu-id="4bdbc-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4bdbc-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4bdbc-127">參考</span><span class="sxs-lookup"><span data-stu-id="4bdbc-127">Reference</span></span>

[<span data-ttu-id="4bdbc-128">Api 類別</span><span class="sxs-lookup"><span data-stu-id="4bdbc-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="4bdbc-129">Api 成員</span><span class="sxs-lookup"><span data-stu-id="4bdbc-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="4bdbc-130">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="4bdbc-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
