---
description: 深入瞭解： InstanceParameters. MaxTransactionSize 屬性
title: InstanceParameters. MaxTransactionSize 屬性
TOCTitle: 'MaxTransactionSize property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.MaxTransactionSize
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.maxtransactionsize(v=EXCHG.10)
ms:contentKeyID: 55103317
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxTransactionSize
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxTransactionSize
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_MaxTransactionSize
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_MaxTransactionSize
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a370d05364142a6fca7d84265dc8d29c7ab5c808
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849768"
---
# <a name="instanceparametersmaxtransactionsize-property"></a><span data-ttu-id="7f55d-103">InstanceParameters. MaxTransactionSize 屬性</span><span class="sxs-lookup"><span data-stu-id="7f55d-103">InstanceParameters.MaxTransactionSize property</span></span>

<span data-ttu-id="7f55d-104">取得或設定在 [VersionStoreOutOfMemory](./jet-err-enumeration.md) (預設值 = 100) 之前，可供最舊交易使用的版本存放區百分比。</span><span class="sxs-lookup"><span data-stu-id="7f55d-104">Gets or sets the percentage of version store that can be used by oldest transaction before [VersionStoreOutOfMemory](./jet-err-enumeration.md) (default = 100).</span></span>

<span data-ttu-id="7f55d-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7f55d-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7f55d-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="7f55d-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7f55d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f55d-107">Syntax</span></span>

``` vb
'Declaration
Public Property MaxTransactionSize As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.MaxTransactionSize

instance.MaxTransactionSize = value
```

``` csharp
public int MaxTransactionSize { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="7f55d-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="7f55d-108">Property value</span></span>

<span data-ttu-id="7f55d-109">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="7f55d-109">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="7f55d-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7f55d-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7f55d-111">參考</span><span class="sxs-lookup"><span data-stu-id="7f55d-111">Reference</span></span>

[<span data-ttu-id="7f55d-112">InstanceParameters 類別</span><span class="sxs-lookup"><span data-stu-id="7f55d-112">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="7f55d-113">InstanceParameters 成員</span><span class="sxs-lookup"><span data-stu-id="7f55d-113">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="7f55d-114">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="7f55d-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
