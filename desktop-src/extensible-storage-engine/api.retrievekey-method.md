---
description: 深入瞭解： RetrieveKey 方法
title: RetrieveKey 方法
TOCTitle: 'RetrieveKey method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.RetrieveKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievekey(v=EXCHG.10)
ms:contentKeyID: 55100880
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.RetrieveKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveKey
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fcabab7639a9cf3128b0b2c314ba60c2de8f8e09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689423"
---
# <a name="apiretrievekey-method"></a><span data-ttu-id="ab2a7-103">RetrieveKey 方法</span><span class="sxs-lookup"><span data-stu-id="ab2a7-103">Api.RetrieveKey method</span></span>

<span data-ttu-id="ab2a7-104">在資料指標的目前位置，抓取索引項目的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="ab2a7-104">Retrieves the key for the index entry at the current position of a cursor.</span></span>

<span data-ttu-id="ab2a7-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ab2a7-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ab2a7-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="ab2a7-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ab2a7-107">語法</span><span class="sxs-lookup"><span data-stu-id="ab2a7-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As RetrieveKeyGrbit _
) As Byte()
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As RetrieveKeyGrbit
Dim returnValue As Byte()

returnValue = Api.RetrieveKey(sesid, _
    tableid, grbit)
```

``` csharp
public static byte[] RetrieveKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
    RetrieveKeyGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="ab2a7-108">參數</span><span class="sxs-lookup"><span data-stu-id="ab2a7-108">Parameters</span></span>

  - <span data-ttu-id="ab2a7-109">sesid</span><span class="sxs-lookup"><span data-stu-id="ab2a7-109">sesid</span></span>  
    <span data-ttu-id="ab2a7-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ab2a7-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="ab2a7-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="ab2a7-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="ab2a7-112">tableid</span><span class="sxs-lookup"><span data-stu-id="ab2a7-112">tableid</span></span>  
    <span data-ttu-id="ab2a7-113">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ab2a7-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="ab2a7-114">從中取出索引鍵的資料指標。</span><span class="sxs-lookup"><span data-stu-id="ab2a7-114">The cursor to retrieve the key from.</span></span>

<!-- end list -->

  - <span data-ttu-id="ab2a7-115">grbit</span><span class="sxs-lookup"><span data-stu-id="ab2a7-115">grbit</span></span>  
    <span data-ttu-id="ab2a7-116">型別： [RetrieveKeyGrbit](./retrievekeygrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="ab2a7-116">Type: [Microsoft.Isam.Esent.Interop.RetrieveKeyGrbit](./retrievekeygrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="ab2a7-117">取得索引鍵選項。</span><span class="sxs-lookup"><span data-stu-id="ab2a7-117">Retrieve key options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="ab2a7-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="ab2a7-118">Return value</span></span>

<span data-ttu-id="ab2a7-119">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="ab2a7-119">Type: \[\]</span></span>  
<span data-ttu-id="ab2a7-120">取出的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="ab2a7-120">The retrieved key.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ab2a7-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ab2a7-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ab2a7-122">參考</span><span class="sxs-lookup"><span data-stu-id="ab2a7-122">Reference</span></span>

[<span data-ttu-id="ab2a7-123">Api 類別</span><span class="sxs-lookup"><span data-stu-id="ab2a7-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="ab2a7-124">Api 成員</span><span class="sxs-lookup"><span data-stu-id="ab2a7-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="ab2a7-125">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="ab2a7-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
