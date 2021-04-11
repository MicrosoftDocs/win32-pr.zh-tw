---
description: 深入瞭解： ColumnStream 的函式
title: ColumnStream 函式
TOCTitle: 'ColumnStream constructor '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnStream.#ctor(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream.columnstream(v=EXCHG.10)
ms:contentKeyID: 55100938
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream.ColumnStream
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 498fed2daf2cad5903d9597689a80eadca7bd569
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943652"
---
# <a name="columnstream-constructor"></a><span data-ttu-id="e7572-103">ColumnStream 函式</span><span class="sxs-lookup"><span data-stu-id="e7572-103">ColumnStream constructor</span></span>

<span data-ttu-id="e7572-104">初始化 ColumnStream 類別的新實例。</span><span class="sxs-lookup"><span data-stu-id="e7572-104">Initializes a new instance of the ColumnStream class.</span></span>

<span data-ttu-id="e7572-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e7572-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e7572-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="e7572-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e7572-107">語法</span><span class="sxs-lookup"><span data-stu-id="e7572-107">Syntax</span></span>

``` vb
'Declaration
Public Sub New ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID

Dim instance As New ColumnStream(sesid, tableid, _
    columnid)
```

``` csharp
public ColumnStream(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="e7572-108">參數</span><span class="sxs-lookup"><span data-stu-id="e7572-108">Parameters</span></span>

  - <span data-ttu-id="e7572-109">sesid</span><span class="sxs-lookup"><span data-stu-id="e7572-109">sesid</span></span>  
    <span data-ttu-id="e7572-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e7572-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="e7572-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="e7572-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="e7572-112">tableid</span><span class="sxs-lookup"><span data-stu-id="e7572-112">tableid</span></span>  
    <span data-ttu-id="e7572-113">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e7572-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="e7572-114">要使用的資料指標。</span><span class="sxs-lookup"><span data-stu-id="e7572-114">The cursor to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="e7572-115">columnid</span><span class="sxs-lookup"><span data-stu-id="e7572-115">columnid</span></span>  
    <span data-ttu-id="e7572-116">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e7572-116">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="e7572-117">要設定/從中取出資料之資料行的 columnid。</span><span class="sxs-lookup"><span data-stu-id="e7572-117">The columnid of the column to set/retrieve data from.</span></span>

## <a name="see-also"></a><span data-ttu-id="e7572-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e7572-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e7572-119">參考</span><span class="sxs-lookup"><span data-stu-id="e7572-119">Reference</span></span>

[<span data-ttu-id="e7572-120">ColumnStream 類別</span><span class="sxs-lookup"><span data-stu-id="e7572-120">ColumnStream class</span></span>](./columnstream-class.md)

[<span data-ttu-id="e7572-121">ColumnStream 成員</span><span class="sxs-lookup"><span data-stu-id="e7572-121">ColumnStream members</span></span>](./columnstream-members.md)

[<span data-ttu-id="e7572-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="e7572-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
