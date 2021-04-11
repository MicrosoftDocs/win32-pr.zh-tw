---
description: '深入瞭解： MakeKey 方法 (JET_SESID、JET_TABLEID、雙重、MakeKeyGrbit) '
title: 'MakeKey 方法 (JET_SESID、JET_TABLEID、Double、MakeKeyGrbit) '
TOCTitle: MakeKey method (JET_SESID, JET_TABLEID, Double, MakeKeyGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.MakeKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Double,Microsoft.Isam.Esent.Interop.MakeKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.makekey(v=EXCHG.10)
ms:contentKeyID: 55100839
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
ms.openlocfilehash: 3b0e78b2828ae8727fea7b7909c903bbc7381505
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848339"
---
# <a name="apimakekey-method-jet_sesid-jet_tableid-double-makekeygrbit"></a><span data-ttu-id="5b270-103">MakeKey 方法 (JET_SESID、JET_TABLEID、Double、MakeKeyGrbit) </span><span class="sxs-lookup"><span data-stu-id="5b270-103">Api.MakeKey method (JET_SESID, JET_TABLEID, Double, MakeKeyGrbit)</span></span>

<span data-ttu-id="5b270-104">建立可供 [JetSeek (JET_SESID、JET_TABLEID、SeekGrbit) ](./api.jetseek-method.md) 和 [JetSetIndexRange (JET_SESID、JET_TABLEID、SetIndexRangeGrbit) ](./api.jetsetindexrange-method.md)使用的搜尋索引鍵。</span><span class="sxs-lookup"><span data-stu-id="5b270-104">Constructs a search key that may then be used by [JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) and [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md).</span></span>

<span data-ttu-id="5b270-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5b270-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5b270-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="5b270-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5b270-107">語法</span><span class="sxs-lookup"><span data-stu-id="5b270-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub MakeKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    data As Double, _
    grbit As MakeKeyGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim data As Double
Dim grbit As MakeKeyGrbitApi.MakeKey(sesid, tableid, data, _
    grbit)
```

``` csharp
public static void MakeKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
    double data,
    MakeKeyGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="5b270-108">參數</span><span class="sxs-lookup"><span data-stu-id="5b270-108">Parameters</span></span>

  - <span data-ttu-id="5b270-109">sesid</span><span class="sxs-lookup"><span data-stu-id="5b270-109">sesid</span></span>  
    <span data-ttu-id="5b270-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5b270-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="5b270-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="5b270-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="5b270-112">tableid</span><span class="sxs-lookup"><span data-stu-id="5b270-112">tableid</span></span>  
    <span data-ttu-id="5b270-113">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5b270-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="5b270-114">要在其上建立索引鍵的資料指標。</span><span class="sxs-lookup"><span data-stu-id="5b270-114">The cursor to create the key on.</span></span>

<!-- end list -->

  - <span data-ttu-id="5b270-115">data</span><span class="sxs-lookup"><span data-stu-id="5b270-115">data</span></span>  
    <span data-ttu-id="5b270-116">類型： [Double](/dotnet/api/system.double)</span><span class="sxs-lookup"><span data-stu-id="5b270-116">Type: [System.Double](/dotnet/api/system.double)</span></span>  
    
    <span data-ttu-id="5b270-117">目前索引之目前索引鍵資料行的資料行資料。</span><span class="sxs-lookup"><span data-stu-id="5b270-117">Column data for the current key column of the current index.</span></span>

<!-- end list -->

  - <span data-ttu-id="5b270-118">grbit</span><span class="sxs-lookup"><span data-stu-id="5b270-118">grbit</span></span>  
    <span data-ttu-id="5b270-119">型別： [MakeKeyGrbit](./makekeygrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="5b270-119">Type: [Microsoft.Isam.Esent.Interop.MakeKeyGrbit](./makekeygrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="5b270-120">索引鍵選項。</span><span class="sxs-lookup"><span data-stu-id="5b270-120">Key options.</span></span>

## <a name="see-also"></a><span data-ttu-id="5b270-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5b270-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5b270-122">參考</span><span class="sxs-lookup"><span data-stu-id="5b270-122">Reference</span></span>

[<span data-ttu-id="5b270-123">Api 類別</span><span class="sxs-lookup"><span data-stu-id="5b270-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="5b270-124">Api 成員</span><span class="sxs-lookup"><span data-stu-id="5b270-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="5b270-125">MakeKey 多載</span><span class="sxs-lookup"><span data-stu-id="5b270-125">MakeKey overload</span></span>](./api.makekey-method.md)

[<span data-ttu-id="5b270-126">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="5b270-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
