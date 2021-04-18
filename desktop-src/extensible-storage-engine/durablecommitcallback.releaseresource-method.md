---
description: 深入瞭解： DurableCommitCallback. ReleaseResource 方法
title: 'DurableCommitCallback. ReleaseResource 方法 (Windows8 的) '
TOCTitle: 'ReleaseResource method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback.ReleaseResource
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.durablecommitcallback.releaseresource(v=EXCHG.10)
ms:contentKeyID: 55104293
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback.ReleaseResource
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback.ReleaseResource
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 634dd081513e576c7aabaac17cc5f9d207a8769f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195201"
---
# <a name="durablecommitcallbackreleaseresource-method"></a><span data-ttu-id="cba3c-103">DurableCommitCallback. ReleaseResource 方法</span><span class="sxs-lookup"><span data-stu-id="cba3c-103">DurableCommitCallback.ReleaseResource method</span></span>

<span data-ttu-id="cba3c-104">釋出持久的認可會話。</span><span class="sxs-lookup"><span data-stu-id="cba3c-104">Frees the durable commit session.</span></span>

<span data-ttu-id="cba3c-105">**命名空間：**  [Microsoft Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="cba3c-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="cba3c-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="cba3c-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="cba3c-107">語法</span><span class="sxs-lookup"><span data-stu-id="cba3c-107">Syntax</span></span>

``` vb
'Declaration
Protected Overrides Sub ReleaseResource
'Usage

Me.ReleaseResource()
```

``` csharp
protected override void ReleaseResource()
```

## <a name="remarks"></a><span data-ttu-id="cba3c-108">備註</span><span class="sxs-lookup"><span data-stu-id="cba3c-108">Remarks</span></span>

<span data-ttu-id="cba3c-109">請勿嘗試將 instance 參數設定為 null，因為在 JetTerm 之後會處置回呼，而且無法在 JetTerm 之後設定回呼。</span><span class="sxs-lookup"><span data-stu-id="cba3c-109">Do not try to set the instance parameter to null, because the callback is disposed after JetTerm and the callback cannot be set after JetTerm.</span></span>

## <a name="see-also"></a><span data-ttu-id="cba3c-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cba3c-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="cba3c-111">參考</span><span class="sxs-lookup"><span data-stu-id="cba3c-111">Reference</span></span>

[<span data-ttu-id="cba3c-112">DurableCommitCallback 類別</span><span class="sxs-lookup"><span data-stu-id="cba3c-112">DurableCommitCallback class</span></span>](./durablecommitcallback-class.md)

[<span data-ttu-id="cba3c-113">DurableCommitCallback 成員</span><span class="sxs-lookup"><span data-stu-id="cba3c-113">DurableCommitCallback members</span></span>](./durablecommitcallback-members.md)

[<span data-ttu-id="cba3c-114">Windows8 命名空間。</span><span class="sxs-lookup"><span data-stu-id="cba3c-114">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
