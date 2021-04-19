---
description: 深入瞭解： JetTerm2 方法
title: JetTerm2 方法
TOCTitle: 'JetTerm2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetTerm2(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.TermGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetterm2(v=EXCHG.10)
ms:contentKeyID: 55100829
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetTerm2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetTerm2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2e8a4aa8c96f9a4d0242657fe7126abf1388a7f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979409"
---
# <a name="apijetterm2-method"></a><span data-ttu-id="f9daf-103">JetTerm2 方法</span><span class="sxs-lookup"><span data-stu-id="f9daf-103">Api.JetTerm2 method</span></span>

<span data-ttu-id="f9daf-104">終止以 [JetInit (JET_INSTANCE) ](./api.jetinit-method.md) 或 [JetCreateInstance (JET_INSTANCE、String) ](./api.jetcreateinstance-method.md)建立的實例。</span><span class="sxs-lookup"><span data-stu-id="f9daf-104">Terminate an instance that was created with [JetInit(JET_INSTANCE)](./api.jetinit-method.md) or [JetCreateInstance(JET_INSTANCE, String)](./api.jetcreateinstance-method.md).</span></span>

<span data-ttu-id="f9daf-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f9daf-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f9daf-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="f9daf-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f9daf-107">語法</span><span class="sxs-lookup"><span data-stu-id="f9daf-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetTerm2 ( _
    instance As JET_INSTANCE, _
    grbit As TermGrbit _
)
'Usage
Dim instance As JET_INSTANCE
Dim grbit As TermGrbitApi.JetTerm2(instance, grbit)
```

``` csharp
public static void JetTerm2(
    JET_INSTANCE instance,
    TermGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="f9daf-108">參數</span><span class="sxs-lookup"><span data-stu-id="f9daf-108">Parameters</span></span>

  - <span data-ttu-id="f9daf-109">instance</span><span class="sxs-lookup"><span data-stu-id="f9daf-109">instance</span></span>  
    <span data-ttu-id="f9daf-110">類型： [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f9daf-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="f9daf-111">要終止的實例。</span><span class="sxs-lookup"><span data-stu-id="f9daf-111">The instance to terminate.</span></span>

<!-- end list -->

  - <span data-ttu-id="f9daf-112">grbit</span><span class="sxs-lookup"><span data-stu-id="f9daf-112">grbit</span></span>  
    <span data-ttu-id="f9daf-113">型別： [TermGrbit](./termgrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="f9daf-113">Type: [Microsoft.Isam.Esent.Interop.TermGrbit](./termgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="f9daf-114">終止選項。</span><span class="sxs-lookup"><span data-stu-id="f9daf-114">Termination options.</span></span>

## <a name="see-also"></a><span data-ttu-id="f9daf-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f9daf-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f9daf-116">參考</span><span class="sxs-lookup"><span data-stu-id="f9daf-116">Reference</span></span>

[<span data-ttu-id="f9daf-117">Api 類別</span><span class="sxs-lookup"><span data-stu-id="f9daf-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="f9daf-118">Api 成員</span><span class="sxs-lookup"><span data-stu-id="f9daf-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="f9daf-119">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="f9daf-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
