---
description: '深入瞭解：實例隱含轉換 (實例至 JET_INSTANCE) '
title: '實例隱含轉換 (實例至 JET_INSTANCE) '
TOCTitle: Implicit conversion (Instance to JET_INSTANCE)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.op_Implicit(Microsoft.Isam.Esent.Interop.Instance)~Microsoft.Isam.Esent.Interop.JET_INSTANCE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.op_implicit(v=EXCHG.10)
ms:contentKeyID: 55103290
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Instance.Implicit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Instance.Implicit
- Microsoft.Isam.Esent.Interop.Instance.op_Implicit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8c7dbac9f0b5736970cf51aef9e99f2877cfd488
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107000259"
---
# <a name="instance-implicit-conversion-instance-to-jet_instance"></a><span data-ttu-id="763a3-103">實例隱含轉換 (實例至 JET_INSTANCE) </span><span class="sxs-lookup"><span data-stu-id="763a3-103">Instance Implicit conversion (Instance to JET_INSTANCE)</span></span>

<span data-ttu-id="763a3-104">將實例物件的隱含轉換提供給 JET_INSTANCE 結構。</span><span class="sxs-lookup"><span data-stu-id="763a3-104">Provide implicit conversion of an Instance object to a JET_INSTANCE structure.</span></span> <span data-ttu-id="763a3-105">這樣做的目的是要讓實例可以在需要 JET_INSTANCE 的任何地方使用。</span><span class="sxs-lookup"><span data-stu-id="763a3-105">This is done so that an Instance can be used anywhere a JET_INSTANCE is required.</span></span>

<span data-ttu-id="763a3-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="763a3-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="763a3-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="763a3-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="763a3-108">語法</span><span class="sxs-lookup"><span data-stu-id="763a3-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Widening Operator CType ( _
    instance As Instance _
) As JET_INSTANCE
'Usage
Dim input As Instance
Dim output As JET_INSTANCE

output = CType(input, JET_INSTANCE)
```

``` csharp
public static implicit operator JET_INSTANCE (
    Instance instance
)
```

#### <a name="parameters"></a><span data-ttu-id="763a3-109">參數</span><span class="sxs-lookup"><span data-stu-id="763a3-109">Parameters</span></span>

  - <span data-ttu-id="763a3-110">instance</span><span class="sxs-lookup"><span data-stu-id="763a3-110">instance</span></span>  
    <span data-ttu-id="763a3-111">類型： [Microsoft. Isam](./instance-class.md) 。</span><span class="sxs-lookup"><span data-stu-id="763a3-111">Type: [Microsoft.Isam.Esent.Interop.Instance](./instance-class.md)</span></span>  
    
    <span data-ttu-id="763a3-112">要轉換的實例。</span><span class="sxs-lookup"><span data-stu-id="763a3-112">The instance to convert.</span></span>

#### <a name="return-value"></a><span data-ttu-id="763a3-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="763a3-113">Return value</span></span>

<span data-ttu-id="763a3-114">類型： [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="763a3-114">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
<span data-ttu-id="763a3-115">由實例包裝的 JET_INSTANCE。</span><span class="sxs-lookup"><span data-stu-id="763a3-115">The JET_INSTANCE wrapped by the instance.</span></span>  

## <a name="see-also"></a><span data-ttu-id="763a3-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="763a3-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="763a3-117">參考</span><span class="sxs-lookup"><span data-stu-id="763a3-117">Reference</span></span>

[<span data-ttu-id="763a3-118">Instance 類別</span><span class="sxs-lookup"><span data-stu-id="763a3-118">Instance class</span></span>](./instance-class.md)

[<span data-ttu-id="763a3-119">實例成員</span><span class="sxs-lookup"><span data-stu-id="763a3-119">Instance members</span></span>](./instance-members.md)

[<span data-ttu-id="763a3-120">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="763a3-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
