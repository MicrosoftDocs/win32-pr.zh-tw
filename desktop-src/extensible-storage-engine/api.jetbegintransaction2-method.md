---
description: 深入瞭解： JetBeginTransaction2 方法
title: JetBeginTransaction2 方法
TOCTitle: 'JetBeginTransaction2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetBeginTransaction2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.BeginTransactionGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetbegintransaction2(v=EXCHG.10)
ms:contentKeyID: 55107226
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetBeginTransaction2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetBeginTransaction2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8d41652c4688bd736ac5f5164ca9b487a24edf8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510854"
---
# <a name="apijetbegintransaction2-method"></a><span data-ttu-id="1242b-103">JetBeginTransaction2 方法</span><span class="sxs-lookup"><span data-stu-id="1242b-103">Api.JetBeginTransaction2 method</span></span>

<span data-ttu-id="1242b-104">導致會話進入交易，或在現有的交易中建立新的儲存點。</span><span class="sxs-lookup"><span data-stu-id="1242b-104">Causes a session to enter a transaction or create a new save point in an existing transaction.</span></span>

<span data-ttu-id="1242b-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1242b-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1242b-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="1242b-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1242b-107">語法</span><span class="sxs-lookup"><span data-stu-id="1242b-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetBeginTransaction2 ( _
    sesid As JET_SESID, _
    grbit As BeginTransactionGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim grbit As BeginTransactionGrbitApi.JetBeginTransaction2(sesid, _
    grbit)
```

``` csharp
public static void JetBeginTransaction2(
    JET_SESID sesid,
    BeginTransactionGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="1242b-108">參數</span><span class="sxs-lookup"><span data-stu-id="1242b-108">Parameters</span></span>

  - <span data-ttu-id="1242b-109">sesid</span><span class="sxs-lookup"><span data-stu-id="1242b-109">sesid</span></span>  
    <span data-ttu-id="1242b-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1242b-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="1242b-111">開始交易的會話。</span><span class="sxs-lookup"><span data-stu-id="1242b-111">The session to begin the transaction for.</span></span>

<!-- end list -->

  - <span data-ttu-id="1242b-112">grbit</span><span class="sxs-lookup"><span data-stu-id="1242b-112">grbit</span></span>  
    <span data-ttu-id="1242b-113">型別： [BeginTransactionGrbit](./begintransactiongrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="1242b-113">Type: [Microsoft.Isam.Esent.Interop.BeginTransactionGrbit](./begintransactiongrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="1242b-114">交易選項。</span><span class="sxs-lookup"><span data-stu-id="1242b-114">Transaction options.</span></span>

## <a name="see-also"></a><span data-ttu-id="1242b-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1242b-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1242b-116">參考</span><span class="sxs-lookup"><span data-stu-id="1242b-116">Reference</span></span>

[<span data-ttu-id="1242b-117">Api 類別</span><span class="sxs-lookup"><span data-stu-id="1242b-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="1242b-118">Api 成員</span><span class="sxs-lookup"><span data-stu-id="1242b-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="1242b-119">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="1242b-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
