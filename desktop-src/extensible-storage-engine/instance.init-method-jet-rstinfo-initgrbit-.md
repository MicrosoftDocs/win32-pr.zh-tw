---
description: '深入瞭解： Instance.Init 方法 (JET_RSTINFO、InitGrbit) '
title: 'Instance.Init 方法 (JET_RSTINFO、InitGrbit) '
TOCTitle: Init method (JET_RSTINFO, InitGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.Init(Microsoft.Isam.Esent.Interop.JET_RSTINFO,Microsoft.Isam.Esent.Interop.InitGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.init(v=EXCHG.10)
ms:contentKeyID: 55103274
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Instance.Init
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1945b0119053a2759b57b8781b86cf682b3a364c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979016"
---
# <a name="instanceinit-method-jet_rstinfo-initgrbit"></a><span data-ttu-id="92cc3-103">Instance.Init 方法 (JET_RSTINFO、InitGrbit) </span><span class="sxs-lookup"><span data-stu-id="92cc3-103">Instance.Init method (JET_RSTINFO, InitGrbit)</span></span>

<span data-ttu-id="92cc3-104">初始化 JET_INSTANCE。</span><span class="sxs-lookup"><span data-stu-id="92cc3-104">Initialize the JET_INSTANCE.</span></span> <span data-ttu-id="92cc3-105">此 API 至少需要 Vista 版本的 ESENT。</span><span class="sxs-lookup"><span data-stu-id="92cc3-105">This API requires at least the Vista version of ESENT.</span></span>

<span data-ttu-id="92cc3-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="92cc3-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="92cc3-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="92cc3-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="92cc3-108">語法</span><span class="sxs-lookup"><span data-stu-id="92cc3-108">Syntax</span></span>

``` vb
'Declaration
<SecurityPermissionAttribute(SecurityAction.LinkDemand)> _
Public Sub Init ( _
    recoveryOptions As JET_RSTINFO, _
    grbit As InitGrbit _
)
'Usage
Dim instance As Instance
Dim recoveryOptions As JET_RSTINFO
Dim grbit As InitGrbit

instance.Init(recoveryOptions, grbit)
```

``` csharp
[SecurityPermissionAttribute(SecurityAction.LinkDemand)]
public void Init(
    JET_RSTINFO recoveryOptions,
    InitGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="92cc3-109">參數</span><span class="sxs-lookup"><span data-stu-id="92cc3-109">Parameters</span></span>

  - <span data-ttu-id="92cc3-110">recoveryOptions</span><span class="sxs-lookup"><span data-stu-id="92cc3-110">recoveryOptions</span></span>  
    <span data-ttu-id="92cc3-111">類型： [Microsoft.Isam.Esent.Interop.JET_RSTINFO](./jet-rstinfo-class.md)</span><span class="sxs-lookup"><span data-stu-id="92cc3-111">Type: [Microsoft.Isam.Esent.Interop.JET_RSTINFO](./jet-rstinfo-class.md)</span></span>  
    
    <span data-ttu-id="92cc3-112">在復原期間重新對應資料庫的其他修復參數、放置停止復原的位置，或復原狀態。</span><span class="sxs-lookup"><span data-stu-id="92cc3-112">Additional recovery parameters for remapping databases during recovery, position where to stop recovery at, or recovery status.</span></span>

<!-- end list -->

  - <span data-ttu-id="92cc3-113">grbit</span><span class="sxs-lookup"><span data-stu-id="92cc3-113">grbit</span></span>  
    <span data-ttu-id="92cc3-114">類型： [Microsoft.Isam.Esent.Interop.InitGrbit](./initgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="92cc3-114">Type: [Microsoft.Isam.Esent.Interop.InitGrbit](./initgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="92cc3-115">初始化選項。</span><span class="sxs-lookup"><span data-stu-id="92cc3-115">Initialization options.</span></span>

## <a name="see-also"></a><span data-ttu-id="92cc3-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="92cc3-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="92cc3-117">參考</span><span class="sxs-lookup"><span data-stu-id="92cc3-117">Reference</span></span>

[<span data-ttu-id="92cc3-118">Instance 類別</span><span class="sxs-lookup"><span data-stu-id="92cc3-118">Instance class</span></span>](./instance-class.md)

[<span data-ttu-id="92cc3-119">實例成員</span><span class="sxs-lookup"><span data-stu-id="92cc3-119">Instance members</span></span>](./instance-members.md)

[<span data-ttu-id="92cc3-120">Init 多載</span><span class="sxs-lookup"><span data-stu-id="92cc3-120">Init overload</span></span>](./instance.init-method2.md)

[<span data-ttu-id="92cc3-121">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="92cc3-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
