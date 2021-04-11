---
description: 深入瞭解： JetDupSession 方法
title: JetDupSession 方法
TOCTitle: 'JetDupSession method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDupSession(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_SESID@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdupsession(v=EXCHG.10)
ms:contentKeyID: 55100689
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDupSession
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDupSession
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9013c3c99c1d6c6067386038ec4a51f37f978650
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112593"
---
# <a name="apijetdupsession-method"></a><span data-ttu-id="5acde-103">JetDupSession 方法</span><span class="sxs-lookup"><span data-stu-id="5acde-103">Api.JetDupSession method</span></span>

<span data-ttu-id="5acde-104">在與指定 sesid 相同的實例中，初始化新的 ESE 會話。</span><span class="sxs-lookup"><span data-stu-id="5acde-104">Initialize a new ESE session in the same instance as the given sesid.</span></span>

<span data-ttu-id="5acde-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5acde-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5acde-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="5acde-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5acde-107">語法</span><span class="sxs-lookup"><span data-stu-id="5acde-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetDupSession ( _
    sesid As JET_SESID, _
    <OutAttribute> ByRef newSesid As JET_SESID _
)
'Usage
Dim sesid As JET_SESID
Dim newSesid As JET_SESIDApi.JetDupSession(sesid, newSesid)
```

``` csharp
public static void JetDupSession(
    JET_SESID sesid,
    out JET_SESID newSesid
)
```

#### <a name="parameters"></a><span data-ttu-id="5acde-108">參數</span><span class="sxs-lookup"><span data-stu-id="5acde-108">Parameters</span></span>

  - <span data-ttu-id="5acde-109">sesid</span><span class="sxs-lookup"><span data-stu-id="5acde-109">sesid</span></span>  
    <span data-ttu-id="5acde-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5acde-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="5acde-111">要複製的會話。</span><span class="sxs-lookup"><span data-stu-id="5acde-111">The session to duplicate.</span></span>

<!-- end list -->

  - <span data-ttu-id="5acde-112">newSesid</span><span class="sxs-lookup"><span data-stu-id="5acde-112">newSesid</span></span>  
    <span data-ttu-id="5acde-113">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5acde-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="5acde-114">傳回新的會話。</span><span class="sxs-lookup"><span data-stu-id="5acde-114">Returns the new session.</span></span>

## <a name="see-also"></a><span data-ttu-id="5acde-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5acde-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5acde-116">參考</span><span class="sxs-lookup"><span data-stu-id="5acde-116">Reference</span></span>

[<span data-ttu-id="5acde-117">Api 類別</span><span class="sxs-lookup"><span data-stu-id="5acde-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="5acde-118">Api 成員</span><span class="sxs-lookup"><span data-stu-id="5acde-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="5acde-119">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="5acde-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
