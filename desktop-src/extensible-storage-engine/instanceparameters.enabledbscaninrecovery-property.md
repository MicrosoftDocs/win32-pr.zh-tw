---
description: 深入瞭解： InstanceParameters. EnableDbScanInRecovery 屬性
title: InstanceParameters. EnableDbScanInRecovery 屬性
TOCTitle: 'EnableDbScanInRecovery property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.EnableDbScanInRecovery
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.enabledbscaninrecovery(v=EXCHG.10)
ms:contentKeyID: 55107448
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.EnableDbScanInRecovery
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.EnableDbScanInRecovery
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_EnableDbScanInRecovery
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_EnableDbScanInRecovery
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c6d492b2c101305b3038c300c77467d14dc480e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851447"
---
# <a name="instanceparametersenabledbscaninrecovery-property"></a><span data-ttu-id="32551-103">InstanceParameters. EnableDbScanInRecovery 屬性</span><span class="sxs-lookup"><span data-stu-id="32551-103">InstanceParameters.EnableDbScanInRecovery property</span></span>

<span data-ttu-id="32551-104">取得或設定值，指出是否應在復原期間執行資料庫維護。</span><span class="sxs-lookup"><span data-stu-id="32551-104">Gets or sets a value indicating whether Database Maintenance should run during recovery.</span></span>

<span data-ttu-id="32551-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="32551-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="32551-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="32551-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="32551-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="32551-107">Syntax</span></span>

``` vb
'Declaration
Public Property EnableDbScanInRecovery As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.EnableDbScanInRecovery

instance.EnableDbScanInRecovery = value
```

``` csharp
public int EnableDbScanInRecovery { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="32551-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="32551-108">Property value</span></span>

<span data-ttu-id="32551-109">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="32551-109">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="32551-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="32551-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="32551-111">參考</span><span class="sxs-lookup"><span data-stu-id="32551-111">Reference</span></span>

[<span data-ttu-id="32551-112">InstanceParameters 類別</span><span class="sxs-lookup"><span data-stu-id="32551-112">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="32551-113">InstanceParameters 成員</span><span class="sxs-lookup"><span data-stu-id="32551-113">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="32551-114">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="32551-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
