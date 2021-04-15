---
description: 深入瞭解： JetEndSession 方法
title: JetEndSession 方法
TOCTitle: 'JetEndSession method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetEndSession(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.EndSessionGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetendsession(v=EXCHG.10)
ms:contentKeyID: 55100690
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetEndSession
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetEndSession
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 10412f6b01b14d63557bf024d65975c271bbe31b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511137"
---
# <a name="apijetendsession-method"></a><span data-ttu-id="6c4c5-103">JetEndSession 方法</span><span class="sxs-lookup"><span data-stu-id="6c4c5-103">Api.JetEndSession method</span></span>

<span data-ttu-id="6c4c5-104">結束會話。</span><span class="sxs-lookup"><span data-stu-id="6c4c5-104">Ends a session.</span></span>

<span data-ttu-id="6c4c5-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6c4c5-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6c4c5-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="6c4c5-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6c4c5-107">語法</span><span class="sxs-lookup"><span data-stu-id="6c4c5-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetEndSession ( _
    sesid As JET_SESID, _
    grbit As EndSessionGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim grbit As EndSessionGrbitApi.JetEndSession(sesid, grbit)
```

``` csharp
public static void JetEndSession(
    JET_SESID sesid,
    EndSessionGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="6c4c5-108">參數</span><span class="sxs-lookup"><span data-stu-id="6c4c5-108">Parameters</span></span>

  - <span data-ttu-id="6c4c5-109">sesid</span><span class="sxs-lookup"><span data-stu-id="6c4c5-109">sesid</span></span>  
    <span data-ttu-id="6c4c5-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6c4c5-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="6c4c5-111">要結束的會話。</span><span class="sxs-lookup"><span data-stu-id="6c4c5-111">The session to end.</span></span>

<!-- end list -->

  - <span data-ttu-id="6c4c5-112">grbit</span><span class="sxs-lookup"><span data-stu-id="6c4c5-112">grbit</span></span>  
    <span data-ttu-id="6c4c5-113">型別： [EndSessionGrbit](./endsessiongrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="6c4c5-113">Type: [Microsoft.Isam.Esent.Interop.EndSessionGrbit](./endsessiongrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="6c4c5-114">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="6c4c5-114">This parameter is not used.</span></span>

## <a name="see-also"></a><span data-ttu-id="6c4c5-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c4c5-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6c4c5-116">參考</span><span class="sxs-lookup"><span data-stu-id="6c4c5-116">Reference</span></span>

[<span data-ttu-id="6c4c5-117">Api 類別</span><span class="sxs-lookup"><span data-stu-id="6c4c5-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="6c4c5-118">Api 成員</span><span class="sxs-lookup"><span data-stu-id="6c4c5-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="6c4c5-119">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="6c4c5-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
