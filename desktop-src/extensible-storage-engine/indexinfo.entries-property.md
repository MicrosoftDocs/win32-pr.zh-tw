---
description: 深入瞭解： IndexInfo 專案屬性
title: IndexInfo 專案屬性
TOCTitle: 'Entries property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.IndexInfo.Entries
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.indexinfo.entries(v=EXCHG.10)
ms:contentKeyID: 55103234
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.IndexInfo.Entries
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.IndexInfo.get_Entries
- Microsoft.Isam.Esent.Interop.IndexInfo.Entries
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f03d5db27e607e8a3c76249e70b78768887d86a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975466"
---
# <a name="indexinfoentries-property"></a><span data-ttu-id="21c73-103">IndexInfo 專案屬性</span><span class="sxs-lookup"><span data-stu-id="21c73-103">IndexInfo.Entries property</span></span>

<span data-ttu-id="21c73-104">取得索引中的專案數。</span><span class="sxs-lookup"><span data-stu-id="21c73-104">Gets the number of entries in the index.</span></span> <span data-ttu-id="21c73-105">此值不是最新值，而且只會由 JetComputeStats 更新。</span><span class="sxs-lookup"><span data-stu-id="21c73-105">This value is not current and is only is updated by Api.JetComputeStats.</span></span>

<span data-ttu-id="21c73-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="21c73-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="21c73-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="21c73-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="21c73-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="21c73-108">Syntax</span></span>

``` vb
'Declaration
Public ReadOnly Property Entries As Integer
    Get
'Usage
Dim instance As IndexInfo
Dim value As Integer

value = instance.Entries
```

``` csharp
public int Entries { get; }
```

#### <a name="property-value"></a><span data-ttu-id="21c73-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="21c73-109">Property value</span></span>

<span data-ttu-id="21c73-110">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="21c73-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="21c73-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="21c73-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="21c73-112">參考</span><span class="sxs-lookup"><span data-stu-id="21c73-112">Reference</span></span>

[<span data-ttu-id="21c73-113">IndexInfo 類別</span><span class="sxs-lookup"><span data-stu-id="21c73-113">IndexInfo class</span></span>](./indexinfo-class.md)

[<span data-ttu-id="21c73-114">IndexInfo 成員</span><span class="sxs-lookup"><span data-stu-id="21c73-114">IndexInfo members</span></span>](./indexinfo-members.md)

[<span data-ttu-id="21c73-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="21c73-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
