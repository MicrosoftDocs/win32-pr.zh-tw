---
description: 深入瞭解： JetResetSessionCoNtext 方法
title: JetResetSessionCoNtext 方法
TOCTitle: 'JetResetSessionContext method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetResetSessionContext(Microsoft.Isam.Esent.Interop.JET_SESID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetresetsessioncontext(v=EXCHG.10)
ms:contentKeyID: 55100785
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetResetSessionContext
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetResetSessionContext
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a34a6c2922c0041f0720b498855b15c4aed23f8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988438"
---
# <a name="apijetresetsessioncontext-method"></a><span data-ttu-id="65207-103">JetResetSessionCoNtext 方法</span><span class="sxs-lookup"><span data-stu-id="65207-103">Api.JetResetSessionContext method</span></span>

<span data-ttu-id="65207-104">解除會話與目前線程之間的之間的解除。</span><span class="sxs-lookup"><span data-stu-id="65207-104">Disassociates a session from the current thread.</span></span> <span data-ttu-id="65207-105">這應該與 [JetSetSessionCoNtext (JET_SESID、IntPtr) ](./api.jetsetsessioncontext-method.md)一起使用。</span><span class="sxs-lookup"><span data-stu-id="65207-105">This should be used in conjunction with [JetSetSessionContext(JET_SESID, IntPtr)](./api.jetsetsessioncontext-method.md).</span></span>

<span data-ttu-id="65207-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="65207-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="65207-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="65207-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="65207-108">語法</span><span class="sxs-lookup"><span data-stu-id="65207-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetResetSessionContext ( _
    sesid As JET_SESID _
)
'Usage
Dim sesid As JET_SESIDApi.JetResetSessionContext(sesid)
```

``` csharp
public static void JetResetSessionContext(
    JET_SESID sesid
)
```

#### <a name="parameters"></a><span data-ttu-id="65207-109">參數</span><span class="sxs-lookup"><span data-stu-id="65207-109">Parameters</span></span>

  - <span data-ttu-id="65207-110">sesid</span><span class="sxs-lookup"><span data-stu-id="65207-110">sesid</span></span>  
    <span data-ttu-id="65207-111">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="65207-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="65207-112">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="65207-112">The session to use.</span></span>

## <a name="see-also"></a><span data-ttu-id="65207-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="65207-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="65207-114">參考</span><span class="sxs-lookup"><span data-stu-id="65207-114">Reference</span></span>

[<span data-ttu-id="65207-115">Api 類別</span><span class="sxs-lookup"><span data-stu-id="65207-115">Api class</span></span>](./api-class.md)

[<span data-ttu-id="65207-116">Api 成員</span><span class="sxs-lookup"><span data-stu-id="65207-116">Api members</span></span>](./api-members.md)

[<span data-ttu-id="65207-117">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="65207-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
