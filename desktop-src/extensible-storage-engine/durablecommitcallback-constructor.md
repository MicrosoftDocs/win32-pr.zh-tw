---
description: 深入瞭解： DurableCommitCallback 的函式
title: 'DurableCommitCallback 函式 (Windows8) '
TOCTitle: 'DurableCommitCallback constructor '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback.#ctor(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.durablecommitcallback.durablecommitcallback(v=EXCHG.10)
ms:contentKeyID: 55104290
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback.DurableCommitCallback
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ade1952615b98d9ea41a7a1b83d0bf1a3c6fc8d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694916"
---
# <a name="durablecommitcallback-constructor"></a><span data-ttu-id="2ac13-103">DurableCommitCallback 函式</span><span class="sxs-lookup"><span data-stu-id="2ac13-103">DurableCommitCallback constructor</span></span>

<span data-ttu-id="2ac13-104">初始化 [DurableCommitCallback](./durablecommitcallback-class.md) 類別的新實例。</span><span class="sxs-lookup"><span data-stu-id="2ac13-104">Initializes a new instance of the [DurableCommitCallback](./durablecommitcallback-class.md) class.</span></span>

<span data-ttu-id="2ac13-105">**命名空間：**  [Microsoft Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2ac13-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="2ac13-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="2ac13-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2ac13-107">語法</span><span class="sxs-lookup"><span data-stu-id="2ac13-107">Syntax</span></span>

``` vb
'Declaration
Public Sub New ( _
    instance As JET_INSTANCE, _
    wrappedCallback As JET_PFNDURABLECOMMITCALLBACK _
)
'Usage
Dim instance As JET_INSTANCE
Dim wrappedCallback As JET_PFNDURABLECOMMITCALLBACK

Dim instance As New DurableCommitCallback(instance, _
    wrappedCallback)
```

``` csharp
public DurableCommitCallback(
    JET_INSTANCE instance,
    JET_PFNDURABLECOMMITCALLBACK wrappedCallback
)
```

#### <a name="parameters"></a><span data-ttu-id="2ac13-108">參數</span><span class="sxs-lookup"><span data-stu-id="2ac13-108">Parameters</span></span>

  - <span data-ttu-id="2ac13-109">instance</span><span class="sxs-lookup"><span data-stu-id="2ac13-109">instance</span></span>  
    <span data-ttu-id="2ac13-110">類型： [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2ac13-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="2ac13-111">要與回呼產生關聯的實例。</span><span class="sxs-lookup"><span data-stu-id="2ac13-111">The instance with which to associate the callback.</span></span>

<!-- end list -->

  - <span data-ttu-id="2ac13-112">wrappedCallback</span><span class="sxs-lookup"><span data-stu-id="2ac13-112">wrappedCallback</span></span>  
    <span data-ttu-id="2ac13-113">類型： [Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK](./jet-pfndurablecommitcallback-delegate.md)</span><span class="sxs-lookup"><span data-stu-id="2ac13-113">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK](./jet-pfndurablecommitcallback-delegate.md)</span></span>  
    
    <span data-ttu-id="2ac13-114">要呼叫的 managed 程式碼回呼。</span><span class="sxs-lookup"><span data-stu-id="2ac13-114">The managed code callback to call.</span></span>

## <a name="see-also"></a><span data-ttu-id="2ac13-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2ac13-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2ac13-116">參考</span><span class="sxs-lookup"><span data-stu-id="2ac13-116">Reference</span></span>

[<span data-ttu-id="2ac13-117">DurableCommitCallback 類別</span><span class="sxs-lookup"><span data-stu-id="2ac13-117">DurableCommitCallback class</span></span>](./durablecommitcallback-class.md)

[<span data-ttu-id="2ac13-118">DurableCommitCallback 成員</span><span class="sxs-lookup"><span data-stu-id="2ac13-118">DurableCommitCallback members</span></span>](./durablecommitcallback-members.md)

[<span data-ttu-id="2ac13-119">Windows8 命名空間。</span><span class="sxs-lookup"><span data-stu-id="2ac13-119">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
