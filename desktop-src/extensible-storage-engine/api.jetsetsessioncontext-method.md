---
description: 深入瞭解： JetSetSessionCoNtext 方法
title: JetSetSessionCoNtext 方法
TOCTitle: 'JetSetSessionContext method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetSessionContext(Microsoft.Isam.Esent.Interop.JET_SESID,System.IntPtr)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetsessioncontext(v=EXCHG.10)
ms:contentKeyID: 55100820
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetSessionContext
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetSessionContext
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5d73a382a2b8e176e2d1ce6fa13585a6b5fa103e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978326"
---
# <a name="apijetsetsessioncontext-method"></a><span data-ttu-id="5c11d-103">JetSetSessionCoNtext 方法</span><span class="sxs-lookup"><span data-stu-id="5c11d-103">Api.JetSetSessionContext method</span></span>

<span data-ttu-id="5c11d-104">使用指定的內容控制碼，將會話與目前的執行緒產生關聯。</span><span class="sxs-lookup"><span data-stu-id="5c11d-104">Associates a session with the current thread using the given context handle.</span></span> <span data-ttu-id="5c11d-105">此關聯會覆寫指定會話的交易必須完全在相同執行緒上執行的預設引擎需求。</span><span class="sxs-lookup"><span data-stu-id="5c11d-105">This association overrides the default engine requirement that a transaction for a given session must occur entirely on the same thread.</span></span> <span data-ttu-id="5c11d-106">使用 [JetResetSessionCoNtext (JET_SESID) ](./api.jetresetsessioncontext-method.md) 來移除關聯。</span><span class="sxs-lookup"><span data-stu-id="5c11d-106">Use [JetResetSessionContext(JET_SESID)](./api.jetresetsessioncontext-method.md) to remove the association.</span></span>

<span data-ttu-id="5c11d-107">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5c11d-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5c11d-108">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="5c11d-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5c11d-109">語法</span><span class="sxs-lookup"><span data-stu-id="5c11d-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetSessionContext ( _
    sesid As JET_SESID, _
    context As IntPtr _
)
'Usage
Dim sesid As JET_SESID
Dim context As IntPtrApi.JetSetSessionContext(sesid, _
    context)
```

``` csharp
public static void JetSetSessionContext(
    JET_SESID sesid,
    IntPtr context
)
```

#### <a name="parameters"></a><span data-ttu-id="5c11d-110">參數</span><span class="sxs-lookup"><span data-stu-id="5c11d-110">Parameters</span></span>

  - <span data-ttu-id="5c11d-111">sesid</span><span class="sxs-lookup"><span data-stu-id="5c11d-111">sesid</span></span>  
    <span data-ttu-id="5c11d-112">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5c11d-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="5c11d-113">要在其上設定內容的會話。</span><span class="sxs-lookup"><span data-stu-id="5c11d-113">The session to set the context on.</span></span>

<!-- end list -->

  - <span data-ttu-id="5c11d-114">內容</span><span class="sxs-lookup"><span data-stu-id="5c11d-114">context</span></span>  
    <span data-ttu-id="5c11d-115">類型： [system.object](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="5c11d-115">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="5c11d-116">要設定的內容。</span><span class="sxs-lookup"><span data-stu-id="5c11d-116">The context to set.</span></span>

## <a name="see-also"></a><span data-ttu-id="5c11d-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5c11d-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5c11d-118">參考</span><span class="sxs-lookup"><span data-stu-id="5c11d-118">Reference</span></span>

[<span data-ttu-id="5c11d-119">Api 類別</span><span class="sxs-lookup"><span data-stu-id="5c11d-119">Api class</span></span>](./api-class.md)

[<span data-ttu-id="5c11d-120">Api 成員</span><span class="sxs-lookup"><span data-stu-id="5c11d-120">Api members</span></span>](./api-members.md)

[<span data-ttu-id="5c11d-121">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="5c11d-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
