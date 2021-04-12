---
description: 深入瞭解： IsInTransaction 屬性
title: IsInTransaction 屬性
TOCTitle: 'IsInTransaction property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Transaction.IsInTransaction
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.transaction.isintransaction(v=EXCHG.10)
ms:contentKeyID: 55104073
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Transaction.IsInTransaction
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Transaction.IsInTransaction
- Microsoft.Isam.Esent.Interop.Transaction.get_IsInTransaction
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: db9755c952e346f5c08c0bd74caa9bf8b90fe252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513781"
---
# <a name="transactionisintransaction-property"></a><span data-ttu-id="c2ae3-103">IsInTransaction 屬性</span><span class="sxs-lookup"><span data-stu-id="c2ae3-103">Transaction.IsInTransaction property</span></span>

<span data-ttu-id="c2ae3-104">取得值，指出這個物件目前是否在交易中。</span><span class="sxs-lookup"><span data-stu-id="c2ae3-104">Gets a value indicating whether this object is currently in a transaction.</span></span>

<span data-ttu-id="c2ae3-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c2ae3-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c2ae3-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="c2ae3-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c2ae3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2ae3-107">Syntax</span></span>

``` vb
'Declaration
Public ReadOnly Property IsInTransaction As Boolean
    Get
'Usage
Dim instance As Transaction
Dim value As Boolean

value = instance.IsInTransaction
```

``` csharp
public bool IsInTransaction { get; }
```

#### <a name="property-value"></a><span data-ttu-id="c2ae3-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="c2ae3-108">Property value</span></span>

<span data-ttu-id="c2ae3-109">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="c2ae3-109">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  

## <a name="see-also"></a><span data-ttu-id="c2ae3-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c2ae3-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c2ae3-111">參考</span><span class="sxs-lookup"><span data-stu-id="c2ae3-111">Reference</span></span>

[<span data-ttu-id="c2ae3-112">Transaction 類別</span><span class="sxs-lookup"><span data-stu-id="c2ae3-112">Transaction class</span></span>](./transaction-class.md)

[<span data-ttu-id="c2ae3-113">交易成員</span><span class="sxs-lookup"><span data-stu-id="c2ae3-113">Transaction members</span></span>](./transaction-members.md)

[<span data-ttu-id="c2ae3-114">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="c2ae3-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
