---
description: 深入瞭解： JET_LGPOS 結構
title: JET_LGPOS 結構
TOCTitle: JET_LGPOS structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_LGPOS
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_lgpos(v=EXCHG.10)
ms:contentKeyID: 39511335
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LGPOS
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LGPOS
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e757f71de04e15c77bab141acb0442fc61d5af0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981893"
---
# <a name="jet_lgpos-structure"></a><span data-ttu-id="79b25-103">JET_LGPOS 結構</span><span class="sxs-lookup"><span data-stu-id="79b25-103">JET_LGPOS structure</span></span>

<span data-ttu-id="79b25-104">描述記錄順序中的位移。</span><span class="sxs-lookup"><span data-stu-id="79b25-104">Describes an offset in the log sequence.</span></span>

<span data-ttu-id="79b25-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="79b25-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="79b25-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="79b25-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="79b25-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="79b25-107">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public Structure JET_LGPOS _
    Implements IEquatable(Of JET_LGPOS), IComparable(Of JET_LGPOS),  _
    INullableJetStruct
'Usage
Dim instance As JET_LGPOS
```

``` csharp
[SerializableAttribute]
public struct JET_LGPOS : IEquatable<JET_LGPOS>, 
    IComparable<JET_LGPOS>, INullableJetStruct
```

## <a name="thread-safety"></a><span data-ttu-id="79b25-108">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="79b25-108">Thread safety</span></span>

<span data-ttu-id="79b25-109">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="79b25-109">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="79b25-110">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="79b25-110">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="79b25-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="79b25-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="79b25-112">參考</span><span class="sxs-lookup"><span data-stu-id="79b25-112">Reference</span></span>

[<span data-ttu-id="79b25-113">JET_LGPOS 成員</span><span class="sxs-lookup"><span data-stu-id="79b25-113">JET_LGPOS members</span></span>](./jet-lgpos-members.md)

[<span data-ttu-id="79b25-114">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="79b25-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
