---
description: '深入瞭解： (會話的會話隱含轉換至 JET_SESID) '
title: " (會話的會話隱含轉換 JET_SESID) "
TOCTitle: Implicit conversion (Session to JET_SESID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Session.op_Implicit(Microsoft.Isam.Esent.Interop.Session)~Microsoft.Isam.Esent.Interop.JET_SESID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.session.op_implicit(v=EXCHG.10)
ms:contentKeyID: 55104121
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Session.Implicit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Session.op_Implicit
- Microsoft.Isam.Esent.Interop.Session.Implicit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 512bc457a84ad1d1b170ac9d31cb04e36d8a05d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966767"
---
# <a name="session-implicit-conversion-session-to-jet_sesid"></a><span data-ttu-id="5a9ae-103"> (會話的會話隱含轉換 JET_SESID) </span><span class="sxs-lookup"><span data-stu-id="5a9ae-103">Session Implicit conversion (Session to JET_SESID)</span></span>

<span data-ttu-id="5a9ae-104">從會話到 JET_SESID 的隱含轉換運算子。</span><span class="sxs-lookup"><span data-stu-id="5a9ae-104">Implicit conversion operator from a Session to a JET_SESID.</span></span> <span data-ttu-id="5a9ae-105">這可讓會話與預期 JET_SESID 的 Api 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="5a9ae-105">This allows a Session to be used with APIs which expect a JET_SESID.</span></span>

<span data-ttu-id="5a9ae-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5a9ae-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5a9ae-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="5a9ae-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5a9ae-108">語法</span><span class="sxs-lookup"><span data-stu-id="5a9ae-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Widening Operator CType ( _
    session As Session _
) As JET_SESID
'Usage
Dim input As Session
Dim output As JET_SESID

output = CType(input, JET_SESID)
```

``` csharp
public static implicit operator JET_SESID (
    Session session
)
```

#### <a name="parameters"></a><span data-ttu-id="5a9ae-109">參數</span><span class="sxs-lookup"><span data-stu-id="5a9ae-109">Parameters</span></span>

  - <span data-ttu-id="5a9ae-110">工作階段 (session)</span><span class="sxs-lookup"><span data-stu-id="5a9ae-110">session</span></span>  
    <span data-ttu-id="5a9ae-111">類型： [Microsoft. Isam](./session-class.md) 。</span><span class="sxs-lookup"><span data-stu-id="5a9ae-111">Type: [Microsoft.Isam.Esent.Interop.Session](./session-class.md)</span></span>  
    
    <span data-ttu-id="5a9ae-112">要轉換的會話。</span><span class="sxs-lookup"><span data-stu-id="5a9ae-112">The session to convert.</span></span>

#### <a name="return-value"></a><span data-ttu-id="5a9ae-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="5a9ae-113">Return value</span></span>

<span data-ttu-id="5a9ae-114">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5a9ae-114">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
<span data-ttu-id="5a9ae-115">會話的 JET_SESID。</span><span class="sxs-lookup"><span data-stu-id="5a9ae-115">The JET_SESID of the session.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5a9ae-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5a9ae-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5a9ae-117">參考</span><span class="sxs-lookup"><span data-stu-id="5a9ae-117">Reference</span></span>

[<span data-ttu-id="5a9ae-118">工作階段類別</span><span class="sxs-lookup"><span data-stu-id="5a9ae-118">Session class</span></span>](./session-class.md)

[<span data-ttu-id="5a9ae-119">會話成員</span><span class="sxs-lookup"><span data-stu-id="5a9ae-119">Session members</span></span>](./session-members.md)

[<span data-ttu-id="5a9ae-120">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="5a9ae-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
