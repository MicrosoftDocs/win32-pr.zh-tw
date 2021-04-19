---
description: 深入瞭解： Update 函數
title: 更新函式
TOCTitle: 'Update constructor '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Update.#ctor(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_prep)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.update.update(v=EXCHG.10)
ms:contentKeyID: 55104189
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Update.Update
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Update..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 841403523e0cae7c71fb8fa0861c1d400a26a726
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975252"
---
# <a name="update-constructor"></a><span data-ttu-id="af17c-103">更新函式</span><span class="sxs-lookup"><span data-stu-id="af17c-103">Update constructor</span></span>

<span data-ttu-id="af17c-104">初始化 Update 類別的新實例。</span><span class="sxs-lookup"><span data-stu-id="af17c-104">Initializes a new instance of the Update class.</span></span> <span data-ttu-id="af17c-105">這會自動開始更新。</span><span class="sxs-lookup"><span data-stu-id="af17c-105">This automatically begins an update.</span></span> <span data-ttu-id="af17c-106">如果未明確儲存，將會取消更新。</span><span class="sxs-lookup"><span data-stu-id="af17c-106">The update will be cancelled if not explicitly saved.</span></span>

<span data-ttu-id="af17c-107">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="af17c-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="af17c-108">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="af17c-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="af17c-109">語法</span><span class="sxs-lookup"><span data-stu-id="af17c-109">Syntax</span></span>

``` vb
'Declaration
Public Sub New ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    prep As JET_prep _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim prep As JET_prep

Dim instance As New Update(sesid, tableid, _
    prep)
```

``` csharp
public Update(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_prep prep
)
```

#### <a name="parameters"></a><span data-ttu-id="af17c-110">參數</span><span class="sxs-lookup"><span data-stu-id="af17c-110">Parameters</span></span>

  - <span data-ttu-id="af17c-111">sesid</span><span class="sxs-lookup"><span data-stu-id="af17c-111">sesid</span></span>  
    <span data-ttu-id="af17c-112">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="af17c-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="af17c-113">要啟動交易的會話。</span><span class="sxs-lookup"><span data-stu-id="af17c-113">The session to start the transaction for.</span></span>

<!-- end list -->

  - <span data-ttu-id="af17c-114">tableid</span><span class="sxs-lookup"><span data-stu-id="af17c-114">tableid</span></span>  
    <span data-ttu-id="af17c-115">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="af17c-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="af17c-116">準備更新的 tableid。</span><span class="sxs-lookup"><span data-stu-id="af17c-116">The tableid to prepare the update for.</span></span>

<!-- end list -->

  - <span data-ttu-id="af17c-117">準備</span><span class="sxs-lookup"><span data-stu-id="af17c-117">prep</span></span>  
    <span data-ttu-id="af17c-118">類型： [Microsoft.Isam.Esent.Interop.JET_prep](./jet-prep-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="af17c-118">Type: [Microsoft.Isam.Esent.Interop.JET_prep](./jet-prep-enumeration.md)</span></span>  
    
    <span data-ttu-id="af17c-119">更新的類型。</span><span class="sxs-lookup"><span data-stu-id="af17c-119">The type of update.</span></span>

## <a name="see-also"></a><span data-ttu-id="af17c-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="af17c-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="af17c-121">參考</span><span class="sxs-lookup"><span data-stu-id="af17c-121">Reference</span></span>

[<span data-ttu-id="af17c-122">Update 類別</span><span class="sxs-lookup"><span data-stu-id="af17c-122">Update class</span></span>](./update-class.md)

[<span data-ttu-id="af17c-123">更新成員</span><span class="sxs-lookup"><span data-stu-id="af17c-123">Update members</span></span>](./update-members.md)

[<span data-ttu-id="af17c-124">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="af17c-124">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
