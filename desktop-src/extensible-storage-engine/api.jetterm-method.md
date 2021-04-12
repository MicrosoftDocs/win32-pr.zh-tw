---
description: 深入瞭解： JetTerm 方法
title: JetTerm 方法
TOCTitle: 'JetTerm method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetTerm(Microsoft.Isam.Esent.Interop.JET_INSTANCE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetterm(v=EXCHG.10)
ms:contentKeyID: 55100813
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetTerm
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetTerm
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1c8e028ecdc6456521b7aaa671cb4f5199e8751e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195208"
---
# <a name="apijetterm-method"></a><span data-ttu-id="b8e6e-103">JetTerm 方法</span><span class="sxs-lookup"><span data-stu-id="b8e6e-103">Api.JetTerm method</span></span>

<span data-ttu-id="b8e6e-104">終止以 [JetInit (JET_INSTANCE) ](./api.jetinit-method.md) 或 [JetCreateInstance (JET_INSTANCE、String) ](./api.jetcreateinstance-method.md)建立的實例。</span><span class="sxs-lookup"><span data-stu-id="b8e6e-104">Terminate an instance that was created with [JetInit(JET_INSTANCE)](./api.jetinit-method.md) or [JetCreateInstance(JET_INSTANCE, String)](./api.jetcreateinstance-method.md).</span></span>

<span data-ttu-id="b8e6e-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b8e6e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b8e6e-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="b8e6e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b8e6e-107">語法</span><span class="sxs-lookup"><span data-stu-id="b8e6e-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetTerm ( _
    instance As JET_INSTANCE _
)
'Usage
Dim instance As JET_INSTANCEApi.JetTerm(instance)
```

``` csharp
public static void JetTerm(
    JET_INSTANCE instance
)
```

#### <a name="parameters"></a><span data-ttu-id="b8e6e-108">參數</span><span class="sxs-lookup"><span data-stu-id="b8e6e-108">Parameters</span></span>

  - <span data-ttu-id="b8e6e-109">instance</span><span class="sxs-lookup"><span data-stu-id="b8e6e-109">instance</span></span>  
    <span data-ttu-id="b8e6e-110">類型： [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b8e6e-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="b8e6e-111">要終止的實例。</span><span class="sxs-lookup"><span data-stu-id="b8e6e-111">The instance to terminate.</span></span>

## <a name="see-also"></a><span data-ttu-id="b8e6e-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b8e6e-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b8e6e-113">參考</span><span class="sxs-lookup"><span data-stu-id="b8e6e-113">Reference</span></span>

[<span data-ttu-id="b8e6e-114">Api 類別</span><span class="sxs-lookup"><span data-stu-id="b8e6e-114">Api class</span></span>](./api-class.md)

[<span data-ttu-id="b8e6e-115">Api 成員</span><span class="sxs-lookup"><span data-stu-id="b8e6e-115">Api members</span></span>](./api-members.md)

[<span data-ttu-id="b8e6e-116">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="b8e6e-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
