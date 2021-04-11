---
description: 深入瞭解： JET_BKLOGTIME 結構
title: JET_BKLOGTIME 結構
TOCTitle: JET_BKLOGTIME structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_BKLOGTIME
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_bklogtime(v=EXCHG.10)
ms:contentKeyID: 39512194
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b718254082095592f097097500d2690be320dd63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114069"
---
# <a name="jet_bklogtime-structure"></a><span data-ttu-id="e89c3-103">JET_BKLOGTIME 結構</span><span class="sxs-lookup"><span data-stu-id="e89c3-103">JET_BKLOGTIME structure</span></span>

<span data-ttu-id="e89c3-104">描述備份發生的日期/時間。</span><span class="sxs-lookup"><span data-stu-id="e89c3-104">Describes a date/time when a backup occured.</span></span>

<span data-ttu-id="e89c3-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e89c3-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e89c3-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="e89c3-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e89c3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e89c3-107">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public Structure JET_BKLOGTIME _
    Implements IEquatable(Of JET_BKLOGTIME), IJET_LOGTIME,  _
    INullableJetStruct
'Usage
Dim instance As JET_BKLOGTIME
```

``` csharp
[SerializableAttribute]
public struct JET_BKLOGTIME : IEquatable<JET_BKLOGTIME>, 
    IJET_LOGTIME, INullableJetStruct
```

## <a name="thread-safety"></a><span data-ttu-id="e89c3-108">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="e89c3-108">Thread safety</span></span>

<span data-ttu-id="e89c3-109">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="e89c3-109">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="e89c3-110">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="e89c3-110">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="e89c3-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e89c3-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e89c3-112">參考</span><span class="sxs-lookup"><span data-stu-id="e89c3-112">Reference</span></span>

[<span data-ttu-id="e89c3-113">JET_BKLOGTIME 成員</span><span class="sxs-lookup"><span data-stu-id="e89c3-113">JET_BKLOGTIME members</span></span>](./jet-bklogtime-members.md)

[<span data-ttu-id="e89c3-114">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="e89c3-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
