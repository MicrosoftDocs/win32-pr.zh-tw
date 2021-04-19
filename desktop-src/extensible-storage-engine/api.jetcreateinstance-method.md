---
description: 深入瞭解： JetCreateInstance 方法
title: JetCreateInstance 方法
TOCTitle: 'JetCreateInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE@,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreateinstance(v=EXCHG.10)
ms:contentKeyID: 55100672
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1e865c443d4f19b14a955204840355ee73be8773
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974019"
---
# <a name="apijetcreateinstance-method"></a><span data-ttu-id="b6b30-103">JetCreateInstance 方法</span><span class="sxs-lookup"><span data-stu-id="b6b30-103">Api.JetCreateInstance method</span></span>

<span data-ttu-id="b6b30-104">配置 database engine 的新實例。</span><span class="sxs-lookup"><span data-stu-id="b6b30-104">Allocates a new instance of the database engine.</span></span>

<span data-ttu-id="b6b30-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b6b30-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b6b30-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="b6b30-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b6b30-107">語法</span><span class="sxs-lookup"><span data-stu-id="b6b30-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateInstance ( _
    <OutAttribute> ByRef instance As JET_INSTANCE, _
    name As String _
)
'Usage
Dim instance As JET_INSTANCE
Dim name As StringApi.JetCreateInstance(instance, _
    name)
```

``` csharp
public static void JetCreateInstance(
    out JET_INSTANCE instance,
    string name
)
```

#### <a name="parameters"></a><span data-ttu-id="b6b30-108">參數</span><span class="sxs-lookup"><span data-stu-id="b6b30-108">Parameters</span></span>

  - <span data-ttu-id="b6b30-109">instance</span><span class="sxs-lookup"><span data-stu-id="b6b30-109">instance</span></span>  
    <span data-ttu-id="b6b30-110">類型： [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b6b30-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="b6b30-111">傳回新的實例。</span><span class="sxs-lookup"><span data-stu-id="b6b30-111">Returns the new instance.</span></span>

<!-- end list -->

  - <span data-ttu-id="b6b30-112">NAME</span><span class="sxs-lookup"><span data-stu-id="b6b30-112">name</span></span>  
    <span data-ttu-id="b6b30-113">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="b6b30-113">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="b6b30-114">執行個體的名稱。</span><span class="sxs-lookup"><span data-stu-id="b6b30-114">The name of the instance.</span></span> <span data-ttu-id="b6b30-115">名稱必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="b6b30-115">Names must be unique.</span></span>

## <a name="see-also"></a><span data-ttu-id="b6b30-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b6b30-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b6b30-117">參考</span><span class="sxs-lookup"><span data-stu-id="b6b30-117">Reference</span></span>

[<span data-ttu-id="b6b30-118">Api 類別</span><span class="sxs-lookup"><span data-stu-id="b6b30-118">Api class</span></span>](./api-class.md)

[<span data-ttu-id="b6b30-119">Api 成員</span><span class="sxs-lookup"><span data-stu-id="b6b30-119">Api members</span></span>](./api-members.md)

[<span data-ttu-id="b6b30-120">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="b6b30-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
