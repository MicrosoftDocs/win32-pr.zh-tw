---
description: 深入瞭解： JetPrepareUpdate 方法
title: JetPrepareUpdate 方法
TOCTitle: 'JetPrepareUpdate method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetPrepareUpdate(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_prep)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetprepareupdate(v=EXCHG.10)
ms:contentKeyID: 55100782
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetPrepareUpdate
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetPrepareUpdate
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e8094fef5fcf008dd5f6eb6f2bfd05a0be1bf077
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195021"
---
# <a name="apijetprepareupdate-method"></a><span data-ttu-id="50db6-103">JetPrepareUpdate 方法</span><span class="sxs-lookup"><span data-stu-id="50db6-103">Api.JetPrepareUpdate method</span></span>

<span data-ttu-id="50db6-104">準備資料指標進行更新。</span><span class="sxs-lookup"><span data-stu-id="50db6-104">Prepare a cursor for update.</span></span>

<span data-ttu-id="50db6-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="50db6-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="50db6-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="50db6-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="50db6-107">語法</span><span class="sxs-lookup"><span data-stu-id="50db6-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetPrepareUpdate ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    prep As JET_prep _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim prep As JET_prepApi.JetPrepareUpdate(sesid, tableid, _
    prep)
```

``` csharp
public static void JetPrepareUpdate(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_prep prep
)
```

#### <a name="parameters"></a><span data-ttu-id="50db6-108">參數</span><span class="sxs-lookup"><span data-stu-id="50db6-108">Parameters</span></span>

  - <span data-ttu-id="50db6-109">sesid</span><span class="sxs-lookup"><span data-stu-id="50db6-109">sesid</span></span>  
    <span data-ttu-id="50db6-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="50db6-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="50db6-111">開始更新的會話。</span><span class="sxs-lookup"><span data-stu-id="50db6-111">The session which is starting the update.</span></span>

<!-- end list -->

  - <span data-ttu-id="50db6-112">tableid</span><span class="sxs-lookup"><span data-stu-id="50db6-112">tableid</span></span>  
    <span data-ttu-id="50db6-113">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="50db6-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="50db6-114">要開始更新的資料指標。</span><span class="sxs-lookup"><span data-stu-id="50db6-114">The cursor to start the update for.</span></span>

<!-- end list -->

  - <span data-ttu-id="50db6-115">準備</span><span class="sxs-lookup"><span data-stu-id="50db6-115">prep</span></span>  
    <span data-ttu-id="50db6-116">類型： [Microsoft.Isam.Esent.Interop.JET_prep](./jet-prep-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="50db6-116">Type: [Microsoft.Isam.Esent.Interop.JET_prep](./jet-prep-enumeration.md)</span></span>  
    
    <span data-ttu-id="50db6-117">要準備的更新類型。</span><span class="sxs-lookup"><span data-stu-id="50db6-117">The type of update to prepare.</span></span>

## <a name="see-also"></a><span data-ttu-id="50db6-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="50db6-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="50db6-119">參考</span><span class="sxs-lookup"><span data-stu-id="50db6-119">Reference</span></span>

[<span data-ttu-id="50db6-120">Api 類別</span><span class="sxs-lookup"><span data-stu-id="50db6-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="50db6-121">Api 成員</span><span class="sxs-lookup"><span data-stu-id="50db6-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="50db6-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="50db6-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
