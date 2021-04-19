---
description: 深入瞭解： JET_RSTINFO pfnStatus 屬性
title: JET_RSTINFO pfnStatus 屬性
TOCTitle: 'pfnStatus property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RSTINFO.pfnStatus
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_rstinfo.pfnstatus(v=EXCHG.10)
ms:contentKeyID: 55103829
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RSTINFO.pfnStatus
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RSTINFO.pfnStatus
- Microsoft.Isam.Esent.Interop.JET_RSTINFO.set_pfnStatus
- Microsoft.Isam.Esent.Interop.JET_RSTINFO.get_pfnStatus
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 57b400e91867d4408fcdb93b979d1a39d8e7eb76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973616"
---
# <a name="jet_rstinfopfnstatus-property"></a><span data-ttu-id="8fa2a-103">JET_RSTINFO pfnStatus 屬性</span><span class="sxs-lookup"><span data-stu-id="8fa2a-103">JET_RSTINFO.pfnStatus property</span></span>

<span data-ttu-id="8fa2a-104">取得或設定要取得或設定狀態函數的回呼。</span><span class="sxs-lookup"><span data-stu-id="8fa2a-104">Gets or sets the callback to Gets or sets the status function.</span></span>

<span data-ttu-id="8fa2a-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8fa2a-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8fa2a-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="8fa2a-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8fa2a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8fa2a-107">Syntax</span></span>

``` vb
'Declaration
Public Property pfnStatus As JET_PFNSTATUS
    Get
    Set
'Usage
Dim instance As JET_RSTINFO
Dim value As JET_PFNSTATUS

value = instance.pfnStatus

instance.pfnStatus = value
```

``` csharp
public JET_PFNSTATUS pfnStatus { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="8fa2a-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="8fa2a-108">Property value</span></span>

<span data-ttu-id="8fa2a-109">類型： [Microsoft.Isam.Esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)</span><span class="sxs-lookup"><span data-stu-id="8fa2a-109">Type: [Microsoft.Isam.Esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="8fa2a-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8fa2a-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8fa2a-111">參考</span><span class="sxs-lookup"><span data-stu-id="8fa2a-111">Reference</span></span>

[<span data-ttu-id="8fa2a-112">JET_RSTINFO 類別</span><span class="sxs-lookup"><span data-stu-id="8fa2a-112">JET_RSTINFO class</span></span>](./jet-rstinfo-class.md)

[<span data-ttu-id="8fa2a-113">JET_RSTINFO 成員</span><span class="sxs-lookup"><span data-stu-id="8fa2a-113">JET_RSTINFO members</span></span>](./jet-rstinfo-members.md)

[<span data-ttu-id="8fa2a-114">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="8fa2a-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
