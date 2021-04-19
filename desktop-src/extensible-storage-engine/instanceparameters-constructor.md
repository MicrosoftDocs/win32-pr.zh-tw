---
description: 深入瞭解： InstanceParameters 的函式
title: InstanceParameters 函式
TOCTitle: 'InstanceParameters constructor '
ms:assetid: M:Microsoft.Isam.Esent.Interop.InstanceParameters.#ctor(Microsoft.Isam.Esent.Interop.JET_INSTANCE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.instanceparameters(v=EXCHG.10)
ms:contentKeyID: 55107431
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.InstanceParameters
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: be5b4415cd231078b23a3f3df19e2c96feba4b9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977180"
---
# <a name="instanceparameters-constructor"></a><span data-ttu-id="ae7d9-103">InstanceParameters 函式</span><span class="sxs-lookup"><span data-stu-id="ae7d9-103">InstanceParameters constructor</span></span>

<span data-ttu-id="ae7d9-104">初始化 InstanceParameters 類別的新實例。</span><span class="sxs-lookup"><span data-stu-id="ae7d9-104">Initializes a new instance of the InstanceParameters class.</span></span>

<span data-ttu-id="ae7d9-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ae7d9-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ae7d9-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="ae7d9-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ae7d9-107">語法</span><span class="sxs-lookup"><span data-stu-id="ae7d9-107">Syntax</span></span>

``` vb
'Declaration
Public Sub New ( _
    instance As JET_INSTANCE _
)
'Usage
Dim instance As JET_INSTANCE

Dim instance As New InstanceParameters(instance)
```

``` csharp
public InstanceParameters(
    JET_INSTANCE instance
)
```

#### <a name="parameters"></a><span data-ttu-id="ae7d9-108">參數</span><span class="sxs-lookup"><span data-stu-id="ae7d9-108">Parameters</span></span>

  - <span data-ttu-id="ae7d9-109">instance</span><span class="sxs-lookup"><span data-stu-id="ae7d9-109">instance</span></span>  
    <span data-ttu-id="ae7d9-110">類型： [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ae7d9-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="ae7d9-111">要在其上設定參數的實例。</span><span class="sxs-lookup"><span data-stu-id="ae7d9-111">The instance to set parameters on.</span></span> <span data-ttu-id="ae7d9-112">如果 JET_INSTANCE，則為。Nil，設定會影響未來實例的預設設定。</span><span class="sxs-lookup"><span data-stu-id="ae7d9-112">If this is JET_INSTANCE.Nil, then the settings affect the default settings of future instances.</span></span>

## <a name="see-also"></a><span data-ttu-id="ae7d9-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ae7d9-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ae7d9-114">參考</span><span class="sxs-lookup"><span data-stu-id="ae7d9-114">Reference</span></span>

[<span data-ttu-id="ae7d9-115">InstanceParameters 類別</span><span class="sxs-lookup"><span data-stu-id="ae7d9-115">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="ae7d9-116">InstanceParameters 成員</span><span class="sxs-lookup"><span data-stu-id="ae7d9-116">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="ae7d9-117">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="ae7d9-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
