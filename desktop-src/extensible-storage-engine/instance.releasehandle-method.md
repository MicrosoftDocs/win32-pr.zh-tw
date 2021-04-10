---
description: 深入瞭解： ReleaseHandle 方法
title: ReleaseHandle 方法
TOCTitle: 'ReleaseHandle method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.ReleaseHandle
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.releasehandle(v=EXCHG.10)
ms:contentKeyID: 55103298
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Instance.ReleaseHandle
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Instance.ReleaseHandle
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8fcac0fcbffc685fb91bd0c0bf2f97865540cb1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027164"
---
# <a name="instancereleasehandle-method"></a><span data-ttu-id="f3295-103">ReleaseHandle 方法</span><span class="sxs-lookup"><span data-stu-id="f3295-103">Instance.ReleaseHandle method</span></span>

<span data-ttu-id="f3295-104">釋放這個實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="f3295-104">Release the handle for this instance.</span></span>

<span data-ttu-id="f3295-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f3295-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f3295-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="f3295-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f3295-107">語法</span><span class="sxs-lookup"><span data-stu-id="f3295-107">Syntax</span></span>

``` vb
'Declaration
Protected Overrides Function ReleaseHandle As Boolean
'Usage
Dim returnValue As Boolean

returnValue = Me.ReleaseHandle()
```

``` csharp
protected override bool ReleaseHandle()
```

#### <a name="return-value"></a><span data-ttu-id="f3295-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="f3295-108">Return value</span></span>

<span data-ttu-id="f3295-109">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="f3295-109">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="f3295-110">如果可以釋放控制碼，則為 True。</span><span class="sxs-lookup"><span data-stu-id="f3295-110">True if the handle could be released.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f3295-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f3295-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f3295-112">參考</span><span class="sxs-lookup"><span data-stu-id="f3295-112">Reference</span></span>

[<span data-ttu-id="f3295-113">Instance 類別</span><span class="sxs-lookup"><span data-stu-id="f3295-113">Instance class</span></span>](./instance-class.md)

[<span data-ttu-id="f3295-114">實例成員</span><span class="sxs-lookup"><span data-stu-id="f3295-114">Instance members</span></span>](./instance-members.md)

[<span data-ttu-id="f3295-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="f3295-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
