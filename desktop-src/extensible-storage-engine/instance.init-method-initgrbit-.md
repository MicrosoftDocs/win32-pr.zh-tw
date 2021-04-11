---
description: '深入瞭解： Instance.Init 方法 (InitGrbit) '
title: 'Instance.Init 方法 (InitGrbit) '
TOCTitle: Init method (InitGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.Init(Microsoft.Isam.Esent.Interop.InitGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.init(v=EXCHG.10)
ms:contentKeyID: 55103295
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Instance.Init
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3f87247a77cb89e6e5e9e20048b04f8d9fae36ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193844"
---
# <a name="instanceinit-method-initgrbit"></a><span data-ttu-id="ee94c-103">Instance.Init 方法 (InitGrbit) </span><span class="sxs-lookup"><span data-stu-id="ee94c-103">Instance.Init method (InitGrbit)</span></span>

<span data-ttu-id="ee94c-104">初始化 JET_INSTANCE。</span><span class="sxs-lookup"><span data-stu-id="ee94c-104">Initialize the JET_INSTANCE.</span></span>

<span data-ttu-id="ee94c-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ee94c-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ee94c-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="ee94c-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ee94c-107">語法</span><span class="sxs-lookup"><span data-stu-id="ee94c-107">Syntax</span></span>

``` vb
'Declaration
<SecurityPermissionAttribute(SecurityAction.LinkDemand)> _
Public Sub Init ( _
    grbit As InitGrbit _
)
'Usage
Dim instance As Instance
Dim grbit As InitGrbit

instance.Init(grbit)
```

``` csharp
[SecurityPermissionAttribute(SecurityAction.LinkDemand)]
public void Init(
    InitGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="ee94c-108">參數</span><span class="sxs-lookup"><span data-stu-id="ee94c-108">Parameters</span></span>

  - <span data-ttu-id="ee94c-109">grbit</span><span class="sxs-lookup"><span data-stu-id="ee94c-109">grbit</span></span>  
    <span data-ttu-id="ee94c-110">類型： [Microsoft.Isam.Esent.Interop.InitGrbit](./initgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="ee94c-110">Type: [Microsoft.Isam.Esent.Interop.InitGrbit](./initgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="ee94c-111">初始化選項。</span><span class="sxs-lookup"><span data-stu-id="ee94c-111">Initialization options.</span></span>

## <a name="see-also"></a><span data-ttu-id="ee94c-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ee94c-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ee94c-113">參考</span><span class="sxs-lookup"><span data-stu-id="ee94c-113">Reference</span></span>

[<span data-ttu-id="ee94c-114">Instance 類別</span><span class="sxs-lookup"><span data-stu-id="ee94c-114">Instance class</span></span>](./instance-class.md)

[<span data-ttu-id="ee94c-115">實例成員</span><span class="sxs-lookup"><span data-stu-id="ee94c-115">Instance members</span></span>](./instance-members.md)

[<span data-ttu-id="ee94c-116">Init 多載</span><span class="sxs-lookup"><span data-stu-id="ee94c-116">Init overload</span></span>](./instance.init-method2.md)

[<span data-ttu-id="ee94c-117">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="ee94c-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
