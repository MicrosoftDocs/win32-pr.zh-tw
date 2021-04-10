---
description: 深入瞭解： JET_PFNDURABLECOMMITCALLBACK 委派
title: 'JET_PFNDURABLECOMMITCALLBACK 委派 (Windows8) '
TOCTitle: JET_PFNDURABLECOMMITCALLBACK delegate
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_pfndurablecommitcallback(v=EXCHG.10)
ms:contentKeyID: 55104327
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK.Invoke
- Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK
- Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK.EndInvoke
- Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK..ctor
- Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK.BeginInvoke
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d9ff2f613138103be56db3fe7084202965a949cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852831"
---
# <a name="jet_pfndurablecommitcallback-delegate"></a><span data-ttu-id="1ef68-103">JET_PFNDURABLECOMMITCALLBACK 委派</span><span class="sxs-lookup"><span data-stu-id="1ef68-103">JET_PFNDURABLECOMMITCALLBACK delegate</span></span>

<span data-ttu-id="1ef68-104">JET_paramDurableCommitCallback 的回呼。</span><span class="sxs-lookup"><span data-stu-id="1ef68-104">Callback for JET_paramDurableCommitCallback.</span></span>

<span data-ttu-id="1ef68-105">**命名空間：**  [Microsoft Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1ef68-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="1ef68-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="1ef68-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1ef68-107">語法</span><span class="sxs-lookup"><span data-stu-id="1ef68-107">Syntax</span></span>

``` vb
'Declaration
Public Delegate Function JET_PFNDURABLECOMMITCALLBACK ( _
    instance As JET_INSTANCE, _
    pCommitIdSeen As JET_COMMIT_ID, _
    grbit As DurableCommitCallbackGrbit _
) As JET_err
'Usage
Dim instance As New JET_PFNDURABLECOMMITCALLBACK(AddressOf HandlerMethod)
```

``` csharp
public delegate JET_err JET_PFNDURABLECOMMITCALLBACK(
    JET_INSTANCE instance,
    JET_COMMIT_ID pCommitIdSeen,
    DurableCommitCallbackGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="1ef68-108">參數</span><span class="sxs-lookup"><span data-stu-id="1ef68-108">Parameters</span></span>

  - <span data-ttu-id="1ef68-109">instance</span><span class="sxs-lookup"><span data-stu-id="1ef68-109">instance</span></span>  
    <span data-ttu-id="1ef68-110">類型： [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1ef68-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="1ef68-111">要使用的實例。</span><span class="sxs-lookup"><span data-stu-id="1ef68-111">Instance to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="1ef68-112">pCommitIdSeen</span><span class="sxs-lookup"><span data-stu-id="1ef68-112">pCommitIdSeen</span></span>  
    <span data-ttu-id="1ef68-113">類型： [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span><span class="sxs-lookup"><span data-stu-id="1ef68-113">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span></span>  
    
    <span data-ttu-id="1ef68-114">剛排清的認可識別碼。</span><span class="sxs-lookup"><span data-stu-id="1ef68-114">Commit-id that has just been flushed.</span></span>

<!-- end list -->

  - <span data-ttu-id="1ef68-115">grbit</span><span class="sxs-lookup"><span data-stu-id="1ef68-115">grbit</span></span>  
    <span data-ttu-id="1ef68-116">型別： [Windows8. DurableCommitCallbackGrbit](./durablecommitcallbackgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="1ef68-116">Type: [Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallbackGrbit](./durablecommitcallbackgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="1ef68-117">目前已保留。</span><span class="sxs-lookup"><span data-stu-id="1ef68-117">Reserved currently.</span></span>

#### <a name="return-value"></a><span data-ttu-id="1ef68-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="1ef68-118">Return value</span></span>

<span data-ttu-id="1ef68-119">類型： [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="1ef68-119">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="1ef68-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1ef68-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1ef68-121">參考</span><span class="sxs-lookup"><span data-stu-id="1ef68-121">Reference</span></span>

[<span data-ttu-id="1ef68-122">Windows8 命名空間。</span><span class="sxs-lookup"><span data-stu-id="1ef68-122">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
