---
description: 深入瞭解： ReleaseResource 方法
title: ReleaseResource 方法
TOCTitle: 'ReleaseResource method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Transaction.ReleaseResource
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.transaction.releaseresource(v=EXCHG.10)
ms:contentKeyID: 55104072
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Transaction.ReleaseResource
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Transaction.ReleaseResource
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 78d3dc358b6c7c5dfe297132fd83f08c64693c85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113592"
---
# <a name="transactionreleaseresource-method"></a><span data-ttu-id="d71c3-103">ReleaseResource 方法</span><span class="sxs-lookup"><span data-stu-id="d71c3-103">Transaction.ReleaseResource method</span></span>

<span data-ttu-id="d71c3-104">當交易在作用中處置時呼叫。</span><span class="sxs-lookup"><span data-stu-id="d71c3-104">Called when the transaction is being disposed while active.</span></span> <span data-ttu-id="d71c3-105">這應該會復原交易。</span><span class="sxs-lookup"><span data-stu-id="d71c3-105">This should rollback the transaction.</span></span>

<span data-ttu-id="d71c3-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d71c3-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d71c3-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="d71c3-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d71c3-108">語法</span><span class="sxs-lookup"><span data-stu-id="d71c3-108">Syntax</span></span>

``` vb
'Declaration
Protected Overrides Sub ReleaseResource
'Usage

Me.ReleaseResource()
```

``` csharp
protected override void ReleaseResource()
```

## <a name="see-also"></a><span data-ttu-id="d71c3-109">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d71c3-109">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d71c3-110">參考</span><span class="sxs-lookup"><span data-stu-id="d71c3-110">Reference</span></span>

[<span data-ttu-id="d71c3-111">Transaction 類別</span><span class="sxs-lookup"><span data-stu-id="d71c3-111">Transaction class</span></span>](./transaction-class.md)

[<span data-ttu-id="d71c3-112">交易成員</span><span class="sxs-lookup"><span data-stu-id="d71c3-112">Transaction members</span></span>](./transaction-members.md)

[<span data-ttu-id="d71c3-113">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="d71c3-113">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
