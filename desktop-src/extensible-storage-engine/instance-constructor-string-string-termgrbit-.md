---
description: '深入瞭解：實例的函式 (字串、字串、TermGrbit) '
title: '實例的函式 (字串、字串、TermGrbit) '
TOCTitle: Instance constructor (String, String, TermGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.#ctor(System.String,System.String,Microsoft.Isam.Esent.Interop.TermGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.instance(v=EXCHG.10)
ms:contentKeyID: 55103289
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Instance..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b9cf90f9678db1074594c7772eb67d895a8a5b8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691328"
---
# <a name="instance-constructor-string-string-termgrbit"></a><span data-ttu-id="3f878-103">實例的函式 (字串、字串、TermGrbit) </span><span class="sxs-lookup"><span data-stu-id="3f878-103">Instance constructor (String, String, TermGrbit)</span></span>

<span data-ttu-id="3f878-104">初始化實例類別的新實例。</span><span class="sxs-lookup"><span data-stu-id="3f878-104">Initializes a new instance of the Instance class.</span></span> <span data-ttu-id="3f878-105">已配置但未初始化基礎 JET_INSTANCE。</span><span class="sxs-lookup"><span data-stu-id="3f878-105">The underlying JET_INSTANCE is allocated, but not initialized.</span></span>

<span data-ttu-id="3f878-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3f878-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3f878-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="3f878-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3f878-108">語法</span><span class="sxs-lookup"><span data-stu-id="3f878-108">Syntax</span></span>

``` vb
'Declaration
Public Sub New ( _
    name As String, _
    displayName As String, _
    termGrbit As TermGrbit _
)
'Usage
Dim name As String
Dim displayName As String
Dim termGrbit As TermGrbit

Dim instance As New Instance(name, displayName, _
    termGrbit)
```

``` csharp
public Instance(
    string name,
    string displayName,
    TermGrbit termGrbit
)
```

#### <a name="parameters"></a><span data-ttu-id="3f878-109">參數</span><span class="sxs-lookup"><span data-stu-id="3f878-109">Parameters</span></span>

  - <span data-ttu-id="3f878-110">NAME</span><span class="sxs-lookup"><span data-stu-id="3f878-110">name</span></span>  
    <span data-ttu-id="3f878-111">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="3f878-111">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="3f878-112">執行個體的名稱。</span><span class="sxs-lookup"><span data-stu-id="3f878-112">The name of the instance.</span></span> <span data-ttu-id="3f878-113">這個字串在主控資料庫引擎的指定進程內必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="3f878-113">This string must be unique within a given process hosting the database engine.</span></span>

<!-- end list -->

  - <span data-ttu-id="3f878-114">displayName</span><span class="sxs-lookup"><span data-stu-id="3f878-114">displayName</span></span>  
    <span data-ttu-id="3f878-115">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="3f878-115">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="3f878-116">實例的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="3f878-116">A display name for the instance.</span></span> <span data-ttu-id="3f878-117">這將用於 eventlog 專案中。</span><span class="sxs-lookup"><span data-stu-id="3f878-117">This will be used in eventlog entries.</span></span>

<!-- end list -->

  - <span data-ttu-id="3f878-118">termGrbit</span><span class="sxs-lookup"><span data-stu-id="3f878-118">termGrbit</span></span>  
    <span data-ttu-id="3f878-119">型別： [TermGrbit](./termgrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="3f878-119">Type: [Microsoft.Isam.Esent.Interop.TermGrbit](./termgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="3f878-120">要在 JetTerm 階段使用的 TermGrbit。</span><span class="sxs-lookup"><span data-stu-id="3f878-120">The TermGrbit to be used at JetTerm time.</span></span>

## <a name="see-also"></a><span data-ttu-id="3f878-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3f878-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3f878-122">參考</span><span class="sxs-lookup"><span data-stu-id="3f878-122">Reference</span></span>

[<span data-ttu-id="3f878-123">Instance 類別</span><span class="sxs-lookup"><span data-stu-id="3f878-123">Instance class</span></span>](./instance-class.md)

[<span data-ttu-id="3f878-124">實例成員</span><span class="sxs-lookup"><span data-stu-id="3f878-124">Instance members</span></span>](./instance-members.md)

[<span data-ttu-id="3f878-125">實例多載</span><span class="sxs-lookup"><span data-stu-id="3f878-125">Instance overload</span></span>](./instance-constructor.md)

[<span data-ttu-id="3f878-126">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="3f878-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
