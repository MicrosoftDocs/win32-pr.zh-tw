---
description: '深入瞭解：實例的函式 (字串) '
title: " (字串) 的實例函式"
TOCTitle: Instance constructor (String)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.#ctor(System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.instance(v=EXCHG.10)
ms:contentKeyID: 55103263
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
ms.openlocfilehash: 8cf184fc9b8d921b1d8bd1003b960bc65a6ffb75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195491"
---
# <a name="instance-constructor-string"></a><span data-ttu-id="500ed-103"> (字串) 的實例函式</span><span class="sxs-lookup"><span data-stu-id="500ed-103">Instance constructor (String)</span></span>

<span data-ttu-id="500ed-104">初始化實例類別的新實例。</span><span class="sxs-lookup"><span data-stu-id="500ed-104">Initializes a new instance of the Instance class.</span></span> <span data-ttu-id="500ed-105">已配置但未初始化基礎 JET_INSTANCE。</span><span class="sxs-lookup"><span data-stu-id="500ed-105">The underlying JET_INSTANCE is allocated, but not initialized.</span></span>

<span data-ttu-id="500ed-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="500ed-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="500ed-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="500ed-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="500ed-108">語法</span><span class="sxs-lookup"><span data-stu-id="500ed-108">Syntax</span></span>

``` vb
'Declaration
Public Sub New ( _
    name As String _
)
'Usage
Dim name As String

Dim instance As New Instance(name)
```

``` csharp
public Instance(
    string name
)
```

#### <a name="parameters"></a><span data-ttu-id="500ed-109">參數</span><span class="sxs-lookup"><span data-stu-id="500ed-109">Parameters</span></span>

  - <span data-ttu-id="500ed-110">NAME</span><span class="sxs-lookup"><span data-stu-id="500ed-110">name</span></span>  
    <span data-ttu-id="500ed-111">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="500ed-111">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="500ed-112">執行個體的名稱。</span><span class="sxs-lookup"><span data-stu-id="500ed-112">The name of the instance.</span></span> <span data-ttu-id="500ed-113">這個字串在主控資料庫引擎的指定進程內必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="500ed-113">This string must be unique within a given process hosting the database engine.</span></span>

## <a name="see-also"></a><span data-ttu-id="500ed-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="500ed-114">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="500ed-115">參考</span><span class="sxs-lookup"><span data-stu-id="500ed-115">Reference</span></span>

[<span data-ttu-id="500ed-116">Instance 類別</span><span class="sxs-lookup"><span data-stu-id="500ed-116">Instance class</span></span>](./instance-class.md)

[<span data-ttu-id="500ed-117">實例成員</span><span class="sxs-lookup"><span data-stu-id="500ed-117">Instance members</span></span>](./instance-members.md)

[<span data-ttu-id="500ed-118">實例多載</span><span class="sxs-lookup"><span data-stu-id="500ed-118">Instance overload</span></span>](./instance-constructor.md)

[<span data-ttu-id="500ed-119">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="500ed-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
