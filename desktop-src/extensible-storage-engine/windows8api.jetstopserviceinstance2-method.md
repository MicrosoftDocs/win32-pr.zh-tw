---
description: 深入瞭解： Windows8Api. JetStopServiceInstance2 方法
title: 'Windows8Api. JetStopServiceInstance2 方法 (Windows8 的) '
TOCTitle: 'JetStopServiceInstance2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetStopServiceInstance2(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetstopserviceinstance2(v=EXCHG.10)
ms:contentKeyID: 55104460
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetStopServiceInstance2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetStopServiceInstance2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0821a00016eb9cd2c511ee37889e0ddaa0b76edb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026369"
---
# <a name="windows8apijetstopserviceinstance2-method"></a><span data-ttu-id="fc74d-103">Windows8Api. JetStopServiceInstance2 方法</span><span class="sxs-lookup"><span data-stu-id="fc74d-103">Windows8Api.JetStopServiceInstance2 method</span></span>

<span data-ttu-id="fc74d-104">準備實例以進行終止。</span><span class="sxs-lookup"><span data-stu-id="fc74d-104">Prepares an instance for termination.</span></span> <span data-ttu-id="fc74d-105">也可以用來繼續先前的靜止。</span><span class="sxs-lookup"><span data-stu-id="fc74d-105">Can also be used to resume a previous quiescing.</span></span>

<span data-ttu-id="fc74d-106">**命名空間：**  [Microsoft Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fc74d-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="fc74d-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="fc74d-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fc74d-108">語法</span><span class="sxs-lookup"><span data-stu-id="fc74d-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetStopServiceInstance2 ( _
    instance As JET_INSTANCE, _
    grbit As StopServiceGrbit _
)
'Usage
Dim instance As JET_INSTANCE
Dim grbit As StopServiceGrbitWindows8Api.JetStopServiceInstance2(instance, _
    grbit)
```

``` csharp
public static void JetStopServiceInstance2(
    JET_INSTANCE instance,
    StopServiceGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="fc74d-109">參數</span><span class="sxs-lookup"><span data-stu-id="fc74d-109">Parameters</span></span>

  - <span data-ttu-id="fc74d-110">instance</span><span class="sxs-lookup"><span data-stu-id="fc74d-110">instance</span></span>  
    <span data-ttu-id="fc74d-111">類型： [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="fc74d-111">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="fc74d-112"> (正在執行) 實例。</span><span class="sxs-lookup"><span data-stu-id="fc74d-112">The (running) instance to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="fc74d-113">grbit</span><span class="sxs-lookup"><span data-stu-id="fc74d-113">grbit</span></span>  
    <span data-ttu-id="fc74d-114">型別： [Windows8. StopServiceGrbit](./stopservicegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="fc74d-114">Type: [Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit](./stopservicegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="fc74d-115">停止或繼續實例的選項。</span><span class="sxs-lookup"><span data-stu-id="fc74d-115">The options to stop or resume the instance.</span></span>

## <a name="see-also"></a><span data-ttu-id="fc74d-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fc74d-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fc74d-117">參考</span><span class="sxs-lookup"><span data-stu-id="fc74d-117">Reference</span></span>

[<span data-ttu-id="fc74d-118">Windows8Api 類別</span><span class="sxs-lookup"><span data-stu-id="fc74d-118">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="fc74d-119">Windows8Api 成員</span><span class="sxs-lookup"><span data-stu-id="fc74d-119">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="fc74d-120">Windows8 命名空間。</span><span class="sxs-lookup"><span data-stu-id="fc74d-120">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
