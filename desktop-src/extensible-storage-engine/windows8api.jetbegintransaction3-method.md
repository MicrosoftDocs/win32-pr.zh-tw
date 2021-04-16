---
description: 深入瞭解： Windows8Api. JetBeginTransaction3 方法
title: 'Windows8Api. JetBeginTransaction3 方法 (Windows8 的) '
TOCTitle: 'JetBeginTransaction3 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetBeginTransaction3(Microsoft.Isam.Esent.Interop.JET_SESID,System.Int64,Microsoft.Isam.Esent.Interop.BeginTransactionGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetbegintransaction3(v=EXCHG.10)
ms:contentKeyID: 55107825
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetBeginTransaction3
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetBeginTransaction3
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7605cdb44c66d929e6663caaad9e40d3c98737b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512473"
---
# <a name="windows8apijetbegintransaction3-method"></a><span data-ttu-id="44cbd-103">Windows8Api. JetBeginTransaction3 方法</span><span class="sxs-lookup"><span data-stu-id="44cbd-103">Windows8Api.JetBeginTransaction3 method</span></span>

<span data-ttu-id="44cbd-104">導致會話進入交易，或在現有的交易中建立新的儲存點。</span><span class="sxs-lookup"><span data-stu-id="44cbd-104">Causes a session to enter a transaction or create a new save point in an existing transaction.</span></span>

<span data-ttu-id="44cbd-105">**命名空間：**  [Microsoft Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="44cbd-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="44cbd-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="44cbd-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="44cbd-107">語法</span><span class="sxs-lookup"><span data-stu-id="44cbd-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetBeginTransaction3 ( _
    sesid As JET_SESID, _
    userTransactionId As Long, _
    grbit As BeginTransactionGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim userTransactionId As Long
Dim grbit As BeginTransactionGrbitWindows8Api.JetBeginTransaction3(sesid, _
    userTransactionId, grbit)
```

``` csharp
public static void JetBeginTransaction3(
    JET_SESID sesid,
    long userTransactionId,
    BeginTransactionGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="44cbd-108">參數</span><span class="sxs-lookup"><span data-stu-id="44cbd-108">Parameters</span></span>

  - <span data-ttu-id="44cbd-109">sesid</span><span class="sxs-lookup"><span data-stu-id="44cbd-109">sesid</span></span>  
    <span data-ttu-id="44cbd-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="44cbd-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="44cbd-111">開始交易的會話。</span><span class="sxs-lookup"><span data-stu-id="44cbd-111">The session to begin the transaction for.</span></span>

<!-- end list -->

  - <span data-ttu-id="44cbd-112">userTransactionId</span><span class="sxs-lookup"><span data-stu-id="44cbd-112">userTransactionId</span></span>  
    <span data-ttu-id="44cbd-113">類型： [Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="44cbd-113">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  
    
    <span data-ttu-id="44cbd-114">使用者提供的選擇性識別碼，用來識別交易。</span><span class="sxs-lookup"><span data-stu-id="44cbd-114">An optional identifier supplied by the user for identifying the transaction.</span></span>

<!-- end list -->

  - <span data-ttu-id="44cbd-115">grbit</span><span class="sxs-lookup"><span data-stu-id="44cbd-115">grbit</span></span>  
    <span data-ttu-id="44cbd-116">型別： [BeginTransactionGrbit](./begintransactiongrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="44cbd-116">Type: [Microsoft.Isam.Esent.Interop.BeginTransactionGrbit](./begintransactiongrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="44cbd-117">交易選項。</span><span class="sxs-lookup"><span data-stu-id="44cbd-117">Transaction options.</span></span>

## <a name="remarks"></a><span data-ttu-id="44cbd-118">備註</span><span class="sxs-lookup"><span data-stu-id="44cbd-118">Remarks</span></span>

<span data-ttu-id="44cbd-119">Windows 8 引進。</span><span class="sxs-lookup"><span data-stu-id="44cbd-119">Introduced in Windows 8.</span></span>

## <a name="see-also"></a><span data-ttu-id="44cbd-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="44cbd-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="44cbd-121">參考</span><span class="sxs-lookup"><span data-stu-id="44cbd-121">Reference</span></span>

[<span data-ttu-id="44cbd-122">Windows8Api 類別</span><span class="sxs-lookup"><span data-stu-id="44cbd-122">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="44cbd-123">Windows8Api 成員</span><span class="sxs-lookup"><span data-stu-id="44cbd-123">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="44cbd-124">Windows8 命名空間。</span><span class="sxs-lookup"><span data-stu-id="44cbd-124">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
