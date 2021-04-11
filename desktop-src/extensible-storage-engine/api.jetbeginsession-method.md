---
description: 深入瞭解： JetBeginSession 方法
title: JetBeginSession 方法
TOCTitle: 'JetBeginSession method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetBeginSession(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_SESID@,System.String,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetbeginsession(v=EXCHG.10)
ms:contentKeyID: 55107223
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetBeginSession
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetBeginSession
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 39174c27043f62de4c1a78685876e79de513b804
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111940"
---
# <a name="apijetbeginsession-method"></a><span data-ttu-id="bcce0-103">JetBeginSession 方法</span><span class="sxs-lookup"><span data-stu-id="bcce0-103">Api.JetBeginSession method</span></span>

<span data-ttu-id="bcce0-104">初始化新的 ESENT 會話。</span><span class="sxs-lookup"><span data-stu-id="bcce0-104">Initialize a new ESENT session.</span></span>

<span data-ttu-id="bcce0-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="bcce0-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="bcce0-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="bcce0-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="bcce0-107">語法</span><span class="sxs-lookup"><span data-stu-id="bcce0-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetBeginSession ( _
    instance As JET_INSTANCE, _
    <OutAttribute> ByRef sesid As JET_SESID, _
    username As String, _
    password As String _
)
'Usage
Dim instance As JET_INSTANCE
Dim sesid As JET_SESID
Dim username As String
Dim password As StringApi.JetBeginSession(instance, sesid, _
    username, password)
```

``` csharp
public static void JetBeginSession(
    JET_INSTANCE instance,
    out JET_SESID sesid,
    string username,
    string password
)
```

#### <a name="parameters"></a><span data-ttu-id="bcce0-108">參數</span><span class="sxs-lookup"><span data-stu-id="bcce0-108">Parameters</span></span>

  - <span data-ttu-id="bcce0-109">instance</span><span class="sxs-lookup"><span data-stu-id="bcce0-109">instance</span></span>  
    <span data-ttu-id="bcce0-110">類型： [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="bcce0-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="bcce0-111">要在其中建立會話的初始化實例。</span><span class="sxs-lookup"><span data-stu-id="bcce0-111">The initialized instance to create the session in.</span></span>

<!-- end list -->

  - <span data-ttu-id="bcce0-112">sesid</span><span class="sxs-lookup"><span data-stu-id="bcce0-112">sesid</span></span>  
    <span data-ttu-id="bcce0-113">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="bcce0-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="bcce0-114">傳回已建立的會話。</span><span class="sxs-lookup"><span data-stu-id="bcce0-114">Returns the created session.</span></span>

<!-- end list -->

  - <span data-ttu-id="bcce0-115">username</span><span class="sxs-lookup"><span data-stu-id="bcce0-115">username</span></span>  
    <span data-ttu-id="bcce0-116">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="bcce0-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="bcce0-117">不使用參數。</span><span class="sxs-lookup"><span data-stu-id="bcce0-117">The parameter is not used.</span></span>

<!-- end list -->

  - <span data-ttu-id="bcce0-118">密碼</span><span class="sxs-lookup"><span data-stu-id="bcce0-118">password</span></span>  
    <span data-ttu-id="bcce0-119">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="bcce0-119">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="bcce0-120">不使用參數。</span><span class="sxs-lookup"><span data-stu-id="bcce0-120">The parameter is not used.</span></span>

## <a name="see-also"></a><span data-ttu-id="bcce0-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bcce0-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bcce0-122">參考</span><span class="sxs-lookup"><span data-stu-id="bcce0-122">Reference</span></span>

[<span data-ttu-id="bcce0-123">Api 類別</span><span class="sxs-lookup"><span data-stu-id="bcce0-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="bcce0-124">Api 成員</span><span class="sxs-lookup"><span data-stu-id="bcce0-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="bcce0-125">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="bcce0-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
