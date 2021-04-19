---
description: 深入瞭解： EsentVersion. SupportsLargeKeys 屬性
title: EsentVersion. SupportsLargeKeys 屬性
TOCTitle: 'SupportsLargeKeys property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.EsentVersion.SupportsLargeKeys
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentversion.supportslargekeys(v=EXCHG.10)
ms:contentKeyID: 55103180
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentVersion.SupportsLargeKeys
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentVersion.SupportsLargeKeys
- Microsoft.Isam.Esent.Interop.EsentVersion.get_SupportsLargeKeys
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 43ee88b7c0e190d9c717c087deeb5fc4556e6575
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982108"
---
# <a name="esentversionsupportslargekeys-property"></a><span data-ttu-id="8e043-103">EsentVersion. SupportsLargeKeys 屬性</span><span class="sxs-lookup"><span data-stu-id="8e043-103">EsentVersion.SupportsLargeKeys property</span></span>

<span data-ttu-id="8e043-104">取得值，這個值表示是否支援大型 (\> 255 位元組) 金鑰。</span><span class="sxs-lookup"><span data-stu-id="8e043-104">Gets a value that indicates whether large (\> 255 byte) keys are supported.</span></span> <span data-ttu-id="8e043-105">您可以在 [JET_INDEXCREATE](./jet-indexcreate-class.md) 物件中指定索引的索引鍵大小。</span><span class="sxs-lookup"><span data-stu-id="8e043-105">The key size for an index can be specified in the [JET_INDEXCREATE](./jet-indexcreate-class.md) object.</span></span>

<span data-ttu-id="8e043-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8e043-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8e043-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="8e043-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8e043-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e043-108">Syntax</span></span>

``` vb
'Declaration
Public Shared ReadOnly Property SupportsLargeKeys As Boolean
    Get
'Usage
Dim value As Boolean

value = EsentVersion.SupportsLargeKeys
```

``` csharp
public static bool SupportsLargeKeys { get; }
```

#### <a name="property-value"></a><span data-ttu-id="8e043-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="8e043-109">Property value</span></span>

<span data-ttu-id="8e043-110">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="8e043-110">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  

## <a name="see-also"></a><span data-ttu-id="8e043-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8e043-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8e043-112">參考</span><span class="sxs-lookup"><span data-stu-id="8e043-112">Reference</span></span>

[<span data-ttu-id="8e043-113">EsentVersion 類別</span><span class="sxs-lookup"><span data-stu-id="8e043-113">EsentVersion class</span></span>](./esentversion-class.md)

[<span data-ttu-id="8e043-114">EsentVersion 成員</span><span class="sxs-lookup"><span data-stu-id="8e043-114">EsentVersion members</span></span>](./esentversion-members.md)

[<span data-ttu-id="8e043-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="8e043-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
