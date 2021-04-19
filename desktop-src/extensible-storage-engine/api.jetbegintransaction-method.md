---
description: 深入瞭解： JetBeginTransaction 方法
title: JetBeginTransaction 方法
TOCTitle: 'JetBeginTransaction method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetBeginTransaction(Microsoft.Isam.Esent.Interop.JET_SESID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetbegintransaction(v=EXCHG.10)
ms:contentKeyID: 55107225
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetBeginTransaction
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetBeginTransaction
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0b8812df332734ee109ea52820346e433e747751
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966692"
---
# <a name="apijetbegintransaction-method"></a><span data-ttu-id="b815b-103">JetBeginTransaction 方法</span><span class="sxs-lookup"><span data-stu-id="b815b-103">Api.JetBeginTransaction method</span></span>

<span data-ttu-id="b815b-104">導致會話進入交易，或在現有的交易中建立新的儲存點。</span><span class="sxs-lookup"><span data-stu-id="b815b-104">Causes a session to enter a transaction or create a new save point in an existing transaction.</span></span>

<span data-ttu-id="b815b-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b815b-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b815b-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="b815b-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b815b-107">語法</span><span class="sxs-lookup"><span data-stu-id="b815b-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetBeginTransaction ( _
    sesid As JET_SESID _
)
'Usage
Dim sesid As JET_SESIDApi.JetBeginTransaction(sesid)
```

``` csharp
public static void JetBeginTransaction(
    JET_SESID sesid
)
```

#### <a name="parameters"></a><span data-ttu-id="b815b-108">參數</span><span class="sxs-lookup"><span data-stu-id="b815b-108">Parameters</span></span>

  - <span data-ttu-id="b815b-109">sesid</span><span class="sxs-lookup"><span data-stu-id="b815b-109">sesid</span></span>  
    <span data-ttu-id="b815b-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b815b-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b815b-111">開始交易的會話。</span><span class="sxs-lookup"><span data-stu-id="b815b-111">The session to begin the transaction for.</span></span>

## <a name="see-also"></a><span data-ttu-id="b815b-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b815b-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b815b-113">參考</span><span class="sxs-lookup"><span data-stu-id="b815b-113">Reference</span></span>

[<span data-ttu-id="b815b-114">Api 類別</span><span class="sxs-lookup"><span data-stu-id="b815b-114">Api class</span></span>](./api-class.md)

[<span data-ttu-id="b815b-115">Api 成員</span><span class="sxs-lookup"><span data-stu-id="b815b-115">Api members</span></span>](./api-members.md)

[<span data-ttu-id="b815b-116">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="b815b-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
