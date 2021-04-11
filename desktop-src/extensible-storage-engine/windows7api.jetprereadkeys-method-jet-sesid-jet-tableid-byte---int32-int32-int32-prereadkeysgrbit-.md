---
description: '深入瞭解： Windows7Api. JetPrereadKeys 方法 (JET_SESID、JET_TABLEID、Byte [] []、Int32、Int32、Int32、PrereadKeysGrbit) '
title: 'Windows7Api. JetPrereadKeys 方法 (JET_SESID、JET_TABLEID、Byte [] []、Int32、Int32、Int32、PrereadKeysGrbit)  (最為理想) '
TOCTitle: JetPrereadKeys method (JET_SESID, JET_TABLEID, Byte[][], Int32 , Int32, Int32, PrereadKeysGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows7.Windows7Api.JetPrereadKeys(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[][],System.Int32[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.Windows7.PrereadKeysGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows7.windows7api.jetprereadkeys(v=EXCHG.10)
ms:contentKeyID: 55107785
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Windows7.Windows7Api.JetPrereadKeys
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 66f85c08c1fccc58702d4ac4cf170d6b0493ab8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026081"
---
# <a name="windows7apijetprereadkeys-method-jet_sesid-jet_tableid-byte-int32--int32-int32-prereadkeysgrbit"></a><span data-ttu-id="d3337-103">Windows7Api. JetPrereadKeys 方法 (JET_SESID、JET_TABLEID、Byte \[ \] \[ \] 、int32、int32、int32、PrereadKeysGrbit) </span><span class="sxs-lookup"><span data-stu-id="d3337-103">Windows7Api.JetPrereadKeys method (JET_SESID, JET_TABLEID, Byte\[\]\[\], Int32 , Int32, Int32, PrereadKeysGrbit)</span></span>

<span data-ttu-id="d3337-104">如果具有指定索引鍵的記錄不在緩衝區快取中，則會啟動非同步讀取，以將記錄帶入資料庫緩衝區快取中。</span><span class="sxs-lookup"><span data-stu-id="d3337-104">If the records with the specified keys are not in the buffer cache then start asynchronous reads to bring the records into the database buffer cache.</span></span>

<span data-ttu-id="d3337-105">**命名空間：**  [Microsoft 最為理想](./microsoft.isam.esent.interop.windows7-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d3337-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows7](./microsoft.isam.esent.interop.windows7-namespace.md)</span></span>  
<span data-ttu-id="d3337-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="d3337-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d3337-107">語法</span><span class="sxs-lookup"><span data-stu-id="d3337-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetPrereadKeys ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    keys As Byte()(), _
    keyLengths As Integer(), _
    keyCount As Integer, _
    <OutAttribute> ByRef keysPreread As Integer, _
    grbit As PrereadKeysGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim keys As Byte()()
Dim keyLengths As Integer()
Dim keyCount As Integer
Dim keysPreread As Integer
Dim grbit As PrereadKeysGrbitWindows7Api.JetPrereadKeys(sesid, tableid, _
    keys, keyLengths, keyCount, keysPreread, _
    grbit)
```

``` csharp
public static void JetPrereadKeys(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[][] keys,
    int[] keyLengths,
    int keyCount,
    out int keysPreread,
    PrereadKeysGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="d3337-108">參數</span><span class="sxs-lookup"><span data-stu-id="d3337-108">Parameters</span></span>

  - <span data-ttu-id="d3337-109">sesid</span><span class="sxs-lookup"><span data-stu-id="d3337-109">sesid</span></span>  
    <span data-ttu-id="d3337-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d3337-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="d3337-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="d3337-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="d3337-112">tableid</span><span class="sxs-lookup"><span data-stu-id="d3337-112">tableid</span></span>  
    <span data-ttu-id="d3337-113">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d3337-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="d3337-114">要針對其發出 prereads 的資料表。</span><span class="sxs-lookup"><span data-stu-id="d3337-114">The table to issue the prereads against.</span></span>

<!-- end list -->

  - <span data-ttu-id="d3337-115">金鑰</span><span class="sxs-lookup"><span data-stu-id="d3337-115">keys</span></span>  
    <span data-ttu-id="d3337-116">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="d3337-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="d3337-117">要 preread 的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="d3337-117">The keys to preread.</span></span> <span data-ttu-id="d3337-118">金鑰必須經過排序。</span><span class="sxs-lookup"><span data-stu-id="d3337-118">The keys must be sorted.</span></span>

<!-- end list -->

  - <span data-ttu-id="d3337-119">keyLengths</span><span class="sxs-lookup"><span data-stu-id="d3337-119">keyLengths</span></span>  
    <span data-ttu-id="d3337-120">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="d3337-120">Type: \[\]</span></span>  
    
    <span data-ttu-id="d3337-121">要 preread 的索引鍵長度。</span><span class="sxs-lookup"><span data-stu-id="d3337-121">The lengths of the keys to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="d3337-122">keyCount</span><span class="sxs-lookup"><span data-stu-id="d3337-122">keyCount</span></span>  
    <span data-ttu-id="d3337-123">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="d3337-123">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="d3337-124">要 preread 的索引鍵數目上限。</span><span class="sxs-lookup"><span data-stu-id="d3337-124">The maximum number of keys to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="d3337-125">keysPreread</span><span class="sxs-lookup"><span data-stu-id="d3337-125">keysPreread</span></span>  
    <span data-ttu-id="d3337-126">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="d3337-126">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="d3337-127">傳回要實際 preread 的索引鍵數目。</span><span class="sxs-lookup"><span data-stu-id="d3337-127">Returns the number of keys to actually preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="d3337-128">grbit</span><span class="sxs-lookup"><span data-stu-id="d3337-128">grbit</span></span>  
    <span data-ttu-id="d3337-129">型別： [最為理想. PrereadKeysGrbit](./prereadkeysgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="d3337-129">Type: [Microsoft.Isam.Esent.Interop.Windows7.PrereadKeysGrbit](./prereadkeysgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="d3337-130">Preread 選項。</span><span class="sxs-lookup"><span data-stu-id="d3337-130">Preread options.</span></span> <span data-ttu-id="d3337-131">用來指定 preread 的方向。</span><span class="sxs-lookup"><span data-stu-id="d3337-131">Used to specify the direction of the preread.</span></span>

## <a name="see-also"></a><span data-ttu-id="d3337-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d3337-132">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d3337-133">參考</span><span class="sxs-lookup"><span data-stu-id="d3337-133">Reference</span></span>

[<span data-ttu-id="d3337-134">Windows7Api 類別</span><span class="sxs-lookup"><span data-stu-id="d3337-134">Windows7Api class</span></span>](./windows7api-class.md)

[<span data-ttu-id="d3337-135">Windows7Api 成員</span><span class="sxs-lookup"><span data-stu-id="d3337-135">Windows7Api members</span></span>](./windows7api-members.md)

[<span data-ttu-id="d3337-136">JetPrereadKeys 多載</span><span class="sxs-lookup"><span data-stu-id="d3337-136">JetPrereadKeys overload</span></span>](./windows7api.jetprereadkeys-method.md)

[<span data-ttu-id="d3337-137">最為理想命名空間。</span><span class="sxs-lookup"><span data-stu-id="d3337-137">Microsoft.Isam.Esent.Interop.Windows7 namespace</span></span>](./microsoft.isam.esent.interop.windows7-namespace.md)
