---
description: '深入瞭解：實例的函式 (字串、字串) '
title: '實例的函式 (字串，字串) '
TOCTitle: Instance constructor (String, String)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.#ctor(System.String,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.instance(v=EXCHG.10)
ms:contentKeyID: 55103267
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Instance..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 02cb629cdfaba17ce9a137b52eb1a6d6fdbaa56b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318668"
---
# <a name="instance-constructor-string-string"></a><span data-ttu-id="51725-103">實例的函式 (字串，字串) </span><span class="sxs-lookup"><span data-stu-id="51725-103">Instance constructor (String, String)</span></span>

<span data-ttu-id="51725-104">初始化實例類別的新實例。</span><span class="sxs-lookup"><span data-stu-id="51725-104">Initializes a new instance of the Instance class.</span></span> <span data-ttu-id="51725-105">已配置但未初始化基礎 JET_INSTANCE。</span><span class="sxs-lookup"><span data-stu-id="51725-105">The underlying JET_INSTANCE is allocated, but not initialized.</span></span>

<span data-ttu-id="51725-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="51725-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="51725-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="51725-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="51725-108">語法</span><span class="sxs-lookup"><span data-stu-id="51725-108">Syntax</span></span>

``` vb
'Declaration
Public Sub New ( _
    name As String, _
    displayName As String _
)
'Usage
Dim name As String
Dim displayName As String

Dim instance As New Instance(name, displayName)
```

``` csharp
public Instance(
    string name,
    string displayName
)
```

#### <a name="parameters"></a><span data-ttu-id="51725-109">參數</span><span class="sxs-lookup"><span data-stu-id="51725-109">Parameters</span></span>

  - <span data-ttu-id="51725-110">NAME</span><span class="sxs-lookup"><span data-stu-id="51725-110">name</span></span>  
    <span data-ttu-id="51725-111">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="51725-111">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="51725-112">執行個體的名稱。</span><span class="sxs-lookup"><span data-stu-id="51725-112">The name of the instance.</span></span> <span data-ttu-id="51725-113">這個字串在主控資料庫引擎的指定進程內必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="51725-113">This string must be unique within a given process hosting the database engine.</span></span>

<!-- end list -->

  - <span data-ttu-id="51725-114">displayName</span><span class="sxs-lookup"><span data-stu-id="51725-114">displayName</span></span>  
    <span data-ttu-id="51725-115">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="51725-115">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="51725-116">實例的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="51725-116">A display name for the instance.</span></span> <span data-ttu-id="51725-117">這將用於 eventlog 專案中。</span><span class="sxs-lookup"><span data-stu-id="51725-117">This will be used in eventlog entries.</span></span>

## <a name="see-also"></a><span data-ttu-id="51725-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="51725-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="51725-119">參考</span><span class="sxs-lookup"><span data-stu-id="51725-119">Reference</span></span>

[<span data-ttu-id="51725-120">Instance 類別</span><span class="sxs-lookup"><span data-stu-id="51725-120">Instance class</span></span>](./instance-class.md)

[<span data-ttu-id="51725-121">實例成員</span><span class="sxs-lookup"><span data-stu-id="51725-121">Instance members</span></span>](./instance-members.md)

[<span data-ttu-id="51725-122">實例多載</span><span class="sxs-lookup"><span data-stu-id="51725-122">Instance overload</span></span>](./instance-constructor.md)

[<span data-ttu-id="51725-123">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="51725-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
