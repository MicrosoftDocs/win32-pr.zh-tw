---
description: 深入瞭解： JetGetInstanceInfo 方法
title: JetGetInstanceInfo 方法
TOCTitle: 'JetGetInstanceInfo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetInstanceInfo(System.Int32@,Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO[]@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetinstanceinfo(v=EXCHG.10)
ms:contentKeyID: 55100729
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetInstanceInfo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetInstanceInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4b618c0eb7bf6e861337ebb40a95cb75d4434038
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191242"
---
# <a name="apijetgetinstanceinfo-method"></a><span data-ttu-id="8b508-103">JetGetInstanceInfo 方法</span><span class="sxs-lookup"><span data-stu-id="8b508-103">Api.JetGetInstanceInfo method</span></span>

<span data-ttu-id="8b508-104">抓取正在執行之實例的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8b508-104">Retrieves information about the instances that are running.</span></span>

<span data-ttu-id="8b508-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8b508-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8b508-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="8b508-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8b508-107">語法</span><span class="sxs-lookup"><span data-stu-id="8b508-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetInstanceInfo ( _
    <OutAttribute> ByRef numInstances As Integer, _
    <OutAttribute> ByRef instances As JET_INSTANCE_INFO() _
)
'Usage
Dim numInstances As Integer
Dim instances As JET_INSTANCE_INFO()

Api.JetGetInstanceInfo(numInstances, _
    instances)
```

``` csharp
public static void JetGetInstanceInfo(
    out int numInstances,
    out JET_INSTANCE_INFO[] instances
)
```

#### <a name="parameters"></a><span data-ttu-id="8b508-108">參數</span><span class="sxs-lookup"><span data-stu-id="8b508-108">Parameters</span></span>

  - <span data-ttu-id="8b508-109">numInstances</span><span class="sxs-lookup"><span data-stu-id="8b508-109">numInstances</span></span>  
    <span data-ttu-id="8b508-110">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="8b508-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="8b508-111">傳回實例的數目。</span><span class="sxs-lookup"><span data-stu-id="8b508-111">Returns the number of instances.</span></span>

<!-- end list -->

  - <span data-ttu-id="8b508-112">執行個體</span><span class="sxs-lookup"><span data-stu-id="8b508-112">instances</span></span>  
    <span data-ttu-id="8b508-113">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="8b508-113">Type: \[\]</span></span>  
    
    <span data-ttu-id="8b508-114">傳回實例資訊物件的陣列，每個執行中的實例各一個。</span><span class="sxs-lookup"><span data-stu-id="8b508-114">Returns an array of instance info objects, one for each running instance.</span></span>

## <a name="see-also"></a><span data-ttu-id="8b508-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8b508-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8b508-116">參考</span><span class="sxs-lookup"><span data-stu-id="8b508-116">Reference</span></span>

[<span data-ttu-id="8b508-117">Api 類別</span><span class="sxs-lookup"><span data-stu-id="8b508-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="8b508-118">Api 成員</span><span class="sxs-lookup"><span data-stu-id="8b508-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="8b508-119">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="8b508-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
