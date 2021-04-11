---
description: '深入瞭解： EsentResource 方法 (布林值) '
title: EsentResource (布林) 的 Dispose 方法
TOCTitle: Dispose method (Boolean)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentResource.Dispose(System.Boolean)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentresource.dispose(v=EXCHG.10)
ms:contentKeyID: 55102624
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentResource.Dispose
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cf74291bf4c54ffa1d61c28bf7caff1e8c2b231b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195371"
---
# <a name="esentresourcedispose-method-boolean"></a><span data-ttu-id="70eba-103">EsentResource (布林) 的 Dispose 方法</span><span class="sxs-lookup"><span data-stu-id="70eba-103">EsentResource.Dispose method (Boolean)</span></span>

<span data-ttu-id="70eba-104">由 Dispose 和完成項呼叫。</span><span class="sxs-lookup"><span data-stu-id="70eba-104">Called by Dispose and the finalizer.</span></span>

<span data-ttu-id="70eba-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="70eba-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="70eba-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="70eba-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="70eba-107">語法</span><span class="sxs-lookup"><span data-stu-id="70eba-107">Syntax</span></span>

``` vb
'Declaration
Protected Overridable Sub Dispose ( _
    isDisposing As Boolean _
)
'Usage
Dim isDisposing As Boolean

Me.Dispose(isDisposing)
```

``` csharp
protected virtual void Dispose(
    bool isDisposing
)
```

#### <a name="parameters"></a><span data-ttu-id="70eba-108">參數</span><span class="sxs-lookup"><span data-stu-id="70eba-108">Parameters</span></span>

  - <span data-ttu-id="70eba-109">isDisposing</span><span class="sxs-lookup"><span data-stu-id="70eba-109">isDisposing</span></span>  
    <span data-ttu-id="70eba-110">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="70eba-110">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
    
    <span data-ttu-id="70eba-111">如果從 Dispose 呼叫，則為 True。</span><span class="sxs-lookup"><span data-stu-id="70eba-111">True if called from Dispose.</span></span>

## <a name="see-also"></a><span data-ttu-id="70eba-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="70eba-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="70eba-113">參考</span><span class="sxs-lookup"><span data-stu-id="70eba-113">Reference</span></span>

[<span data-ttu-id="70eba-114">EsentResource 類別</span><span class="sxs-lookup"><span data-stu-id="70eba-114">EsentResource class</span></span>](./esentresource-class.md)

[<span data-ttu-id="70eba-115">EsentResource 成員</span><span class="sxs-lookup"><span data-stu-id="70eba-115">EsentResource members</span></span>](./esentresource-members.md)

[<span data-ttu-id="70eba-116">Dispose 多載</span><span class="sxs-lookup"><span data-stu-id="70eba-116">Dispose overload</span></span>](./esentresource.dispose-method.md)

[<span data-ttu-id="70eba-117">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="70eba-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
